# flixplayer
FlixPlayer is a simple app for LG webOS TVs to launch a website full-screen from the menu.

LG’s official webOS workflow is to create an app, package it into an .ipk, install it, and launch it. 

**Build from source**

*Install the CLI:*

```bash
npm install -g @webos-tools/cli
```
Package the project:

```bash
ares-package .
```
This produces an .ipk file.

Or, simply download the [latest FlixPlayer .ipk binary] (https://github.com/alexxic/flixplayer/releases/latest).


**Install .ipk**

Enable Developer Mode on the TV:

1. Install Developer Mode from the LG Content Store.

2. Sign in with an LG developer account.

3. Turn on Dev Mode Status.

4. Enable Key Server if requested.

5. Note the TV IP address and passphrase.

Install the latest [Device/DevMode Manager for webOS TV] (https://github.com/webosbrew/dev-manager-desktop/releases).

Connect webOS DevManager to the LG TV.

Install the ipk.


<img width="2152" height="1544" alt="image" src="https://github.com/user-attachments/assets/f0fb748a-d232-4ebc-9bb3-ee9afa5067e0" />

**Enjoy FlixPlayer**

Launch FlixPlayer and type in a website URL. When the app is opened again, FlixPlayer will only restore the last URL, not credentials or session data.
