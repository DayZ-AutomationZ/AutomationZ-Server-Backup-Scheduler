# AutomationZ Server Backup Scheduler with Discord WebHooks  [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R51QD7BU)

AutomationZ Backup Scheduler is a lightweight, server-side automation tool designed to **automatically back up remote servers via FTP/FTPS** on a schedule — without requiring any mods, plugins, or manual intervention.

Originally built for **DayZ server owners**, this tool is intentionally **generic and multifunctional**, making it just as useful for **website owners, developers, and system administrators** who need reliable, scheduled backups of remote folders.

---

## Why this tool exists

Server owners often face a simple problem:

- You want **regular backups**
- You don’t want to **log in every time**
- You don’t want to **babysit your server**
- You don’t want to install heavy or risky software on the server itself

AutomationZ Backup Scheduler solves this by running **locally** (PC, VPS, or admin machine) and handling everything via FTP/FTPS.

Set it once — and let it run.

---

## What this tool does

- Connects to one or more servers via **FTP or FTPS**
- Recursively downloads **entire folders** (full server snapshots)
- Stores backups in **timestamped directories**
- Supports **multiple servers (profiles)**
- Supports **multiple backup jobs**
- Runs continuously and executes jobs automatically
- Optional **Discord webhook notifications**
- Simple, readable UI
- No server-side installation required

---

## What this tool is NOT

- ❌ Not a DayZ mod
- ❌ Not added to server startup parameters
- ❌ Not running on the game server itself
- ❌ Not cloud-based
- ❌ Not intrusive

This tool operates **entirely client-side** using standard FTP.

---

## Automation explained (FAQ)

**“This still feels manual — how is it automated?”**

Automation here means:

- You define **jobs once**
- Each job has:
  - a server profile
  - a remote folder to back up
  - a local destination
  - a schedule (day / hour / minute)
- The application keeps running
- Jobs execute automatically at the configured times
- No further interaction required

You can:
- Go offline
- Go on holiday
- Leave the app running on a PC or VPS

The backups still happen.

---

## Typical use cases

### DayZ / game server owners
- Full server folder backups
- Config & database snapshots
- Pre-update safety backups
- Scheduled nightly backups

### Website owners
- Back up website folders
- Download content before deployments
- Archive live site states

### Developers & admins
- Mirror remote folders
- Keep historical snapshots
- Lightweight alternative to complex backup systems

---

## Folder structure

Backups are stored like this:


Each run creates a **clean, timestamped snapshot**.

---

## Discord notifications (optional)

You can enable Discord webhook notifications for:

- Job start
- Job success
- Job failure

This is useful for:
- Monitoring unattended jobs
- Receiving instant alerts
- Running the tool on a remote machine

Webhook settings are configured in `settings.json`.

---

## Requirements

- Python 3.10+ (tested on Windows & Linux)
- FTP or FTPS access to the remote server
- Network connection while jobs run

No additional libraries required.

---

## Security notes

- FTP credentials are stored locally
- No data is uploaded anywhere except your configured destination
- No telemetry
- No tracking
- No external services required (Discord optional)

---

## Credits

Created by **Danny van den Brande**

Part of the **AutomationZ** project  
Built to reduce admin workload and remove unnecessary manual server management.

If this tool saves you time or stress, consider supporting development.
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R51QD7BU)
---

## Final note

This tool was designed with one goal in mind:

> **Let server owners live their lives while automation handles the boring stuff.**

Enjoy — and automate responsibly.
