# 📊 Mac Stats

[![Stars](https://img.shields.io/github/stars/hardlygospel/mac-system-monitor?style=for-the-badge&color=yellow)](https://github.com/hardlygospel/mac-system-monitor/stargazers) [![Forks](https://img.shields.io/github/forks/hardlygospel/mac-system-monitor?style=for-the-badge&color=blue)](https://github.com/hardlygospel/mac-system-monitor/network/members) [![Last Commit](https://img.shields.io/github/last-commit/hardlygospel/mac-system-monitor?style=for-the-badge&color=green)](https://github.com/hardlygospel/mac-system-monitor/commits) [![License](https://img.shields.io/github/license/hardlygospel/mac-system-monitor?style=for-the-badge)](https://github.com/hardlygospel/mac-system-monitor/blob/main/LICENSE)
### *Modern TUI system monitor for macOS*

> Beautiful 256-colour terminal dashboard — CPU, memory, network, disk and process management, all in one view. 🖥️

---

## ⚡ Quick Start

```bash
pip3 install psutil
python3 -m tony_mac_stats
```

Or from the parent directory:

```bash
cd tools
python3 -m tony_mac_stats
```

---

## ✨ Features

- 🗂️ **5 Views** — Overview, Network, CPU Deep, Full Net, Processes
- 🎨 **38 Themes** — Dark/Vivid, Pastel/Soft, High Contrast categories
- 📈 **Live Graphs** — Vertical history graphs with auto-scaling
- 🧠 **Per-Core CPU** — Grid layout showing individual core utilisation
- 🌐 **Network** — TX/RX bytes + packets, per-interface stats, errors, drops
- 💾 **Disk I/O** — Read/write throughput with history graphs
- ⚙️ **Process Management** — Kill (SIGKILL), Pause (SIGSTOP), Resume (SIGCONT)
- 🔍 **Process Detail** — RSS, VMS, FDs, CWD, origin classification
- 🔎 **Filter** — Search processes by name
- 🔀 **Sort** — By CPU%, Memory%, PID, or Name

---

## ⌨️ Keyboard Reference

| Key | Action |
|---|---|
| `q` | Quit |
| `Tab` / `1-5` | Switch view |
| `t` / `T` | Next / previous theme |
| `Ctrl+T` | Theme picker menu |
| `H` | Help popup |
| `S` | System info popup |
| `F` | Filter processes |
| `↑↓` / `PgUp/PgDn` / `Home/End` | Navigate |
| `K` | Kill process (SIGKILL) |
| `Z` | Pause process (SIGSTOP) |
| `R` | Resume process (SIGCONT) |
| `I` / `Enter` | Process detail |
| `c/m/p/n` | Sort by CPU / Mem / PID / Name |
| `G` | Toggle graph ↔ list view |
| `r` | Force data refresh |

---

## ✅ Requirements

- 🐍 Python 3.8+
- 📦 `psutil >= 5.9.0` (`pip3 install psutil`)
- 🖥️ 256-colour terminal (`xterm-256color` recommended)
- 🍎 macOS or 🐧 Linux

---

## 📁 Project Structure

```
tony_mac_stats/
├── __init__.py     # Package metadata
├── __main__.py     # Entry point
├── palette.py      # 256-colour palette, Theme dataclass, 38 themes
├── data.py         # System metrics, process collection, history buffers
├── drawing.py      # Safe drawing primitives, graphs, bars, sparklines
├── popups.py       # Popup system (scrollable, confirm, filter, menu)
├── views.py        # 5 views + shared components (banner, statusbar)
├── app.py          # Main loop and input handling
└── requirements.txt
```

---

## 📄 Licence

MIT — do whatever you like with it.
