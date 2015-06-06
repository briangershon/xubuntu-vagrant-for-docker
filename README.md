xubuntu-vagrant-for-docker
==========================

Playing with Xubuntu as a light-weight system for running Docker containers.

Features include easy creation of environment via Vagrant, along with a window GUI environment to run a code editor.

How to Use
----------

* `vagrant up`

* Login as vagrant, pw vagrant

Prepare for Desktop mode

* `sudo vim /etc/X11/Xwrapper.config` and edit it to allowed_users=anybody

Start XFCE

* `sudo VBoxClient --clipboard --display`  [NEEDED?]

* `startxfce4&`

First time setup and manual steps

* "Icons missing": Head over to Settings > Appearance and make sure Icons, Style and Font is what you want. Raleigh style, Tango icons, Monospace 10 font.

* Settings > Preferred Apps: Use XFCE4-terminal as default. Chromium as default.

* Right-click on Panel 1 at top and pick Preferences: shrink height, autosize

* So docker works without sudo, need to run `newgrp docker`. Tried to do this in Vagrant file, but not working yet, so have to do manually.

* Enable 256 color mode in terminal via `export TERM=xterm-256color` in the `~/.bashrc`
