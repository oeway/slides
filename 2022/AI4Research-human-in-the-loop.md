<!-- .slide: data-background="white" -->
AI4Research open seminar 29/03/2022

## Human-in-the-loop AI for data-driven life science

Wei OUYANG

SciLifeLab | KTH Royal Institute of Technology

-----
<!-- .slide: data-background="white" -->
## Challenges in AI

Generalization & Interpretability

<br>
<img style="height:30%" src="https://miro.medium.com/max/1200/1*5KizicdVpwvNCAo2Zy4hFQ.png">
<img style="height:25%" src="https://www.kdnuggets.com/wp-content/uploads/blackbox.jpg">

<p style="font-size: 12px">Image from Wikipedia</p>

-----
<!-- .slide: data-background="white" -->
## Making AI human compatible

<img style="width:40%" src="https://upload.wikimedia.org/wikipedia/commons/4/4d/Skynet_Terminator_logo.png"> 
<img style="width:23%;" src="https://people.eecs.berkeley.edu/~russell/images/HumanCompatible-Cover-UK.jpg">

_Machines are benificial to the extent that their actions can be expected to achive our objective._

-- Stuart Russell


-----
<!-- .slide: data-background="white" -->
## Human-in-the-loop AI for life science

<img src="https://cdn.clickworker.com/wp-content/uploads/2019/04/human-in-the-loop.jpg">

Building machines by leveraging the power of the machine and human intelligence

-----
## Tools for human-in-the-loop AI

* **Usability**: User friendly GUI
* **Flexibility**: Flexible for different data types
* **Interactivity**: Respond to GUI on laptop/mobile
* **Scalability**: Remote storage and compute resources
* **Privacy**: Edge computing

-----
## Building AI infrastructure for human-in-the-loop
 * ImJoy: Supercharging interactivity
 * BioImage Model Zoo: AI models in one-click 
 * OpenAI Codex: A sneak peak into the future

-----
<!-- .slide: data-background="white" -->
### ImJoy https://imjoy.io
Data science tools in the browser

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSBsdhDBrp4L2zWfL_9YOUHCS2zQ51HtjplGa-l_a1hMpNjbqENzmXrcSmYs6yed_NACNZSRH-7qsph/pub?w=1248&amp;h=573">

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

### 🔥Demo: Visualization with Vizarr

Made by Trevor Manz et. al.
<iframe width="100%" height="500px" src="https://hms-dbmi.github.io/vizarr/?source=https://uk1s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>

-----
<!-- .slide: data-state="ij-macro-1" -->
### 🔥Demo: ImageJ.JS macro editor

<div id="macro-editor-1"></div>

-----
<!-- .slide: data-background="white" -->
### 🔥Human-in-the-loop: Interactive Annotation

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSnrIWRqUPX5wotapCcUOIATiXXlJ12MtEfzAXAJePLUDbJy5KcfIKLaY3s5nYQZ1-TE9zhzewR8i_2/pub?w=1190&amp;h=916">

-----
### 🔥Human-in-the-loop: Interactive Annotation with ImJoy and Colab

<iframe width="100%" height="500px" src="https://www.youtube.com/embed/VIZDkhCZtJo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

-----
# <img alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo-white.svg">
### Advanced AI models in one click!

-----
<!-- .slide: data-background="white" -->
### 🤔How it works

<img style="height:calc(100% - 200px);object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vSh8qO-jxZcGKjg5w52IMTesAUMbOaOxc3XQgmW7zBBj6btMGAUjcgh6iHgaTyzI18Ld7SSHkbie2k2/pub?w=1057&amp;h=689">

-----
## 🔥Try it yourself!
 https://bioimage.io

-----
## BioEngine -- AI model and application serving
 * Provide web API for model training and inference
 * Support test run models and ImJoy applications
 * Suitable for deploying AI workflows for institutions, facilities or labs

-----
Running models in JupyterLite via the BioEngine
<iframe style="width:100%;height:calc(100vh - 20px)" src="https://jupyter.imjoy.io/retro/notebooks/?path=bioengine-demo.ipynb"></iframe>

-----
## 🚀AI-assisted Bioimage Analysis
### A taste of the future!

-----
<!-- .slide: data-background="white" -->
## The trending NLP models
The exploding Natural Language Processing (NLP) model size
![](https://miro.medium.com/max/582/1*C-KNWQC_wXh-Q2wc6VPK1g.png)

-----
## GPT-3 -- the most powerful AI in the world

* Made by OpenAI, released in June 2020
* 175 billion parameters
* Trained on 45TB of text data
* Take 355 years to train GPT-3 on a Tesla V100
* Costs $12 million to train once

(Brown et. al, 2020)
-----
<iframe style="width:100%;height:100vh" src="https://jalammar.github.io/how-gpt3-works-visualizations-animations/"></iframe>

-----
## Codex model for code generation
 * OpenAI Codex is a descendant of GPT-3
 * Trained on billions of lines of source code
 * Made for code generation in **Python**, Go, JavaScript, Perl, PHP, Ruby, Shell, Swift, and TypeScript etc.

(Chen et. al 2021)
-----
## Key Concepts: Autocompletion & few-shot learning
<!-- .slide: data-background="white" -->
<img src="https://raw.githubusercontent.com/oeway/slides/master/2021/robot-autocompletion-example.png">
<img src="https://miro.medium.com/max/1000/1*q-P5aQ7A6VlsfroP3ckg8A.jpeg">

-----
# 🔥Codex live demos!
## Disclaimer!
 * All the demo applications have not yet been approved for launch
 * Please don't record the demos

-----
<iframe style="width:100%;height:calc(100vh - 20px)" src="https://www.youtube.com/embed/pkOp_oUybsc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
-----
## Using existing knowledge and tools in AI

Codex provides a way for making hybrid solutions:
 * Analytical solutions backed by math
 * Deep neural networks

-----
## Advantages of code generation
 * Improve interpretability: Source code can be inspected
 * Improve generalization and enable extrapolation

<!-- .slide: data-background="white" -->

<img style="width:40%" src="https://miro.medium.com/max/1435/1*wgDdR3Wrfca4EDxvtSbzJw.png">

<img style="width:42%" src="https://miro.medium.com/max/1487/1*PbNoFOwNP2i6pS5zgrR16w.png">

<p style="font-size: 12px">Illustrations by Halem Rostt (https://morioh.com/p/9bd69a11b02a)</p>


-----
## Other advantages of Codex
 * Zero/Few-shot learning for low data domain
 * Building trust between human & AI

-----
## Conclusions
 * Safeguarding AI via human-in-the-loop
 * ImJoy for scalability and interactivity
 * BioImage Model Zoo for sharing AI models
 * BioEninge for AI model serving in the cloud
 * AI-assisted bioimage anlysis via Code generation

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
### Acknowledgements (3)

We thank OpenAI for providing beta testing access to GPT-3 and Codex

The demos during this talk has not been approved by OpenAI


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
