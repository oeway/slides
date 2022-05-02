From Images to Knowledge Conference - 2022

## Hypha: Scalable Data Management and AI Model Serving

Wei OUYANG

SciLifeLab | KTH Royal Institute of Technology, Stockholm

-----
## Next-generation bioimage analysis tools

* **Scalability**: Massive dataset and heavy computation
* **Usability**: User friendly GUI
* **Flexibility**: Flexible for different data types
* **Interactivity**: Respond to GUI on laptop/mobile
* **Privacy**: Federated learning etc.

-----
## Desktop software DO NOT scale
* Hardware: Lack of storage and computation resources
* Software: UI + Computation coupling
* New paltforms: Tablets & mobile phones

-----
<!-- .slide: data-background="white" -->
## We need a cloud native solution
 * Handle data and computation in the cloud
 * Desktop software and browser as a client

<img src="https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/media/cloud-native-foundational-pillars.png">

-----
<!-- .slide: data-background="white" -->
## Introducing Hypha
<img style="max-height: calc(100vh - 200px);"  src="https://docs.google.com/drawings/d/e/2PACX-1vTdYT__2bIZISzNpRuEmV2XjmLNYKmiv5L8-KzYNN6bSNpf32PgEV5OujrtaOPKwApRpWL1GlAH4z-I/pub?w=845&amp;h=528">

-----
<!-- .slide: data-background="white" -->
## Hypha App Engine
<img  style="max-height: calc(100vh - 200px);" src="https://docs.google.com/drawings/d/e/2PACX-1vRgAdZiOm_BNCxkeAOh8GzYx3qyYPznvmw7GBhmBWYJQE5mxAH6I_rtNEMC5DcIPrg1lIA21SyoJsqp/pub?w=1440&amp;h=1080">

-----
<!-- .slide: data-background="white" -->
<img style="max-height: calc(100vh - 100px);"  src="https://docs.google.com/drawings/d/e/2PACX-1vR5TfCEbqfUtHPUgnEHwqdRPnXVTKHwFE6W2v7_1M9cjLrhgmrswXNycyM07r0QNkQOrghML_VDGqZB/pub?w=1559&amp;h=1211">
<!-- <img style="max-height: calc(100vh - 200px);"  src="https://docs.google.com/drawings/d/e/2PACX-1vQ05EKTXCsRcnqpQIu2R8sOEiVi7ahWjO-Eo9Y8H6BonmKlBO3i1Xi3ndfr9r0vBKoPVi6NztNeyLFh/pub?w=1559&amp;h=1211"> -->

-----
## 🔥 A Quick Tour to Hypha App Engine
<button class="button" onclick='loadNotebook("hypha-quick-tour.ipynb", "hypha-tour-window", "https://raw.githubusercontent.com/oeway/slides/master/2022/hypha-quick-tour.ipynb", true)'>A quick tour to Hypha</button>
<div id="hypha-tour-window" style="width: 100%; height: 100vh;"></div>

-----
<!-- .slide: data-background="white" -->
## Building AI Platforms for the Masses
<img style="width: 500px" src="https://imjoy.io/static/img/imjoy-logo-black.png">

Data science tools in the browser

<img style="width: 500px" alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo.svg">

A repository for sharing AI Models in BioImage Analysis

-----
<!-- .slide: data-background="white" -->
## BioEngine: Hypha-powered AI infrastructure for BioImaging
<img style="max-height: calc(100vh - 200px);" src="https://docs.google.com/drawings/d/e/2PACX-1vQCVUJDbgT_cPVsm--P75h13xbl7kW1Kt4RESW2opDb8MYOQrYQxToaFMFYdUwEBDBC4EWKwto0EExB/pub?w=1550&amp;h=983">

-----
<!-- .slide: data-background="white" -->
## Deploying the BioEngine
<img style="max-height: calc(100vh - 200px);" src="https://docs.google.com/drawings/d/e/2PACX-1vSoG7ywI0qbNAbG-bV7J9LomhlK8r1xyhxS70LcA4_XNt_oUiWoYLcMFJlUFB2oA80hgL5TQzAWUhNW/pub?w=1510&amp;h=1050">

-----
## Hands on workshop for BioEngine at I2K

Available here: https://youtu.be/EEo_GPjbxn4
<iframe width="560" height="315" src="https://www.youtube.com/embed/EEo_GPjbxn4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

-----
## 🚀AI-assisted Bioimage Analysis
Available here: https://youtu.be/pkOp_oUybsc
<iframe width="560" height="315" src="https://www.youtube.com/embed/pkOp_oUybsc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Powered by OpenAI GPT-3 and Codex
-----
## Conclusions
 * Hypha: Scalable Data Management and AI Model Serving
 * Powering next generation bioimage analysis platform with Hypha App Engine
 * Hypha-powered BioEngine for the BioImage Model Zoo

-----
### Acknowledgements (1)
Work carried out at Cell Profiling group @ SciLifeLab headed by Emma Lundberg

ImJoy is powered by the 🧠 and ❤️ of the ImJoy Team including:
 * Florian Mueller
 * Martin Hjelmare
 * Craig Russell
 * ...

Follow us on twitter @ImJoyTeam

-----
### Acknowledgements (2)

BioImage.IO is powered by the 🧠 and ❤️ of:
 * deepImageJ Team
 * EBI Bioimage Archive Team
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

async function loadNotebook(name, window_id, url, overwrite){
    const jupyter = await api.createWindow({src: "https://jupyter.imjoy.io/lab/index.html", window_id})
    const bid = window_id.replace("window", "reset")
    const button = document.getElementById(bid)
    if(await jupyter.fileExists(name)){
        if(overwrite){
            const content = await (await fetch(url)).text()
            await jupyter.removeFile(name)
            await jupyter.loadFile(name, content, 'application/json')
        }
        await jupyter.openFile(name)
    } else{
        const content = await (await fetch(url)).text()
        const filePath = await jupyter.loadFile(name, content, 'application/json')
        await jupyter.openFile(filePath)
    }
    button.style.display = "inline-block";
}


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
