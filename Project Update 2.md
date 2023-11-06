# Project Update

In the past few weeks, I have continued to look into AV1 video codec and the GPUs used in the NVIDIA Now data servers. I have been looking at a more techinical overview
of both AV1, how frames are partitioned into blocks and how the blocks are then transformed and quantized and finally entropy encoded, and the Ada GPU architecture, what
encoders are used as well as how parallelizm is achieved. 

# Changes to my Topic

Originally, I was looking at NVIDIA Now in terms of reducing latency while maintaining or improving quality and user usability. This is still the premise of the 
project, however, I have now split the analyzsis into two parts. The first is to do with the new RTX 4000 series graphics cards, these include AV1 encoders as well as
Ada Lovlace architecture

I have realized that the scope of this topic leaves a lot of room for surface level research that would not be insightful. So, I have decided to focus on
a couple of aspects of the NVIDIA system and then research their effects on latency, quality, and user experience. I will focus specifically on the AV1 codec and Ada GPU architecture
as previously mentioned, but also on the NVIDIA Relfex sdk, which I have not previouslt mentioned. NVIDIA Reflex in a way is a combination of hardware and software which
work to analyze and report on the latency of the gameplay. There have also been some posts about the use of AI in NVIDIA DLSS, which I was thinking of including in the
project.
