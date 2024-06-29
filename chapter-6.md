# Chapter 6

# Installing the generated ISO image

ISOs created by eggs, can use two differents system installer to install the system:
* calamares system installer:
* krill system installer: an inside a TUI installer built with eggs.


## calamares Installer (GUI)

[calamares](https://calamares.io/) is a graphical installer framework that provides a
user-friendly interface for installing your distribution.

It offers a visual systematic installation process, making it easier
for users who prefer a graphical interface.

To use the Calamares installer, you can run the eggs
calamares command. This command allows you to configure,
install, or configure Calamares.

## krill Installer (TUI):
`krill` is a command-line interface (CLI) system installer
provided by eggs.

It offers a text-based installation process, allowing you to
install your distribution without a graphical interface.

The `krill` installer is designed for users who need a
command-line installation experience, it's little, but 
it's look and feel take very much from the giant calamares,
just little and CLI. Also his name: `krill`. come as an omage
to the big `calamares` project.

To use the krill installer, just run: `eggs install` command. 

## considerations
* calamares let you to get dual boot (Windows/Linux), it's generally
safe and it's the most diffused GUI installer;
* calamares, as GUI software, need the presence of a GUI interface - 
both X or Wayland, it's not available on CLI systems;
* as external software, calamares must to be installed before produce the ISO;
* krill - as part of eggs - is always availabe, for CLI and GUI systems;
* if calamares is present, krill rely on calamares configuration under `/etc/calamares`,
without calamares, krill generate it's own configuration on `/etc/penguins-eggs.d/krill.d`;
* calamares and krill can install and remove packages during system installation, using the same 
module: `packages.conf`, the same is valid for `partitions.conf` module.
* sometime is convenient to use krill, in place of calamares, when we don't
need dual boot, becouse is light and fastest, with the possibility
to get unattended system installation with various parameters;

# Installing with calamares installer (GUI)

## What is calamares

Calamares is an open-source installation framework designed to
simplify the installation process of Linux distributions. It
provides a user-friendly, modular, and customizable graphical
installer for Linux operating systems. Calamares aims to be
distribution-agnostic, meaning it can be used by various Linux
distributions with different desktop environments. The main goal of
Calamares is to provide an easy-to-use installation experience
for both novice and experienced users. It offers a simple and
intuitive interface that guides users through the installation process,
allowing them to configure various aspects of the system, such as disk
partitioning, user accounts, localization settings, and more.

Calamares is written in C++ and uses the Qt framework for its
graphical user interface. It is designed to be highly customizable
and extensible, allowing Linux distributions to tailor the installer to
their specific needs. Distribution developers can customize the
appearance, behavior, and functionality of Calamares by creating or
modifying modules, which are individual components that handle specific
installation tasks. By using Calamares, Linux distributions can
provide a consistent and user-friendly installation experience,
making it easier for users to install and try out their operating
systems. It abstracts away many of the complexities of the
installation process, making it accessible to a wider range of users and
contributing to a more welcoming Linux ecosystem.

## Calamares views

  These are the commonly view in a typical Calamares
installation:

* Welcome: This module provides an introduction and overview of the
installation process. It may include information about the
distribution and its features.
* Location: This module allows users to select their geographic
location, which is used to set the system\'s time zone.
* Keyboard: This module enables users to choose their preferred
keyboard layout or input method.
* Partitions: The partitions module allows users to configure disk
partitions for the installation. It provides options for
automatic partitioning or manual partitioning, including the ability
to create, resize, or format partitions.
* Users: This module allows users to set up user accounts and
configure user-related settings, such as usernames, passwords,
and user privileges.
* Summary: The summary module provides a summary of the chosen
installation settings and allows users to review and confirm their
choices before proceeding with the installation.
* Install: This module handles the actual installation process,
copying the necessary files to the designated partitions and
configuring the system accordingly.
* Finish: The finish module marks the completion of the installation
process and may prompt users to reboot their system.

Additionally, there are optional modules available in Calamares, 
which are used for specific use cases or distributions:

## Calamares installation 

Calamares is a great tool and can be found on Debian, Devuan, Manjaro and Ubuntu original repositories, but not on Arch repositories.

Due the need to find it and configure it's policy to remove the need to introduce root password to start the installation from the live, the right way is to install i by eggs.

```
sudo eggs calamares --install
```
Wait for the installation process to complete. 
The package manager will download and install Calamares along with 
any necessary dependencies.

## Calamares configuration

After installing calamares, the configuration files can be
found in the following path:

```
/etc/calamares
```

In this directory, you will find various configuration files that allow
you to customize and fine-tune the behavior of Calamares during the
installation process. These files include:

### /etc/calamares/settings.conf
This file serves as the main configuration file
for calamares. It contains global settings and options that
determine the behavior of the installer. You can modify various
parameters such as the theme, language, keyboard layout,
partitioning scheme, and more.

#### `sequence`
The provided sequence of steps and exec in the settings.conf file
appears to be a configuration for an installation or deployment
process. Here's a breakdown of the sequence and their corresponding
actions:

##### `show:`

* `welcome`
* `locale`
* `keyboard`
* `partition`
* `users`
* `summary`

These  are steps to display various screens or prompts to the user during the
installation process, including welcome messages, language/locale
selection, keyboard configuration, partitioning options, user account
setup, and a summary of the installation choices.

##### `exec:`
This section contains a series of actions to be executed
during the installation process. Each action represents a specific
task or operation:

* `partition`: Handles partitioning of the disk.
* `mount`: Mounts the necessary file systems.
* `unpackfs`: Unpacks the file system.
* `sources-yolk`: Configures software sources.
* `machineid`: Sets the machine ID.
* `fstab`: Configures the file system table.
* `locale`: Sets the system locale.
* `keyboard`: Configures the keyboard layout.
* `localecfg`: Configures locale-related settings.
* `luksbootkeyfile`: Handles LUKS boot key file setup.
* `users`: Sets up user accounts.
* `displaymanager`: Configures the display manager.
* `networkcfg`: Configures network settings.
* `hwclock`: Handles hardware clock configuration.
* `services-systemd` : Configure systemd
* `bootloader-config` : configura bootloader
* `grubcfg` : configure grub
* `bootloader`: install grub
* `packages`: install/remove packages
* `luksbootkeyfile`: 
* `plymouthcfg`: configure plymouth
* `initramfscfg`: configure initramfs
* `initramfs`: create inittramfs
* `dpkg-unsafe-io-undo`
* `removeuser`: remove live user
* `sources-yolk-undo`: remove sources-yolk 
* `cleanup`: cleaup
* `umount`: umount filesystem

### /etc/calamares/branding

This directory defines the branding information for
Calamares. It allows you to specify the name, logo, and other visual
elements that will be displayed during the installation process. By
customizing this file, you can create a consistent branding experience
for your distribution.

The branding directory in Calamares allows you to define the branding
information for your distribution during the installation process.
By customizing this file, you can create a consistent and personalized
branding experience. Here is what you can specify in
the `branding.desc` file:

#### /etc/calamares/branding/branding-name/branding.desc

* `name`: You can set the name of your distribution or customize 
the name that will be displayed during the installation. This helps users identify your distribution throughout the installation process.
* `logo`: You can specify the logo or icon that represents your
distribution. This image will be displayed in various places
during the installation, such as the installer\'s welcome screen or
progress bar.
* Visual Elements: Apart from the name and logo, you can also define
other visual elements to create a cohesive branding experience.
This may include specifying colors, fonts, or any other design
elements that align with your distribution\'s brand identity.

By customizing the branding.desc file, you can ensure that the
installer reflects the unique identity of your distribution. It
helps create a consistent and recognizable experience for users during
the installation process.


#### /etc/calamares/branding/branding-name/show.qml

The `/etc/calamares/branding/branding-name/show.qml` file refers to
a specific QML (Qt Meta-Object Language) file used in the
Calamares installer framework. This file is typically located in
the `/etc/calamares/branding/branding-name` directory.

The purpose of the `show.qml` file within the branding
directory is to define the graphical user interface (GUI) for
displaying screens or pages during the installation process,
specifically for a particular branding or customization of the Calamares
installer.

By modifying the `show.qml` file, you can customize the appearance,
layout, and behavior of the installer\'s user interface to match a
specific branding or theme. This allows Linux distributions and
system integrators to tailor the installation experience to their
desired look and feel. Please note that the specific contents and
structure of the show.qml file can vary depending on the branding or
customization being applied. The file may contain QML code that
defines the layout, styling, and interactive elements of the installer
screens, such as labels, buttons, input fields, and progress
indicators.

To view the contents of the `/etc/calamares/branding/show.qml` file 
on your system, you can use a text editor or command-line tools
like cat or less. For example, you can run the following command in
a terminal:

```
less /etc/calamares/branding/eggs/show.qml
```

### /etc/calamares/modules
This directory lists the modules that calamares should
load during the installation. Each module represents a specific step
or functionality in the installation process.

By enabling or disabling modules, you can control which features are
available to the user during installation. EXAMPLES: of modules
include partitioning, user account creation, bootloader installation,
and more.

* Partitioning: The partitioning module handles the disk partitioning
process, allowing users to create, resize, or delete partitions as
needed.

* User Account Creation: This module enables users to create user
accounts during the installation process, specifying usernames,
passwords, and other account details.

* Bootloader Installation: The bootloader module handles the
installation and configuration of the bootloader, allowing users to
choose the boot device and configure boot options.

* Localization: This module allows users to select the system\'s
language, keyboard layout, timezone, and other regional
settings.

* Package Selection: The package selection module enables users to
choose the software packages they want to install, allowing for
customization and fine-tuning of the system\'s software
selection.

* Summary and Installation: This module presents a summary of the
selected options and performs the actual installation process.

These are just a few EXAMPLES: of the modules that can be included in
the modules.conf file. By modifying this file, you can enable or
disable specific modules based on your requirements, thus controlling
which features are available to the user during the installation.

# Using Krill installer (TUI)

The krill installer (TUI) in the eggs tool allows for a
command-line installation experience. Here's a breakdown of the
usage, flags, and descriptions provided:

**Usage:**


The command `sudo eggs install` or `sudo eggs krill` provides various
flags to customize the installation process. 
```
  -H, --halt            Halt the system after installation
  -N, --none            Swap none: 256M
  -S, --suspend         Swap suspend: RAM x 2
  -b, --btrfs           Format btrfs
  -c, --chroot          chroot before to end
  -d, --domain=<value>  Domain name, defult: .local
  -h, --help            Show CLI help.
  -i, --ip              hostname as ip, eg: ip-192-168-1-33
  -k, --crypted         Crypted CLI installation
  -n, --nointeractive   no user interaction
  -p, --pve             Proxmox VE install
  -r, --random          Add random to hostname, eg: colibri-ay412dt
  -s, --small           Swap small: RAM
  -u, --unattended      Unattended installation
  -v, --verbose         Verbose
```

The command must run with administrative privileges using `sudo`.
The description mentions that it is a CLI system installer 
where the °egg became a penguin,° possibly
indicating a transition or transformation of some sort.

## `/etc/penguins-eggs.d/krill.yaml

The YAML configuration file named `krill.yaml` is used for
configuring the installation settings of krill.

Let's go show the different sections of the configuration:

```
 Penguins' eggs
# krill.yaml
---
# welcome (put your language, example: it_IT.UTF-8)
language: 'en_US.UTF-8'

# location (put your location, example region: "Europe", zone: "Rome")
region: 'America'
zone: 'New_York'

# keyboard (put your values example: keyboardModel: "pc105", keyboardLayout: "it")
keyboardModel: 'pc105'
keyboardLayout: 'us'
keyboardVariant: ''
keyboardOption: ''

# partition (leave it unchanged)
installationDevice: ''
installationMode: 'standard'
filesystemType: 'ext4'
userSwapChoice: 'small'

# users (Here you can put your default user, password, etc)
name: 'artisan'
fullname: 'artisan'
password: 'evolution'
rootPassword: 'evolution'
autologin: true
hostname: ''

# network (leave it unchanged)
iface: ""
addressType: 'dhcp'
address: ''
netmask: ''
gateway: ''
domain: ''
dns: ''
```

![image43](media/image43.jpg)
