## <img src="https://imjoy.io/static/img/imjoy-logo-white.svg" style="width:500px">

## AI-powered image analysis on the web

Wei OUYANG

SciLifeLab | KTH Royal Institute of Technology
-----
## Challenges in AI for bioimaging

* **Usability**: User friendly GUI
* **Flexibility**: Flexible for different data types
* **Interactivity**: Respond to GUI on laptop/mobile
* **Scalability**: Remote storage and compute resources
* **Privacy**: Edge computing

-----
## Oppotunities with the web
* Cloud computing: unlimited storage and compute power
* Modern UI frameworks and libraries
* WebAssembly and WebGPU
* Scalable storage (e.g, S3).

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

Customize annotation workflow with Kaibu

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
<!-- .slide: data-background="white" -->
### Kaibu: Web-based annotation tool
<img src="https://kaibu.org/static/img/kaibu-logo.gif" style="width:400px">

https://kaibu.org/docs/#/api

Built with ITK/VTK Viewer, OpenLayers etc.
-----
<!-- .slide: data-background="white" -->
### AI for Cervical Cancer
 * Started in Jan 2021, built with Kaibu & ImJoy
 * Support multi-user collabration and running on mobile
 * Data and server hosted at Institut Pasteur
<img style="height:calc(100vh - 400px);" src="https://github.com/oeway/slides/blob/master/2021/msf-kaibu-ipad-annotation.png?raw=true">

-----
<!-- .slide: data-state="ai4cc-demo" data-background="white"  -->
### 🔥Demo: AI for Cervical Cancer

<button class="button" onclick="runAI4CC()">Start</button>

-----
<!-- .slide: data-background="white" -->
### 🔥Example: Interactive Annotation

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSnrIWRqUPX5wotapCcUOIATiXXlJ12MtEfzAXAJePLUDbJy5KcfIKLaY3s5nYQZ1-TE9zhzewR8i_2/pub?w=1190&amp;h=916">

-----
### 🔥Example: Interactive Annotation with ImJoy and Colab

<iframe width="100%" height="500px" src="https://www.youtube.com/embed/A0DNcN7L5t0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


-----
## ImageJ.JS
 * ImageJ compiled into Javascript (with CheerpJ)
 * Running in web browser, support tablets & mobile phones

See it in action: [https://t.co/0cpPjNdJG1](https://t.co/0cpPjNdJG1)

(Plant segmentation demo by Jerome Mutterer)

-----
<!-- .slide: data-state="ij-macro-1" -->
### 🔥Demo: ImageJ.JS macro editor

<div id="macro-editor-1"></div>

-----

### 🔥Demo: Visualization with Vizarr

Made by Trevor Manz et. al.
<iframe width="100%" height="500px" src="https://hms-dbmi.github.io/vizarr/?source=https://uk1s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>


-----
### Works with Jupyter Notebooks, JupyterLab and Colab

<img style="height:70%;object-fit:contain;background-color: white;"  src="https://raw.githubusercontent.com/imjoy-team/imjoy-demo-assets/main/image125.gif">

-----

## 🚀A rapid growing list of plugins
 * [ImageJ.JS](https://ij.imjoy.io) <button onclick="api.showDialog({src:'https://ij.imjoy.io'})">Run</button>
 * [File Manager](https://imjoy-team.github.io/elFinder/) <button onclick="api.showDialog({src:'https://imjoy-team.github.io/elFinder/'})">Run</button>
 * [Vizarr](https://github.com/hms-dbmi/vizarr) for visualizing zarr images <button onclick="api.showDialog({src:'https://hms-dbmi.github.io/vizarr/?source=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr', passive:true})">Run</button>
 * [ITK/VTK Viewer](https://kitware.github.io/itk-vtk-viewer/docs/) for 3D visualizing <button onclick="api.getPlugin({src: ZarrPythonCode}).then(p=>{p.run({})})">Run</button>
 * [ImJoy Slides](https://slides.imjoy.io)
 * [ImJoy Chart Editor](https://chart.imjoy.io)
 * ...

-----
# <img alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo-white.svg">
### Advanced AI models in one click!

https://bioimage.io

-----
## Hypha: Powering Privacy-preserving AI
<img src="https://amun.ai/images/cartoon-tree-ai.png">

-----
## 🚀AI-assisted Bioimage Analysis

Powered by OpenAI GPT-3 and Codex

-----
### Acknowledgements

 * AI4CC annotation is a collabrative project between KTH and MSF

 * Data and backend server in the AI4CC project are kindly hosted by Institut Pasteur 

-----
### Acknowledgements

Work carried out at Cell Profiling group @ SciLifeLab headed by Emma Lundberg

ImJoy is powered by the 🧠 and ❤️ of the ImJoy Team including:
 * Florian Mueller
 * Martin Hjelmare
 * Craig Russell
 * ...

Follow us on twitter @ImJoyTeam


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

window.runAI4CC = async ()=>{
   const p = await api.loadPlugin({src: "https://gist.githubusercontent.com/oeway/c6cc23fecddd2aaa15fb7486f0da871a/raw/Cervical-Annotator.imjoy.html"})
   await p.run()
}


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

async function runHPADemo(){
    const plugin = await api.getPlugin("https://gist.githubusercontent.com/oeway/b318a26ef7191679b175be5216accbda/raw/HPA-UMAP-Studio.imjoy.html")
    await plugin.run({})
}


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

```
