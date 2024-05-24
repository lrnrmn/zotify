# Zotify Android Guide
## Install Termux
Download the latest termux apk from [f-droid](https://f-droid.org/en/packages/com.termux/)

Install it on your device.
## Give the correct permissions
Tap and hold the app icon, tap on "App Info".

Tap on `Permissions` and give termux all the permissions it asks for.
## Install base packages
Open termux.

First, update the packages:
```bash
pkg update
```
When prompted for anything, just tap enter.
## Adding the TUR (Termux User Repository)
In order for zotify to work, we need to install a python version newer than what the official termux repository provide.

The python package we need can be found in the TUR.

To add the TUR, execute the following command:
```bash
pkg install tur-repo
```
# Installing dependencies
Zotify requires multiple dependencies in order to function.

Install them all with this line:
```bash
pkg install python3.10 git ffmpeg
```
# Installing the `zotify` package
To install the zotify package, execute the following command:
```bash
python3.10 -m pip install git+https://zotify.xyz/zotify/zotify.git
```
# Initial setup
First, run `zotify`.

It will ask you for a username.

Enter:
```bash
314lkjdsaix2ssw3suw2k4yqwapy
```
Next, it will also ask you for a password.

Enter:
```bash
AAcc123456
```
Now, zotify is in search mode.

Because we haven't configured it yet, cancle the search:

Tap `ctrl`, `c` and then `enter` to cancel the search.

# Configuring zotify
We need to tell zotify where to download our music.

To do that, edit zotify's config.

Enter the config's directory:
```bash
cd .config/zotify
```
Edit the config:
```bash
nano config.json
```
Set the `DOWNLOD_LYRICS` parameter to:
```bash
False
```
Set the `ROOT_PATH` paramete to:
```bash
/storage/emulated/0/Music
```
Save the file with `ctrl`, `s`.

Exit `nano` with `ctrl`, `x`

---
DONE! Go ahead and download some music!

> From my experience, [Poweramp](https://forum.mobilism.org/viewtopic.php?f=1332&t=5533524&hilit=poweramp+poweramp) works best with zotify.
