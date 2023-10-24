# NVIDIA-Now-Research-Project

# Project Update
So far, I have focused on getting some firsthand experience with the NVIDIA Now product by playing select games streamed from the cloud and then comparing them with a local copy of the same game. 
On top of that, I have read through multiple technical blogs that NVIDIA has posted. Many of these were to do with how they are compressing video. A couple of areas that have caught my eye are NVIDIAs 
new Ada GPUs and the NVENC AV1 compression codec. The frame splitting capabilities of the Ada GPU look extremely promising. By the Adas hardware design, video data can be compressed in parallel by means of 
multiple encoders in the GPU, enabling parallel encoding of data instead of the serialized encoding which is done on other GPUs. This is specifically exciting as the number of users using the product have 
steadily incrased. As a result, data streams flowing upstream to the NVIDIA servers are causing issues with the latency and quality, which are two very important factors in cloud gaming. With this, the 
amount of streams, or users, will be irrelevent (*) to the overall quality of NVIDIA Now for all users using it.


The NVENC AV1 codec is equally as interesting. As is said on a NVIDIA blog post, "AV1 is the new gold standard video format, with superior efficiency and quality compared to older H.264 and H.265 formats.",
giving us an insight to the thoughts of experts on this new method. To illustrate the effect the AV1 codec has compared to its predecessors, the next image show both NVENC H.264 and NVENC AV1 encodings of 
a still frame of video game gameplay, both in 1080p60 with 60Mbps data rate. 

![image](https://github.com/AngusMilne17/NVIDIA-Now-Research-Project/assets/78343375/6666448b-0728-4cb6-b7cd-f288d4ebba73)

It is clear how much of a quality improvement the newer codec can achieve all without increasing the size of the data needed to represent it. To put some numbers to this, the AV1 encoding "~1.5-2 dB higher"
peak signal-to-noise ratio (PSNR) PSNR compared to NVENC H.264 at the same bit rate", with the key phrase there being "at the same bitrate". Even more AV1 favoring results like these are all over.  

# Going Forward

As the semester goes on, even more research into NVIDIA Now will be done. First of all would be getting a better understanding of the Ada GPU and understanding the mechanism behind the AV1 codec, but other 
aspects of NVIDIA Now as well, such as: 
  - proximities of data centers
  - adaptive bitrate streaming
  - keyframe insertion
  - latancey analysis and how that affects how data is sent
and more as I dive deeper into the area.

Eventually I want to get into predictive and "buffering" methods for cloud gaming.

# Links
(1)	https://developer.nvidia.com/blog/improving-video-quality-and-performance-with-av1-and-nvidia-ada-lovelace-architecture/
(2)	https://developer.nvidia.com/blog/av1-encoding-and-fruc-video-performance-boosts-and-higher-fidelity-on-the-nvidia-ada-architecture/

(3) https://arxiv.org/pdf/2008.06091.pdf


(*) I say irrelevent, but there will always be some cost to this processing power.
