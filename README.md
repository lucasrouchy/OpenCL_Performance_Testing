# OpenCL_Performance_Testing

## Introduction
This project is focused on measuring matrix multiplication performance using OpenCL.
This aims to visualize how GPU threads operate in OpenCL. Each GPU thread operates in groups of 32 known as warps. 
With this knowledge the results from the graphs become more understandable. 
When GPU threads operate in parallel on a block with size 64 one thread can work on items 0-31 while the second thread does items 32-63. This allows for peak optimization when blocks have a local size of 64 as you can see in the performance graphs.
It is important to note this program was ran on the OSU DGX server which uses NVidia chipsets which are generally considered to be better suited for CUDA.

DGX server specs:
• 16 NVidia Tesla V100 GPUs
• 28TB of disk, all SSD
• two 24-core Intel Xeon 8168 Platinum 2.7GHz CPUs
• 1.5TB of DDR4-2666 System Memory
• Runs the CentOS 7 Linux operating system
Overall compute power:
• Each V100 NVidia Tesla card has 5,120 CUDA Cores and 640 Tensor Cores
• This gives each16-V100 DGX server a total of 81,920 CUDA cores and 10,240 Tensor cores

## Table
Performance Metric is GigaMultiplies per second which means how many billion multiplications can be done per second.
<img width="779" alt="Screenshot 2023-10-23 at 6 23 20 PM" src="https://github.com/lucasrouchy/OpenCL_Performance_Testing/assets/55973521/988b68a6-3a22-4185-8578-0561d859cff5">

## Graphs
<img width="929" alt="Screenshot 2023-10-23 at 6 25 33 PM" src="https://github.com/lucasrouchy/OpenCL_Performance_Testing/assets/55973521/7cd2949a-37f1-4f44-9841-d5378e3e5347">

<img width="932" alt="Screenshot 2023-10-23 at 6 25 57 PM" src="https://github.com/lucasrouchy/OpenCL_Performance_Testing/assets/55973521/df927c61-7f58-49e0-a9f6-e5807c575e14">






