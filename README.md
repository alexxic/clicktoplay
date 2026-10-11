# ClickToPlay
ClickToPlay is a simple app for LG webOS TVs to launch a website full-screen from the app menu.

## ⚠️ Disclaimer

This is an independent, open-source project created solely for educational and personal use. This project is **not** affiliated with, associated with, authorized by, endorsed by, or in any way officially connected with **LG Electronics** or any of its subsidiaries or affiliates. 

The official LG webOS website can be found at https://lge.com.

The software is provided "as is", without warranty of any kind, express or implied. In no event shall the authors be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or the use of it.


## How it works
LG’s official webOS workflow is to create an app, package it into an .ipk, install it, and launch it. 

## 🛠️ Build from Source

1. Install the CLI

```bash
npm install -g @webos-tools/cli
```
2. Package the Project

```bash
ares-package .
```
This produces an .ipk file.

Or, simply download the [latest ClickToPlay .ipk binary] (https://github.com/alexxic/clicktoplay/releases/latest).


## Install .ipk

** Enable Developer Mode on the TV: **

1. Install Developer Mode from the LG Content Store.

2. Sign in with an LG developer account.

3. Turn on Dev Mode Status.

4. Enable Key Server if requested.

5. Note the TV IP address and passphrase.

** Deploy using DevMode Manager **

1. Install the latest [Device/DevMode Manager for webOS TV] (https://github.com/webosbrew/dev-manager-desktop/releases).

2. Connect webOS DevManager to your LG TV using the IP and Passphrase noted earlier.

3. Drag and drop or install the `.ipk` file through the manager.

<img width="2152" height="1544" alt="image" src="https://github.com/user-attachments/assets/f0fb748a-d232-4ebc-9bb3-ee9afa5067e0" />

## 🚀 Enjoy ClickToPlay

Launch ClickToPlay and type in a website URL. When the app is opened again, ClickToPlay will only restore the last URL, not credentials or session data.
