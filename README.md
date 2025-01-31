<h3 align="center">Marzbanish - Marzban subscription page template</h3>

<p align="center">
  Simple, beautiful, and user-friendly HTML template for <a href="https://github.com/Gozargah/Marzban">Marzban</a> and <a href="https://github.com/marzneshin/marzneshin">Marzneshin</a> subscription page based on <a href="https://getbootstrap.com/docs/5.3/">Bootstrap 5 CSS framework</a>
  <br>
  <br>
  <a href="https://persizer.github.io/marzban-sub-page/"><strong>Live demo »</strong></a>
  <br>
  <br>
  <a href="https://github.com/persizer/marzban-sub-page/tree/main#features">Features</a>
  ·
  <a href="https://github.com/persizer/marzban-sub-page/tree/main#installation">Installation</a>
  ·
  <a href="https://github.com/persizer/marzban-sub-page/tree/main#personalization">Personalization</a>
</p>

<p>
  <picture>
    <img alt="Marzban Subscription page template" src="https://raw.githubusercontent.com/persizer/marzban-sub-page/refs/heads/main/.github/assets/screen.png">
  </picture>
</p>

# Features

- Simple and intuitive design.
- Minimal code with comments for easy editing.
- Language switching: 
	- **English**
	- **Russian (Русский)**
	- **Chinese (中文)**
	- **Persian (فارسی)**
- Automatic detection of the user's language.
- QR code with subscription link.
- Separate links and QR codes for each node, display name for each connection (including emoji symbols in all browsers).
- Detailed guides are provided for Windows, Android, iOS, MacOS and Linux apps:

	- **iOS / macOS:** Happ, Streisand, FoxRay, V2Box
	- **Android:** Happ, V2RayNG
	- **Windows:** v2rayN
	- **Linux:** v2rayA

# Installation

<h2>Marzban:</h2>
Use the instruction below to install the page to <a href="https://github.com/Gozargah/Marzban">Marzban</a>
<h3>Install:</h3>

1. Upload the file to the server.
```
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/persizer/marzban-sub-page/main/index.html
```
2. Enter these commands to automatically specify the file path to the subscription page.
```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
Or specify them manually by editing the Marzban `.env` file.
```
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```
3. Restart Marzban to apply the changes.
```
marzban restart
```
<h3>Update:</h3>
Reupload the page file to the server (redo first step from install):

```
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/persizer/marzban-sub-page/main/index.html
```
After updating, you need to redo personalization steps.

<h2>Marzneshin:</h2>
Use the instruction below to install page to <a href="https://github.com/marzneshin/marzneshin">Marzneshin</a>
<h3>Install:</h3>

1. Upload the file to the server.
```
sudo wget -N -P /var/lib/marzneshin/templates/subscription/ https://raw.githubusercontent.com/persizer/marzban-sub-page/main/marzneshin/index.html
```
1. Enter these commands to automatically specify the file path to the subscription page.
```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzneshin/templates/"' | sudo tee -a /etc/opt/marzneshin/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /etc/opt/marzneshin/.env
```
Or specify them manually by editing the Marzneshin `.env` file.
```
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzneshin/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```
1. Restart Marzneshin to apply the changes.
```
marzneshin restart
```
<h3>Update:</h3>
Reupload the page file to the server (redo first step from install):

```
sudo wget -N -P /var/lib/marzneshin/templates/subscription/ https://raw.githubusercontent.com/persizer/marzban-sub-page/main/marzneshin/index.html
```
After updating, you need to redo personalization steps.

# Personalization

To customize the favicons, logo, support and donate links, you need to edit the `index.html` file. Replace the following default values with your own.

Favicons:
```
https://raw.githubusercontent.com/persizer/marzban-sub-page/refs/heads/main/img/apple-touch-icon.png
https://raw.githubusercontent.com/persizer/marzban-sub-page/refs/heads/main/img/favicon-16x16.png
https://raw.githubusercontent.com/persizer/marzban-sub-page/refs/heads/main/img/favicon-32x32.png
```
Support link:
```
https://t.me/gozargah_marzban
```
Donate link:
```
https://github.com/Gozargah/Marzban#donation
```
Logo:
```
https://raw.githubusercontent.com/persizer/marzban-sub-page/refs/heads/main/img/logo.png
```

## Hide donate button
If you need to remove the Donate button from bottom of the page, you can remove its `button` block. Simply find and delete this line in the file:
```
<a id="href-donate"><button type="button" class="btn my-btn mt-4 w-100" x-text="$t('donate')"></button></a>
```

## Hide support button
If you need to remove the Support button from the top of the page, you can remove its `button` block. Simply find and delete this line in the file:
```
<li class="nav-item"><a class="nav-link my-nav-link fw-semibold px-2" id="href-support" rel="noopener noreferrer" target="_blank" x-text="$t('support')"></a></li>
```

After making changes, save the file and restart Marzban / Marzneshin.


<p align="center">
  <br>
  Based on <a href="https://github.com/dermv/marzbanify-template">streletskiy's Marzbanify template</a>, which is based on <a href="https://github.com/dermv/marzbanify-template">dermw's Marzbanify Template</a>
  <br>
</p>
