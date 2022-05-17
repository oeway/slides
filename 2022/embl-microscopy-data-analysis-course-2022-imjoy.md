EMBL-EBI Training - Microscopy data analysis

## Web- and AI-powered Bioimage Analysis with ImJoy and the BioEngine

Wei OUYANG

SciLifeLab | KTH Royal Institute of Technology, Stockholm
-----
## Learning objectives
 * The basic concepts in web-based image analysis and ImJoy
 * Develop your own ImJoy plugins for image visualization and annotation
 * Use BioEngine to do deep learning based image analysis

-----
# Part 1: Introduction

The basic concept in web-based image analysis and ImJoy

-----
## Challenges in AI for bioimaging

* **Usability**: User friendly GUI
* **Flexibility**: Flexible for different data types
* **Interactivity**: Respond to GUI on laptop/mobile
* **Scalability**: Remote storage and compute resources
* **Privacy**: Edge computing

-----

## Human-in-the-loop AI for life science

<img src="https://cdn.clickworker.com/wp-content/uploads/2019/04/human-in-the-loop.jpg">

Building machines by leveraging the power of the machine and human intelligence

-----
## Trends in Bioimaging
 * Use deep learning
 * Large models (transformers!)
 * Massive dataset
 * Scalabile file format (Zarr, N5, NGFF)

🚀A Future of Web- and AI-powered Bioimage Analysis

-----
## Existing solutions
* Desktop software: DeepImageJ, ilastik, napari
* Notebooks: Colab/ZeroCost4Mic, Jupyter Notebooks
* Web Apps: NucleAIzer, CellPose, DeepCell, ImJoy

-----
## Browser-based computation

* Rich and interactive UI libraries
* Computation in the browser (+cloud)
* Offline support

-----
## WebAssembly

