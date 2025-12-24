# AutomationZ Server Backup Scheduler with (optional) Discord WebHooks  [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R51QD7BU)
[![Dash-Board-Server-Backups.png](https://i.postimg.cc/NMzQ0d4t/Dash-Board-Server-Backups.png)](https://postimg.cc/YGY5nfZD)
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
[![Discord-Backup-Server-Webhooks.png](https://i.postimg.cc/bJBqvmTy/Discord-Backup-Server-Webhooks.png)](https://postimg.cc/34msSCVV)
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

# FAQ

## Is this a DayZ mod?
No. This is an external desktop tool. You do not add it to server parameters and it does not run inside DayZ.
You can use it for any Game server, Website or anything you can reach via FTP/FTPS to make back ups.

## Why is it called “AutomationZ” if it runs on a schedule?
Because it removes the need for you to be online at the right time. Once configured, backups happen automatically on the schedule you set.

## Can I use this for other servers or websites?
Yes. Anything you can reach via FTP/FTPS can be backed up.

## Does it download my entire server?
It can, if your host exposes the full root folder via FTP and you set the job path accordingly (example: `/` with subfolders enabled).
Some hosts restrict access to certain folders.

## Why is it slower than a “true backup”?
FTP backups are limited by:
- your host’s FTP speed
- your internet upload/download
- the number of files (many small files take longer)

For many server owners, FTP snapshots are still the simplest reliable solution.

## Where are backups stored?
Backups are saved into your chosen local destination folder, grouped by:
- profile
- job name
- timestamp

## I see a `__pycache__` folder, is that normal?
Yes. Python creates it automatically to speed up loading. You can ignore it.


## Security notes

- FTP credentials are stored locally
- No data is uploaded anywhere except your configured destination
- No telemetry
- No tracking
- No external services required (Discord optional)

---
🧩 Part of AutomationZ Control Center
This tool is part of the AutomationZ Admin Toolkit:

- AutomationZ Mod Update Auto Deploy (steam workshop)
- AutomationZ Uploader
- AutomationZ Scheduler
- AutomationZ Server Backup Scheduler
- AutomationZ Server Health
- AutomationZ Config Diff 
- AutomationZ Admin Orchestrator
- AutomationZ Log Cleanup Scheduler

Together they form a complete server administration solution.

### 💚 Support the project

AutomationZ tools are built for server owners by a server owner.  
If these tools save you time or help your community, consider supporting development.

☕ Ko-fi: https://ko-fi.com/dannyvandenbrande  
💬 Discord: https://discord.gg/6g8EPES3BP  

Created by **Danny van den Brande**  
DayZ AutomationZ


Part of the **AutomationZ** project  
Built to reduce admin workload and remove unnecessary manual server management.

If this tool saves you time or stress, consider supporting development.
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/R6R51QD7BU)
## Final note

This tool was designed with one goal in mind:

> **Let server owners live their lives while automation handles the boring stuff.**

Enjoy — and automate responsibly.
