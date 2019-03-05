**Digital Signal Processing (DSP) and Data Science**

  

RISC-V based Anasim Processor for FPGA (Soft Processor) and ASIC (Hard
Processor) is optimized for Digital Signal Processing (DSP) and
Artificial Intelligence (AI). For more details on RISC-V, please visit
<span lang="zxx"><span class="underline"><https://riscv.org/></span></span>
.

  

Please visit
<span lang="zxx"><span class="underline"><http://www.differencebetween.net/technology/difference-between-asic-and-fpga/></span></span>
to know more on FPGA and ASIC.

  

<span id="__DdeLink__144_360745694"></span> Our Proprietary Anasim
Processor is improved upon RISC-V and extended with DSP (VLSI based) and
AI capabilities which is suitable for FPGA and ASIC implementations. The
Aansim Processor is aimed at AI and DSP related applications at cloud,
in IoT and Edge Devices. We understand that to lower costs and volume
production, customers have to go for ASIC ulitmately. Indian Central and
State Governments may choose SCL
(<span lang="zxx"><span class="underline"><http://www.scl.gov.in/></span></span>)
as their semiconductor partner to fabricate AI Chips (ASIC) based on our
Proprietary Anasim Processor IPCores; for privately owned organizations
we have prototyping and production arrangements with international
semiconductor fabrication facilities, Governments of other friendly
countries may also choose SCL as their semiconductor partner with SCL’s
prior approval. As per our policy we charge for Proprietary IPCores
licensing costs and new IPCore design, development & testing costs;
hardware and fabrication charges are directly born by the customers
resulting in significantly lower per chip costs.

  

  

  

![](dsp-and-data-science_html_1da49f1f1483ef20.jpg)  

  

  

  

  

  

**Convert your AI Research into AI Chip, download our Proprietary Free
of Charge Anasim App (to be made available soon) from Apple iStore to
automate your AI Chip Development Process. Apart from you need not to
spend thousands of US Dollars on licenses of Semiconductor Design,
Synthesis, Verification and Validation Tools and on hiring highly paid
teams of highly skilled Engineers for months to run these Tools for you
in order to design AI Chip for you, the Anasim App lets you:**

**1. Test Trained Data Model on your iPhone/iPad. You may go through the
pre-requisites given below to obtain you Trained Data Model.**

**2. Obtain Anasim AI Soft Processor based on Your Trained Data Model
for your FPGA Board. Both can be flashed with the FPGA flashing tools
mentioned at the bottom of the page. Ship your FPGA board (single piece)
for testing to us if it is not Xilinx Zynq 7000 Zybo Board.**

**3. Connect, Test and Debug your FPGA Board through JTAG USB Cable.**

**4. Obtain technical support from us and resolve your technical
issues.**

**5. Obtain commercial and non-commercial/academic licenses for our
IPCores.**

<span id="__DdeLink__139_3839206482"></span> **6. Know semiconductor
fabrication facilities production schedule including for (Multi Project
Wafer) MPW.**

**7. Obtain commercial quotes from fabrication facilities.**

**8. Make volume and prototype ASIC fabrication order.**

**9. Make payment for the licenses and the order.**

**10. Know order and delivery status.**

<span style="font-weight: normal">We hope that following material and
the material given in this repository will also be helpful for data
scientists in general apart from our Anasim App. </span>

  

**Pre-requisites:**

  

Visitors may soon expect several regularly updated Caffe Model Zoo
trained models optimized ready to run example HDL SoC codes for Xilinx
Zynq 7000 Zybo Board under GPL License for non-commercial/academic use
in this repository. You may also train your models by following the
procedure given below:

  

Please visit
<span lang="zxx"><span class="underline"><http://caffe.berkeleyvision.org/></span></span>
for more information on Caffe and visit
<span lang="zxx"><span class="underline"><http://docker.com/></span></span>
for more information on docker container. Please visit
<span lang="zxx"><span class="underline"><https://aws.amazon.com/docker/></span></span>
to run docker image at Amazon AWS and visit
<span lang="zxx"><span class="underline"><https://docs.microsoft.com/en-us/azure/docker/></span></span>
to run docker image at Microsoft Azure cloud services. Our Caffe
installations are tested with NVIDIA CUDA 10.0 and NVIDIA cuDNN 10.0 on
Ubuntu 18.04 LTS, so please do not expect our free support on Caffe
other than this.

  

  

Please visit
<span lang="zxx"><span class="underline"><https://github.com/BVLC/caffe></span></span>
to download latest version of Caffe to build from scratch or visit
<span lang="zxx"><span class="underline"><http://caffe.berkeleyvision.org/install_apt.html></span></span>
`for Caffe installation steps for Ubuntu.`

  

According to this Caffe Github Site, you may run Caffe docker image as
follows:

  

### <span id="__DdeLink__95_2003088534"></span> <span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal">**Running an official image**</span></span></span>

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">You
can run one of the version:</span></span></span></span>

`docker run -ti bvlc/caffe:cpu caffe
--version`

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">or
for GPU support (You need a CUDA 10.0 capable driver
and </span></span></span></span><span lang="zxx">[<span style="font-variant: normal"><span style="text-decoration: none"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">nvidia-docker</span></span></span></span></span>](https://github.com/NVIDIA/nvidia-docker)</span><span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">):</span></span></span></span>

`nvidia-docker run -ti bvlc/caffe:gpu caffe
--version`

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">You
might see an error about libdc1394, ignore
it.</span></span></span></span>

### <span id="user-content-docker-run-options"></span> <span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal">**Docker run options**</span></span></span>

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">By
default caffe runs as root, thus any output files, e.g. snapshots, will
be owned by root. It also runs by default in a container-private
folder.</span></span></span></span>

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">You
can change this using flags, like user (-u), current directory, and
volumes (-w and -v). E.g. this behaves like the usual caffe
executable:</span></span></span></span>

`docker run --rm -u $(id -u):$(id -g) -v $(pwd):$(pwd) -w $(pwd)
bvlc/caffe:cpu caffe train
--solver=example_solver.prototxt`

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Containers
can also be used interactively, specifying
e.g. </span></span></span></span>`bash`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> or </span></span></span></span>`ipython`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> instead
of </span></span></span></span>`caffe`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></span>

``` western
docker run -ti bvlc/caffe:cpu ipython
import caffe
...
```

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">The
caffe build requirements are included in the container, so this can be
used to build and run custom versions of caffe.
Also, </span></span></span></span>`caffe/python`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> is
in PATH, so python utilities can be used directly,
e.g. </span></span></span></span>`draw_net.py`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">, </span></span></span></span>`classify.py`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">,
or </span></span></span></span>`detect.py`<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></span>

  

### <span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal">**Building images yourself**</span></span></span>

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Examples:</span></span></span></span>

`docker build -t caffe:cpu cpu`

`docker build -t caffe:gpu
gpu`

<span style="font-variant: normal"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">You
can also build Caffe and run the tests in the
image:</span></span></span></span>

`docker run -ti caffe:cpu bash -c "cd /opt/caffe/build; make
runtest"`

  

### `Study Material:`

  

  

<span lang="zxx"><span class="underline">[**http://caffe.berkeleyvision.org/**](http://caffe.berkeleyvision.org/)</span></span>

  

<span lang="zxx"><span class="underline">[**http://caffe.berkeleyvision.org/tutorial/**](http://caffe.berkeleyvision.org/tutorial/)</span></span>

  

<span lang="zxx"><span class="underline">[**http://caffe.berkeleyvision.org/gathered/examples/imagenet.html**](http://caffe.berkeleyvision.org/gathered/examples/imagenet.html)</span></span>

  

<span lang="zxx"><span class="underline">[**http://shengshuyang.github.io/A-step-by-step-guide-to-Caffe.html**](http://shengshuyang.github.io/A-step-by-step-guide-to-Caffe.html)</span></span>

  

<span lang="zxx"><span class="underline">[**http://vision.stanford.edu/teaching/cs231n/slides/2015/caffe\_tutorial.pdf**](http://vision.stanford.edu/teaching/cs231n/slides/2015/caffe_tutorial.pdf)</span></span>

  

<span lang="zxx"><span class="underline">[**https://www.panderson.me/images/Caffe.pdf**](https://www.panderson.me/images/Caffe.pdf)</span></span>

  

<span lang="zxx"><span class="underline">[**http://3dvision.princeton.edu/courses/COS598/2015sp/slides/Caffe/caffe\_tutorial.pdf**](http://3dvision.princeton.edu/courses/COS598/2015sp/slides/Caffe/caffe_tutorial.pdf)</span></span>

  

**Flashing Tools:**

Free of Cost
<span style="font-variant: normal"><span style="letter-spacing: normal">Quartus
II Stand-Alone Programmer from Intel may be downloaded from following
link to flash Altera FPGA based
boards:</span></span>

<span lang="zxx"><span class="underline"><http://fpgasoftware.intel.com/16.1/?product=qprogrammer#tabs-4></span></span>

Free of Cost Vivado Lab Solutions from Xilinx may be downloaded from
following link to flash Xilinx 7 Family FPGA based
boards:

<span lang="zxx"><span class="underline"><https://www.xilinx.com/support/download.html></span></span>

  

*<span style="font-weight: normal">Please go through
AI-Development-and-Deployment-Process.pdf and other files in the
DSP-and-Data-Science repository for more details.</span>*
