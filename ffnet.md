# Friends & Family Net (ffnet)

## Welcome!
Welcome, dear Spacemesh friend, to the Spacemesh ffnet! This is an early tech preview of the Spacemesh App and full node. Expect things to be rough around the edges and for some things that should be automated to be manual and sub-optimal.

## What to expect?
Chaos and broken things and a sub-optimal user experience, but also a glimpse of an awesome near future where anyone in the world can mine a fair cryptocurrency from home using their existing computer, while still being able to play FortNite and without understanding what CLI and Terminal mean. 🤓

## Why are we doing this?

We want to give you a sneak peek of the Spacemesh technology and product, test them with your help, and improve them with your feedback!

## How to Join?

To join the ffnet, you need to run the Spacemesh App on an always-on desktop computer. Please ensure that your system meets the [minimum system requirements](requirements).

**Step 1.** Download the App installer for your platform and run it to install the App:

> Windows 10: [Spacemesh Setup 0.0.1.exe](https://storage.googleapis.com/smapp/open_testnet_installers/windows/Spacemesh%20Setup%200.0.1.exe)

> OS X: [Spacemesh-0.0.1.dmg](https://storage.googleapis.com/smapp/open_testnet_installers/osx/Spacemesh-0.0.1.dmg)


> Linux: [smapp_0.0.1_amd64.deb](https://storage.googleapis.com/smapp/open_testnet_installers/linux/smapp_0.0.1_amd64.deb)


> If the above links dont work for you, t installers: [Spacemesh App Installers - (ffnet release)](https://tinyurl.com/sl5jpxc)

**Step 2.** Run the Spacemesh App. You will be prompted to enter a port number. Enter `7153` and continue to setup your wallet and smeshing!

> You should get your first smeshing reward in 24-49 hours from the time you finished the smeshing setup. Just leave the app open (minimize the main window) until you get your first reward.

> Join the [ffnet discord channel](https://discord.gg/KyyQKst). On this channel we provide additional info, answer your questions, announce app updates, and get your feedback!

---

!> Please do NOT attempt to join from a laptop if you often move between different WIFI networks or put it to sleep. Things will not work properly.

!> Please do NOT join if your computer or network connection doesn't meet the recommended requirements.

---

## Getting some Smesh
You can also request some Smesh from the ffnet tap by copying and pasting your account address from your wallet screen into the [ffnet discord channel](https://discord.gg/KyyQKst). This should allow you to execute Smesh transactions before getting your first reward.

## Helping us to improve Spacemesh
You can help us to improve Spacemesh by reporting any bug or issue you come across while using the App. Learn how to [submit a bug report](issues). When submitting report - please always attach your log file.

## How long will this net run?
Until we soft launch the open Spacemesh testnet. Likely around 2-3 weeks.

## How do I give feedback or get help?
Use the [ffnet discord channel](https://discord.gg/KyyQKst).

---

## Known Issues
- Slow transaction confirmation time. We only report the `confirmed` state but not the `approved` state, therefore it will take up from 15 to 20 minutes for transactions to get confirmed. Once we add the `approved` state, transactions should be approved in about 5 minutes (between 3 and 8 minutes).

- Most of the issues we have occur when stopping a running node and trying to sync again. As such, it's best if you can leave the app open 24x7 on your computer and minimize app restarts.

- Can't connect to the p2p network or sync.

    1. Quit the App
    2. Copy the file `peers.json` from the installers g drive extras folder to the following directory:

        - OS X: `/Users/[your_user_name]/Library/Application Support/Spacemesh/spacemeshtestdata/p2p`

        - Windows: `C:\Users\[your_user_name]\AppData\Roaming\Spacemesh\spacemeshtestdata\p2p`

        - Linux: `~/.config/Spacemesh/spacemeshtestdata/p2p`
    3. Start the app again, enter `7153` when asked, and proceed to set up wallet and smeshing. [Follow this guide](/guide/setup) for step by step instructions.

---

## Peeking Under the Hood
To view the logs in realtime open a Terminal and type:
- Windows 10 Powershell: `Get-Content ~\AppData\Roaming\Spacemesh\spacemesh-log.txt -Wait -Tail 1`
- OS X: `tail -f ~/Library/Application\ Support/spacemesh/spacemesh-log.txt`
- Linux: `tail -f ~/.config/Spacemesh/spacemesh-log.txt`
- Node sync status: `curl -d '' localhost:9090/v1/nodestatus`
