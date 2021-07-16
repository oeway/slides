EMBL-EBI Training: Microscopy data analysis 2021

# ImJoy and BioImage Model Zoo

Wei Ouyang 

KTH | SciLifeLab, Stockholm

-----
## <img alt="ImJoy" src="https://imjoy.io/static/img/imjoy-logo-white.svg">
Supercharging interactivity and scalability

-----
## Challenges in AI for bioimaging

* **Usability**: User friendly GUI
* **Interactivity**: Respond to GUI on laptop/mobile
* **Scalability**: Remote storage and compute resources
* **Privacy**: Edge computing

-----
## Progressive Web App

* Rich and interactive UI libraries
* Computation in the browser (+cloud)
* Offline support

-----
<!-- .slide: data-background="white" -->
### ImJoy https://imjoy.io
Data science tools in the browser

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSBsdhDBrp4L2zWfL_9YOUHCS2zQ51HtjplGa-l_a1hMpNjbqENzmXrcSmYs6yed_NACNZSRH-7qsph/pub?w=1248&amp;h=573">
-----
# Key concepts
 * Sandboxed plugins connected via Remote Procedure calls
 * Workflow composition via asynchronous programming
 * Open Integration with existing software/website

-----
<!-- .slide: data-state="demo1" -->
### Calling Python from JS with RPC
<div>
Python (cloud)  ⇔  Javascript (local)
</div>
<div>
<div id="window-1" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>

<div id="window-2" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>
</div>
-----

### 👐Open Integration with Web Apps

Create a window via URL and call functions directly

```js
// load the web app via its URL
viewer = await api.createWindow({src: "https://kaibu.org/#/app"})
// call api functions directly via RPC
// add an image layer
await viewer.view_image("https://images.proteinatlas.org/61448/1319_C10_2_blue_red_green.jpg")
// add an annotation layer
await viewer.add_shapes([], {name:"annotation"})
```
<button class="button" onclick="runDemo2()">Run</button>

-----
<!-- .slide: data-state="ij-macro-1" -->
## 🔥Demo: ImJoy + ImageJ => ImageJ.JS

<div id="macro-editor-1"></div>

-----

### 🔥Demo: Visualization with Vizarr

Made by Trevor Manz et. al.
<iframe width="100%" height="500px" src="https://hms-dbmi.github.io/vizarr/?source=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>


-----

## 🚀A rapid growing list of plugins
 * [ImageJ.JS](https://ij.imjoy.io) <button onclick="api.showDialog({src:'https://ij.imjoy.io'})">Run</button>
 * [File Manager](https://imjoy-team.github.io/elFinder/) <button onclick="api.showDialog({src:'https://imjoy-team.github.io/elFinder/'})">Run</button>
 * [Vizarr](https://github.com/hms-dbmi/vizarr) for visualizing zarr images <button onclick="api.showDialog({src:'https://hms-dbmi.github.io/vizarr/?source=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr', passive:true})">Run</button>
 * [ITK/VTK Viewer](https://kitware.github.io/itk-vtk-viewer/docs/) for 3D visualizing <button onclick="api.getPlugin({src: ZarrPythonCode}).then(p=>{p.run({})})">Run</button>
 * [ImJoy Slides](https://slides.imjoy.io)
 * [ImJoy Chart Editor](https://chart.imjoy.io)

-----
### Works with Jupyter/Binder and Colab
<button class="button" onclick="window.open('https://imjoy.io/lite?binder=https://binder.bioimagearchive.org&plugin=https://github.com/imjoy-team/imjoy-plugins/blob/master/repository/PixelClassifier.imjoy.html')">Pixel Classifier</button>

<img style="height:70%;object-fit:contain;background-color: white;"  src="https://raw.githubusercontent.com/imjoy-team/imjoy-demo-assets/main/image125.gif">

-----
# <img alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo-white.svg">
### Advanced AI models in one click!

-----
# Challenges
 * Training models is difficult
  - Complex hardware/software setup
  - Environmental impact: "Training a single AI model can emit as much carbon as five cars in their lifetimes"
 * Lack of interoperability
 * Hard for non-expert to run
 
-----
# 🦒BioImage Model Zoo
 * AI model file standard
 * Hosting pretrained models
 * Test run service
 * User/Developer services

-----
<!-- .slide: data-background="white" -->
### 🦒BioImage Model Zoo: Overview
<img style="height:calc(100% - 200px);object-fit:contain;background-color: white;"  src="https://docs.google.com/drawings/d/e/2PACX-1vRSNdb6sW-nrTjmHgqwG8sOTdQTjdNjWH0y4DveZwairx_NUKiHg3dm0-0Z7VU4ppFdwSiK2BLn4hKo/pub?w=1732&amp;h=1343">

-----
<!-- .slide: data-background="white" -->
### 🤔How it works

<img style="height:calc(100% - 200px);object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vSh8qO-jxZcGKjg5w52IMTesAUMbOaOxc3XQgmW7zBBj6btMGAUjcgh6iHgaTyzI18Ld7SSHkbie2k2/pub?w=1057&amp;h=689">

-----
## 🔥Demos!
 * Overview: https://bioimage.io/
 * Upload and download Models
 * Test run models: HPA-classification, 

-----
## 🚀BioImage.IO: Beyond the Model Zoo
 * A hub for advanced bioimage analysis workflows, tools and datasets
 * Distributed bioimage computing toolkit
     - Like Binder, but for models, workflows and datasets
     - RDFs => BioImage.IO + ImJoy App Engine => API/RPC endpoints

-----
### Acknowledgements

BioImage.IO is powered by the 🧠 and ❤️ of:
 * deepImageJ Team
 * Fiji/ImageJ Team
 * ilastik Team
 * ImJoy Team
 * ZeroCostDL4Mic Team
 * ...

Follow us on twitter @bioimageio



-----

# 🙏Thank You!


<!-- startup script  -->
```javascript execute
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

window.ZarrPythonCode = `
<config lang="json">
{
  "name": "ZarrPythonPlugin",
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
  "requirements": ["zarr", "fsspec"],
  "dependencies": []
}
</config>

<script lang="python">
import zarr
from imjoy_rpc import api
from imjoy_rpc import register_default_codecs
from fsspec.implementations.http import HTTPFileSystem
register_default_codecs()

fs = HTTPFileSystem()
http_map = fs.get_mapper("https://openimaging.github.io/demos/multi-scale-chunked-compressed/build/data/medium.zarr")
z_group = zarr.open(http_map, mode='r')

class ImJoyPlugin:
    async def setup(self):
        pass

    async def run(self, ctx):
        viewer = await api.createWindow(
            src="https://kitware.github.io/itk-vtk-viewer/app/",
            name="ITK/VTK Viewer"
        )
        await viewer.setImage(z_group)

api.export(ImJoyPlugin())
</script>
`
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

Reveal.addEventListener('demo1', async function(){
    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1]}, data: {code: PythonPluginCode}, window_id: "window-1"})

    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1, 29]}, data: {code: JSPluginCode}, window_id: "window-2"})
})

async function runDemo2(){
 const viewer = await api.showDialog({src: "https://kaibu.org/#/app", name: "Kaibu"})
        await viewer.view_image("https://images.proteinatlas.org/61448/1319_C10_2_blue_red_green.jpg")
        await viewer.add_shapes([], {name:"annotation"})
}




```
