# flixplayer
FlixPlayer is a simple app for LG webOS TVs to launch a website full-screen from the menu

Build and install
LG’s official webOS workflow is to create an app, package it into an .ipk, install it, and launch it. The current webOS Studio documentation recommends the webOS CLI and the Developer Mode app.

Install the CLI:

bash
npm install -g @webos-tools/cli
Package the project:

bash
ares-package .
This produces an .ipk file.

Enable Developer Mode on the TV:

Install Developer Mode from the LG Content Store.

Sign in with an LG developer account.

Turn on Dev Mode Status.

Enable Key Server if requested.

Note the TV IP address and passphrase.

Register the TV:

bash
ares-setup-device --add tv \
  -i "username=prisoner" \
  -i "host=TV_IP_ADDRESS" \
  -i "port=9922"
Retrieve the key:

bash
ares-novacom --device tv --getkey
Enter the passphrase shown on the TV, then install the package:

bash
ares-install --device tv ./ru.shipov.puzzlemovies_1.0.0_all.ipk
Launch it:

bash
ares-launch --device tv ru.shipov.puzzlemovies
The same Developer Mode and .ipk installation process is used by other webOS applications, and webOS 5.x is within the supported compatibility range for ordinary web apps.
