# Scalable data sharing and standards

Wei Ouyang

HPA & Emma Lundberg group @ SciLifeLab

(BACH Meeting, July 2021)
-----
## Overview
* Sharing massive images and point cloud
   * NGFF/Zarr reference maker file + ImJoy
   * Point cloud data
   * ShareLoc.XZY

* Sharing AI models
   * Bioimage.IO RDF spec
   * BioImage Model Zoo

* ImJoy App Engine

-----
## NGFF/Zarr: Scalable image file format
 * Large file size vs quick exploration
 * Key idea of Next-generation file formats (NGFF):
   1. Precomputed multi-resolution pyramid
   2. Serving small chunks in a lazy fashion
 * Community-driven standard (Leading team: IDR)

-----
### Visualization with Vizarr

An ImJoy plugin, made by Trevor Manz et. al.
<iframe width="100%" height="500px" src="https://oeway.github.io/vizarr/?source=https://s3.embassy.ebi.ac.uk/idr/zarr/v0.1/4495402.zarr"  frameborder="0" allowfullscreen></iframe>

-----
### Supporting private sharing via reference maker
 * Private sharing of Zarr files?
 * Solution: FSSPEC Reference Maker
   * Save files in OME-TIFF/ZIP format in S3 server
   * Generate a byte-offsets file
   * Generate pre-signed URL
   * Access the chunks with HTTP RANGE requests
   
 <button class="button" onclick="api.getPlugin({src: 'https://gist.githubusercontent.com/muellerflorian/0c19e7d96eaa79377907f28fa10c8c52/raw/hani-ms2-sample1.imjoy.html'}).then(plugin=>plugin.run())">Run Demo</button>
 <button class="button" onclick="window.open('https://gist.github.com/oeway/d8b5bad5cbb7bc234a87d2e8948d9164#file-vizarrreferencestore-imjoy-html-L88-L89')">Source Code</button>

-----
### Sharing large point cloud dataset
 * Needs: Single-Molecule Localization Microscopy, smFISH, single-cell RNA-seq 
 * SMLM file format: zip(binary array + json meta info)
 * Potree format: Generate Multi-resolution Octree, access by chunks (like NGFF)

 <button class="button" onclick="window.open('https://shareloc.xyz')">ShareLoc.XYZ</button>
 <button class="button" onclick="window.open('http://potree.org/potree/examples/ca13.html')">WIP: Potree</button>

-----
### BioImage.IO Resource Description File (RDF)
 * YAML files for annotating resources (AI models/dataset/notebook/application)
 * Hosted on Zenodo and Github
 * Render as static website (serverless)
 * Visualization, test run features powered by ImJoy
 * Collabrative efforts: together with Kreshuk Group, Jug Group

Available at: https://github.com/bioimage-io/spec-bioimage-io
-----
### BioImage Model Zoo
<img style="height:100%;object-fit:contain;background-color: white;"   src="https://docs.google.com/drawings/d/e/2PACX-1vSuRHrs1p6omG_CRC_1t_19gsP6RJOHwnelTKNrD-1opsXzGZ0AwZPYBT4SBQHkvyYlGB-UumyZAigG/pub?w=1261&amp;h=902">

-----
### BioImage Model Zoo

Available at: https://bioimage.io/

-----
### WIP: ImJoy App Engine
 * Decentralized cloud infrastructure for reproducible science
 * Key Idea:
     * Serving RDF files hosted on Zenodo/Github, provide HTTP/RPC endpoint
     * Exposing resource to the IPFS network and using content addressing
     * Example 1: serving zipped tiff files on zenodo and get Zarr array interface
     * Example 2: serving AI models and provide inference/training functions
 * Kubernetes deployment kit for desktop/servers

-----
## Thank you!

Interactive slides powered by ImJoy Slides [@ImJoyTeam](https://twitter.com/imjoyteam)
