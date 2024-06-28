
# Chapter 7

# Eggs Configuration 

## Part1: configuration automatically 

You can configure eggs tool automatically and also manually. To
configure the Eggs tool automatically, you can follow the steps outlined
below:

[\$]{dir="rtl"}sudo eggs autocomplete

Autocomplete command is indeed a handy tool for quickly accessing
available commands and their supported flags in the eggs package
manager. To utilize autocomplete in the eggs package manager, you
can start by typing eggs and then press the TAB key. This action
will display a list of the available commands that you can choose
from. Here\'s an example of the available commands:

![](media/image44.png){width="5.183963254593176in"
height="1.045767716535433in"}

Once you have selected a command, you can type it out and then press TAB
to see the flags supported by that specific command. For instance,
if you enter eggs produce **\--** and then press TAB, you will be
presented with the available flags for the produce command, like this:

![](media/image45.png){width="5.254300087489064in"
height="1.0216852580927385in"}

If you wish to access the help screen for a particular command, you can
utilize the **\--**help flag. For instance, to obtain detailed
information about the usage and options available for
the produce command, you can enter the following:

eggs produce \--help

Executing this command will provide you with comprehensive information
about the produce command, including its usage and available
options.

![](media/image46.png){width="5.130082020997375in"
height="3.45290791776028in"}

The eggs autocomplete \[SHELL\] command in the eggs package manager is
used to display autocomplete installation instructions for a specific
shell type. Here is the usage and options for the eggs autocomplete
\[SHELL\] command:

**USAGE:**

\$ sudo eggs autocomplete \[SHELL\] \[-r\]

![](media/image47.png){width="5.001957567804024in"
height="2.4025021872265966in"}

**ARGUMENTS:**

-   SHELL: Specifies the shell type for which you want to display
    autocomplete installation instructions.

**FLAGS:**

-   **-**r, **\--**refresh**-**cache: Refreshes the cache and ignores
    displaying instructions.

**DESCRIPTION**: This command is used to display autocomplete
installation instructions for the specified shell type.

**EXAMPLES:**:

To display autocomplete installation instructions for all available
shell types:

\$ sudo eggs autocomplete

To display autocomplete installation instructions for the bash shell:

\$ sudo eggs autocomplete bash

![](media/image48.png){width="5.114340551181102in"
height="2.2394466316710413in"}

To display autocomplete installation instructions for the zsh shell:

\$ sudo eggs autocomplete zsh

![](media/image49.png){width="5.13542760279965in"
height="2.2242858705161854in"}

To refresh the cache and ignore displaying instructions:

\$ sudo eggs autocomplete \--refresh-cache

![](media/image50.png){width="5.236781496062992in"
height="0.7098086176727909in"}

## Eggs adaptive resolutions 

The eggs adapt command allows you to conveniently resize the video
output to fit the size of a virtual machine window. This feature is
particularly useful when working with virtual machines that have
graphical interfaces other than cinnamon, gnome3, and KDE, as it
provides a way to adjust the screen resolution accordingly. This
functionality is not directly associated with ISO production but proves
extremely handy when dealing with virtual machine environments.

**Usage:**

\$ eggs adapt \[-h\] \[-v\]

![](media/image51.png){width="4.3787576552930885in"
height="3.1845505249343833in"}

**Flags:**

-   **-**h, **\--**help: Displays the help documentation for the
    CLI.

-   **-**v, **\--**verbose: Enables verbose mode for more detailed
    output.

**Description:**

The eggs adapt command is specifically designed to adapt the monitor
resolution for virtual machines. By invoking this command, the
underlying mechanism **(**utilizing xrandr**)** adjusts the screen
resolution to match the current settings of the virtual machine.
This ensures that the video output is properly scaled and fits the
dimensions of the virtual machine window. This feature is
particularly useful when working with virtual machines that have
different graphical interfaces, allowing for a seamless and optimized
viewing experience.

**EXAMPLES::**

