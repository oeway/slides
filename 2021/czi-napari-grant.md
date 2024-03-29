<img style="width: 100vw" src="https://docs.google.com/drawings/d/e/2PACX-1vQIa26wyOOlnLYLcVZECV-784YBF4PmQVDdlVabrB2ymrwd5BvUalVrtSir8YAkzR9gsszWa7cnJs9p/pub?w=961&amp;h=599">
-----
## Deep learning models for napari via the BioImage Model Zoo
Wei Ouyang
KTH | SciLifeLab, Stockholm

Joint grant with Anna Kreshuk and Florian Jug Group


-----
## Sharing deep learning models
 * Traning models is challenging <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
 * Pretrained models, generalist models <!-- .element: class="fragment fade-up" data-fragment-index="2" -->
 * Model & weights file format <!-- .element: class="fragment fade-up" data-fragment-index="3" -->
 * Search and find models <!-- .element: class="fragment fade-up" data-fragment-index="4" -->
 * Interoperability between consumer software <!-- .element: class="fragment fade-up" data-fragment-index="5" -->
 * Reducing the carbon footprint! <!-- .element: class="fragment fade-up" data-fragment-index="6" -->

-----
# <img alt="BioImage Model Zoo" src="https://bioimage.io/static/img/bioimage-io-logo-white.svg">
### Advanced AI models in one click!

-----
<!-- .slide: data-background="white" -->
### 🤔How it works

<img style="height:calc(100% - 200px);object-fit:contain;background-color: white;" src="https://docs.google.com/drawings/d/e/2PACX-1vSh8qO-jxZcGKjg5w52IMTesAUMbOaOxc3XQgmW7zBBj6btMGAUjcgh6iHgaTyzI18Ld7SSHkbie2k2/pub?w=1057&amp;h=689">