***"a portable compilation target for programming languages"***

 * [Windows XP in your browser](https://lrusso.github.io/VirtualXP/VirtualXP.htm)
 * Pyodide: Python and Scientific stack in your browser ([JupyterLite](https://jupyter.imjoy.io/lab/index.html))

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
### Asynchronous Workflow Composition

Concurrent Execution
```python
promise1 = plugin1.process(input1)
promise2 = plugin2.process(input2)
output1, output2 = await asyncio.gather(promise1, promise2)

output3 = await plugin3(output1, output2)
```

Sequential Execution
```python
output1 = await plugin1.process(input1)
output2 = await plugin2.process(input2)

output3 = await plugin3(output1, output2)
```

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
<!-- .slide: data-state="ij-macro-1" -->
## 🔥Demo: ImJoy + ImageJ => ImageJ.JS

<div id="macro-editor-1"></div>

-----

### 🔥Demo: Visualization with Vizarr

Made by Trevor Manz et. al.
<iframe width="100%" height="500px" src="https://hms-dbmi.github.io/vizarr/?source=https://uk1s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>

-----

# Part 2: Hands on tutorial - ImJoy

Create your own ImJoy plugins

-----
## Your first ImJoy plugin
<!-- .slide: data-state="tutorial-code-1" -->
<div id="window-tutorial-1" style="display: inline-block;width: 100%; height: calc(50vh);" ></div>

 * Open the browser console to see the error
 * Fix the error and try it again

-----
## Tutorial 1: Develop a Python plugin
<button class="button" onclick='loadNotebook("embl-imjoy-tutorial-1.ipynb", "embl-tutorial-1-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/1-plugin-development/embl-imjoy-tutorial-1.ipynb")'>Click to start the notebook</button>
<button id="embl-tutorial-1-reset" class="button" style="background-color:red;display:none;" onclick='loadNotebook("embl-imjoy-tutorial-1.ipynb", "embl-tutorial-1-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/1-plugin-development/embl-imjoy-tutorial-1.ipynb", true)'>Reset</button>
<div id="embl-tutorial-1-window" style="width: 100%; height: 100vh;"></div>

-----

# Part 3: Hands on tutorial - BioEngine

Run deep learning models via the BioEngine

-----
<!-- .slide: data-background="white" -->
## Meet the BioEngine
<img style="max-height: calc(100vh - 100px);" src="https://docs.google.com/drawings/d/e/2PACX-1vQCVUJDbgT_cPVsm--P75h13xbl7kW1Kt4RESW2opDb8MYOQrYQxToaFMFYdUwEBDBC4EWKwto0EExB/pub?w=1550&amp;h=983">

-----
<!-- .slide: data-background="white" -->
## Deploying the BioEngine
<img src="https://docs.google.com/drawings/d/e/2PACX-1vSoG7ywI0qbNAbG-bV7J9LomhlK8r1xyhxS70LcA4_XNt_oUiWoYLcMFJlUFB2oA80hgL5TQzAWUhNW/pub?w=1510&amp;h=1050">


-----
## BioEngine feature hightlights
* **Many models**
* **Many users**
* **Many applications**
* **Shared GPU resources**
* **Both inference and training**
* **Local or cloud deployment**

-----
# 🔥Hands on tutorial
Try the BioEngine

-----
<!-- .slide: data-state="tutorial-1" -->
## Tutorial 2: Getting Started with BioEngine
<button class="button" onclick='loadNotebook("embl-bioengine-tutorial-0.ipynb", "embl-bioengine-tutorial-0-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/2-bioengine/1-bioengine-engine-tutorial.ipynb")'>Click to start the notebook</button>
<button id="embl-bioengine-tutorial-0-reset" class="button" style="background-color:red;display:none;" onclick='loadNotebook("embl-bioengine-tutorial-0.ipynb", "embl-bioengine-tutorial-0-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/2-bioengine/1-bioengine-engine-tutorial.ipynb", true)'>Reset</button>
<div id="embl-bioengine-tutorial-0-window" style="width: 100%; height: 100vh;"></div>

-----
<!-- .slide: data-state="tutorial-3" -->
## Tutorial 3: Create UI with ImJoy and Kaibu
<button class="button" onclick='loadNotebook("embl-bioengine-tutorial-1.ipynb", "embl-bioengine-tutorial-1-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/2-bioengine/embl-bioengine-tutorial-1.ipynb")'>Click to start the notebook</button>
<button id="embl-bioengine-tutorial-1-reset" class="button" style="background-color:red;display:none;" onclick='loadNotebook("embl-bioengine-tutorial-1.ipynb", "embl-bioengine-tutorial-1-window", "https://raw.githubusercontent.com/imjoy-team/imjoy-tutorials/master/2-bioengine/embl-bioengine-tutorial-1.ipynb", true)'>Reset</button>
<div id="embl-bioengine-tutorial-1-window" style="width: 100%; height: 100vh;"></div>


-----
## 🚀AI-assisted Bioimage Analysis
<iframe width="560" height="315" src="https://www.youtube.com/embed/pkOp_oUybsc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Powered by OpenAI GPT-3 and Codex
-----
## Conclusions
 * Web and Browser based Image Analysis
 * Create your own ImJoy plugins
 * Connecting to the BioEngine

To learn more: https://imjoy.io/docs/#/i2k_tutorial

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
  "type": "web-python",
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


const tutorialCode1 = `
<config lang="json">
{
  "name": "PokemonChooser",
  "type": "web-python",
  "version": "0.1.0",
  "description": "A Pokémon chooser plugin",
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
    async def setup(self):
        pass

    async def run(self, ctx):
        # pokemon = await api.prompt("What is your favorite Pokémon?", "Pikachu")
        await api.showMessage("Your have chose " + pokemon + " as your Pokémon.")

api.export(ImJoyPlugin())
</script>
`
Reveal.addEventListener('tutorial-code-1', async function(){
    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1]}, data: {code: tutorialCode1}, window_id: "window-tutorial-1"})
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
