# Fedora 37 Workstation with Ansible
This is a small Ansible project that quickly set up my Fedora 37 Workstation. As I frequently experiment with various OSes, I find this project quite handy during the configuration process.

In summary, here is what it does:
- Removes unwanted pre-installed packages
- Installs essential components for work readiness
- Sets preferences in gnome-settings and gnome-tweaks using 'dconf'
- Adds custom keybinds
- Applies a theme

![Screenshot from 2023-02-03 09-57-12](https://user-images.githubusercontent.com/123499791/216639763-078b401a-a4c1-44a1-975f-dbdf729e46d6.png)

## Limitations
- At this time, only Fedora 37 Workstation is supported
- GNOME extensions have not yet been added to the automation process

## Theme
- [Tela icon theme](https://github.com/vinceliuice/Tela-icon-theme)
- [Adwaita Gtk3](https://github.com/lassekongo83/adw-gtk3)
- Wallpaper is "PastelHills", one of the default wallpapers from the Fedora 37 KDE spin

## How to use
Download the files
```bash
$ git clone https://github.com/oli-moreau/fedora-ansible.git
```
Install the dependencies
```bash
$ sudo dnf -y install ansible pip && pip install psutil && ansible-galaxy collection install community.general
```
Run the script
```bash
$ ansible-playbook main.yml --ask-become-pass
```
