![Densar BK: rebuild the PC, not just the files](https://www.chrononyte.com/assets/img/og/densar.png?v=2)

# Densar BK

**Rebuild the PC, not just the files.**

[Densar BK](https://www.chrononyte.com/projects/densar/) is an encrypted backup that rebuilds an entire **Windows** working setup on a new machine: the folder links (junctions), the credentials, your AI assistants' memory, the programs a project needs and the dependencies to reinstall. Not just the files.

This repository hosts the **downloads** for Densar BK. The program is a commercial product and is **not open source**.

## Download

Get the latest build from the [**Releases**](../../releases) page.

- **Version:** 3.0.0 · Windows · one file, ~15 MB
- **SHA256:** `1bc988d19f3e590da738bba900e4ab74ac6650eedd9e08a0df1e85972cf73e30`

Verify what you downloaded. In PowerShell, in the folder where you saved it:

```powershell
Get-FileHash densar.exe
```

If the hash matches the one above, character for character, the file is byte for byte the one we published.

### "Windows says it's suspicious"

Densar is **not code-signed yet**, so the first time Windows may show a warning screen (it can be red): it is not a virus, and nothing was found in the file. It is simply a new program with no download history. To go ahead, click the small link under the message ("More info" / "More details"): the **Run anyway** button then appears. Downloading from GitHub Releases and checking the SHA256 above is exactly how you make sure the file is genuine.

## What it does

Unlike an ordinary copy, Densar reads the machine as it is today and **puts the setup back together** on the new PC: it remaps Windows junctions instead of turning them into diverging duplicates, carries the credentials and config that git ignores, re-homes an AI assistant's memory under the new user, works out which programs the projects need (via `winget`) and installs them, and after restoring it lists the exact steps still missing to actually run each project.

- **Classic backups** (Mirror, Full, Differential, Incremental) are **free forever**, in open formats (`age`, `.tar.gz`).
- **BK Smart AI** (the smart one that rebuilds the machine) is **59 € once**, not a subscription.
- **Restoring is always free**, for anyone, on any machine, even offline.

## Links

- Product & pricing: <https://www.chrononyte.com/projects/densar/>
- FAQ: <https://www.chrononyte.com/projects/densar/faq.html>
- Honest comparison (vs copying by hand, cloud sync, a disk image, Docker/Ansible): <https://www.chrononyte.com/projects/densar/alternatives.html>

---

© 2026 Chrononyte. Densar BK is a commercial product; all rights reserved. This repository provides the installer and release notes only.
