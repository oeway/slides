# Coffee and Codex

## AI-assisted coding with GPT-3

Wei Ouyang, Anthony Cesnik

KTH | SciLifeLab, Stockholm

-----
## GPT-3 -- the most powerful AI in the world

* Made by OpenAI, released in June 2020
* 175 billion parameters
* Trained on 45TB of text data
* Take 355 years to train GPT-3 on a Tesla V100
* Costs $12 million to train once
* Not open-source (yet), only API access

-----
<!-- .slide: data-background="white" -->
## The exploding model size
![](https://miro.medium.com/max/582/1*C-KNWQC_wXh-Q2wc6VPK1g.png)

Many models can be downloaded from https://huggingface.co/

-----
<!-- .slide: data-background="white" -->
## Understand GPT-3 

![](https://daleonai.com/images/cnn.png)

![](https://daleonai.com/images/renn.png) <!-- .element: class="fragment" data-fragment-index="1" -->

-----
<!-- .slide: data-background="white" -->
## "Attention is all you need"
<img style="height:80%" src="https://daleonai.com/images/screen-shot-2021-05-06-at-12.12.21-pm.png">

-----
<!-- .slide: data-background="white" -->
## Attention is all you need
 * Positional Encodings
 * Attention
 * Self-Attention

<footer style="font-size: 12px">https://daleonai.com/transformers-explained</footer>

-----
<!-- .slide: data-background="white" -->
## Attention is all you need
![](https://daleonai.com/images/screen-shot-2021-05-06-at-12.40.39-pm.png)
<footer style="font-size: 12px">Figure from the paper, "Neural Machine Translation by Jointly Learning to Align and Translate (2015)</footer>

-----
<iframe style="width:100%;height:100vh" src="https://jalammar.github.io/how-gpt3-works-visualizations-animations/"></iframe>

-----
## GPT-3: Autocompletion & few-shot learning
<!-- .slide: data-background="white" -->
<img src="https://raw.githubusercontent.com/oeway/slides/master/2021/robot-autocompletion-example.png">
<img src="https://miro.medium.com/max/1000/1*q-P5aQ7A6VlsfroP3ckg8A.jpeg">

-----
## Codex
 * OpenAI Codex is a descendant of GPT-3
 * GPT-3 trained on billions of lines of source code
 * Longer context (upto 4096 tokens)

-----
# 🔥Codex live demos!
## Disclaimer!
 * All the demo applications have not yet been approved for launch
 * Please don't record the demos
-----
## 1. Codex basic demos
 * Explain code
 * Write a Python docstring
 * Python bug fixer

---
## 2. Javascript UI generation demo
```
Make a snowstorm on a black background
Make a red ball bounce around the screen
Make a website for a cat that's an attorney. Provide a bio and a phone number. Create a small round avatar image: https://bit.ly/3fsc0rH. Center everything.
```
---
### 3. HPA image manipulation
```
Display this cell images on the screen: https://images.proteinatlas.org/115/672_E2_1_blue_red_green.jpg and set the width to 100px.
Add a button and when I click it make the image rotate with a random angle.
Add another button to only show the blue cells in the image.
Add a third button to make the cells a little bit blurred.
Add a fourth button for restore the image to its original state.
```
---
### 4. Display CSV table
```
display a drag and drop file field and make it visible
when the file changes, load the file content, parse the file content as a csv table, store the rows as an array of objects, then display the table on the screen!
add a button when the user click it, highlight the rows in the table contains "membrane"
Parse the x and y column in the table and save them as separate variables
add another button for parsing the x and y column in the table and save them as separate variables, then make a scatter plot with x and y (DO NOT use d3 !!!)
```

---
### 5. 🔥Voice programming demo by Anthony Cesnik

---
### 6. Using API document

```markdown
# Get api docs from https://www.uniprot.org/help/api_retrieve_entries
# make a function for fetching a sequence (in fasta format) from a uniprot entry
# import the requests library
```

```markdown
# test the fetch sequence function
```

-----
## Tips on using Codex
 * Think it as an **autocompletion** tool
 * Guide it, not command it
 * Show and tell: Provide context and examples
 * Make it clear what you want either through instructions, examples, or a combination of the two.

-----
## Why Codex is important?
 * Better generalization and interpretability
 * Zero/Few-shot learning for low data domain
 * Building trust between human & AI
 * Applications in life science

-----
## Implications for software UX design
 * Challenges: Flexibility vs Simplicity
 * Solution: Chat or voice-based UX
 * Codex + hidden context + user input => magical intelligent application!

-----
## Discussion
 * Limitations and criticisms
 * Ethical issues
 * Try it yourself with Github Copilot
 * What do you think?
 
 [On the Opportunities and Risks of Foundation Models](https://fsi.stanford.edu/publication/opportunities-and-risks-foundation-models)

 "GPT-4 will have 100 trillion parameters!" <!-- .element: class="fragment" data-fragment-index="1" -->
-----
## Upcoming Seminar at SciLifeLab
[A sneak peek into the future of AI-assisted life science](https://www.scilifelab.se/event/scilifelab-ai-seminar-series-wei-ouyang/)
* November 23rd, 10:00 - 11:00
* Hybrid seminar
* Register now!

-----
### Acknowledgements

We thank OpenAI for providing beta testing access to GPT-3 and Codex

The demos during this talk has not been approved by OpenAI

-----

# 🙏Thank You!
