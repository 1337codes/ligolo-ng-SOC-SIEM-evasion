# ligolo-ng SOC/SIEM evasion — standalone `ligoloup`

One self-extracting file (~34 MB) containing the Ligolo-NG pivot wizard, `proxy`,
TUN/route helper and all cross-platform agents. Source and docs live in
[1337codes/OSCP-Ligolo](https://github.com/1337codes/OSCP-Ligolo).

> ⚠️ Authorized use only — systems and networks you own or have written permission to assess.

```bash
curl -LO https://github.com/1337codes/ligolo-ng-SOC-SIEM-evasion/raw/main/ligoloup
curl -LO https://github.com/1337codes/ligolo-ng-SOC-SIEM-evasion/raw/main/ligoloup.sha256
sha256sum -c ligoloup.sha256
chmod +x ligoloup && ./ligoloup
```

| Command | What it does |
|---|---|
| `./ligoloup` | Interactive proxy wizard (nginx/stunnel TLS front, random agent URLs, cheat-sheet) |
| `./ligoloup fix` | TUN interfaces + route cleanup |
| `./ligoloup install` | Adds `ligoloup` / `ligolofix` aliases to ~/.zshrc + ~/.bashrc |
| `./ligoloup extract DIR` | Unpack the full toolkit to inspect or edit |
| `./ligoloup version` | Version + cache location |

First run extracts to `~/.cache/ligoloup/` and offers to install missing host packages
(Kali: `nginx libnginx-mod-stream` or `stunnel4`). Needs `sudo` for TUN, routes and :443/:80.

**v1.0.7** — SHA-256 `ea189b46be33d7a13d8a5d9919947ca762acfcdbb2642fabcb9f9faeffa38059`
