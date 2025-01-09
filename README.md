<h3 align="center">Marzban Subscription page template</h3>

<p align="center">
  Simple, beautiful, and user-friendly HTML template for <a href="https://github.com/Gozargah/Marzban">Marzban</a> subscription page based on Bootstrap CSS framework
  <br>
  <br>
  Based on deeply rewrited <a href="https://github.com/dermv/marzbanify-template">dermw Marzbanify Template</a>
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
    <img alt="Marzban Subscription page template" src="./.github/assets/scr.png">
  </picture>
</p>

# Features

- The design is simple and intuitive, with minimal code.
- Language switching: English and Russian.
- Detailed guides are provided for PC, Android, iOS, MacOS and Linux.
- Automatic detection of the user's language.

# Installation

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
https://t.me/
```
Donate link:
```
https://boosty.to/
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

After making changes, save the file and restart Marzban.
