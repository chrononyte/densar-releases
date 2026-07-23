# Densar BK

**Rebuild the PC, not just the files.**

[Densar BK](https://www.chrononsync.com/projects/densar/) is an encrypted backup that rebuilds an entire **Windows** working setup on a new machine — the folder links (junctions), the credentials, the programs a project needs and the dependencies to reinstall — not just the files.

This repository hosts the **downloads** for Densar BK. The program is a commercial product and is **not open source**.

## Download

Get the latest build from the [**Releases**](../../releases) page.

- **Version:** 1.1.0 · Windows · one file, ~13 MB
- **SHA256:** `2142b07311eafa7efd7d99e013f2418ac41e4923b1122dca68c2226aee560cf9`

Verify what you downloaded — in PowerShell, in the folder where you saved it:

```powershell
Get-FileHash densar.exe
```

If the hash matches the one above, character for character, the file is byte for byte the one we published.

### "Windows says it's suspicious"

Densar is **not code-signed yet**, so the first time Windows may show a warning screen (it can be red): it is not a virus, and nothing was found in the file — it is simply a new program with no download history. To go ahead, click the small link under the message ("More info" / "More details"): the **Run anyway** button then appears. Downloading from GitHub Releases and checking the SHA256 above is exactly how you make sure the file is genuine.

## What it does

Unlike an ordinary copy, Densar reads the machine as it is today and **puts the setup back together** on the new PC: it remaps Windows junctions instead of turning them into diverging duplicates, carries the credentials and config that git ignores, re-homes an AI assistant's memory under the new user, works out which programs the projects need (via `winget`) and installs them, and after restoring lists the exact steps still missing to actually run each project.

- **Classic backups** (Mirror, Full, Differential, Incremental) are **free forever**, in open formats (`age`, `.tar.gz`).
- **BK Intelligente AI** — the smart one that rebuilds the machine — is **39 € once**, not a subscription.
- **Restoring is always free**, for anyone, on any machine, even offline.

## Links

- Product & pricing: <https://www.chrononsync.com/projects/densar/>
- FAQ: <https://www.chrononsync.com/projects/densar/faq.html>
- Honest comparison (vs copying by hand, cloud sync, a disk image, Docker/Ansible): <https://www.chrononsync.com/projects/densar/alternatives.html>

---

© 2026 Chronon Sync. Densar BK is a commercial product; all rights reserved. This repository provides the installer and release notes only.
