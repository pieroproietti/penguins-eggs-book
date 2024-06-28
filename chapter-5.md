# Chapter 5

# Installing Eggs

penguins-eggs, starting from version 10.x require nodejs>18, 
Debian bookworm, Devuan daedalus and Ubuntu noble have nodejs on their
repositories, others distros not.

We need to add repository for nodejs>18 or better from [nodesource](https://github.com/nodesource/distributions).


## Ubuntu 20.04 focal, Ubuntu 22.04 jammy

```
sudo apt-get install -y curl
curl -fsSL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh
sudo -E bash nodesource_setup.sh
```

## UBUNTU 18.04 bionic, Debian stretch and derivatives**

If you are using Ubuntu 18.04 bionic, or derivatives, you can't use nodejs>16, but I have good news
too: we have a special version called penguins-eggs-10.0.x-bionic-x.deb compiled against nodejs 16!

Just add node16 repo from [nodesource](https://github.com/nodesource/distributions).

```
sudo apt-get install -y curl
curl -fsSL https://deb.nodesource.com/setup_16.x -o nodesource_setup.sh
sudo -E bash nodesource_setup.sh
```

There are multiple ways to install eggs as a .deb package.

The most practical method is to add and use the `penguins-eggs-ppa` repository.

## Method1: using `get-eggs` (Arch/Debian/Devuan/Ubuntu)

The `get-eggs` command is used to add the `penguins-eggs-ppa`
repository and configure it on Arch, Debian, Devuan, Ubuntu, or their
derivatives. Here's how you can use it:

```
git clone https://github.com/pieroproietti/get-eggs
cd get-eggs
sudo ./get-eggs
```

By executing `sudo ./get-eggs` with root privileges, it will add
the necessary repositories to your system. On Arch Linux, it will
add the `chaotic-aur` repository while on Debian-based systems, including 
Ubuntu, it will add `penguins-eggs-ppa`

Please note that running scripts with root privileges should be done
with caution. Make sure you trust the source and understand the
actions being performed by the script.

## Method2: download the package from sourceforge (Debian/Devuan/Ubuntu)

If you prefer not to include the `penguins-eggs-ppa`
repository in your system's repositories, you have an alternative
method to install the eggs package. Follow these steps:

1)  Visit the sourceforge site to download the latest version of the
    eggs package in .deb format.

2)  Once the package is downloaded, open a terminal and navigate to the
    directory [DEBS](https://sourceforge.net/projects/penguins-eggs/files/DEBS/)  
    where the .deb file is located.


3)  Install the eggs package using the dpkg command with sudo. For
    example:

```
sudo dpkg -i eggs-10.0.13.deb
```

4)  Since this is your first installation, there may be missing
    dependencies preventing the package from being fully installed.
    To resolve this, run the following command:

```
sudo apt install -f
```

This command will automatically install any missing
dependencies required by the eggs package.

5)  If you have the gdebi package manager installed on your system, you
    can use it to install the eggs package in graphical mode. Simply
    right-click on the .deb file, select "Open with GDebi
    Package Installer," and follow the on-screen
    instructions.

More details:

