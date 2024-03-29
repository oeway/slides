### Supercharging interactivity and scalability of data science

Wei Ouyang

Emma Lundberg Group @ KTH Royal Institute of Technology
-----
## Overview
 * Deep learning based whole-cell modeling
 * HPA image classification competition
 * Interactive Segmentation
 * ImJoy and BioImage Model Zoo

-----
<iframe style="width:100vw;height:100vh;" src="https://docs.google.com/presentation/d/e/2PACX-1vSZQtEP6SjCfh3JrLJgJFrGYt4LZ5ywfK07cDm6USdQdYyUHsYwh7whXrnS2eBLQy_5KfFGHQ6x-cFq/embed?start=false&loop=false&delayms=3000" frameborder="0" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
<!-- Published-Whole-cell modeling-slides-Wei https://docs.google.com/presentation/d/15Sk7A78NMFjFwBw5Mag3m-O-WGkkDlA9_VyGiXCPHbc/edit -->
-----
<iframe style="width:100vw;height:100vh;" src="https://docs.google.com/presentation/d/e/2PACX-1vRW2zbBDsFIedRfPj6dJHCC7_AR-0lh1mooj4Zai-NKleIMspcirathLjDQ3nC2haAsQds1FUwmXZ_h/embed?start=false&loop=false&delayms=3000" frameborder="0" width="1440" height="839" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<!-- Published-HPA Kaggle competition 2021: https://docs.google.com/presentation/d/14rQ9zoyAErg6LJ1tTs_hG5pBGEgApPcQQfPL2rLc--k/edit -->

-----
### Interactive Annotation

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSnrIWRqUPX5wotapCcUOIATiXXlJ12MtEfzAXAJePLUDbJy5KcfIKLaY3s5nYQZ1-TE9zhzewR8i_2/pub?w=1190&amp;h=916">

-----

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQPwfawLJPOKMco9N2gt4x86ENWr2bvyswiB_96Ja17d4_lQY5pJwZ4Nm_XhIuD01nucgGVSYWKIAya/pub?w=1221&amp;h=1313">

-----
### Interactive Annotation with ImJoy and Colab

<iframe width="100%" height="500px" src="https://www.youtube.com/embed/A0DNcN7L5t0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


-----
# ImJoy
### Supercharging interactivity and scalability of data science
* **Interactivity**: Respond to GUI on laptop/mobile
* **Scalability**: Remote storage and compute resources
* **Privacy**: Edge computing

-----
# Progressive Web App

* Rich and interactive interface in the browser
* Access remote storage and compute power
* Computation in the browser
* Offline support

-----
### ImJoy https://imjoy.io
Data science tools in the browser

<img src="https://raw.githubusercontent.com/imjoy-team/ImJoy/master/docs/assets/imjoy-overview.jpg" style="height: 450px;"></img>


-----
# Key concept
 * Sandboxed plugins connected via Remote Procedure calls
 * Workflow composition via asynchronous programming
 * Open Integration with existing software


-----
<!-- .slide: data-state="demo1" -->
### Calling Python from JS with RPC
<div id="window-1" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>

<div id="window-2" style="display: inline-block;width: 46%; height: calc(100vh - 200px);"></div>

-----

### Open Integration with Web Apps

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

### A rapid growing list of plugins
 * [ImageJ.JS](https://ij.imjoy.io) <button onclick="api.showDialog({src:'https://ij.imjoy.io'})">Run</button>
 * [File Manager](https://imjoy-team.github.io/elFinder/) <button onclick="api.showDialog({src:'https://imjoy-team.github.io/elFinder/'})">Run</button>
 * Vizarr for visualizing zarr images
 * ITK/VTK Viewer for visualizing 3D volume
 * ImJoy Slides
 * ImJoy Chart Editor

-----

### Visualization with Vizarr

<p style="font-size:20px;">Made by Trevor Manz et. al.</p>
<iframe width="100%" style="height: calc(100vh - 100px);"  src="https://hms-dbmi.github.io/vizarr/?source=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>

-----
<!-- .slide: data-state="demo3" -->
### 3D Visualization with ITK/VTK + Zarr

<p style="font-size:20px;">In collabration with Matt McCormick @ Kitware</p>
<div id="window-4" style="display: inline-block;width: 100%; height: calc(100vh - 250px);"></div>

-----
### ImJoy + Jupyter/Binder/Colab
<img style="height:70%;object-fit:contain;background-color: white;"  src="https://raw.githubusercontent.com/imjoy-team/imjoy-demo-assets/main/image125.gif">
<br><a style="font-size:20px;" onclick="window.open('https://imjoy.io/lite?binder=https://binder.bioimagearchive.org&plugin=https://github.com/imjoy-team/imjoy-plugins/blob/master/repository/PixelClassifier.imjoy.html')">Pixel Classifier</a>

-----
### The ImJoy ecosystem

 * Web plugins/apps for UI/web computing
 * Jupyter/Binder for prototyping
 * WIP: ImJoy Engine Cluster for production

-----
### Powering the BioImage Model Zoo
<img style="height:100%;object-fit:contain;background-color: white;"  src="https://docs.google.com/drawings/d/e/2PACX-1vRSNdb6sW-nrTjmHgqwG8sOTdQTjdNjWH0y4DveZwairx_NUKiHg3dm0-0Z7VU4ppFdwSiK2BLn4hKo/pub?w=1732&amp;h=1343">

-----
### https://bioimage.io

<iframe width="100%" style="height: calc(100vh - 100px);" src="https://bioimage.io"  frameborder="0" allowfullscreen></iframe>

-----
### BioImage.IO + BioImage Archive
(ongoing colabration)
<img style="height:100%;object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vQmW38Iws9J6G36cchqaI8BS9RrdBKja7t2Rmn7Qhs9_jXGdVDENyB5Gmm3r8TGpg1uNuJvbd_RxDN5/pub?w=960&amp;h=720">


-----
### Acknowledgements
 * Emma Lundberg Group
 * ImJoy Team
 * KTH Royal Institute of Technology
 * Science for Life Laboratory
 * Knut and Alice Wallenberg Foundation

-----

# Thank You!


-----

# Thank You!


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

const ZarrPythonCode = `
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

Reveal.addEventListener('demo1', async function(){
    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1]}, data: {code: PythonPluginCode}, window_id: "window-1"})

    await api.createWindow({src: 'https://if.imjoy.io', config: {fold: [1, 29]}, data: {code: JSPluginCode}, window_id: "window-2"})
})

async function runDemo2(){
 const viewer = await api.showDialog({src: "https://kaibu.org/#/app", name: "Kaibu"})
        await viewer.view_image("https://images.proteinatlas.org/61448/1319_C10_2_blue_red_green.jpg")
        await viewer.add_shapes([], {name:"annotation"})
}

Reveal.addEventListener('demo3', async function(){
    await api.createWindow({src: 'https://if.imjoy.io', fullscreen: true, config: {fold: [2]}, data: {code: ZarrPythonCode}, window_id: "window-4"})
})

```