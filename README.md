# urZONE PVE - Demo Plan

**By Osiris Simmons (Osiris83)** https://urzone.org/ https://dnl.urzone.org/

**urZONE PVE - Demo Plan** lets visitors try your Proxmox hosting before they buy. It adds a front-page demo for any logged-in user, limits how long it lasts, and automatically deletes every demo instance when time is up.

> **Important:** This plugin does not work on its own. It requires both **urZONE PVE Core** and **urZONE PVE Settings**. Core provides the engine and panel, and Settings provides the configuration. Install and activate both first.

## What it does

- Adds a **Demo** plan to urZONE PVE, open to every logged-in user
- Adds the shortcode `[urzone_pve_demo]` (also works as `[urzone-pve-demo]`) to show the demo panel on any page
- Limits each demo by time and by number of instances
- Cleans up demo instances automatically
- Shows a clear notice if urZONE PVE Core is not active

## Usage

Put the shortcode on any page or post:

```
[urzone_pve_demo]
```

Logged-in visitors see the demo panel. The `[urzone-pve-demo]` form does exactly the same thing.

## Settings

You do not need to edit any files by hand. The demo settings are saved to `wp-config.php` automatically by **urZONE PVE Settings** when you press Save, and the plugin keeps a backup of the previous file. The options are:

| Setting | Default | What it controls |
|---|:---:|---|
| Demo length (minutes) | 60 | Length of one demo |
| Warning before end (minutes) | 10 | Warning before the demo ends (0 = off) |
| Max instances | 2 | Instances allowed per demo (minimum 1) |
| Cooldown (minutes) | 0 | Wait before the same user can start another demo |
| Demo bridge | empty | Network bridge for demo guests, e.g. an isolated one |

## Requirements

- WordPress
- **urZONE PVE Core** (free or Pro), installed and active
- **urZONE PVE Settings** (free or Pro), installed and active

## License

GPL-2.0-or-later
