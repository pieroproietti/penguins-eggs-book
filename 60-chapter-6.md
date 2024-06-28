
# Chapter 6

# Eggs Installer

The Eggs tool provides two different installers for installing your
distribution after creating the ISO file image:

## 1.Calamares Installer (GUI):

1.  Calamares is a graphical installer framework that provides a
    user**-**friendly interface for installing your distribution.

2.  It offers a visual systematic installation process, making it easier
    for users who prefer a graphical interface.

3.  To use the Calamares installer, you can run the eggs
    calamares command. This command allows you to configure,
    install, or configure Calamares.

## 2.Krill Installer (TUI):

4.  Krill is a command**-**line interface **(**CLI**)** system installer
    provided by Eggs.

5.  It offers a text**-**based installation process, allowing you to
    install your distribution without a graphical interface.

6.  The Krill installer is designed for users who prefer a
    command**-**line installation experience.

7.  To use the Krill installer, you can run the eggs
    install command. This command installs Krill, transforming the
    **"**egg**"** into a **"**penguin**"** and enabling the CLI system
    installer functionality.

**You can choose the installer that suits your preference and
installation requirements.**

## Method 1. Calamares installer (GUI)

# What is calamares

Calamares is an open**-**source installation framework designed to
simplify the installation process of Linux distributions. It
provides a user**-**friendly, modular, and customizable graphical
installer for Linux operating systems. Calamares aims to be
distribution**-**agnostic, meaning it can be used by various Linux
distributions with different desktop environments. The main goal of
Calamares is to provide an easy**-**to**-**use installation experience
for both novice and experienced users. It offers a simple and
intuitive interface that guides users through the installation process,
allowing them to configure various aspects of the system, such as disk
partitioning, user accounts, localization settings, and more.

Calamares is written in C**++** and uses the Qt framework for its
graphical user interface. It is designed to be highly customizable
and extensible, allowing Linux distributions to tailor the installer to
their specific needs. Distribution developers can customize the
appearance, behavior, and functionality of Calamares by creating or
modifying modules, which are individual components that handle specific
installation tasks. By using Calamares, Linux distributions can
provide a consistent and user**-**friendly installation experience,
making it easier for users to install and try out their operating
systems. It abstracts away many of the complexities of the
installation process, making it accessible to a wider range of users and
contributing to a more welcoming Linux ecosystem.

## Calamares modules

  These are the commonly used modules in a typical Calamares
installation:

1)  Welcome: This module provides an introduction and overview of the
    installation process. It may include information about the
    distribution and its features.

2)  Location: This module allows users to select their geographic
    location, which is used to set the system\'s time zone.

3)  Keyboard: This module enables users to choose their preferred
    keyboard layout or input method.

4)  Partitions: The partitions module allows users to configure disk
    partitions for the installation. It provides options for
    automatic partitioning or manual partitioning, including the ability
    to create, resize, or format partitions.

5)  Users: This module allows users to set up user accounts and
    configure user**-**related settings, such as usernames, passwords,
    and user privileges.

6)  Summary: The summary module provides a summary of the chosen
    installation settings and allows users to review and confirm their
    choices before proceeding with the installation.

7)  Install: This module handles the actual installation process,
    copying the necessary files to the designated partitions and
    configuring the system accordingly.

8)  Finish: The finish module marks the completion of the installation
    process and may prompt users to reboot their system.

**Additionally**, **there are optional modules available in Calamares**,
**which are used for specific use cases or distributions:**

1)  License: This module presents the end**-**user license agreement
    **(**EULA**)** and requires users to accept the terms before
    proceeding with the installation.

2)  Netinstall: The netinstall module enables network**-**based
    installation, allowing users to download and install packages
    directly from the internet during the installation process.

3)  Notesqml: This module provides a text**-**based note or information
    to the user during the installation process.

4)  Packagechooser: The packagechooser module allows users to select
    additional software packages or components to be installed alongside
    the base system.

5)  Plasmalnf: This module is specific to KDE Plasma**-**based
    distributions and provides additional configuration options for the
    Plasma desktop environment.

6)  Tracking: The tracking module allows distributions to collect
    anonymous usage data or statistics regarding the installation
    process, helping developers gather insights and improve the
    installer.

7)  Webview: This module integrates a web browser or web**-**based
    interface within the installer, allowing users to access online
    resources or perform specific tasks during the installation.

These optional modules offer flexibility and customization options for
specific installation scenarios or distribution requirements.

# Calamares installation 

How to install Calamares?

## Step 1:  installing Calamares using the distribution\'s repository 

Here are the instructions to install Calamares on Debian, Ubuntu, Arch
Linux, Manjaro, and Fedora:

