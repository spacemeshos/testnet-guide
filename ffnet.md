# Friends & Family Net (ffnet)

## Welcome!
Welcome, dear Spacemesh friend, to the Spacemesh ffnet! This is an early tech preview of the Spacemesh App and full node. Expect things to be rough around the edges and for some things that should be automated to be manual and sub-optimal. This is only temporary.

## What to expect?

Chaos and broken things and a sub-optimal user experience, but also a glimpse of an awesome near future where anyone in the world can mine a fair cryptocurrency from home using their existing computer, while still being able to play FortNite and without understanding what CLI and Terminal mean. 🤓

## Why are we doing this?

We want to give you a sneak peek of the Spacemesh technology and product, test them with your help, and improve them with your feedback!

## Joining

1. Join the [ffnet discord channel](https://discord.gg/KyyQKst). On this channel we will provide additional info, answer your questions, announce app updates, and get your feedback!

2. To join the ffnet, you need to run the Spacemesh App on an always-on desktop computer. Please ensure that your system meets the [recommended system requirements](requirements).

!> Please do NOT attempt to join from a laptop if you often move between different WIFI networks. Things will not work properly.

!> Please do NOT join if your computer or network connection doesn't meet the recommended requirements.

3. Download the App installer and run it to install the App:

        [Spacemesh App Installer (ffnet release)](#)


4. Before running the Spacemesh App for the first time, please configure your network to forward TCP and UDP packets on a specific port number to your computer and your computer firewall to accept incoming TCP and UDP packets on this port. Please [follow this guide](netconfig.md). Note that you can use any port and not just 7153.

!> You will NOT be able to join the network unless you have completed this step.

5. Run the Spacemesh App. You will be prompted to enter a port number. Enter the port number you have configured to be forwarded to your computer and to accept incoming packets from the Internet.

6. Proceed to set up wallet and smeshing. [Follow this guide](/guide/setup) for step by step instructions.

> You should start getting your first smeshing reward in 24-49 hours from the time you finish the smeshing setup. Just leave the app open (minimize the main window) until you get your first reward.


## Getting some Smesh
You can also request some Smesh from the ffnet tap by copying and pasting your account address from your wallet screen into the [ffnet discord channel](https://discord.gg/KyyQKst). This should allow you to execute Smesh transactions before getting your first reward.

## Peeking Under the Hood
The logs of the full node managed by the app are saved as `spacemesh-log.txt` in your documents folder.

To view the logs in realtime open a Terminal and type:
- Windows 10: `Get-Content $HOME/documents/spacemesh-log.txt -Wait -Tail 1`
- OS X and Linux: `tail -f ~/documents/spacemesh-log.txt`

## Helping us to improve Spacemesh
You can help us to improve Spacemesh by reporting any bug or issue you come across while using the App. Learn how to [submit a bug report](issues). When submitting report - please always attach your log file.

## How long will this net run?
Until we soft launch the open Spacemesh testnet. Likely around 2-3 weeks.

## How do I give feedback or get help?
Use the [ffnet discord channel](https://discord.gg/KyyQKst).

## Major Known Issues
- Slow transaction confirmation time. We only report the `confirmed` state but not the `approved` state, therefore it will take up from 15 to 20 minutes for transactions to get confirmed. Once we add the `approved` state, transactions should be approved in about 3 minutes.
- Insufficient node statuses display in the smeshing tab. We plan to display node sync and network status in this tab, so users can tell what their node is doing.
- Most of the issues we have occur when stopping a running node and trying to sync again. As such, it's best if you can leave the app open 24x7 on your computer and minimize app restarts.
