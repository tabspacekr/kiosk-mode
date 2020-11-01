# kiosk-mode

[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)

Hides the header and sidebar drawer in [Home Assistant](https://www.home-assistant.io/)

![image](example1.png)

## Installation

*If you previously used [custom-header](https://github.com/maykar/custom-header) you need to uninstall it from [HACS](https://hacs.xyz/)*

### HACS

Search for `Kiosk Mode` and install it. Add to resources using UI or `configuration.yaml`

```yaml
resources:
  - url: /hacsfiles/kiosk-mode/kiosk-mode.js
    type: module
```

### Manual

Download [kiosk-mode.js](https://raw.githubusercontent.com/matt8707/kiosk-mode/master/kiosk-mode.js) and place it in your `www` folder. Add to resources using UI or `configuration.yaml`

```yaml
resources:
  - url: /local/kiosk-mode.js
    type: module
```

*If you have trouble installing please [read this guide](https://github.com/thomasloven/hass-config/wiki/Lovelace-Plugins)*

## Usage
Add the query string `?kiosk` to the end of your URL

```
https://hass:8123/lovelace/default_view?kiosk
```

**OR** name a dashboard path `kiosk`

```yaml
views:
  - title: Tablet
    path: kiosk

```

## Additional options

Optional query strings are `?hide_header` and `?hide_sidebar`. For example, you can just hide the sidebar to still be able to navigate between views.

### Cache

You save settings in a devices cache by using the cache keyword once on the device.<br>This will also make it so the options work on all views and dashboards.

Example: `?hide_header&cache` will make every view and dashboard hide the header, this works for all query strings.

**Utility Query Strings**

* `?clear_cache` in the URL will clear all cached preferences
* `?disable_kiosk` will temporarily disable any modification

### Related

* [Fully Kiosk Browser](https://www.fully-kiosk.com/) - Great for wall mounted tablets
* [Applicationize](https://applicationize.me/) - Convert web apps into desktop apps
* [KTibow/fullscreen-card](https://github.com/KTibow/fullscreen-card) - Make your Home Assistant browser fullscreen

### Credit
This is based on [ciotlosm's kiosk mode gist](https://gist.github.com/ciotlosm/1f09b330aa5bd5ea87b59f33609cc931) and includes features from [corrafig's fork](https://gist.github.com/corrafig/c8288df960e7f59e82c12d14de26fde8) as well as [maykar's Custom Header](https://github.com/maykar/custom-header/).
