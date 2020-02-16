# Friends & Family Net (ffnet)

## Welcome!
Welcome, dear Spacemesh friend, to the Spacemesh ffnet! This is an early tech preview of the Spacemesh App and full node. Expect things to be rough around the edges and for some things that should be automated to be manual and sub-optimal. This is only temporary.

![](images/v1.0/welcome.png)

## What to expect?

Chaos and broken things and a sub-optimal user experience, but also a glimpse of an awesome near future where anyone in the world can mine a fair cryptocurrency from home using their existing computer, while still being able to play FortNite and without understanding what CLI and Terminal mean. 🤓

## Why are we doing this?

We want to give you a sneak peek of the Spacemesh technology and product, test them with your help, and improve them with your feedback!

## Joining

1. Join the [ffnet discord channel](https://discord.gg/KyyQKst). On this channel we will provide additional info, answer your questions, announce app updates, and get your feedback!

2. To join the ffnet, you need to run the Spacemesh App on an always-on desktop computer. Please ensure that your system meets the [minimum system requirements](requirements).

!> Please do NOT attempt to join from a laptop if you often move between different WIFI networks or put it to sleep. Things will not work properly.

!> Please do NOT join if your computer or network connection doesn't meet the recommended requirements.

3. Download the App installer for your platform and run it to install the App:

[Spacemesh App Installers - (ffnet release)](https://tinyurl.com/sl5jpxc)

4. Run the Spacemesh App. You will be prompted to enter a port number. Enter `7153`.

5. Quit the App and copy the file `peers.json` from the installers g drive folder to the following directory:

- OS X: `/Users/[your_user_name]/Library/Application Support/Spacemesh/spacemeshtestdata/p2p/`

- Windows: `C:\Users\[your_user_name]\AppData\Roaming\Spacemesh\spacemeshtestdata\p2p`

- Linux: `~/.config/Spacemesh/spacemeshtestdata/p2p`

> We know this ia a major PITA - just go online to the [ffnet discord chat channel](https://discord.gg/KyyQKst) if you get stuck and we'll help you out. Upcoming releases are not going to require this hack.



6. Start the app again, enter `7153` as part and Proceed to set up wallet and smeshing. [Follow this guide](/guide/setup) for step by step instructions.

> You should get your first smeshing reward in 24-49 hours from the time you finished the smeshing setup. Just leave the app open (minimize the main window) until you get your first reward.


## Getting some Smesh
You can also request some Smesh from the ffnet tap by copying and pasting your account address from your wallet screen into the [ffnet discord channel](https://discord.gg/KyyQKst). This should allow you to execute Smesh transactions before getting your first reward.

## Peeking Under the Hood
To view the logs in realtime open a Terminal and type:
- Windows 10 Poweshell: `Get-Content ~\AppData\Roaming\Spacemesh\spacemesh-log.txt -Wait -Tail 1`
- OS X: `tail -f ~/Library/Application\ Support/spacemesh/spacemesh-log.txt`
- Linux: `tail -f ~/.config/Spacemesh/spacemesh-log.txt`
- Node sync status: `curl -d '' localhost:9090/v1/nodestatus`

## Helping us to improve Spacemesh
You can help us to improve Spacemesh by reporting any bug or issue you come across while using the App. Learn how to [submit a bug report](issues). When submitting report - please always attach your log file.

## How long will this net run?
Until we soft launch the open Spacemesh testnet. Likely around 2-3 weeks.

## How do I give feedback or get help?
Use the [ffnet discord channel](https://discord.gg/KyyQKst).

## Major Known Issues
- Slow transaction confirmation time. We only report the `confirmed` state but not the `approved` state, therefore it will take up from 15 to 20 minutes for transactions to get confirmed. Once we add the `approved` state, transactions should be approved in about 5 minutes (between 3 and 8 minutes).
- Insufficient node statuses display in the smeshing tab. We plan to display node sync and network status in this tab, so users can tell what their node is doing.
- Most of the issues we have occur when stopping a running node and trying to sync again. As such, it's best if you can leave the app open 24x7 on your computer and minimize app restarts.
