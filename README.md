<h3 align="center">Marzbanner - Marzban subscription page template</h3>

<p align="center">
  Simple, beautiful, and user-friendly HTML template for <a href="https://github.com/Gozargah/Marzban">Marzban</a> subscription page based on <a href="https://getbootstrap.com/docs/5.3/">Bootstrap 5 CSS framework</a>
  <br>
  <br>
  <a href="https://streletskiy.github.io/marzban-sub-page/"><strong>Live demo »</strong></a>
  <br>
  <br>
  <a href="https://github.com/streletskiy/marzban-sub-page/tree/main#features">Features</a>
  ·
  <a href="https://github.com/streletskiy/marzban-sub-page/tree/main#installation">Installation</a>
  ·
  <a href="https://github.com/streletskiy/marzban-sub-page/tree/main#personalization">Personalization</a>
</p>

<p>
  <picture>
    <img alt="Marzban Subscription page template" src="./.github/assets/screen.png">
  </picture>
</p>

# Features

- The design is simple and intuitive.
- The code is minimal and with comments for easy editing.
- Language switching: 
	- **English**
	- **Russian (Русский)**
	- **Chinese (中文)**
	- **Persian (فارسی)**
- Automatic detection of the user's language.
- QR code with subscription link.
- Separate links and QR codes for each node, display name for each connection (including emoji symbols in all browsers).
- Detailed guides are provided for Windows, Android, iOS, MacOS and Linux apps:

	- **iOS / macOS:** Hiddify, Streisand, FoxRay, V2Box, Shadowrocket, SingBox, Happ
	- **Android:** Hiddify, V2RayNG, V2RayTun, Clash Meta, SingBox, Happ
	- **Windows:** Hiddify, NekoRay, v2rayN, InvisibleMan, Clash Verge Rev
	- **Linux:** Clash Verge Rev, v2rayA

# Installation

<h2>Marzban:</h2>
Use the instruction below to install page to <a href="https://github.com/Gozargah/Marzban">Marzban</a>
<h3>Install:</h3>

1. Upload the file to the server.
```
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/streletskiy/marzban-sub-page/main/index.html
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
Re-upload the page file to the server (re-do first step from install):

```
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/streletskiy/marzban-sub-page/main/index.html
```
After update need to repeat personalization.

# Personalization

To customize the favicons, logo, support and donate links, you need to edit the `index.html` file. Replace the following default values with your own.

Favicons:
```
https://raw.githubusercontent.com/streletskiy/marzban-sub-page/refs/heads/main/img/apple-touch-icon.png
https://raw.githubusercontent.com/streletskiy/marzban-sub-page/refs/heads/main/img/favicon-16x16.png
https://raw.githubusercontent.com/streletskiy/marzban-sub-page/refs/heads/main/img/favicon-32x32.png
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
https://raw.githubusercontent.com/streletskiy/marzban-sub-page/refs/heads/main/img/logo.png
```

## Hide Username
If you don't need to display the username, you can replace the subscription title.
Simply find this line in the file:
```
<span class="text-break fs-3 fw-bold me-auto"><span x-text="$t('subscriptionFor')"></span> {{ user.username }}</span>
```
and replace it with:
```
<span class="text-break fs-3 fw-bold me-auto" x-text="$t('subscription')"></span>
```

## Hide donate button
If you need to remove donate button from bottom of the page you can remove button block. Simply find and delete this line in the file:
```
<a id="href-donate"><button type="button" class="btn my-btn mt-4 w-100" x-text="$t('donate')"></button></a>
```

## Hide support button
If you need to remove support button from the top of the page you can remove button block. Simply find and delete this line in the file:
```
<li class="nav-item"><a class="nav-link my-nav-link fw-semibold px-2" id="href-support" rel="noopener noreferrer" target="_blank" x-text="$t('support')"></a></li>
```

After making changes, save the file and restart Marzban / Marzneshin.

# Using attributes in url
You can use the following attributes placed in url to override some page content:
- sub — link to other marzban subscription page. Override all user info and connection links on page when specified.
- support — link in support button. Use your link with https:// to override button link, or use **null** to remove this button
- donate — link in donate button. Use your link with https:// to override button link, or use **null** to remove this button

Example with overriding:
```
https://streletskiy.com/marzban-sub-page/?support=https://example.com/&donate=https://example.com/&sub=https://example.com/
```
Example with disable support and donate buttons:
```
https://streletskiy.com/marzban-sub-page/?support=null&donate=null
```

***
<h3 align="center">Contributors:</h3>
<p align="center">
<a href="https://github.com/streletskiy/marzban-sub-page/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=streletskiy/marzban-sub-page" />
</a>
</p>
<br>

***
<p align="center">
  <br>
  Based on deeply rewrited <a href="https://github.com/dermv/marzbanify-template">dermw Marzbanify Template</a>
  <br>
</p>