-----
## Model sharing infrastructure for napari <svg class="w-4 h-4 screen-875:w-6 screen-875:h-6 mr-1" width="60" style="margin-bottom: -10px;" height="60" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M27.8387 0H2.16127C0.967636 0 0 0.967636 0 2.16127V27.8387C0 29.0324 0.967636 30 2.16127 30H27.8387C29.0324 30 30 29.0324 30 27.8387V2.16127C30 0.967636 29.0324 0 27.8387 0Z" fill="#26283D"></path><path d="M27.7779 1.03139H2.22356C1.56514 1.03139 1.03139 1.56514 1.03139 2.22357V27.7779C1.03139 28.4363 1.56514 28.9701 2.22356 28.9701H27.7779C28.4363 28.9701 28.9701 28.4363 28.9701 27.7779V2.22357C28.9701 1.56514 28.4363 1.03139 27.7779 1.03139Z" fill="url(#paint0_radial)"></path><path d="M17.4655 27.3361C17.099 27.3361 16.7542 27.3201 16.4124 27.2897C16.0096 27.2645 15.61 27.202 15.2187 27.1028C14.4296 26.8759 13.6918 26.4986 13.0459 25.9918C12.1394 25.2971 11.3826 24.4265 10.8209 23.4322C10.5949 23.0338 10.3863 22.4775 9.83293 20.9899C9.71125 20.661 9.61999 20.4104 9.54321 20.2091C9.36359 19.7209 9.3042 19.5558 9.15789 19.2385C8.96705 18.7853 8.73274 18.3516 8.45823 17.9435C8.12277 17.4768 7.73384 17.0509 7.29937 16.6745C7.13279 16.5297 7.05601 16.4616 6.91405 16.3515C6.73732 16.2067 6.49396 16.0183 6.02752 15.6098C5.2395 14.9174 4.94254 14.5958 4.66876 14.2453C4.25597 13.7417 3.92726 13.1748 3.69532 12.5664C3.49242 12.0272 3.37416 11.4599 3.34476 10.8846C3.32978 10.3829 3.38289 9.88145 3.50265 9.39401C3.69467 8.45513 4.01235 7.54642 4.44713 6.69241C4.7481 6.05734 5.13833 5.46858 5.60599 4.94398C6.16001 4.34736 6.8007 3.83754 7.50652 3.43167C7.8302 3.24114 8.16941 3.07832 8.52052 2.94495C9.04221 2.75721 9.59283 2.66258 10.1473 2.66537C10.6436 2.66652 11.1376 2.73375 11.6161 2.86528C12.5756 3.10049 13.433 3.64024 14.0599 4.40366C14.7204 5.22066 14.987 6.2477 15.2028 7.63978C15.2578 8.00193 15.2796 8.18879 15.2984 8.35248C15.31 8.46547 15.323 8.57846 15.352 8.77836C15.5273 9.97199 15.6142 10.5167 15.8141 10.9324C16.1038 11.5408 16.6572 11.8957 17.0208 12.1304C17.9131 12.7098 18.8344 12.788 19.4442 12.8416C19.6847 12.8633 19.9585 12.8749 20.2569 12.8749C20.703 12.8749 21.0739 12.8503 21.2115 12.8402C21.4853 12.8199 21.7141 12.7938 21.9358 12.7677C22.272 12.7223 22.6106 12.6972 22.9498 12.6924C23.3746 12.6921 23.7976 12.7491 24.2071 12.8619C25.0966 13.067 25.8989 13.547 26.5002 14.2337C27.1101 14.958 27.2738 15.6721 27.4795 16.5804C27.6193 17.187 27.707 17.8044 27.7417 18.4259C27.7764 19.1313 27.8242 20.0946 27.4925 21.2303C27.1727 22.2747 26.6228 23.234 25.8831 24.0377C25.1073 24.908 24.1734 25.6233 23.1309 26.1453C22.5393 26.4354 21.9207 26.6669 21.2839 26.8363C20.4006 27.0835 19.4935 27.2365 18.578 27.2926C18.1912 27.3216 17.8175 27.3361 17.4655 27.3361Z" fill="#26283D"></path><path d="M17.4655 26.2265C17.1323 26.2265 16.8194 26.2134 16.5109 26.1859C16.1688 26.1658 15.8293 26.1139 15.4969 26.0309C14.8468 25.8412 14.2394 25.5279 13.7079 25.1082C12.924 24.5046 12.2698 23.7494 11.7842 22.8875C11.6016 22.5645 11.3873 21.9908 10.8701 20.6031C10.7484 20.2786 10.6586 20.0323 10.5804 19.8295C10.4008 19.3385 10.3269 19.1342 10.1618 18.7764C9.94359 18.2639 9.6768 17.7735 9.36504 17.3119C8.98218 16.7792 8.53831 16.293 8.04249 15.8633C7.84694 15.6852 7.74264 15.6026 7.59778 15.4882C7.41961 15.3433 7.19942 15.1738 6.75471 14.7842C6.03042 14.1497 5.76968 13.8672 5.53791 13.5703C5.19569 13.1552 4.92274 12.6875 4.7296 12.1854C4.41134 11.3736 4.36059 10.4814 4.58474 9.63882C4.75558 8.79295 5.04066 7.97424 5.43216 7.20521C5.68904 6.6581 6.02321 6.15074 6.42443 5.69869C6.89941 5.18449 7.44931 4.74497 8.05553 4.39498C8.32534 4.23625 8.6078 4.1001 8.90005 3.98793C9.29948 3.84394 9.72125 3.77185 10.1458 3.77499C10.5448 3.77727 10.9417 3.83182 11.3264 3.93723C12.0597 4.10871 12.7166 4.51577 13.1965 5.09609C13.6311 5.6422 13.8846 6.37663 14.1062 7.80492C14.1584 8.14389 14.1772 8.31048 14.1946 8.47127C14.2076 8.5944 14.2221 8.71753 14.254 8.93481C14.4336 10.1531 14.5321 10.8252 14.8146 11.4104C15.2492 12.2984 15.9734 12.7735 16.4182 13.056C17.5394 13.7803 18.6692 13.8817 19.3443 13.9425C19.6166 13.9672 19.9237 13.9788 20.2554 13.9788C20.7393 13.9788 21.142 13.9527 21.2941 13.9411C21.5838 13.9194 21.8387 13.8904 22.0604 13.8643C22.3529 13.8246 22.6474 13.8019 22.9425 13.7962C23.2691 13.7958 23.5942 13.8401 23.9087 13.9281C24.2796 14.028 25.0502 14.238 25.647 14.9421C26.0816 15.4592 26.2062 16.001 26.393 16.8252C26.5186 17.3689 26.5976 17.9223 26.6292 18.4795C26.661 19.14 26.7016 19.9614 26.422 20.9174C26.1469 21.8088 25.6746 22.6267 25.0401 23.3105C24.3582 24.0719 23.5378 24.6968 22.6224 25.1516C22.0928 25.4117 21.5387 25.6184 20.9681 25.7687C20.1555 25.9947 19.3214 26.1345 18.4795 26.1859C18.1333 26.2192 17.7929 26.2265 17.4655 26.2265Z" fill="#A59678"></path><path d="M9.21149 4.83535C10.0328 4.53405 10.8513 4.74409 11.0946 4.80783C11.6453 4.93454 12.1384 5.24019 12.4969 5.67697C12.8199 6.07533 13.0212 6.69098 13.2211 7.95558C13.3124 8.5437 13.295 8.56978 13.366 9.07823C13.5529 10.3472 13.6644 11.1062 14.0077 11.816C14.548 12.9314 15.4563 13.521 15.9329 13.8267C17.2366 14.6726 18.5403 14.7885 19.2646 14.8537C19.9624 14.9053 20.663 14.9053 21.3607 14.8537C22.4718 14.7711 22.9121 14.6045 23.6712 14.8117C24.0058 14.9015 24.549 15.0579 24.9546 15.536C25.2443 15.8851 25.337 16.2603 25.5109 17.0324C25.625 17.5246 25.6967 18.0257 25.7253 18.5302C25.7571 19.169 25.7904 19.86 25.5543 20.6697C25.3157 21.4363 24.906 22.1387 24.3563 22.7238C23.7531 23.3969 23.027 23.9485 22.2168 24.3491C21.736 24.5834 21.2327 24.7683 20.7146 24.901C19.9602 25.1106 19.1857 25.2397 18.4042 25.2863C17.7992 25.3373 17.1911 25.3373 16.5862 25.2863C16.2975 25.2698 16.0109 25.2267 15.7301 25.1574C15.1926 24.9997 14.6912 24.7384 14.254 24.3882C13.5654 23.8599 12.9908 23.1976 12.5649 22.4413C12.4201 22.1806 12.1811 21.5476 11.7088 20.2801C11.2916 19.1603 11.2323 18.943 10.9845 18.3969C10.7451 17.8345 10.451 17.297 10.1067 16.7919C9.68854 16.2019 9.20233 15.6632 8.65814 15.1869C8.19314 14.7639 8.16417 14.8044 7.35442 14.0961C6.64751 13.4761 6.43168 13.2342 6.25205 13.0053C5.96697 12.6629 5.73947 12.2764 5.57846 11.8609C5.45202 11.5217 5.37825 11.1651 5.35973 10.8035C5.35202 10.4734 5.39004 10.1439 5.47272 9.82425C5.62675 9.05475 5.88556 8.31001 6.24191 7.61082C6.46342 7.13752 6.75173 6.69847 7.09802 6.3071C7.32105 6.06667 7.56328 5.84479 7.82231 5.64366C8.03967 5.47474 8.26863 5.3213 8.50748 5.18446C8.73275 5.05002 8.96813 4.93329 9.21149 4.83535V4.83535Z" fill="url(#paint1_linear)"></path><defs><radialGradient id="paint0_radial" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(15 15) scale(28.521)"><stop stop-color="#746B7F"></stop><stop offset="0.12" stop-color="#615B6F"></stop><stop offset="0.26" stop-color="#514C60"></stop><stop offset="0.37" stop-color="#4B475B"></stop><stop offset="0.44" stop-color="#4F4B5F"></stop><stop offset="0.51" stop-color="#5A566C"></stop><stop offset="0.59" stop-color="#6D6881"></stop><stop offset="0.67" stop-color="#87829E"></stop><stop offset="0.74" stop-color="#A9A2C3"></stop><stop offset="0.78" stop-color="#BCB5D9"></stop></radialGradient><linearGradient id="paint1_linear" x1="5.54949" y1="7.79624" x2="23.9884" y2="23.7393" gradientUnits="userSpaceOnUse"><stop offset="0.05" stop-color="#448491"></stop><stop offset="0.15" stop-color="#4A7986"></stop><stop offset="0.33" stop-color="#506E7B"></stop><stop offset="0.52" stop-color="#526A77"></stop><stop offset="0.6" stop-color="#56707C"></stop><stop offset="0.7" stop-color="#607F8B"></stop><stop offset="0.82" stop-color="#7099A3"></stop><stop offset="0.94" stop-color="#87BDC4"></stop><stop offset="1" stop-color="#94D1D6"></stop></linearGradient></defs></svg>
 * Simplify the development of AI-powered plugins
 * Load models from the BioImage Model Zoo
 * Enable sharing of pretrained AI models across plugins and other tools
 * Run models in the cloud via the BioEngine
