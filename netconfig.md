# Network configuration

> The Spacemesh App (the App) should work on most home broadband Internet connections without a need to manually configure your network or firewall. If you see a network connection error in the App then try following the steps described below to resolve this issue.

## Overview

In order to participate in the Spacemesh network and to earn smeshing rewards your network and computer firewall (and in some cases your home network router) needs to be configured, so the App is able to accept incoming Internet connections on `port 7513` for both `TCP` and `UDP`.

The App attempts to automatically configure your network using UPnP so in most cases you do not need to manually configure your network to support Spacemesh.


## Computer Clock Configuration
Please make sure that your computer clock is synced to a time server such as `time.windows.com` or `time.apple.com`. You must be synced to NTP time to be able to connect to the Spacemesh network.

> Verify you are synced with an NTP server using your computer's `Date & Time` settings.

## Windows 10

### Security Alert on first run

> You may see a Windows security alert when you launch the App for the first time. Check the checkbox 'Private networks' and click 'Allow access'.

If you didn't click on `Allow access` when prompted by Windows, you may need to manually permit the App to receive connections from the internet on TCP port 7513 and on UDP port 7513.

> Follow these instructions to configure incoming connections rules for these two ports.

### TCP Port 7513 Rule

1. Type `Firewall` in your Windows task bar search box.
2. Open the `Windows Defender Firewall` app from the search results.
3. Click on `Advanced settings`.
4. Right-click `Inbound Rules` and select `New Rule...`.
5. Select `Port` for the new rule type and click `Next`.
6. Select `TCP` and, enter `7513` in the `Specific local ports` text box click `Next`.
7. Select `Allow the connection` in the next screen and click `Next`.
8. Don't change the default options in the `Apply Rule` screen and click `Next`.
9. Name the rule `Spacemesh TCP` and click Finish.


### UDP Port 7513 Rule

1. Type `Firewall` in your Windows task bar search box.
2. Open the `Windows Defender Firewall` app from the search results.
3. Click on `Advanced settings`.
4. Right-click `Inbound Rules` and select `New Rule...`.
5. Select `Port` for the new rule type and click `Next`.
6. Select `UDP` and, enter `7513` in the `Specific local ports` text box click `Next`.
7. Select `Allow the connection` in the next screen and click `Next`.
8. Don't change the default options in the `Apply Rule` screen and click `Next`.
9. Name the rule `Spacemesh UDP` and click Finish.



## OS X
The App may be able to accept incoming connections by default depending on your Firewall settings. For example, when you download a signed app distribution from Spacemesh.

Follow these steps if you see a connection error status displayed in the App.

1. Open the `System Preferences App`.
2. Click on `Privacy and Security`.
3. Click on the `Firewall` tab.
4. Click the `Firewall Options` button.
5. Uncheck the `Block all incoming connections` checkbox if it is checked.
6. Check the `Automatically allow downloaded signed software to receive incoming connections` checkbox OR add the `Spacemesh App` to the list of apps and chose `Allow incoming connections` for it.
7. Click OK.

For additional information about the OS X Firewall please [read this guide](https://support.apple.com/en-il/HT201642) from Apple.


## Linux
If you are running Linux then you should be able to configure your firewall via the command line. Check your linux distribution documentation for additional info.

---

## Router Configuration

Your home router or Internet access point (or both) may be blocking the App from receiving data from the network. The App attempts to automatically configure your router using UPnP so in most cases you do not need to manually configure your router.

If you still can't connect to the p2p network then you need to configure your router to forward both UDP and TCP incoming network traffic on port 7513 to the computer that you are running the App on.

To configure your router follow the instructions provided by your router hardware maker for your router model.
