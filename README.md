<p align="center">
  <img src="./logo.png" alt="Brogrammer GTK Logo" width="320">
</p>
<h1 align="center">Brogrammer GTK</h1>
<p align="center">
A complete Brogrammer recolor of the classic Adwaita Dark GTK theme.
</p>
<p align="center">
<img src="https://img.shields.io/badge/GTK-3%2F4-blue">
<img src="https://img.shields.io/badge/Cinnamon-6.x-orange">
<img src="https://img.shields.io/badge/Theme-Brogrammer-green">
</p>

---
## Preview
![Brogrammer GTK Preview](./preview.png)

---
## Color Palette
| Element | Color |
|--------|------|
| Primary Accent | `#2a84d2` |
| Background | `#1f1f1f` |
| Dark Surface | `#2e2e2e` |
| Borders | `#3a3a3a` |
| Primary Text | `#d6dbe5` |
| Secondary Text | `#8a8f9a` |
| Highlight Yellow | `#ecba0f` |
| Success Green | `#2dc55e` |
| Error Red | `#f81118` |
| Warning Red | `#de352e` |
| Purple Accent | `#4e5ab7` |

---
## Coverage
| Layer | Status |
|------|-------|
| GTK2 | ✓ Legacy app support |
| GTK3 | ✓ Full, all widget states |
| GTK4 / libadwaita | ✓ See setup below |
| Cinnamon 6.x shell | ✓ Panel, menus, OSD, dialogs, notifications |
| Gnome Shell | ✓ Top bar, overview, notifications, quick settings, calendar |

---
# Installation
Clone the repository:
```bash
mkdir -p ~/.themes
git clone https://github.com/librerob/Brogrammer-GTK \
~/.themes/Brogrammer-GTK
# or
git clone https://codeberg.org/librerob/Brogrammer-GTK \
~/.themes/Brogrammer-GTK
```
Or download the archive and extract it to:
```
~/.themes
```
Open **System Settings → Themes** and set:
```
Applications
Desktop
```
to:
```
Brogrammer-GTK
```
OR

Activate Theme (Terminal)

Set the theme using gsettings:
```bash
gsettings set org.cinnamon.desktop.interface gtk-theme 'Brogrammer-GTK'
gsettings set org.cinnamon.desktop.wm.preferences theme 'Brogrammer-GTK'
gsettings set org.cinnamon.theme name 'Brogrammer-GTK'
```
To reload the Cinnamon shell without logging out:
```
Alt + F2
r
Enter
```

---
# Libadwaita Setup
Libadwaita applications do **not read themes from `~/.themes`**.
They instead read configuration from:
```
~/.config/gtk-4.0
```
Copy the theme files:
```bash
mkdir -p ~/.config/gtk-4.0
cp -r ~/.themes/Brogrammer-GTK/gtk-4.0/assets \
~/.config/gtk-4.0/
cp ~/.themes/Brogrammer-GTK/gtk-4.0/gtk.css \
~/.config/gtk-4.0/
cp ~/.themes/Brogrammer-GTK/gtk-4.0/gtk-dark.css \
~/.config/gtk-4.0/
```
Restart affected applications or log out and back in.

---
# Flatpak Configuration
Allow Flatpak applications to access installed themes:
```bash
flatpak override --user \
--filesystem=xdg-config/gtk-4.0 \
--filesystem=home/.themes/
```
For programs run as **root**, create a symlink so the theme is visible system wide:
```bash
sudo ln -s ~/.themes/Brogrammer-GTK /usr/share/themes/
```

---
# Credits
**Adwaita**  
Original theme by the GNOME project.

**Brogrammer**  
Color scheme by https://github.com/kenwheeler/brogrammer-theme

---
# License
This project is licensed under the LGPL-2.1 license.
You are free to use, modify, and redistribute this theme under the terms of the GNU Lesser General Public License version 2.1.

See the LICENSE file in this repository for the full license text.
