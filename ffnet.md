# Friends & Family Net (ffnet)

## Welcome!
Welcome, dear Spacemesh friend, to the Spacemesh ffnet! This is an early tech preview of the Spacemesh App and full node. Expect things to be rough around the edges and for some things that should be automated to be manual and sub-optimal.

![](/images/v1.0/release0.0.2.png)

## How to Join?

To join the ffnet, you need to run the Spacemesh App on an always-on desktop computer. Please ensure that your system meets the [minimum system requirements](requirements).

**Step 1.** Download the App installer for your platform and run it to install the App:

> Windows 10: [Spacemesh Setup 0.0.3.exe](https://storage.googleapis.com/smapp/0.0.3/Spacemesh%20Setup%200.0.3.exe)

> OS X: [Spacemesh-0.0.3.dmg](https://storage.googleapis.com/smapp/0.0.3/Spacemesh-0.0.3.dmg)

> Linux: [smapp_0.0.3_amd64.deb](https://storage.googleapis.com/smapp/0.0.3/spacemesh_app_0.0.3_amd64.deb)

**Step 2.** Run the app and setup your wallet and smeshing!

> You should get your first smeshing reward in 24-49 hours from the time you finished the smeshing setup. Just leave the app open (minimize the main window) until you get your first reward.

> Join the [ffnet discord channel](https://discord.gg/KyyQKst). On this channel we provide additional info, answer your questions, announce app updates, and get your feedback!

!> Please do NOT attempt to join from a laptop if you often move between different WIFI networks or put it to sleep. Things will not work properly.

!> Please do NOT join if your computer or network connection doesn't meet the recommended requirements.

## What to expect?
Chaos and broken things and a sub-optimal user experience, but also a glimpse of an awesome near future where anyone in the world can mine a fair cryptocurrency from home using their existing computer, while still being able to play FortNite and without understanding what CLI and Terminal mean. 🤓

## Why are we doing this?

We want to give you a sneak peek of the Spacemesh technology and product, test them with your help, and improve them with your feedback!

## Getting some Smesh
You can also request some Smesh from the ffnet tap by copying and pasting your account address from your wallet screen into the [ffnet discord channel](https://discord.gg/KyyQKst). This should allow you to execute Smesh transactions before getting your first reward.

## How long will this net run?
Until we soft launch the open Spacemesh Tweedledee testnet. Likely until March 1st 2020.

## How do I give feedback, get help or report a bug?
Use the [ffnet discord channel](https://discord.gg/KyyQKst).

---

## Release Notes - Release 0.0.3

- Added mesh info section to the settings.
- Fixed smeshing coinbase address formatting.
- Misc. minor ui improvements and bug fixes.
- Remove unused pause / resume smeshing button from Smesher.

Check out our [issues tracker](https://github.com/orgs/spacemeshos/projects/5) to view additional fixes and known issues.

## Known Issues
- Slow transaction confirmation time. We only report the `confirmed` status but not the `approved` status, therefore it will take up from 15 to 20 minutes for transactions to get confirmed. Once we add the `approved` status, transactions should be approved in about 5 minutes (between 3 and 8 minutes).

- Can't connect to the p2p network or sync

    > Configure your router to forward TCP and UDP traffic to your computer and your computer firewall to not block your computer for accepting TCP or UDP packets on the app's port (defaults to 7153).

    If router configuration doesn't work and you still can't connect to the p2p network then try the following:

    1. Quit the App
    2. Browse [peers.json](https://storage.googleapis.com/smapp/0.0.3/peers.json) and save it to your computer.
    3. Copy peers.json to the following directory:

        - OS X: `/Users/[your_user_name]/Library/Application Support/Spacemesh/spacemeshtestdata/p2p`

        - Windows: `C:\Users\[your_user_name]\AppData\Roaming\Spacemesh\spacemeshtestdata\p2p`

        - Linux: `~/.config/Spacemesh/spacemeshtestdata/p2p`

    4. Start the app again and proceed to set up wallet and smeshing. [Follow this guide](/guide/setup) for step by step instructions.

## Peeking Under the Hood
To view the logs in realtime open a terminal and enter:
- Windows 10 Powershell: `Get-Content ~\AppData\Roaming\Spacemesh\spacemesh-log.txt -Wait -Tail 1`
- OS X: `tail -f ~/Library/Application\ Support/spacemesh/spacemesh-log.txt`
- Linux: `tail -f ~/.config/Spacemesh/spacemesh-log.txt`

Display node sync status: `curl -d '' localhost:9090/v1/nodestatus`
