---
title: Setting up CentOS 7 with minimal desktop
tags:
  - centos
id: 210
categories:
  - devops
date: 2016-04-03 10:21:59
---

I have tired to install server with GUI (not GNOME Desktop, there are a lot of package that's not necessary for me).
This blog, I would like to remind my self for php server and laravel installations on CentOS 7 follow step below.

## Prerequisites

1.  [Centos 7.0 ISO](https://www.centos.org/download/)
2.  [Reference](http://www.dokuwiki.tachtler.net/doku.php?id=tachtler:centos_7_-_minimal_desktop_installation)

### Install Centos
1. If you are installing on a regular PC, you can burn it to an optical disk or create a bootable USB flash drive. Otherwise, just attach the ISO image using the virtual machine software of your choice.
2. Start machine and select `Install CentOS 7`.
{% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_38_44.png 600 %}
3. Configure installation
  * Select `Minimal Install` for `SOFTWARE SELECTION`.
  {% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_40_56-focus.png 600 %}
  * Complete setting up. Then click `Begin Installation`.
  {% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_40_56.png 600 %}
4. Set root password and create user while installing CentOS 7.
{% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_41_08.png 600 %}
5.  Reboot after installation completed.
{% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_43_22.png 600 %}
6.  Now we have minimal installation.
{% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_16_58_20.png 600 %}
7.  Login and install gnome
<pre>
sudo yum groupinstall "X Window System"
sudo yum install gnome-classic-session gnome-terminal nautilus-open-terminal control-center liberation-mono-fonts
sudo systemctl set-default graphical.target
reboot
</pre>

8. Now we have server with minimal gnome
{% img /images/minimum_centos/virtualbox_minimal-server_03_04_2016_15_59_45.png 600 %}