-----
### Targeted audience: napari developers
<img style="width: 100vw" src="https://docs.google.com/drawings/d/e/2PACX-1vTiVaKFJbJRpkJKzpYCsxwW4Kx4k6yD8cAdZv6Cieae4a0V6AcJUnJEKxzsY7siSgx0D29WEQ1UpRGE/pub?w=950&amp;h=518">

-----
## Working plan
 * Utility library for interacting with resources in the model zoo
 * A test suite for CI testing against napari
 * Example models and plugins
 * Connect napari to our cloud model serving infrastructure
 * Connecting to the napari plugin hub website with the model zoo

-----
## Milestones
* M1: Release of the first napari plugin
* M2: Listing of the first napari-compatible model in the BMZ
* M3: Public release of the libraries, documentation and contribution guidelines 

-----
## Collaborations: Napari + BioImage Model Zoo
 * Help napari users to use models in the model zoo
 * Help your plugins to consume or produce compatible models
 * Advertise your AI models and plugins
 * Run AI models through our cloud infrastructure
 * Join us as a community partner!

-----
### Acknowledgements

Thank Chan Zuckerberg Initiative for the napari Plugin Accelerator Grant!

BioImage.IO is powered by the 🧠 and ❤️ of:
 * deepImageJ Team
 * EBI Bioimage Archive Team
 * Fiji/ImageJ Team
 * ilastik Team
 * ImJoy Team
 * ZeroCostDL4Mic Team
 * ...

-----
### Acknowledgements

Work supported by the Cell Profiling group headed by Emma Lundberg

Follow us on twitter @bioimageio

-----

# 🙏Thank You!
