# Project Update

In the past few weeks, I have continued to look into AV1 video codec and the GPUs used in the NVIDIA Now data servers. I have been looking at a more techinical overview
of both AV1, how frames are partitioned into blocks and how the blocks are then transformed and quantized and finally entropy encoded, and the Ada GPU architecture, what
encoders are used as well as how parallelizm is achieved. 

# Changes to my Topic

Originally, I was looking at NVIDIA Now in terms of reducing latency while maintaining or improving quality and user usability. This is still the premise of the 
project, however, I have now split the analyzsis into two parts. 

The first is to do with the new RTX 4000 series graphics cards. This will encompass AV1 encoders as well as the Ada architecture. In addition to this, the graphics
cards include new-generation RT cores and Tensor cores and CUDA cores all of which lend a helping hand to the latency and quality problems. This new encompassed topic 
would also allow me to mention the newest version of deep learning super sampling or DLSS 3 and vision AI acceleration which is included in the Ada architecture. Going 
forward I would include these in the analysis of NVIDIA Now.

I wanted to note that I thought that the Ada Lovelace was the actual GPU, but it is in fact just the architecture of the RTX 4000 series GPU. Now, graphics cards are often
defined by the architecture which makes them up, but I thought that interchanging the RTX 4000 series GPU and the Ada lovelace Architecture was mischaracterizing. In any
case, I wanted to broaden that aspect and talk about the RTX 4000s which follows the Ada architecture which INCLUDES all of the previously mentioned components.

The second part will consist of the NVIDIA Reflex and its corresponding sdk for optimizing and measuring latency in cloud gaming. NVIDIA Reflex is, in a way, a 
combination of hardware and software which is used to optimize the latency for a users device by monitoring input registration times and network traffic. I will
further split this topic into two different aspects, network latency and system latency, and will go through what NVIDIA Reflex does to minimize these as well as how
effective it is in doing this.

After the analysis of these two core componenets, I will discuss the effects that these two have on the latency, quality, and user accessability in general, taking 
into account all aspects at the same time.

# Overview of Research Done

### AV1

Starting with the AV1 codec, I learned about how video is actually compressed. The flow is seemingly similar to previous video encoders as seen in the image below,

![image](https://github.com/AngusMilne17/NVIDIA-Now-Research-Project/assets/78343375/c04f02c2-909e-401a-a593-ceb23b63ab25)

but there are many differences in the way each step is performed and the many more options for each step as well. For example, the image below shows the ways to partition
the frame into blocks. Noticing the max block size increased from 64x64 in the VP9(*) codec to 128x128 in AV1 and there are more ways to recursively split the block in AV1
than in VP9.

![image](https://github.com/AngusMilne17/NVIDIA-Now-Research-Project/assets/78343375/fd255f19-db4a-4751-b754-e8719578221c)

All of the additions to partitioning, as mentioned above, prediction, both inter and intra, transformation, quantization, filtering, and entropy encoding that are added in AV1 will
be talked about in the project.

### RTX 4000 Ada GPU

A single slot graphics card with many advantages

![image](https://github.com/AngusMilne17/NVIDIA-Now-Research-Project/assets/78343375/5729d7ba-ed9e-4350-bee6-f881115126fe)


(*) VP9 is most recent video compression algorithm prior to AV1 and is still used a lot today. Many sources compare AV1 to it.
