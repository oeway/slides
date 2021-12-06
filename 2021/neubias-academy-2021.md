NEUBIAS Academy
# Introduction to ImJoy

AI-powered image analysis on the web

Wei OUYANG

SciLifeLab | KTH Royal Institute of Technology
-----
## Overview
 * Introduction to ImJoy & web image analsysis
 * Session 1: Develop your own ImJoy Plugin
 * Session 2: Train your own deep learning model
-----
 1. General Introduction to deep learning
 2. Web Image analsysis
 3. Trend
 4. How ImJoy is used
 6. Examples
     1. Visualization & Annotation
     2. ImageJ.JS for analysis
     1. Interactive annnotation and training (Kaibu interactive demo)
     2. Prediction & feature extraction (?)
     3. Demo on ImJoy 
     3. Interactive plot, imjoy-chart ([HPA UMAP Studio](https://imjoy.io/lite?plugin=https://gist.githubusercontent.com/oeway/b318a26ef7191679b175be5216accbda/raw/HPA-UMAP-Studio.imjoy.html))
     4. Presentation, imjoy-slides

-----
## Session 1: Develop your own ImJoy Plugin

VS CODE

-----
## ImageJ.JS
 * ImageJ compiled into Javascript (with CheerpJ)
 * Running in web browser, support tablets & mobile phones
 * Share macro via URL
 * Easy integration with website/apps
 * Suited for teaching


See it in action: [https://t.co/0cpPjNdJG1](https://t.co/0cpPjNdJG1)

(Plant segmentation demo by Jerome Mutterer)

---
<!-- .slide: data-state="ij-macro-1" -->
## Try ImageJ Macro

A basic ImageJ macro example:
<div id="macro-editor-1"></div>

---
<!-- .slide: data-state="ij-macro-2" -->
## Another example

<div id="macro-editor-2"></div>

-----
## Powered by ImJoy

ImJoy: a web plugin framework for building interactive computational tools

* Integration with ITK/VTK viewer for 3D volume rendering
* Extend with Imjoy plugins
* Running DeepImageJ models with Tensorflow.js
* Loading NGFF/Zarr images as virtual stack

-----
## Open Integration
 * Integrate with OMERO (by Will Moore)
 * Integrated with OpenFlexure/UC2 microscope software
 * Embedded in ImJoy Slides for teaching

---
## NGFF Demo

https://ij.imjoy.io/?open=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/6001240.zarr

---
## Virutal Stack Demo

<button class="button" onclick="api.getPlugin('https://gist.github.com/oeway/7a30f3d0c6eb24e9de68e3cece9a5441')">Load HPA Cell Atlas image virtual stack (800GB)</button>

-----
## Try it yourself
## https://ij.imjoy.io

Follow us on Twitter @ImJoyTeam


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

```