[sourceForge.net](https://sourceforge.net) is a widely recognized platform that
has been serving the software development community for many years.

It has established itself as a reliable source for hosting and
distributing open-source software projects. By hosting projects
on sourceForge.net, developers can showcase their work, collaborate
with other developers, and make their software easily accessible to
users. 

When it comes to the installation of eggs, SourceForge.net provides a
convenient location to download the necessary .deb package files. 

These files contain the software package that you need to install 
on your system. By navigating to the designated page for the 
[penguins-eggs project](https://sourceforge.net/projects/penguins-eggs/)  on
sourceforge.net, you can access the list of available .deb
files.

Downloading the appropriate .deb file for your system
architecture is crucial for a successful installation. 

Whether you are using an AMD64 or i386 system, sourceForge.net 
offers the necessary files to cater to your specific requirements. 

Once you have downloaded the desired .deb file, you can proceed 
with the installation process. Using the `dpkg` command with the `-i`
flag, you can install the eggs package onto your system. 

It is important to note that running the installation command as a superuser
(using `sudo`) ensures that the necessary permissions are granted for the
installation process.

During the installation, you may encounter dependency
issues. 

Dependencies are additional software components that need to
be present on your system for the eggs package to function
correctly. 

Resolving these dependencies is essential for a smooth
installation. Fortunately, the \`apt\` package manager provides a
convenient way to automatically resolve and install any missing
dependencies. 

By running `sudo apt -f install`, you can prompt
the package manager to fix any dependency-related issues.

After successfully installing the eggs package and resolving any
dependencies, it is always a good idea to verify the installation.
Using the `eggs status` command, you can check the current status of
the eggs package on your system. This command provides information
about the installed version and any relevant updates or
notifications.

By following these steps and utilizing sourceForge.net as a reliable
source for the eggs package, you can ensure a seamless installation
process and enjoy the benefits of this software on your system.

Once `penguins-eggs` package is installed, you can easyly add `penguins-eggs-ppa`
repository, just:

```
sudo eggs tools ppa --add
```


## Method3: adding penguins-eggs-ppa manually (Debian/Devuan/Ubuntu)

Using ppa depository on Debian based:

To use the repository, follow these steps:

1.  Copy and paste the following two lines into a terminal window:

```
curl -fsSL https://pieroproietti.github.io/penguins-eggs-ppa/KEY.gpg
| sudo gpg \--dearmor -o /etc/apt/trusted.gpg.d/penguins-eggs.gpg
$sudo echo "deb \[arch=\$(dpkg \--print-architecture)\]
https://pieroproietti.github.io/penguins-eggs-ppa ./" | sudo tee
/etc/apt/sources.list.d/penguins-eggs.list \> /dev/null
```

Now, you can use standard apt commands to install and upgrade the eggs
package. Remember to run sudo apt update to update the package lists
before installing or upgrading the eggs package.

```
sudo apt update
sudo apt install penguins-eggs
```

Once the eggs package is successfully installed, you can
use the eggs command-line tool to add the penguins-eggs-ppa
repository and receive updates via apt. To add the repository,
execute the following command:


By following these steps, you can install the eggs package,
resolve any missing dependencies, and add the penguins-eggs-ppa
repository for future updates.


## Methos6: adding chaoth-aur repository manually (Archlinux)

To configure the Chaotic-AUR repository and install the
penguins-eggs package on Arch Linux, follow these steps:

1)  Import the Chaotic-AUR repository key by running the following
    command:

```
pacman-key --recv-key FBA220DFC880C036 --keyserver keyserver.ubuntu.com
```

Description: The pacman-key --recv-key command
is used in Arch Linux-based distributions, such as Manjaro, to
import and trust a specific GPG key. This command is typically used
to validate the authenticity and integrity of packages downloaded from
specific repositories.

In the example you provided, FBA220DFC880C036 is the key ID that you
want to import, and keyserver.ubuntu.com is the keyserver from
which you want to retrieve the key.

To import the key using pacman**-**key **\--**recv**-**key, follow these
steps:

Open a terminal or command prompt.

Run the following command:

```
sudo pacman-key --recv-key FBA220DFC880C036 --keyserver keyserver.ubuntu.com
```

This command will retrieve the specified key from the
keyserver and import it into your system\'s keyring. After the key
is imported, you need to trust it by running the following command:

```
sudo pacman-key --lsign-key FBA220DFC880C036
```

This command will locally sign the key, indicating that you
trust it.

By importing and trusting the key, you can ensure the authenticity of
packages signed with that key when you install them using pacman or
related package managers.

2)  Sign the imported key by running the following command:

```
sudo pacman-key --lsign-key FBA220DFC880C036
```

3)  Install the Chaotic-AUR keyring and mirrorlist packages by
    running the following command:

```
sudo pacman -U https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst https://cdn-mirror.chaotic.cx/chaotic-aur chaotic-mirrorlist.pkg.tar.zst
```


4)  Open the `/etc/pacman.conf` file in a text editor and add
    the following lines at the end:

```
[chaotic-aur\]
Include = /etc/pacman.d/chaotic-mirrorlist
```

5)  Save the changes and exit the text editor.

6)  Update the package lists by running the following command:

```
sudo pacman -Sy
```

7)  Finally, install the penguins-eggs package by running the
    following command:
```
sudo pacman -Sy penguins-eggs
```

By following these steps, you will successfully configure
the chaotic-aur repository and install the penguins-eggs package
on your Arch Linux system.

**on Arch Linux**, you have multiple options to install eggs. 

One popular choice is to use the yay, an AUR helper. Here's how you can
install eggs using yay:

1)  Open a terminal and run the following command to install yay if you
    don't already have it:

```
sudo pacman -Sy yay
```

2)  Once yay is installed, you can use it to install eggs by running the
    following command:
```
sudo yay -S penguins-eggs
```

yay will handle the installation process, including fetching the package
from the AUR and resolving any dependencies.

Alternatively, if you prefer a more traditional approach, you can
manually build and install the penguins-eggs package from the AUR
using git and pkgbuild commands. Here's how:

1)  Open a terminal and run the following command to clone
    the penguins-eggs AUR repository:

```
git clone https://aur.archlinux.org/packages/penguins-eggs
```

2)  Change your current directory to the newly cloned repository:

```
cd penguins-eggs
```

3)  Build and install the package using pkgbuild command:

```
sudo makepkg -si
```

This command will build the package and prompt you for confirmation
before installing it.

## Method6: Installing on Manjaro Linux

On Manjaro, you can easily install the penguins-eggs package from the Manjaro community repository
using the pamac package manager. Here are the steps to install it:

1)  Open a terminal and run the following command to update your system
    packages:

```
sudo pamac upgrade
```

This command ensures that your system is up to date before installing
any new packages.

2)  Once the system is updated, you can install penguins-eggs by
    running the following command:

```
sudo pamac install penguins-eggs
```

The pamac command will handle the installation process, including
fetching the package from the Manjaro community repository and resolving
any dependencies. By following these steps, you should be able to
successfully install the penguins-eggs package on Manjaro using
the pamac package manager.

## Method7: installing by npm command

While it is technically possible to install penguins-eggs directly
as an npm package, it is worth noting that the npm packages may still
have dependencies that need to be installed separately.
Additionally, since penguins-eggs is developed with Node.js, it
is more commonly distributed as a package for specific Linux
distributions or available in the AUR. 

If you still prefer to install penguins-eggs using npm and handle the installation of
dependencies separately, you can follow these general steps:

1)  Ensure that you have Node.js and npm installed on your
    system.

This is the website of npm how to install it:

https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

or use the following steps based on your Linux distro:

# installing node.js

To install Node.js and npm on different Linux distributions, here
are the steps for Debian**-**based, Arch**-**based, Red Hat**-**based,
and Fedora**-**based systems:

## Debian-based (e.g., Ubuntu, Linux Mint):

1)  Open a terminal and update the package lists:

```
sudo apt update
```

2)  Install Node.js and npm:

```
sudo apt install nodejs npm
```

3)  Verify the installation:

```
node --version
npm --version
```

## Arch-based (e.g., Arch Linux, Manjaro):

1)  Open a terminal and update the package lists:

```
sudo pacman -Syu
```

2)  Install Node.js and npm:

```
sudo pacman -S nodejs npm
```
3)  Verify the installation:

```
node --version
npm --version
```

2)  Once you have Node.js and npm installed, you can
    install penguins-eggs by running the following command in a
    terminal:

```
sudo npm install -g penguins-eggs
```

This command will install the penguins-eggs package globally on your
system.

3)  After installing penguins-eggs, you will need to manually handle
    the installation of any dependencies that are required by the
    package. You can refer to the documentation or instructions
    provided with penguins-eggs to identify and install the
    necessary dependencies.

Please note that this method may require more manual effort and may not
be as straightforward as using the distribution-specific package
managers like `apt`, pacman or pamac. 

## Method 8: Using penguins-eggs from npm source

Using penguins-eggs from the source code can indeed provide benefits
such as easier debugging and the ability to review the code running on
your machine. It can also offer greater security and the potential
for collaboration on the project. Here are the steps to install and
use penguins-eggs from the source code:

1)  Install the required dependencies, including Node.js and
    the pnpm package manager. On Manjaro, you can run the following
    command to install them:

```
sudo pamac install nodejs pnpm devel-base
```

On Debian/Devuan/Ubuntu, it is recommended to use the NodeSource
repository to install Node.js version 18.x.

2)  Once Node.js and npm are installed, you can
    install pnpm globally by running the following command:

```
sudo npm i pnpm -g
```

3)  Clone the penguins-eggs source code repository by running the
    following command:

```
git clone https://github.com/pieroproietti/penguins-eggs
```

4)  Change your current directory to the penguins-eggs directory:

cd penguins-eggs

5)  Install the project dependencies using pnpm by running the following
    command:

```
sudo pnpm install
```
Note that pnpm is used instead of the traditional npm command, which
allows for faster compilation.

Once the installation is complete, you can
use penguins-eggs directly from the source code. For example, to
run the produce command with verbose output, you can use the following
command:

```
sudo ./eggs produce --verbose
```

Please note that when using the source code, you need to specify the
path to start eggs as `/eggs`, and you should launch it from
the `~/penguins-eggs` directory. 

The functionality remains the same as when using precompiled packages, 
but you have the advantage of being able to interact with the 
code directly.

Keep in mind that using the source code requires some technical
knowledge and may involve additional steps compared to using precompiled
packages.

# Updating the eggs

Once the package is installed, you can use the command 
`eggs tools ppa --add` to add the repository `penguins-eggs-ppa` and get all the
updates to eggs via the command apt. To do this simply issue the
command:

```
sudo eggs tools ppa --add
```


The eggs tools ppa command is used to add or remove PPA (Personal
Package Archive) repositories in the Debian family of operating
systems. Here is a breakdown of its usage:

In the EXAMPLES: section, you can find two usage EXAMPLES::

```
sudo eggs tools ppa \--add
```

This command adds the penguins-eggs PPA repository to the
system. PPAs are commonly used in Debian**-**based systems to
provide additional software packages that are not available in the
official repositories.

```
sudo eggs tools ppa --remove
```

This command removes the penguins-eggs PPA repository from the
system. Removing a PPA repository can be useful if you no longer
need the packages provided by that repository or if you want to clean up
your system. Please note that adding or removing PPA repositories
can have implications for your system, such as introducing new software
sources or removing access to certain packages. Exercise caution and
ensure that you are familiar with the PPA and its contents before adding
or removing it.

Here's a more detailed description of each flag used in the eggs tools
ppa command:

-   `-a, --add`: This flag adds the penguins-eggs PPA
    repository to the system. PPAs are additional software
    repositories commonly used in Debian**-**based systems to provide
    access to packages not available in the official repositories.
    Adding a PPA allows you to install software from that
    repository.

-   `-h, --help`: This flag displays the help message for
    the eggs tools ppa command. It provides information about the
    command\'s usage, flags, and EXAMPLES:.

-   `-n, --nointeractive`: This flag allows the operation to be
    performed without any user interaction. When this flag is used,
    the command will not prompt for any confirmation or additional
    input. It can be useful when you want to automate the process of
    adding or removing a PPA repository.

-   `-r, --remove`: This flag removes the penguins-eggs PPA
    repository from the system. Removing a PPA repository can be
    useful if you no longer need the packages provided by that
    repository or if you want to clean up your system.

-   `-v, --verbose`: This flag enables verbose output, providing
    more detailed information during the execution of the eggs tools
    ppa command. It can be helpful for understanding the progress
    and actions taken during the operation.

The eggs tools ppa command is used to add or remove PPA repositories in
the Debian family of operating systems. Adding a PPA allows you to
access additional software packages, while removing a PPA removes access
to those packages.

Here are a couple of EXAMPLES::
```
sudo eggs tools ppa --add
```
This command adds the penguins-eggs PPA repository to the system,
allowing you to install software packages from that repository.

```
sudo eggs tools ppa --remove
```
This command removes the penguins-eggs PPA repository from the
system, preventing further installations or updates from that
repository. Please note that adding or removing PPA repositories can
have implications for your system, such as introducing new software
sources or removing access to certain packages. Exercise caution and
ensure that you are familiar with the PPA and its contents before adding
or removing it.

**More details in source code:**

https://github.com/pieroproietti/penguins-eggs/blob/master/src/commands/tools/ppa.ts

# eggs version 

The eggs version command is used to display information about the
version of the **"**eggs**"** command**-**line interface **(**CLI**)**
tool. Here is a breakdown of its usage:

**USAGE**

\$ eggs version \[\--json\] \[\--verbose\]

![](media/image27.png){width="5.198173665791776in"
height="0.9246205161854768in"}

The command has the following flags:

**FLAGS**

`--verbose` Shows additional information about the CLI.

`--json` Formats the output as JSON.

By running the eggs version command without any flags, you will get the
version of the **"**eggs**"** CLI tool. It will display the version
number of the tool.

Note:

If you want more detailed information, you can use the \--verbose flag.
This will show additional information about the CLI, including the
architecture, Node.js version, operating system, and versions of any
plugins being used.


If you prefer the output to be in JSON format, you can use
the **\--**json flag. This will format the output as JSON, which can
be useful if you want to programmatically parse the version
information. []{dir="rtl"}Remember to include the eggs command
before the version subcommand when running the command.


![image30.jpg](media/image30.jpg)
