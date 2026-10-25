# urZONE PVE - Demo Plan

**By Osiris Simmons (Osiris83)** https://dnl.urzone.org/

**urZONE PVE - Demo Plan** lets visitors try your Proxmox hosting before they buy. It adds a front-page demo for any logged-in user, limits how long it lasts, and automatically deletes every demo instance when time is up. It requires **urZONE PVE Core**.

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

All settings are optional and live in `wp-config.php`. Defaults are shown below.

```php
define( 'URZONE_PROXMOX_DEMO_MINUTES', 60 );           // length of one demo
define( 'URZONE_PROXMOX_DEMO_WARN_MINUTES', 10 );      // warning before it ends (0 = off)
define( 'URZONE_PROXMOX_DEMO_MAX_INSTANCES', 2 );      // instances per demo
define( 'URZONE_PROXMOX_DEMO_COOLDOWN_MINUTES', 0 );   // wait before the same user can start another demo
define( 'URZONE_PROXMOX_DEMO_BRIDGE', '' );            // e.g. an isolated bridge for demo guests
```

| Setting | Default | What it controls |
|---|:---:|---|
| `URZONE_PROXMOX_DEMO_MINUTES` | 60 | Length of one demo |
| `URZONE_PROXMOX_DEMO_WARN_MINUTES` | 10 | Warning before the demo ends (0 = off) |
| `URZONE_PROXMOX_DEMO_MAX_INSTANCES` | 2 | Instances allowed per demo (minimum 1) |
| `URZONE_PROXMOX_DEMO_COOLDOWN_MINUTES` | 0 | Wait before the same user can start another demo |
| `URZONE_PROXMOX_DEMO_BRIDGE` | empty | Network bridge for demo guests, e.g. an isolated one |

## Requirements

- WordPress
- **urZONE PVE Core** (free or Pro) installed and active

## License

GPL-2.0-or-later
