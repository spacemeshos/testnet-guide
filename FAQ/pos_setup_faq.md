# Tweedledum (0.2) Proof of Space Setup FAQ

## How long is it going to create Proof of Space data?

The exact time depends on your GPU or CPU capabitlites and the amount of space you commit, but it should be around 12-24 hours for 250GiB using a mid-level discrete GPU card. We will publish more accurate estimates closer to mainnet.

## How often do I need to do the setup?

Only once, and you can use the data as long as you keep the files.

## Will I need to redo the entire Proof of Space data setup if I add more space?

No, the process will only be required for the additional space, and not the space you've already committed.

## Do I need a GPU to create Proof of Space data?

No, but creating the data with your CPU will take much longer than with GPU.

## What kind of GPUs can I use to create the PoST data?

Most AMD and Nvidia cards, Apple M1, Intel graphics cards, and any other GPUs that support CUDA or Vulkan compute.

## Do I need a GPU to run a node after initial setup is done?

No. You only need a GPU to efficiently create the initial PoST data, and it will not be used by the node in any way once this setup is done.

## Is it possible to have multiple GPUs create proof of space data in parallel?

Yes, but the software for this needs to be written by the community. We are focused on software for the baseline users who have only one or no GPU.

## How about SSD, RAM and CPU requirements when creating Proof of Space data?

No SSD is needed. No extra space larger than the committed size is needed. The init process is not RAM-intensive and doesn't require a large amount of memory beyond having some free memory for apps on your computer. If a GPU is used, the process is not CPU-intensive and does not require some threads to do constant work.

## How many times will the process write on my disk?

Only once per setup.
