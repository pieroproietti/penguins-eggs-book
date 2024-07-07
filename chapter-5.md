![](/media/chapter-5/chapter-5.jpg)

# Chapter 5

# Installing penguins-eggs
penguins-eggs is the package name of the package containig the eggs tool.

There are multiple ways to install penguins-eggs, the most practical way
is to use [get-eggs](https://github.com/pieroproietti/get-eggs) repository.

## Method1: using `get-eggs` (Arch/Debian/Devuan/Ubuntu)

The `get-eggs` command is used to add the `penguins-eggs-ppa`
repository, nodesource repository - when need - and configure 
penguins-eggs on Arch, Debian, Devuan, Ubuntu, or their
derivatives. 

You need just a prerequisites: `git`. If you don't have `git` installed, just install it before: 
`sudo apt install git` on Debian, or `sudo pacman -Sy git` for Arch,

Here's how you can use it, just copy and paste:

```
git clone https://github.com/pieroproietti/get-eggs
cd get-eggs
sudo ./get-eggs
```

By executing `sudo ./get-eggs` with root privileges, it will add
the necessary repositories to your system. On Arch Linux, it will
add the [chaotic-aur](https://aur.chaotic.cx/) repository while on Debian-based systems, including Devuan and
Ubuntu, it will add [penguins-eggs-ppa](https://github.com/pieroproietti/penguins-eggs-ppa).

Not only, `get-eggs` will take cure to add [nodesource repository](https://github.com/nodesource/distributions) , 
when `nodejs>18` is not available on the original repositories of the distro.

Please note that running scripts with root privileges should be done
with caution. Make sure you trust the source and understand the
actions being performed by the script.

## Method2: download the package from sourceforge (Debian/Devuan/Ubuntu)

If you prefer not to include the `penguins-eggs-ppa`
repository in your system's repositories, you have an alternative
method to install the eggs package. Follow these steps:

1)  Visit the [sourceforge page](https://sourceforge.net/projects/penguins-eggs/files/DEBS/) 
    to download the latest version of the eggs package in .deb format.

2)  Once the package is downloaded, open a terminal and go 
    where the .deb file is located.

3)  Install the eggs package using the dpkg command with sudo. For
    example:

```
sudo dpkg -i eggs-10.0.x-amd64.deb
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

When it comes to the installation of eggs, sourceForge.net provides a
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


## Methos3: adding chaothic-aur repository manually (Archlinux)

To configure the [chaotic-aur](https://aur.chaotic.cx/docs) follow the instructions on their site.

Finally, install the penguins-eggs package by running:

```
sudo pacman -Sy penguins-eggs
```
## Method4: using yay (Archlinux)

One popular choice on Arch is to use the yay, an AUR helper. 
Here's how you can install penguins-eggs using yay:

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

## Method5: build the package (Arch)

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


## Use penguins-eggs from source code

Using penguins-eggs from the source code can indeed provide benefits
such as easier debugging and the ability to review the code running on
your machine. It can also offer greater security and the potential
for collaboration on the project. Here are the steps to install and
use penguins-eggs from the source code:

1)  Install the required dependencies, including Node.js >18 and
    the pnpm package manager. 
    
On Debian/Devuan/Ubuntu, can be necessary to configure and use the NodeSource
repository to install Node.js > 18.x.

On Arch, a `sudo pacman -Syu nodejs`, will be enpught, on Manjaro, you can 
run the following command: `sudo pamac install nodejs pnpm devel-base`


2)  Once nodejs and npm are installed, you can
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

```
cd penguins-eggs
```

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

Another advantage of using source code, come from the possibility to create your 
de packages. Just use:

```
cd penguins-eggs
pnpm deb
```
you will get your package under `./perrisbrewery/work...`.


# Updating penguins-eggs

If you are on Debian and configured the `penguins-eggs-ppa` repository, then you can use just `sudo apt update` to update penguins-eggs.

The same on Arch with `chaoric-aur` or in Manjaro using community repo, with:
```
sudo pacman -Syu
```

![image30.jpg](media/image30.jpg)
