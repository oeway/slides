# ImageJ.JS: Bringing ImageJ to the browser

Wei Ouyang 

KTH | SciLifeLab, Stockholm

-----
## The story
<img style="width: 400px" src="https://raw.githubusercontent.com/oeway/slides/master/2021/bob-java2script-hackathon.png">
<br>
<img style="height: 120px" src="https://raw.githubusercontent.com/oeway/slides/master/2021/cheerpj-browser.png">
<img style="height: 120px" src="https://raw.githubusercontent.com/oeway/slides/master/2021/cheerpj-html5-conversion.png">
-----
## What is ImageJ.JS?
 * ImageJ compiled into Javascript with CheerpJ
 * Runs completely in the browser and offline

-----
## ImJoy Integration
<img style="width: 200px" src="https://imjoy.io/static/img/imjoy-logo-white.png">
<br>

 * Support Volume rendering with ITK/VTK Viewer
 * Support NGFF/Zarr
 * CellPose
 * DeepImageJ integration


-----
## See it in action!

Start ImageJ.JS: [https://ij.imjoy.io](https://ij.imjoy.io)
-----
<!-- .slide: data-state="demo1" -->
### Key concept: ImJoy RPC
<div>
Javascript (local)  ⇔  Python (cloud)
</div>
<div>
<div id="window-1" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>

<div id="window-2" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>
</div>

-----
<!-- .slide: data-state="ij-macro-1" -->
## Interactive slides and teaching

A basic ImageJ macro example:
<div id="macro-editor-1"></div>

-----
<!-- .slide: data-state="ij-macro-2" -->
## Another example

<div id="macro-editor-2"></div>

-----
## Limitations

 * Single-threaded
 * <4GB memory
 * ImageJ-1 only
 * File system


Is it just a toy?
----- 
<!-- .slide: data-background="white" -->
## The bigger picture

<img style="width:100%;object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vQkX5zYF7Di41xuS4hfq0gctS28uZNdt9Nlc5d8oUMNoOsxuwGuNzAhCGaoXpq87yY_4iyDQd_mm_tm/pub?w=1310&amp;h=513">

-----
## The bigger picture
 * Massive dataset
 * Heavy and long computation
 * 6+ billion mobile users
 * Mature web industry
     - Ract/Vue/Angular, D3 etc.
 * Exciting new standards:
     - WebAssembly
     - WebGPU

-----
## The idea
ImageJ.JS <= `imjoy-rpc` => Binder + Fiji

 * Web Viewers <== N5/Zarr Store ==> Remote Fiji
 * Custom distributions of Fiji (similar to Binder)

-----
<!-- .slide: data-background="black" -->
### <img style="height:100px;" alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo-white.svg">

<img style="height:calc(100% - 200px);object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vSh8qO-jxZcGKjg5w52IMTesAUMbOaOxc3XQgmW7zBBj6btMGAUjcgh6iHgaTyzI18Ld7SSHkbie2k2/pub?w=1057&amp;h=689">


-----
### Acknowledgements

ImageJ.JS is powered by the 🧠 and ❤️ of the ImJoy-Team, with the help from:
 * Wayne Rasband
 * Fiji/ImageJ community
 * Leaning Technologies


Follow us on twitter @ImJoyTeam


<!-- startup script  -->
```javascript execute
function startImageJ(){
  api.createWindow({src:"https://ij.imjoy.io", name:"ImageJ.JS"})  
}

async function initializeMacroEditor(editor_container, code){
    const editorElm = document.getElementById(editor_container);
    if(!editorElm) throw new Error("editor container not found: " + editor_container)
    editorElm.style.width = '90%';
    editorElm.style.display = 'inline-block';
    editorElm.style.height = 'calc(100vh - 200px)';
    // force update the slide
    Reveal.layout();
    let editorWindow;
    const config = {lang: 'javascript'}
    config.templates = [
        {
          name: "New",
          url: null,
          lang: 'javascript',
        },
        {
          name: "Sphere",
          url: "https://wsr.imagej.net/download/Examples/Macro/Sphere.ijm",
          lang: 'javascript',
        },
        {
          name: "OpenDialog Demo",
          url: "https://wsr.imagej.net/download/Examples/Macro/OpenDialog_Demo.ijm",
          lang: 'javascript',
        },
        {
          name: "Overlay",
          url: "https://wsr.imagej.net/download/Examples/Macro/Overlay.ijm",
          lang: 'javascript',
        }
      ]
    config.ui_elements = {
      run: {
          _rintf: true,
          type: 'button',
          label: "Run",
          icon: "play",
          visible: true,
          shortcut: 'Shift-Enter',
          async callback(content) {
              try {
                  let ij = await api.getWindow("ImageJ.JS-" + editor_container)
                  if(!ij){
                      //put the editor side by side
                      editorElm.style.width = '38.2%';
                      const ijElm = document.createElement('div');
                      ijElm.id = 'imagej-' + editor_container
                      ijElm.style.display = 'inline-block';
                      ijElm.style.width = '61.8%';
                      ijElm.style.height = editorElm.style.height;
                      editorElm.parentNode.insertBefore(ijElm, editorElm.nextSibling);
                      ij = await api.createWindow({src:"https://ij.imjoy.io", name:"ImageJ.JS-" + editor_container, window_id: 'imagej-' + editor_container})
                  }
                  await ij.runMacro(content)
              } catch (e) {
                  api.showMessage("Failed to run macro, error: " + e.toString());
              } finally {
                  editorWindow.updateUIElement('stop', {
                      visible: false
                  })
                  editorWindow.setLoader(false);
                  api.showProgress(100);
              }
          }
      },
    }
    editorWindow = await api.createWindow({
        src: 'https://if.imjoy.io',
        name: 'ImageJ Script Editor',
        config,
        window_id: editor_container,
        data: {code}
    })
}

Reveal.addEventListener('ij-macro-1', async ()=>{
    const code = `run("Blobs (25K)");
setAutoThreshold("Default");
setOption("BlackBackground", true);
run("Convert to Mask");
run("Analyze Particles...", "size=5-Infinity add");
`
    initializeMacroEditor('macro-editor-1', code)
})

Reveal.addEventListener('ij-macro-2', async ()=>{
    const response = await fetch("https://wsr.imagej.net/download/Examples/Macro/Colors_of_2021.ijm")
    const code = await response.text()
    initializeMacroEditor('macro-editor-2', code)
})

const PythonPluginCode = `
<config lang="json">
{
  "name": "PythonPlugin",
  "type": "native-python",
  "version": "0.1.0",
  "description": "[TODO: describe this plugin with one sentence.]",
  "tags": [],
  "ui": "",
  "cover": "",
  "inputs": null,
  "outputs": null,
  "flags": [],
  "icon": "extension",
  "api_version": "0.1.8",
  "env": "",
  "permissions": [],
  "requirements": [],
  "dependencies": []
}
</config>

<script lang="python">
from imjoy import api


class ImJoyPlugin():
    def setup(self):
        api.showMessage('Python plugin initialized')

    def add(self, a, b):
        return a + b

api.export(ImJoyPlugin())
</script>
`

const JSPluginCode = `
<config lang="json">
{
  "name": "JSPlugin",
  "type": "window",
  "tags": [],
  "ui": "",
  "version": "0.1.0",
  "cover": "",
  "description": "[TODO: describe this plugin with one sentence.]",
  "icon": "extension",
  "inputs": null,
  "outputs": null,
  "api_version": "0.1.8",
  "env": "",
  "permissions": [],
  "requirements": [],
  "dependencies": [],
  "defaults": {"w": 20, "h": 10}
}
</config>

<script lang="javascript">
window.callPython = async function(){
    const pythonPlugin = await api.getPlugin('PythonPlugin')
    const result = await pythonPlugin.add(10, 99)
    document.getElementById("result").innerHTML = "10 + 99 =" + result
}

class ImJoyPlugin {
  async setup() {
    api.log('initialized')
  }

  async run(ctx) {
  }
}
api.export(new ImJoyPlugin())
</script>

<window lang="html">
  <div>
    <button class="button" onclick="callPython()"> Calculate in Python</button>
    <h3 id="result"></h3>
  </div>
</window>

<style lang="css">

</style>
`
Reveal.addEventListener('demo1', async function(){
    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1]}, data: {code: PythonPluginCode}, window_id: "window-2"})

    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1, 29]}, data: {code: JSPluginCode}, window_id: "window-1"})
})
```
