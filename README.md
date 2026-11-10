![Densar BK: rebuild the PC, not just the files](https://www.chrononyte.com/assets/img/og/densar.png?v=2)

# Densar BK

**Rebuild the PC, not just the files.**

[Densar BK](https://www.chrononyte.com/projects/densar/) is an encrypted backup that rebuilds an entire **Windows** working setup on a new machine: the folder links (junctions), the credentials, your AI assistants' memory, the programs a project needs and the dependencies to reinstall. Not just the files.

This repository hosts the **downloads** for Densar BK. The program is a commercial product and is **not open source**.

## Download

Get the latest build from the [**Releases**](../../releases) page.

- **Version:** 4.0.0 · Windows · one file, ~18 MB
- **SHA256:** `3663ef0be7d599d845e216c9fba9fba9f2c3881c991f86edb0378c84cda7408f`

Verify what you downloaded. In PowerShell, in the folder where you saved it:

```powershell
Get-FileHash densar.exe
```

If the hash matches the one above, character for character, the file is byte for byte the one we published.

### Beta channel

Next to the stable version there is a **beta**: the same program with the latest work in it, before it has been tried on enough machines to be called stable. It is published as a **pre-release**, so the "latest" link above never points to it and the stable version's in-app update never offers it. It carries the number of the version to come.

- **Beta:** 4.1.0-beta.2 (10 November 2026) · [download](https://github.com/chrononyte/densar-releases/releases/download/v4.1.0-beta.2/densar.exe) · Windows · one file, ~18 MB
- **SHA256 of the beta:** `62ce9b1d02b4fc601ee760ff2981f5324c88544847ee1728b8d24d996837ff0f`
- What is in it: *Clone system* from an MBR disk staying MBR (the copy boots from a BIOS with no UEFI, boot rebuilt on the copy); the Windows recovery environment (WinRE) attached to the copy; *Clone system* to a smaller disk goes on when a file's record has no room for its new list of pieces; *Clone disk* from disks with factory 32 KB NTFS; disk health for NVMe drives in USB enclosures (JMicron bridge); finishing errors carry Windows' own words; the boot is rebuilt from Windows 10 as well. New in 4.1.0-beta.2: *BK Mirror* lets you pick a disk from the list or folders, and two ways to copy ("Mirror into", each folder in its own subfolder, or "Exact mirror from A to B", the destination made the same as the source, never on the Windows disk or a system folder), with a free-space check before it starts; *Disk health* shows one box per disk and a sheet with all its data and the SMART table, and reads disks in USB enclosures by trying the common bridges in turn (SAT, Sunplus, JMicron, Cypress, Prolific, ASMedia, Realtek); the partition manager can wipe a whole disk, including partitions Windows does not recognise, and switch an empty disk between MBR and GPT. The exact mirror, the disk wipe, the MBR copy and WinRE are the newest parts and have had the least road: that is what the beta is for.

Keep the stable one for the backups you depend on.

### "Windows says it's suspicious"

Densar is **not code-signed yet**, so the first time Windows may show a warning screen (it can be red): it is not a virus, and nothing was found in the file. It is simply a new program with no download history. To go ahead, click the small link under the message ("More info" / "More details"): the **Run anyway** button then appears. Downloading from GitHub Releases and checking the SHA256 above is exactly how you make sure the file is genuine.

## What it does

Unlike an ordinary copy, Densar reads the machine as it is today and **puts the setup back together** on the new PC: it remaps Windows junctions instead of turning them into diverging duplicates, carries the credentials and config that git ignores, re-homes an AI assistant's memory under the new user, works out which programs the projects need (via `winget`) and installs them, and after restoring it lists the exact steps still missing to actually run each project.

**Since 4.0.0 it also works on whole disks.** *Clone system* copies only what Windows needs to start and fits a smaller disk too, as long as the data does; *Clone disk* copies every partition; *Clone partition* copies just one. The copy reads from a snapshot, so Windows can stay on, and the new disk boots on its own once fitted in place of the old one. Next to it there is a partition manager (create, resize, format, delete) and a disk health check (status, life left, temperature, power-on hours, data written).

- **Classic backups** (Mirror, Full, Differential, Incremental) and the **disk health check** are **free forever**; the backups are in open formats (`age`, `.tar.gz`).
- **BK Smart AI** (the smart one that rebuilds the machine), **disk cloning** and the **partition manager** are **59 € once**, not a subscription.
- **Restoring is always free**, for anyone, on any machine, even offline.

## Links

- Product & pricing: <https://www.chrononyte.com/projects/densar/>
- FAQ: <https://www.chrononyte.com/projects/densar/faq.html>
- Honest comparison (vs copying by hand, cloud sync, a disk image, Docker/Ansible): <https://www.chrononyte.com/projects/densar/alternatives.html>

---

© 2026 Chrononyte. Densar BK is a commercial product; all rights reserved. This repository provides the installer and release notes only.