1. **Debian**:

**-** Open a terminal.

**-** Update the package lists:

sudo apt update

**-** Install Calamares:

sudo apt install calamares

2. **Ubuntu**:

**-** Open a terminal.

**-** Update the package lists:

sudo apt update

**-** Install Calamares:

sudo apt install calamares

3. **Arch Linux**:

**-** Open a terminal.

Install Calamares from the Arch User Repository **(**AUR**)** using an
AUR helper like yay or paru:

 \$ sudo yay -S calamares-git 

or

 \$ sudo paru -S calamares-git

4. **Manjaro**:

**-** Open a terminal.

**-** Install Calamares from the official repositories:

sudo pacman -S calamares

5. **Fedora**:

**-** Open a terminal.

**-** Install Calamares from the official repositories:

sudo dnf install calamares

**Or**

Add the RPM Fusion repository, which provides Calamares:

sudo dnf install -y
https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-\$(rpm
-E %fedora).noarch.rpm

sudo dnf install -y
https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-\$(rpm
-E %fedora).noarch.rpm

Update the package lists: 

sudo dnf update

Install Calamares: 

sudo dnf install calamares

After installing Calamares, you can launch it from the application menu
or by running the \`calamares\` command in the terminal. Keep in
mind that Calamares is primarily designed to be used during the
installation process of a Linux distribution, so you might not find it
as a standalone application for everyday use.

Check the default installer:

![](media/image31.png){width="3.9956528871391077in"
height="0.5771500437445319in"}

Then, you can see which installer is installed.

![](media/image32.png){width="5.408383639545057in"
height="2.6542366579177603in"}

## Step 2: installing calamares with eggs

**Debian based**

\$ sudo apt install calamares

\$ sudo eggs calamares \--install

![](media/image33.png){width="5.238406605424322in"
height="1.7634623797025373in"}

**Arch Linux using Chaotic-AUR**

1)  Open a terminal.

2)  Install the Chaotic**-**AUR key and mirrorlist:

pacman-key \--recv-key 3056513887B78AEB \--keyserver
keyserver.ubuntu.com

pacman-key \--lsign-key 3056513887B78AEB

pacman -U
\'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst\'

pacman -U
\'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst\'

Open the **/**etc**/**pacman.conf file using a text editor:

\$ sudo nano /etc/pacman.conf

Append the following lines to the end of the file:

\[chaotic-aur\]

Include = /etc/pacman.d/chaotic-mirrorlist

1)  Save and exit the text editor.

2)  Update the package lists:

\$ sudo pacman -Syu

Install Calamares using pacman or sudo eggs:

\$ sudo pacman -S calamares

then

\$ sudo eggs calamares \--install

Wait for the installation process to complete. The package manager
will download and install Calamares along with any necessary
dependencies.

**With yay**

To install Calamares using yay on Arch Linux, you can follow these
steps:

1)  Open a terminal.

2)  Clone the penguins**-**eggs**-**pkgbuilds repository from GitHub:

git clone https://github.com/pieroproietti/penguins-eggs-pkgbuilds

Change into the ckbcomp directory:

cd penguins-eggs-pkgbuilds/aur/ckbcomp

Build and install the ckbcomp package using makepkg:

makepkg -si

Once ckbcomp is installed, you can install Calamares using yay:

yay calamares

1)  yay will search for the Calamares package in the AUR **(**Arch User
    Repository**)**, present you with the available options, and prompt
    you to choose the package to install. Select the appropriate
    Calamares package when prompted.

2)  Review the installation details and dependencies, and confirm the
    installation.

3)  yay will handle the download, build, and installation process for
    Calamares, along with any necessary dependencies.

**On Manjaro** Linux, you can install Calamares directly from eggs using
the following command:

sudo eggs calamares \--install

This command will use the eggs package manager to install Calamares on
your system. Make sure you have eggs installed before running this
command. If eggs tool is not installed, you can install it using the
package manager provided by Manjaro. After executing the
command, eggs will handle the download, installation, and any necessary
dependencies for Calamares. Once the installation is complete, you
can launch Calamares from the application menu or by running
the calamares command in the terminal.

# Calamares settings

[]{dir="rtl"}After installing Calamares, the configuration files can be
found in the following path:

/etc/calamares

![](media/image34.png){width="5.129708005249344in"
height="2.6745089676290466in"}

In this directory, you will find various configuration files that allow
you to customize and fine**-**tune the behavior of Calamares during the
installation process. These files include:

## settings.conf

1.  **settings.conf**: This file serves as the main configuration file
    for Calamares. It contains global settings and options that
    determine the behavior of the installer. You can modify various
    parameters such as the theme, language, keyboard layout,
    partitioning scheme, and more.

![](media/image35.png){width="5.119178696412948in"
height="6.6549879702537185in"}

The provided sequence of steps and exec in the settings.conf file
appears to be a configuration for an installation or deployment
process. Here\'s a breakdown of the sequence and their corresponding
actions:

1. Show Welcome, Locale, Keyboard, Partition, Users, Summary: These
are steps to display various screens or prompts to the user during the
installation process, including welcome messages, language**/**locale
selection, keyboard configuration, partitioning options, user account
setup, and a summary of the installation choices.

2. Exec: This section contains a series of actions to be executed
during the installation process. Each action represents a specific
task or operation:

-   Partition: Handles partitioning of the disk.

-   Mount: Mounts the necessary file systems.

-   Unpackfs: Unpacks the file system.

-   Sources**-**yolk: Configures software sources.

-   Machineid: Sets the machine ID.

-   Fstab: Configures the file system table.

-   Locale: Sets the system locale.

-   Keyboard: Configures the keyboard layout.

-   Localecfg: Configures locale**-**related settings.

-   Luksbootkeyfile: Handles LUKS boot key file setup.

-   Users: Sets up user accounts.

-   Displaymanager: Configures the display manager.

-   Networkcfg: Configures network settings.

-   Hwclock: Handles hardware clock configuration.

## Branding

**2.branding**: This directory defines the branding information for
Calamares. It allows you to specify the name, logo, and other visual
elements that will be displayed during the installation process. By
customizing this file, you can create a consistent branding experience
for your distribution.

![](media/image36.png){width="5.1050371828521435in"
height="2.3582436570428698in"}

The branding directory in Calamares allows you to define the branding
information for your distribution during the installation process.
By customizing this file, you can create a consistent and personalized
branding experience. Here is what you can specify in
the branding.desc file:

-   Name: You can set the name of your distribution or customize the
    name that will be displayed during the installation. This helps
    users identify your distribution throughout the installation
    process.

-   Logo: You can specify the logo or icon that represents your
    distribution. This image will be displayed in various places
    during the installation, such as the installer\'s welcome screen or
    progress bar.

-   Visual Elements: Apart from the name and logo, you can also define
    other visual elements to create a cohesive branding experience.
    This may include specifying colors, fonts, or any other design
    elements that align with your distribution\'s brand identity.

By customizing the branding.desc file, you can ensure that the
installer reflects the unique identity of your distribution. It
helps create a consistent and recognizable experience for users during
the installation process.

Default eggs branding.desc:

![](media/image37.png){width="5.272345800524934in"
height="3.5597944006999125in"}

Show.qml file

The **/**etc**/**calamares**/**branding**/**show.qml file refers to
a specific QML **(**Qt Meta**-**Object Language**)** file used in the
Calamares installer framework. This file is typically located in
the **/**etc**/**calamares**/**branding**/** directory.
[]{dir="rtl"}The purpose of the show.qml file within the branding
directory is to define the graphical user interface **(**GUI**)** for
displaying screens or pages during the installation process,
specifically for a particular branding or customization of the Calamares
installer.

By modifying the show.qml file, you can customize the appearance,
layout, and behavior of the installer\'s user interface to match a
specific branding or theme. This allows Linux distributions and
system integrators to tailor the installation experience to their
desired look and feel. Please note that the specific contents and
structure of the show.qml file can vary depending on the branding or
customization being applied. The file may contain QML code that
defines the layout, styling, and interactive elements of the installer
screens, such as labels, buttons, input fields, and progress
indicators.

To view the contents of
the **/**etc**/**calamares**/**branding**/**show.qml file on your
system, you can use a text editor or command**-**line tools
like cat or less. For example, you can run the following command in
a terminal:

\$ cat /etc/calamares/branding/eggs/show.qml

![](media/image38.png){width="5.159548337707786in"
height="7.3502832458442695in"}

## modules

**3.modules**: This directory lists the modules that Calamares should
load during the installation. Each module represents a specific step
or functionality in the installation process.

![](media/image39.png){width="4.808214129483814in"
height="2.9571052055993in"}

By enabling or disabling modules, you can control which features are
available to the user during installation. EXAMPLES: of modules
include partitioning, user account creation, bootloader installation,
and more.

**Partitioning**: The partitioning module handles the disk partitioning
process, allowing users to create, resize, or delete partitions as
needed.

-   User Account Creation: This module enables users to create user
    accounts during the installation process, specifying usernames,
    passwords, and other account details.

-   Bootloader Installation: The bootloader module handles the
    installation and configuration of the bootloader, allowing users to
    choose the boot device and configure boot options.

-   Localization: This module allows users to select the system\'s
    language, keyboard layout, timezone, and other regional
    settings.

-   Package Selection: The package selection module enables users to
    choose the software packages they want to install, allowing for
    customization and fine**-**tuning of the system\'s software
    selection.

-   Summary and Installation: This module presents a summary of the
    selected options and performs the actual installation process.

These are just a few EXAMPLES: of the modules that can be included in
the modules.conf file. By modifying this file, you can enable or
disable specific modules based on your requirements, thus controlling
which features are available to the user during the installation.

## Method2: The Krill installer (TUI)

The Krill installer **(**TUI**)** in the Eggs tool allows for a
command**-**line installation experience. Here\'s a breakdown of the
usage, flags, and descriptions provided:

**Usage:**

![](media/image40.png){width="5.139589895013123in"
height="3.9725601487314086in"}

The **"**eggs install**"** or **"**eggs krill**"** command seems to be a
CLI system installer. It provides various flags to customize the
installation process, such as specifying a custom unattended
configuration, domain name, IP address, swap settings, Proxmox VE
installation, and more. The command can be run with administrative
privileges using sudo. The description mentions that it is a CLI
system installer where the **"**egg became a penguin,**"** possibly
indicating a transition or transformation of some sort.

The EXAMPLES: demonstrate different ways to use the command, such as
running a standard installation, running an unattended installation, and
running a custom installation with the configuration specified as
**"**it**".**

## Config krill manually:

Got the following path:

![](media/image41.png){width="5.1821128608923885in"
height="2.1504155730533685in"}

Then you can see the krill config file:

/etc/ penguins-eggs/conf/krill.yaml

![](media/image42.png){width="5.158114610673666in"
height="4.988772965879265in"}

## The content of krill.yaml

The YAML configuration file named **"**krill.yaml**"** for
configuring the installation settings of the **"**eggs install**"** or
**"**eggs krill**"** CLI system installer. Let\'s go through the
different sections of the configuration:

welcome

**language**: Specifies the language for the installation. In this
case, it is set to \'en_US.UTF**-**8\' for English language with
UTF**-**8 encoding.

location

**region**: Specifies the region**/**location. In this case, it is
set to \'America\'.

**zone**: Specifies the zone within the region. In this case, it is
set to \'New_York\'.

keyboard

**keyboardModel**: Specifies the keyboard model. In this case, it is
set to \'pc105\'.

**keyboardLayout**: Specifies the keyboard layout. In this case, it
is set to \'us\'.

**keyboardVariant**: Specifies the keyboard variant. It is left
empty **(**\'\'**)** in this configuration.

**keyboardOption**: Specifies any additional keyboard options. It is
left empty **(**\'\'**)** in this configuration.

partition

**installationDevice**: Specifies the installation device. It is
left empty **(**\'\'**)** in this configuration.

**installationMode**: Specifies the installation mode. It is set to
\'standard\'.

**filesystemType**: Specifies the filesystem type. In this case, it
is set to \'ext4\'.

**userSwapChoice**: Specifies the user\'s swap choice. It is set to
\'small\'.

users

**name**: Specifies the default username. In this case, it is set to
\'artisan\'.

**fullname**: Specifies the full name of the default user. In this
case, it is set to \'artisan\'.

**password**: Specifies the password for the default user. In this
case, it is set to \'evolution\'.

**rootPassword**: Specifies the root password. In this case, it is
set to \'evolution\'.

**autologin**: Specifies whether autologin should be enabled for the
default user. In this case, it is set to \'true\'.

**hostname**: Specifies the hostname. It is left empty
**(**\'\'**)** in this configuration.

network

**iface**: Specifies the network interface. It is left empty
**(**\'\'**)** in this configuration.

**addressType**: Specifies the type of address configuration
**(**e.g., dhcp or static**).** In this case, it is set to
\'dhcp\'.

**address**: Specifies the IP address. It is left empty
**(**\'\'**)** in this configuration.

**netmask**: Specifies the network mask. It is left empty
**(**\'\'**)** in this configuration.

**gateway**: Specifies the gateway address. It is left empty
**(**\'\'**)** in this configuration.

**domain**: Specifies the domain name. It is left empty
**(**\'\'**)** in this configuration.

**dns**: Specifies the DNS server address. It is left empty
**(**\'\'**)** in this configuration.

**See more details and source code:**

https://github.com/pieroproietti/penguins-eggs/tree/master/src/krill/modules

![](media/image43.jpg){width="7.103583770778653in"
height="9.05511811023622in"}
