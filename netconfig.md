# Network configuration

In order to participate in the Spacemesh network and to earn mining awards your computer firewall (and in some cases your home network router) so the Spacemesh App is able to accept incoming Internet connections on `port 7153` for both `TCP` and `UDP`.

You only need to configure your network if you are planning to run a Miner and not if you plan to use the App in the custom wallet only mode.

---

## Windows 10
You need to manually permit the Spacemesh App to access the internet by opening a firewall port. You will need to know what port it uses and the protocol to make this work.

1. Navigate to Control Panel, System and Security and Windows Firewall.
2. Select Advanced settings and highlight Inbound Rules in the left pane.
3. Right click Inbound Rules and select New Rule.
4. Add the port you need to open and click Next.
5. Add the protocol (`TCP`) and use `7153` as the port number and click Next.
6. Select Allow the connection in the next window and hit Next.
7. Select the network type as you see fit and click Next.
8. Name the rule something meaningful and click Finish.
9. Repeat these steps but in step 6 select `UDP` instead of `TCP`.

This guide is based on the nice guide from [Tomshardware.com](https://www.tomshardware.com/news/how-to-open-firewall-ports-in-windows-10,36451.html)

---

## OS X
The Spacemesh App might be able to accept incoming connections by default depending on your Firewall settings. For example, when you download a signed distribution from Spacemesh. We recommend you follow these steps to confirm that the App can accept incoming connections.

1. Open the `System Preferences App`.
2. Click on `Privacy and Security`.
3. Click on the `Firewall` tab.
4. Click the `Firewall Options` button.
5. Uncheck the `Block all incoming connections` checkbox if it is checked.
6. Check the `Automatically allow downloaded signed software to receive incoming connections` checkbox OR add the `Spacemesh App` to the list of apps and chose `Allow incoming connections` for it.
7. Click OK.

For additional information about the OS X Firewall please [read this guide](https://support.apple.com/en-il/HT201642) from Apple.

---

## Linux
If you are running Linux then you should be able to configure your firewall via the command line. Check your linux distro documentation for additional info.

---

## Router Configuration

Your home router or Internet access point (or both) may be blocking incoming connections to any device on your home network.

In this case, you need to configure your router to not to block and to forward both UDP and TCP incoming network requests on port 7153 to the computer that you are running the Spacemesh App on.

To configure your router follow the instructions provided by your router or access point hardware maker for your router model.
