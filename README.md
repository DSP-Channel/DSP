**Digital Signal Processing (DSP) and Data Science**


RISC-V based Anasim Processor for FPGA (Soft Processor) and ASIC (Hard
Processor) is optimized for Digital Signal Processing (DSP) and
Artificial Intelligence (AI). For more details on RISC-V, please visit
[[<https://riscv.org/>]{.underline}]{lang="zxx"}


Please visit
[[<http://www.differencebetween.net/technology/difference-between-asic-and-fpga/>]{.underline}]{lang="zxx"}
to know more on FPGA and ASIC.


Our Proprietary Anasim Processor is improved upon RISC-V and extended
with DSP (VLSI based) and AI capabilities which is suitable for FPGA and
ASIC implementations. The Aansim Processor is aimed at AI and DSP
related applications at cloud, in IoT and Edge Devices. We understand
that to lower costs and volume production, customers have to go for ASIC
ulitmately. Indian Central and State Governments may choose SCL
([[<http://www.scl.gov.in/>]{.underline}]{lang="zxx"}) as their
semiconductor partner to fabricate AI Chips (ASIC) based on our
Proprietary Anasim Processor IPCores; for privately owned organizations
we have prototyping and production arrangements with international
semiconductor fabrication facilities, Governments of other friendly
countries may also choose SCL as their semiconductor partner with SCL's
prior approval. As per our policy we charge for Proprietary IPCores
licensing costs and new IPCore design, development & testing costs;
hardware and fabrication charges are directly born by the customers
resulting in significantly lower per chip costs.


**Kindly download Anasim App (to be made available soon) from Apple
iStore to automate your AI Chip Development Process.**


Visitors can expect several regularly updated DSP examples with VHDL
codes under GPL License in this repository soon. Caffe Docker images are
also provided, please visit
[[<http://caffe.berkeleyvision.org/>]{.underline}]{lang="zxx"} for more
information on Caffe and visit
[[<http://docker.com/>]{.underline}]{lang="zxx"} for more information on
docker contain. Please visit
[[<https://aws.amazon.com/docker/>]{.underline}]{lang="zxx"} to run
docker image at Amazon AWS and visit
[[<https://docs.microsoft.com/en-us/azure/docker/>]{.underline}]{lang="zxx"}
to run docker image at Microsoft Azure cloud services. Our docker images
are tested with NVIDIA CUDA 10.0 and NVIDIA cuDNN 10.0 on Ubuntu 18.04
LTS.


Please visit <https://github.com/BVLC/caffe> to download latest version
of Caffe.


According to this site, you may run caffe docker image as follows:


### [[[**Running an official image**]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"} {#running-an-official-image .western align="justify"}

[[[[You can run one of the
version:]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

`docker run -ti bvlc/caffe:cpu caffe --version`{.western}

[[[[or for GPU support (You need a CUDA 10.0 capable driver
and ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}[[[[[[[nvidia-docker]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="text-decoration: none"}]{style="font-variant: normal"}](https://github.com/NVIDIA/nvidia-docker)]{lang="zxx"}[[[[):]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

`nvidia-docker run -ti bvlc/caffe:gpu caffe --version`{.western}

[[[[You might see an error about libdc1394, ignore
it.]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

### []{#user-content-docker-run-options} [[[**Docker run options**]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"} {#docker-run-options .western style="margin-top: 0.64cm; margin-bottom: 0.42cm; line-height: 125%; orphans: 2; widows: 2"}

[[[[By default caffe runs as root, thus any output files, e.g.
snapshots, will be owned by root. It also runs by default in a
container-private
folder.]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

[[[[You can change this using flags, like user (-u), current directory,
and volumes (-w and -v). E.g. this behaves like the usual caffe
executable:]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

`docker run --rm -u $(id -u):$(id -g) -v $(pwd):$(pwd) -w $(pwd) bvlc/caffe:cpu caffe train --solver=example_solver.prototxt`{.western}

[[[[Containers can also be used interactively, specifying
e.g. ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`bash`{.western}[[[[ or ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`ipython`{.western}[[[[ instead
of ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`caffe`{.western}[[[[.]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

``` {.western style="line-height: 145%; orphans: 2; widows: 2; background: #f6f8fa"}
docker run -ti bvlc/caffe:cpu ipython
import caffe
...
```

[[[[The caffe build requirements are included in the container, so this
can be used to build and run custom versions of caffe.
Also, ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`caffe/python`{.western}[[[[ is
in PATH, so python utilities can be used directly,
e.g. ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`draw_net.py`{.western}[[[[, ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`classify.py`{.western}[[[[,
or ]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}`detect.py`{.western}[[[[.]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}


### [[[**Building images yourself**]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"} {#building-images-yourself .western align="justify"}

[[[[Examples:]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

`docker build -t caffe:cpu cpu`{.western}

`docker build -t caffe:gpu gpu`{.western}

[[[[You can also build Caffe and run the tests in the
image:]{style="font-weight: normal"}]{style="font-style: normal"}]{style="letter-spacing: normal"}]{style="font-variant: normal"}

`docker run -ti caffe:cpu bash -c "cd /opt/caffe/build; make runtest"`{.western}


Free of Cost [[Quartus II Stand-Alone Programmer
]{style="letter-spacing: normal"}]{style="font-variant: normal"}[[from
Intel may be downloaded from following link to flash Altera FPGA based
boards:]{style="letter-spacing: normal"}]{style="font-variant: normal"}

<http://fpgasoftware.intel.com/16.1/?product=qprogrammer#tabs-4>

Free of Cost Vivado Lab Solutions from Xilinx may be downloaded from
following link to flash Xilinx 7 Family FPGA based boards:

<https://www.xilinx.com/support/download.html>


*[Please go through AI-Development-and-Deployment-Process.pdf and other
files in the DSP-and-Data-Science repository for more
details.]{style="font-weight: normal"}*


