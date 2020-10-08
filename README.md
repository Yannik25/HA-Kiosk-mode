[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

# HA-Kiosk-mode

## Installation

Add `kiosk.js` file to your `www` folder in config, or install via [HACS](https://hacs.xyz/).

Like any other custom script, use `ui-lovelace.yaml` resources section to reference the `kiosk.js` file.

```
resources:
  - url: /hacsfiles/HA-Kiosk-mode/kiosk.js
    type: js
```

Make sure you add `kiosk` somewhere in your URL. You can use it in the id of your view or in the query string.

Examples:

```
/lovelace/0?kiosk
```

```yaml
views:
  - title: Kiosk
    icon: mdi:heart
    id: kiosk_alarm


title: Lovelace Demo
views:
  - title: Home
    icon: mdi:heart
    id: kiosk_thermostat
    panel: true
    cards:
      - type: custom:thermostat-card
        title: HVAC
        entity: climate.hvac
```

## Keep tabs
If you still want to keep the Lovelace tabs and hide everything else use add `show_tabs` in your URL as query string.

```
/lovelace/0?kiosk&show_tabs
```

## Note

If this is your first file in `www` make sure you restart Home Assistant.

## Update
Fixed based on the working fork here: https://gist.github.com/corrafig/c8288df960e7f59e82c12d14de26fde8

## Credits
Thanks to @corrafig & @manualmanul for the fixes



    
