# Coffee and Codex

## AI-assisted coding with GPT-3

Wei Ouyang, Anthony Cesnik

KTH | SciLifeLab, Stockholm

-----
## GPT-3 -- the most powerful AI in the world

* Made by OpenAI, released in June 2020
* 175 billion parameters
* Trained on 45TB of text data
* Costs $12 million to train once
* Not open-source (yet), only API access

-----
<!-- .slide: data-background="white" -->
## The exploding model size
![](https://miro.medium.com/max/582/1*C-KNWQC_wXh-Q2wc6VPK1g.png)

Many models can be downloaded from https://huggingface.co/

"GPT-4 will have 100 trillion parameters!" <!-- .element: class="fragment" data-fragment-index="1" -->
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
 
-----
<!-- .slide: data-background="white" -->
## Attention is all you need
![](https://daleonai.com/images/screen-shot-2021-05-06-at-12.40.39-pm.png)
<footer style="font-size: 12px">Figure from the paper, "Neural Machine Translation by Jointly Learning to Align and Translate (2015)</footer>

-----
<iframe style="width:100%;height:100vh" src="https://jalammar.github.io/how-gpt3-works-visualizations-animations/"></iframe>

-----
## Few-shot learning
<!-- .slide: data-background="white" -->
<img src="https://opendatascience.com/wp-content/uploads/2020/08/gpt3header-1.png">


-----
<!-- .slide: data-background="white" -->
## Further reading

 * [Transformers, Explained](https://daleonai.com/transformers-explained)
 * [How GPT-3 works](https://jalammar.github.io/how-gpt3-works-visualizations-animations/)
 * [On the Opportunities and Risks of Foundation Models](https://fsi.stanford.edu/publication/opportunities-and-risks-foundation-models)

-----
## Codex
 * OpenAI Codex is a descendant of GPT-3
 * GPT-3 trained on billions of lines of source code
 * Longer context (upto 4096 tokens)

-----
# 🔥Codex live demos!
## disclaimer: All the demo applications have not yet been approved for launch
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
### 5. Copilot in vscode
[Signup here](https://copilot.github.com/)

🔥Voice programming demo by Anthony Cesnik

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
 * Show and tell: Provide context and examples
 * Use API document
 * Make it clear what you want either through instructions, examples, or a combination of the two.
 * Hidden context + user input => magical application

-----
## Why Codex is important?
 * Better generalization and interpretability
 * Zero/Few-shot learning for low data domain
 * Human + AI
 * Applications in life science

-----
## Discussion
 * Drawbacks and criticisms
 * GPT-4?
 * Ethical issues
 * What do you think?

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
