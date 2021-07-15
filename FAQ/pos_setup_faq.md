# Tweedledum (0.2) Proof of Space Setup FAQ

## How long is it going to create Proof of Space data?

The exact time depends on your GPU or CPU capabitlites and the amount of space you commit, but it should be around 12-24 hours for 250GiB using a mid-level discrete GPU card. We will publish more accurate estimates closer to mainnet.

## How often do I need to do the setup?

Only once, and you can use the data as long as you keep the files.

## Can I add or remove committed space after the first time I set up Proof of Space data?

Yes.

## Will I need to redo the entire Proof of Space data setup if I add more space?

No, the process will only be required for the additional space, and not the space you've already committed.

## Do I need a GPU to create Proof of Space data?

No, but creating the data with your CPU will take much longer than with GPU.

## What kind of GPUs can I use to create the PoST data?

- A GPU and drivers with CUDA 11.0 support amd (with minimum compute compatibility 5.0 and maximum compute compatibility 8.6) such as a modern Nvidia GPU and Nvidia drivers version R450 or newer 
- A GPU and drivers with Vulkan 1.2 support such as a modern AMD, Apple M1 processor, and Intel GPU
- Both discrete and on-board GPUs are supported as long as they support the minimum CUDA or Vulkan runtime version.

## What are the GPU memory requirements?

### Minimum GPU RAM:
- 16 KiB per CUDA core for CUDA
- 4 MiB per compute unit for Vulkan

### Recommended GPU RAM:
- 2080 MiB

## Do I need a GPU to run a node after initial setup is done?

No. You only need a GPU to efficiently create the initial PoST data, and it will not be used by the node in any way once this setup is done.

## Is it possible to have multiple GPUs create proof of space data in parallel?

Yes, but the software for this needs to be written by the community. We are focused on software for the baseline users who have only one or no GPU.

## How about SSD, RAM and CPU requirements when creating Proof of Space data?

No SSD is needed. No extra space larger than the committed size is needed. The init process is not RAM-intensive and doesn't require a large amount of memory beyond having some free memory for apps on your computer. If a GPU is used, the process is not CPU-intensive and does not require some threads to do constant work.

## How many times will the process write on my disk?

Only once per setup.
