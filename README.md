# flixplayer
FlixPlayer is a simple app for LG webOS TVs to launch a website full-screen from the menu


**Build from source**

LG’s official webOS workflow is to create an app, package it into an .ipk, install it, and launch it. The current webOS Studio documentation recommends the webOS CLI and the Developer Mode app.

*Install the CLI:*

```bash
npm install -g @webos-tools/cli
```
Package the project:

```bash
ares-package .
```
This produces an .ipk file.


**Install .ipk**

Enable Developer Mode on the TV:

1. Install Developer Mode from the LG Content Store.

2. Sign in with an LG developer account.

3. Turn on Dev Mode Status.

4. Enable Key Server if requested.

5. Note the TV IP address and passphrase.

Install the latest [Device/DevMode Manager for webOS TV] (https://github.com/webosbrew/dev-manager-desktop/releases), connect and install the ipk from there

or

Register the LG TV and upload from CLI:

```bash
ares-setup-device --add tv \
  -i "username=<name>" \
  -i "host=TV_IP_ADDRESS" \
  -i "port=9922"
```
Retrieve the key:

```bash
ares-novacom --device tv --getkey
```
Enter the passphrase shown on the TV, then install the package:

```bash
ares-install --device tv ./com.flixplayer_<version>_all.ipk
```
Launch it:

```bash
ares-launch --device tv com.flixplayer
```

**Enjoy FlixPlayer**

Launch FlixPlayer and type in a website URL. When the app is opened again, FlixPlayer will only restore the last URL, not credentials or session data.