\$ sudo eggs adapt

In this example, the eggs adapt command is executed without any
additional flags or arguments. This triggers the process of adapting
the monitor resolution for the virtual machine, ensuring that the video
output is properly scaled and fits the size of the virtual machine
window.

![](media/image52.png){width="4.972542650918635in"
height="2.160559930008749in"}

\$ sudo xrandr \--output Virtual-0 \--auto\'

The command \`\'xrandr **\--**output Virtual**-**0 **\--**auto\'\` is a
command**-**line instruction that utilizes the \`xrandr\` tool to adjust
the display output settings for a specific output named
**"**Virtual**-**0**".** Here\'s a breakdown of the command:

**-** \`**xrandr**\`: This is the command**-**line tool used for
configuring the screen settings in X Window System.

**-** **\`\--output Virtual-0**\`: This option specifies the output
display that we want to modify, in this case, **"**Virtual**-**0**".**
It refers to a virtual display output within the virtual machine.

**-** **\`\--auto**\`: This option tells \`xrandr\` to automatically
detect and set the optimal resolution and refresh rate for the specified
output.

By executing this command, \`xrandr\` will adjust the display settings
for the **"**Virtual**-**0**"** output in the virtual machine,
automatically determining the best resolution and refresh rate based on
the capabilities of the virtual display.

The purpose of using this command in the provided code snippet is likely
to ensure that the display output named **"**Virtual**-**0**"** in the
virtual machine is set to the appropriate resolution and refresh rate,
adapting it to the size of the window where the virtual machine is
running.

## eggs analyze

Eggs will analyze your system, to get users and servers data.

The eggs analyze command is used to perform system analysis and gather
data related to users and servers. Here\'s a description of the
command and its options:

**Usage:**

\$ sudo eggs analyze \[-h\] \[-v\]

![](media/image53.png){width="2.8855314960629923in"
height="2.5951629483814522in"}

**Flags:**

-   **-**h, **\--**help: Displays the help documentation for the
    CLI.

-   **-**v, **\--**verbose: Enables verbose mode, providing more
    detailed output during the analysis process.

**Description**: The eggs analyze command is designed to conduct a
comprehensive analysis of the system, specifically targeting user and
server**-**related data. By executing this command, the program will
gather relevant information and insights about the system\'s users and
servers.

**EXAMPLES::**

\$ []{dir="rtl"}sudo eggs analyze

![](media/image54.png){width="5.147337051618548in"
height="2.62284230096238in"}

In this example, the sudo command is used to execute the eggs
analyze command with administrative privileges. This allows the
system analysis to access and collect data that may require elevated
permissions.

Please note that the provided information is a combination of the
original text and additional descriptions to enhance understanding.

## Eggs Config

DESCRIPTION: The eggs config command sets up and installs the necessary
Debian packages needed to run the program. It ensures that all
dependencies and prerequisites are properly configured.

**USAGE**:

\$ eggs config \[-c\] \[-h\] \[-n\] \[-v\]

![](media/image55.png){width="5.184145888013998in"
height="3.5560640857392825in"}

**FLAGS:**

-   **-**c, **\--**clean: Removes the previous configuration before
    creating a new one.

-   **-**h, **\--**help: Displays the command**-**line interface
    **(**CLI**)** help.

-   **-**n, **\--**nointeractive: Performs the configuration without
    requiring user interaction.

-   **-**N, **\--**noicons: Disables the display of icons.

**EXAMPLES::**

To configure and install the required Debian packages for the program
with administrative privileges:

\$ sudo eggs config

![](media/image56.png){width="5.275413385826772in"
height="1.8377351268591426in"}

To remove the previous configuration before creating a new one, ensuring
a fresh installation of the necessary packages:

sudo eggs config \--clean

![](media/image57.png){width="5.363873578302712in"
height="2.8345352143482065in"}

After choosing yes:

![](media/image58.png){width="5.247166447944007in"
height="3.162811679790026in"}

**You can use --v option to see more details:**

![](media/image59.png){width="5.247575459317585in"
height="2.6739195100612423in"}

To remove the previous configuration and perform the setup process
without requiring any user interaction:

sudo eggs config \--clean \--nointeractive

![](media/image60.png){width="5.135422134733158in"
height="1.3129757217847768in"}

## eggs dad

The **"**eggs dad**"** command is a CLI **(**Command Line Interface**)**
command that provides a TUI **(**Text User Interface**)** configuration
helper. It allows you to interactively configure certain settings or
options using a command line interface. []{dir="rtl"}Here is a
breakdown of the different components of the command:

**Command: **

sudo eggs dad

![](media/image61.png){width="3.9684339457567805in"
height="3.01455271216098in"}

**Flags:**

-   **-**c, **\--**clean: This flag indicates that the old configuration
    should be removed before creating a new one.

![](media/image62.png){width="5.3405041557305335in"
height="3.2190726159230096in"}

![](media/image63.png){width="5.511811023622047in"
height="1.60873031496063in"}

-   **-**d, **\--**default: This flag indicates that the old
    configuration should be removed and the default configuration should
    be applied.

-   **-**h, **\--**help: This flag displays the help information for the
    command.

-   **-**v, **\--**verbose: This flag enables verbose output, providing
    more detailed information during the configuration process.

Description: **"**ask help from daddy **-** TUI configuration
helper**"**

This description suggests that the **"**eggs dad**"** command is a tool
that assists in configuring settings or options, with the help of a TUI
**(**Text User Interface**)** that guides the user through the
configuration process.

**EXAMPLES:**:

sudo dad

This example runs the **"**dad**"** command with default settings.

![](media/image64.png){width="5.147857611548557in"
height="3.509977034120735in"}

sudo dad --clean

This example runs the **"**dad**"** command and removes the old
configuration before creating a new one.

sudo dad --default

This example runs the **"**dad**"** command and removes the old
configuration, then applies the default configuration.

# Eggs Configuration 

## Part2: configuration manually 

During the installation of the eggs program, three different
configuration files are automatically generated. These files can be
found in the following directory. The eggs configuration file path
is: 

/etc/penguins-eggs.d

![](media/image65.png){width="4.963931539807524in"
height="2.687639982502187in"}

After installing eggs, the main configuration file can be found at the
above**-**mentioned path. This file allows manual configuration of
the eggs program.

The contents of the configuration **eggs.yaml** file are as follows:

![](media/image66.png){width="5.09543416447944in"
height="3.742639982502187in"}

Now, let\'s provide some explanations for the lines in the configuration
file:

By modifying these configuration options within the file, you can
manually configure the eggs program according to your specific
requirements. []{dir="rtl"}The provided text has been rewritten, and
additional explanations have been included for each line to enhance
understanding. Information from the web has been used to provide
accurate descriptions of the purpose and functionalities of the
configuration file. This configuration file will change with this
command: we introduced this command before.

\$sudo eggs config

## Krill config file

The krill config file described before. This is the entry of it:

![](media/image67.png){width="5.217258311461068in"
height="5.0878313648293965in"}

## Tools.yaml

![](media/image68.png){width="5.177933070866142in"
height="3.8151727909011375in"}

YAML is a human**-**readable data serialization format often used for
configuration files. Based on the provided YAML content, it appears
to be a configuration file for the Calamares installer, specifically for
setting up the installation environment with certain parameters.
Let\'s go through the different sections:

-   language: Specifies the language to be used during the installation
    process. In this case, it\'s set to \'en_US.UTF**-**8\',
    indicating American English.

-   region and zone: Define the geographical region and time zone for
    the installation. Here, it\'s set to \'America\' and
    \'New_York\', respectively.

-   keyboardModel, keyboardLayout, keyboardVariant, and keyboardOption:
    Specify keyboard**-**related settings. It seems to be set for a
    PC with a US keyboard layout.

-   installationDevice, installationMode, and filesystemType: These
    settings are related to the installation process and file system
    type. They are left unchanged in the provided configuration.

-   name, fullname, password, rootPassword, autologin, and hostname:
    These settings define the default user account, password, and system
    hostname. In this case, the default user is named \'artisan\'
    with the password \'evolution\', and autologin is enabled.

-   iface, addressType, address, netmask, gateway, domain, and dns:
    These settings are related to network configuration. They are
    left unchanged in the provided configuration.

## Exclude.list files

We wrote about it in the previous chapter.

/etc/penguins-eggs.d/exclude.list.d/

Or

/etc/penguins-eggs.d/exclude.list

![](media/image69.png){width="5.017258311461068in"
height="1.7896456692913385in"}

/etc/penguins-eggs.d/addons/

![](media/image70.png){width="4.971931321084864in"
height="1.7640310586176728in"}

/etc/penguins-eggs.d/addons/eggs/

![](media/image71.png){width="5.137774496937883in"
height="2.355469160104987in"}

Adopt

![](media/image72.png){width="5.314303368328959in"
height="2.1228040244969377in"}

/etc/penguins-eggs.d/addons/eggs/theme/livecd/

![](media/image73.png){width="5.410588363954505in"
height="2.3851596675415574in"}

![](media/image74.png){width="5.511811023622047in"
height="2.9546052055993in"}

Grub.main.cfg

![](media/image75.png){width="4.040761154855643in"
height="3.0541382327209097in"}

# Part3: Configuration status

## eggs status

The eggs status command provides information about the status of the
**"**eggs**"** system. Here is some information about the command:

![](media/image76.png){width="4.97088801399825in"
height="2.094772528433946in"}

**USAGE**

![](media/image77.png){width="3.250582895888014in"
height="2.54130905511811in"}

**FLAGS**

-   **-**h, **\--**help: Displays help information about the
    command.

-   **-**v, **\--**verbose: Provides more detailed and verbose
    output.

**DESCRIPTION** The eggs status command is used to retrieve information
about the status of the **"**eggs**"** system. It can provide
details about the current state of the system, including information
about running processes, system health, resource usage, and more.

**EXAMPLES:** Here are some EXAMPLES: of how to use the eggs
status command:

\$ sudo eggs status

This command will display the status information of the **"**eggs**"**
system. Please note that the specific output and available
information may vary depending on the implementation of the
**"**eggs**"** system and the version of the CLI tool you are using.

# Eggs Change log notes

## penguins-eggs-9.6.x

Since version 9.6.x Penguins' eggs is released - as Debian package -
for: amd64, i386 and arm64 architectures, supporting the majority of
PCs, old ones and single board systems like Raspberry Pi. Read more on
the article [Triple
somersault!](https://penguins-eggs.net/blog/triple-somersault)

https://penguins-eggs.net/blog/triple-somersault

## penguins-eggs-10.0.13

-   dad: bugfix on flag \--file;

-   exclude.list.d: usr.list is now completely - intentionally - empty;

-   produce: removed flag \--sidecar, not necessary.

## penguins-eggs-10.0.11-2

The **/usr/bin/penguins-links-add.sh** script called
**by /etc/xdg/autostart/penguins-links-add.desktop** now waits for the
Desktop folder to be present before copying the links to the desktop,
with the result that all links are shown correctly.

## penguins-eggs-10.0.11-1

-   produce \--excludes, now accept static, homes and home,

```{=html}
<!-- -->
```
-   sudo eggs \--excludes static you can use a static exclude.list;

-   sudo eggs \--excludes homes you want to clean all users\' homes;

-   sudo eggs \--excludes home don\'t save my home dir.

## penguins-eggs-10.0.10-1

-   dad: added a new flag \--file to have own configuration defaults.

Configuration defaults are passed with own YAML file, eg: custom.yaml

\# custom.yaml

\-\--

root_passwd: secret

snapshot_basename: columbus

snapshot_prefix: \'\' \# none

user_opt_passwd: secret

user_opt: user

Usage: 

sudo eggs dad \--file ./custom.yaml

## penguins-eggs-10.0.9-1

krill: fixed a noising problem, when use resolvectl krill was not able
to create to link /etc/resolv.conf to /run/systemd/resolve/resolv.conf,
now I fixed this. I\'m using krill sudo eggs install more than calamares
due it\'s much fast and can be used with flags
like \--unattended, \--nointeractive, etc.

## penguins-eggs-10.0.8-2

just a new pratical way to add/remove local repository yolk, during
installation.

Yolk was created mostly to let installation without internet connection
during the system installation. Before, I decided to remove all repos
during installation with calamares/krill and use
just /etc/apt/sources.list.d/yolk.list, now I changed this strategy: I
just add /etc/apt/sources.list.d/yolk.list during installation process
without remove the others repos. The result is a light slow
initializations - when we are not on the net - but the possibility to
add every packages during installation when we are connected.

## penguins-eggs-10.0.8-1

-   removed the code that allowed genisoimage to be used instead
    of xorriso to generate the ISO;

-   restored the operation of eggs produce \--script for both: Debian
    and Ubuntu derivatives (for the moment it has been tested only on
    Debian bookworm and Linuxmint 21.3 Virginia;

-   using eggs produce \--script actually generated a link
    in /home/eggs to the ISO in .mnt;

-   Warning: I checked eggs produce \--script on ArchLinux too, but
    actually don\'t work.

## penguins-eggs-10.0.7-1

For the joy of all respin producer who don\'t like to have my eggs on
the desktop, I changed a flag in sudo eggs produce.

I already add flag \--noicons, equivalent to not create icons at all on
the desktop: not eggs, not calamares, and so on, I think too much. So I
update it to: sudo eggs produce \--noicon in singular form, and remove
just my eggs symbol and my blog link. For someone this can be important.

For others, don\'t take cure, always is better to have eggs on the
fridge!

## penguins-eggs-10.0.6-3

Generate debian packages for all Debian/Devuan/Ubuntu distros plus a
specific for Ubuntu bionic, from the same codebase. Thanks to mods
in [perrisbrewery](https://github.com/pieroproietti/perrisbrewery).

Of course Arch and Manjaro are generated aside, thanks
his [PKGBUILD](https://github.com/pieroproietti/eggs-pkgbuilds).

### Note about bionic version

To have bionic, and armonize with all the others version, I did:

-   package.json: \"engines\": { \"node\": \"\>=16.0.0\" },

Now we have two template for control file:

-   perrisbrewery/template/dependencies.yaml;

-   perrisbrewery/template/dependencies-bionic.yaml I removed
    line: live-config-systemd \| live-config-sysinitv, added live \--
    live-boot, and put \`nodejs (\>= 16);

-   live-boot package: on bionic - for same reason - when the system is
    installed, directory /lib/live/boot is erased. The system work, eggs
    work and can produce, but the resulting ISO will not boot! To solve
    this problem, before generate the ISO, give: sudo apt install
    live-boot \--reinstall. This will restore /lib/live/boot and it\'s
    full contents.

## penguins-eggs-10.0.6-1

I received from Glenn Chugg same informations about fixes on README and
on eggs skel command.

-   README: added link to the important
    issue [#368](https://github.com/pieroproietti/penguins-eggs/issues/368) regarding
    nodejs 18, fixes on the text;

-   skel: cinnamon desktop. not more copy./conf/cinnamon in /etc/skel.

## penguins-eggs-10.0.5-2

-   produce: default compression is now zstd 1M Xcompression-level 3,
    fast the same and better in decompression;

-   produce: added flag \--pendrive, using zstd 1M Xcompression-level
    15 optimized to use with pendrives.

## penguins-eggs-10.0.4

-   calamares: calamares now receive branding\'s configuration
    parameters homeUrl, supportUrl and bugReportUrl from
    /etc/os-release;

-   node-proxy-dhcpd: I am trying to restore the operation of eggs
    cuckoo. I have not succeeded yet, you can refer to the
    related [issue](https://github.com/pieroproietti/penguins-eggs/issues/367).

## penguins-eggs-10.0.3

-   krill installaler: sudo eggs install now have a new option to chroot
    on the installed system before reboot. This let you di add/remove
    last time packages, before your system is rebooted;

-   again in krill: krill now respect the calamares
    module: packages.conf or it\'s own, packages are added/removed after
    it\'s configuration. This born becouse of Devuan daedalus amd64
    version, I noted it go in kernel panic after installation, if
    penguins-eggs and it\'s dependecies are not removed. The problem
    arise - probably - from the package live-config-sysvinit. I solved
    using the option \--release in command produce, to configurate
    calamares/krill to remove penguins-eggs, calamares and it\'s
    dependencies before to finish the installation process;

-   Other little fixes on wardrobe.

## penguins-eggs-10.0.2

A whole series of tweaks to make the Debian package more standard, a
pity not to have been able to generate a single package -any for all
architectures.

## penguins-eggs-10.0.0

There would be many ways to change the version number and emphasize an
important fact in the code. I don\'t pretend to be right, but having
spent a full morning reintroducing new headers on the sources and, a few
days switching from commonjs modules to a more modern node16 to support
both CommonJS and ECMAScript modules, I decided this way. Don\'t hold it
against me\... :-)

In this version all dependencies have finally been updated.
from [oclif](https://oclif.io/), [ink](https://github.com/vadimdemedes/ink),
etc.

Another new feature, for those who want to try their hand at
penguins-eggs development: you can create your penguins-eggs deb
packages with these simple commands, of course after installing nodejs
and pnpm.

To make your life easier and save yourself from installation of nodejs
and pnpm, you can use any recent version of my live [colibri
ISO](https://sourceforge.net/projects/penguins-eggs/files/ISOS/debian/bookworm/amd64/).

-   git clone https://github.com/pieroproietti/penguins-eggs

-   cd penguins-eggs

-   pnpm i

-   pnpm deb

In short, what I am about to tell you is that it is a good time to get
on board!

## penguins-eggs-9.8.3

I consider the cleanup and adjustments resulting from the switch to
oclif4 and Debian package name change to be over. I put the new version
in the PPA and you can install it with the command: sudo apt install
penguins-eggs.

## penguins-eggs-9.8.2

Removed a lot of unusefull code, when eggs started I thought to use npm
packages to distribuite it, so inside there was the code to install
necessary packages. From long time now, we produce deb packages and arch
packages so there was no need ot that code. I tested it working on i386
Debian Bookworm, amd64 Debian Bookworm, Arch.

## penguins-eggs-9.8.1

Released for i386, arm64 and amd64. Checked on i386 Debian Bookworm,
amd64 Debian Bookworm, Arch.

## penguins-eggs-9.8.0

It had been a long time since I was forced to use an outdated version
of [oclif](https://oclif.io/) because I had modified it to be able to
use [pnpm](https://pnpm.io/it/) instead
of [npm](https://github.com/pieroproietti/penguins-eggs/blob/master).
Recently, I think in March, with version 4 of oclif it is possible to
use oclif with pnpm and I could then try to upgrade the package. The
next step was to put the pieces back together. I do in fact use - in
addition to oclif - another mine Debian package building tool
called [perrisbrewery](https://github.com/pieroproietti/perrisbrewery) and,
of course, I had to update/modify that as well.

Basically this version is different, although on the surface it does not
seem too distant to the previous one.

For that reason I decided to highlight the change by changing in
addition to the release also the name of the package itself, no
longer eggs but penguins-eggs. Commands and logic remain the same.

![](media/image78.jpg){width="7.103583770778653in"
height="9.05511811023622in"}
