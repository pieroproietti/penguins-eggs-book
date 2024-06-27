# Chapter 5

# Installing Eggs

[]{dir="rtl"}There are multiple ways to install eggs as a **.**deb
package.

Important: Before installing Penguins\' Eggs, be aware that versions in
the penguins-eggs-10.0.x series require Node.js version 18 or higher.
This version may not be available by default on all Linux distributions.

However, you can easily install the required Node.js version using
NodeSource. This chapter provides instructions for installing Node.js
Binary Distributions using both .rpm and .deb packages, along with setup
and support scripts.

## Installing Nodejs

DEB Available architectures

NodeSource will continue to maintain the following architectures and may
add additional ones in the future.

-   amd64 (64-bit)

-   armhf (ARM 32-bit hard-float, ARMv7 and up: arm-linux-gnueabihf)

-   arm64 (ARM 64-bit, ARMv8 and up: aarch64-linux-gnu)

### DEB Supported Versions

#### **Ubuntu versions**

  -----------------------------------------------------------------------
  Distro Name             Node 18x    Node 20x    Node 21x    Node 22x
  ----------------------- ----------- ----------- ----------- -----------
  Ubuntu Bionic \^18.04   ❌          ❌          ❌          ❌

  Ubuntu Focal \^20.04    ✅          ✅          ✅          ✅

  Ubuntu Jammy \^22.04    ✅          ✅          ✅          ✅
  -----------------------------------------------------------------------

#### **Debian versions**

  -----------------------------------------------------------------------
  Distro Name             Node 18x    Node 20x    Node 21x    Node 22x
  ----------------------- ----------- ----------- ----------- -----------
  Debian 8 Jessie         ❌          ❌          ❌          ❌

  Debian 9 Stretch        ❌          ❌          ❌          ❌

  Debian 10 Buster        ✅          ✅          ✅          ✅

  Debian 11 Bullseye      ✅          ✅          ✅          ✅

  Debian 12 Bookworm      ✅          ✅          ✅          ✅
  -----------------------------------------------------------------------

Installation Instructions (DEB)

####  

**Node.js 22:**

##### Using Ubuntu (Node.js 22)

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo apt-get install -y curl

1.  **Download the Node.js setup script:**

**curl -fsSL https://deb.nodesource.com/setup_22.x -o**
nodesource_setup.sh

2.  **Run the Node.js setup script with sudo:**

sudo -E bash nodesource_setup.sh

3.  **Install Node.js:**

sudo apt-get install -y nodejs

4.  **Verify the installation:**

node -v

##### **Using Debian, as root (Node.js 22)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

apt-get install -y curl

1.  **Download the Node.js setup script:**

**curl -fsSL https://deb.nodesource.com/setup_22.x -o**
**nodesource_setup.sh**

2.  **Run the Node.js setup script with sudo:**

bash nodesource_setup.sh

3.  **Install Node.js:**

apt-get install -y nodejs

4.  **Verify the installation:**

node -v

**Node.js v20.x**:

##### **Using Ubuntu (Node.js 20)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo apt-get install -y curl

1.  **Download the Node.js setup script:**

**curl -fsSL https://deb.nodesource.com/setup_20.x -o**
**nodesource_setup.sh**

2.  **Run the Node.js setup script with sudo:**

sudo -E bash nodesource_setup.sh

3.  **Install Node.js:**

sudo apt-get install -y nodejs

4.  **Verify the installation:**

node -v

##### **Using Debian, as root (Node.js 20)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

apt-get install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh

2.  **Run the Node.js setup script with sudo:**

bash nodesource_setup.sh

3.  **Install Node.js:**

apt-get install -y nodejs

4.  **Verify the installation:**

node -v

**No**

**de.js v18.x**:

##### **Using Ubuntu (Node.js 18)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo apt-get install -y curl

1.  **Download the Node.js setup script:**

**curl -fsSL https://deb.nodesource.com/setup_18.x -o**
**nodesource_setup.sh**

2.  **Run the Node.js setup script with sudo:**

sudo -E bash nodesource_setup.sh

3.  **Install Node.js:**

sudo apt-get install -y nodejs

4.  **Verify the installation:**

node -v

## Removing Nodejs

Uninstall nodejs Ubuntu & Debian packages

To completely remove Node.js installed from the deb.nodesource.com
package methods above:

**Use sudo on Ubuntu or run this as root on debian**

apt-get purge nodejs &&\\

rm -r /etc/apt/sources.list.d/nodesource.list &&\\

rm -r /etc/apt/keyrings/nodesource.gpg

**Installing Nodejs**

Enterprise Linux Based Distributions

### **RPM Available architectures**

NodeSource will continue to maintain the following architectures and may
add additional ones in the future.

-   **x86_64** (64-bit)

-   **arm64** (ARM 64-bit, ARMv8 and up: *aarch64-linux-gnu*)

### **RPM Supported Versions**

#### Fedora versions

  ------------------------------------------------------------------------
  **Distro Name**          **Node      **Node      **Node      **Node
                           18x**       20x**       21x**       22x**
  ------------------------ ----------- ----------- ----------- -----------
  Fedora \>= 20 (20-\>28)  ❌          ❌          ❌          ❌

  Fedora \>= 29            ✅          ✅          ✅          ✅

  Fedora \>= 36            ✅          ✅          ✅          ✅
  ------------------------------------------------------------------------

#### Redhat versions

  ------------------------------------------------------------------------
  **Distro Name**      **Node 18x** **Node 20x** **Node 21x** **Node 22x**
  -------------------- ------------ ------------ ------------ ------------
  Redhat 7             ❌           ❌           ❌           ❌

  Redhat 8             ✅           ✅           ✅           ✅

  Redhat 9             ✅           ✅           ✅           ✅

  Redhat 9-minimal     ✅           ✅           ✅           ✅
  ------------------------------------------------------------------------

#### Amazon Linux versions

  --------------------------------------------------------------------------
  **Distro Name**        **Node 18x** **Node 20x** **Node 21x** **Node 22x**
  ---------------------- ------------ ------------ ------------ ------------
  Amazon Linux 2         ❌           ❌           ❌           ❌

  Amazon Linux 2023      ✅           ✅           ✅           ✅
  --------------------------------------------------------------------------

### RPM Installation Instructions

**Node.js v22.x**

##### Using RPM-based Systems (Node.js 22)

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo yum install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://rpm.nodesource.com/setup_22.x -o nodesource_setup.sh

2.  **Run the Node.js setup script as root:**

sudo bash nodesource_setup.sh

3.  **Install Node.js:**

sudo yum install -y nodejs

4.  **Verify the installation:**

node -v

##### 

##### **No root privileges (Node.js 22)**

Before you begin, ensure that curl is installed on your system.
If curl is not **installed, you can install it using the following
command:**

yum install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://rpm.nodesource.com/setup_22.x -o nodesource_setup.sh

2.  **Run the Node.js setup script as root:**

bash nodesource_setup.sh

3.  **Install Node.js:**

yum install -y nodejs

4.  **Verify the installation:**

node -v

**Node.js v20.x**

##### **As root (Node.js 20)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo yum install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://rpm.nodesource.com/setup_20.x -o nodesource_setup.sh

2.  **Run the Node.js setup script as root:**

sudo bash nodesource_setup.sh

3.  **Install Node.js:**

sudo yum install -y nodejs

4.  **Verify the installation:**

node -v

##### 

##### **No root privileges (Node.js 20)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

yum install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://rpm.nodesource.com/setup_20.x -o nodesource_setup.sh

2.  **Run the Node.js setup script as root:**

bash nodesource_setup.sh

3.  **Install Node.js:**

yum install -y nodejs

4.  **Verify the installation:**

node -v

**Node.js v18.x**

##### **As root (Node.js 18)**

Before you begin, ensure that curl is installed on your system.
If curl is not installed, you can install it using the following
command:

sudo yum install -y curl

1.  **Download the Node.js setup script:**

curl -fsSL https://rpm.nodesource.com/setup_18.x -o nodesource_setup.sh

2.  **Run the Node.js setup script as root:**

sudo bash nodesource_setup.sh

3.  **Install Node.js:**

sudo yum install -y nodejs

4.  **Verify the installation:**

node -v

**Uninstall nodejs Enterprise Linux packages**

To completely remove Node.js installed from the rpm.nodesource.com
package methods above:

Use sudo or run this as root

yum remove nodejs &&\\

rm -r /etc/yum.repos.d/nodesource\*.repo &&\\

yum clean all

**Installing Nodejs**

Other Distro

**Debian buster / bullseye, Ubuntu 20.04 / 22.04**

Changing from version 9.7.x to 10.0.x I\'m using a new way to package
penguins-eggs: nodejs is not more included on the package like before,
but rely on it\'s presence in available repos.

This is configured on the penguins-eggs package, who actually ask for
: nodejs (\>= 18)  on it\'s DEBIAN/control file.

Unfortunately, distros on this note and derivatives, have nodejs \>=18
available on the their original repository.

sudo apt-get install -y curl

curl -fsSL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh

sudo -E bash nodesource_setup.sh

**UBUNTU 18.04 bionic, Debian stretch and derivatives**

If you are using Ubuntu 18.04 bionic, or derivatives, I have good news
too!

It\'s not possible to install nodejs 18 on Ubuntu 18.04, but it\'s
possible to use the same procedure to install nodejs 16.

sudo apt-get install -y curl

curl -fsSL https://deb.nodesource.com/setup_16.x -o nodesource_setup.sh

sudo -E bash nodesource_setup.sh

Installing eggs

The most practical method is to add and use the
penguins**-**eggs**-**ppa repository**.**

## Method1:

## Install from source

Install penguins**-**eggs and configure it with a single
command[.]{dir="rtl"}

The get**-**eggs command is used to add the **"**penguins**-**eggs**"**
repository and configure it on Arch, Debian, Devuan, Ubuntu, or their
derivatives**.** Here\'s how you can use it:

1.  Clone the get**-**eggs repository:

![](media/image10.png){width="4.700588363954505in"
height="3.0358081802274715in"}

git clone https://github.com/pieroproietti/get-eggs

![](media/image11.png){width="5.125984251968504in"
height="1.5060531496062992in"}

Change into the get**-**eggs directory:

\$ cd get-eggs

![](media/image12.png){width="5.361157042869642in"
height="0.8749442257217848in"}

Run the get**-**eggs script with root privileges:

![](media/image13.png){width="4.582352362204724in"
height="1.6591863517060368in"}

sudo ./get-eggs

[]{dir="rtl"}By executing this script with root privileges, it will add
the necessary repositories to your system**.** On Arch Linux, it will
add the AUR repository **(**formerly known as **"**addaura**").** On
Debian**-**based systems, including Ubuntu, it will add a PPA
**(**Personal Package Archive**)** for **"**penguins**-**eggs**".**

Please note that running scripts with root privileges should be done
with caution**.** Make sure you trust the source and understand the
actions being performed by the script**.**

![](media/image14.png){width="5.144325240594926in"
height="2.9400798337707785in"}

## Method2: 

## penguins-eggs-ppa 

**Repository (Debian based)**

Using ppa depository on Debian based:

To use the repository, follow these steps:

1.  Copy and paste the following two lines into a terminal window:

\$curl -fsSL https://pieroproietti.github.io/penguins-eggs-ppa/KEY.gpg
\| sudo gpg \--dearmor -o /etc/apt/trusted.gpg.d/penguins-eggs.gpg

\$sudo echo "deb \[arch=\$(dpkg \--print-architecture)\]
https://pieroproietti.github.io/penguins-eggs-ppa ./" \| sudo tee
/etc/apt/sources.list.d/penguins-eggs.list \> /dev/null

![](media/image15.png){width="5.212497812773403in"
height="1.4185389326334208in"}

Now, you can use standard apt commands to install and upgrade the eggs
package**.** Remember to run sudo apt update to update the package lists
before installing or upgrading the eggs package**.**

\$sudo apt update

\$ sudo apt install eggs

[]{dir="rtl"}Once the eggs package is successfully installed, you can
use the eggs command**-**line tool to add the penguins**-**eggs**-**ppa
repository and receive updates via apt**.** To add the repository,
execute the following command:

\$ sudo eggs tools ppa \--add

![](media/image16.png){width="5.34287510936133in"
height="1.336706036745407in"}

Final:

![](media/image17.png){width="5.4301891951006125in"
height="2.1295417760279967in"}

[]{dir="rtl"}By following these steps, you can install the eggs package,
resolve any missing dependencies, and add the penguins**-**eggs**-**ppa
repository for future updates**.**

##  Method4: eggs package (Debian based)

[]{dir="rtl"}If you prefer not to include the penguins**-**eggs**-**ppa
repository in your system\'s repositories, you have an alternative
method to install the eggs package**.** Follow these steps:

1)  Visit the sourceforge site to download the latest version of the
    eggs package in **.**deb format**.**

2)  Once the package is downloaded, open a terminal and navigate to the
    directory where the **.**deb file is located**.**

https://sourceforge.net/projects/penguins-eggs/files/DEBS/

![](media/image18.png){width="5.322057086614174in"
height="1.4489162292213473in"}

3)  Install the eggs package using the dpkg command with sudo**.** For
    example:

sudo dpkg -i eggs-9.4.x.deb

![](media/image19.png){width="5.356871172353456in"
height="1.259342738407699in"}

4)  Since this is your first installation, there may be missing
    dependencies preventing the package from being fully installed**.**
    To resolve this, run the following command:

\$ sudo apt install -f

[]{dir="rtl"}This command will automatically install any missing
dependencies required by the eggs package**.**

![](media/image20.png){width="5.192057086614173in"
height="1.279242125984252in"}

5)  If you have the gdebi package manager installed on your system, you
    can use it to install the eggs package in graphical mode**.** Simply
    right**-**click on the **.**deb file, select **"**Open with GDebi
    Package Installer,**"** and follow the on**-**screen
    instructions**.**

![](media/image21.png){width="5.3798468941382325in"
height="4.09976924759405in"}

More details:

[]{dir="rtl"}SourceForge**.**net is a widely recognized platform that
has been serving the software development community for many years**.**
It has established itself as a reliable source for hosting and
distributing open**-**source software projects**.** By hosting projects
on SourceForge**.**net, developers can showcase their work, collaborate
with other developers, and make their software easily accessible to
users**.** When it comes to the installation of eggs,
SourceForge**.**net provides a convenient location to download the
necessary **.**deb package files**.** These files contain the software
package that you need to install on your system**.** By navigating to
the designated page for the penguins**-**eggs project on
SourceForge**.**net, you can access the list of available **.**deb
files**.**

[]{dir="rtl"}Downloading the appropriate **.**deb file for your system
architecture is crucial for a successful installation**.** Whether you
are using an AMD64 or i386 system, SourceForge**.**net offers the
necessary files to cater to your specific requirements**.** Once you
have downloaded the desired **.**deb file, you can proceed with the
installation process**.** Using the \`dpkg\` command with the \`**-**i\`
flag, you can install the eggs package onto your system**.** It is
important to note that running the installation command as a superuser
**(**using \`sudo\`**)** ensures that the necessary permissions are
granted for the installation process**.**

[]{dir="rtl"}During the installation, you may encounter dependency
issues**.** Dependencies are additional software components that need to
be present on your system for the eggs package to function
correctly**.** Resolving these dependencies is essential for a smooth
installation**.** Fortunately, the \`apt\` package manager provides a
convenient way to automatically resolve and install any missing
dependencies**.** By running **\`sudo apt -f install\`**, you can prompt
the package manager to fix any dependency**-**related issues**.**

After successfully installing the eggs package and resolving any
dependencies, it is always a good idea to verify the installation**.**
Using the \`eggs status\` command, you can check the current status of
the eggs package on your system**.** This command provides information
about the installed version and any relevant updates or
notifications**.**

By following these steps and utilizing SourceForge**.**net as a reliable
source for the eggs package, you can ensure a seamless installation
process and enjoy the benefits of this software on your system**.**

## Method5: installing on Arch Linux

To configure the Chaotic**-**AUR repository and install the
penguins**-**eggs package on Arch Linux, follow these steps:

1)  Import the Chaotic**-**AUR repository key by running the following
    command:

pacman-key \--recv-key FBA220DFC880C036 \--keyserver
keyserver.ubuntu.com

[]{dir="rtl"}Description: The pacman**-**key **\--**recv**-**key command
is used in Arch Linux**-**based distributions, such as Manjaro, to
import and trust a specific GPG key**.** This command is typically used
to validate the authenticity and integrity of packages downloaded from
specific repositories**.**

In the example you provided, FBA220DFC880C036 is the key ID that you
want to import, and keyserver**.**ubuntu**.**com is the keyserver from
which you want to retrieve the key**.**

To import the key using pacman**-**key **\--**recv**-**key, follow these
steps:

Open a terminal or command prompt**.**

Run the following command:

\$ sudo pacman-key \--recv-key FBA220DFC880C036 \--keyserver
keyserver.ubuntu.com

[]{dir="rtl"}This command will retrieve the specified key from the
keyserver and import it into your system\'s keyring**.** After the key
is imported, you need to trust it by running the following command:

\$ sudo pacman-key \--lsign-key FBA220DFC880C036

[]{dir="rtl"}This command will locally sign the key, indicating that you
trust it**.**

By importing and trusting the key, you can ensure the authenticity of
packages signed with that key when you install them using pacman or
related package managers**.**

2)  Sign the imported key by running the following command:

\$ sudo pacman-key \--lsign-key FBA220DFC880C036

3)  Install the Chaotic**-**AUR keyring and mirrorlist packages by
    running the following command:

\$sudo pacman -U
\'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst\'
\'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst\'

4)  Open the **/**etc**/**pacman**.**conf file in a text editor and add
    the following lines at the end:

\[chaotic-aur\]

Include = /etc/pacman.d/chaotic-mirrorlist

5)  Save the changes and exit the text editor**.**

6)  Update the package lists by running the following command:

\$ sudo pacman -Sy

7)  Finally, install the penguins**-**eggs package by running the
    following command:

\$ sudo pacman -Sy penguins-eggs

[]{dir="rtl"}By following these steps, you will successfully configure
the Chaotic**-**AUR repository and install the penguins**-**eggs package
on your Arch Linux system**.**

**on Arch Linux**, you have multiple options to install eggs**.** One
popular choice is to use the yay AUR helper**.** Here\'s how you can
install eggs using yay:

1)  Open a terminal and run the following command to install yay if you
    don\'t already have it:

\$sudo pacman -Sy yay

2)  Once yay is installed, you can use it to install eggs by running the
    following command:

\$ sudo yay -S penguins-eggs

yay will handle the installation process, including fetching the package
from the AUR **(**Arch User Repository**)** and resolving any
dependencies**.**

Alternatively, if you prefer a more traditional approach, you can
manually build and install the penguins**-**eggs package from the AUR
using git and pkgbuild commands**.** Here\'s how:

1)  Open a terminal and run the following command to clone
    the penguins**-**eggs AUR repository:

\$ git clone https://aur.archlinux.org/penguins-eggs.git
penguins-eggs-aur

2)  Change your current directory to the newly cloned repository:

\$ cd penguins-eggs-aur

3)  Build and install the package using pkgbuild command:

\$sudo makepkg -si

This command will build the package and prompt you for confirmation
before installing it**.**

## Method6: Installing on Manjaro Linux

[]{dir="rtl"}On Manjaro, you can easily install
the penguins**-**eggs package from the Manjaro community repository
using the pamac package manager**.** Here are the steps to install it:

1)  Open a terminal and run the following command to update your system
    packages:

\$ sudo pamac upgrade

This command ensures that your system is up to date before installing
any new packages**.**

2)  Once the system is updated, you can install penguins**-**eggs by
    running the following command:

\$ sudo pamac install penguins-eggs

The pamac command will handle the installation process, including
fetching the package from the Manjaro community repository and resolving
any dependencies**.** By following these steps, you should be able to
successfully install the penguins**-**eggs package on Manjaro using
the pamac package manager**.**

## Method7: installing by npm command

While it is technically possible to install penguins**-**eggs directly
as an npm package, it is worth noting that the npm packages may still
have dependencies that need to be installed separately**.**
Additionally, since penguins**-**eggs is developed with Node**.**js, it
is more commonly distributed as a package for specific Linux
distributions or available in the AUR**.** If you still prefer to
install penguins**-**eggs using npm and handle the installation of
dependencies separately, you can follow these general steps:

1)  Ensure that you have Node**.**js and npm installed on your
    system**.**

This is the website of npm how to install it:

https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

or use the following steps based on your Linux distro:

# installing node.js

To install Node**.**js and npm on different Linux distributions, here
are the steps for Debian**-**based, Arch**-**based, Red Hat**-**based,
and Fedora**-**based systems:

## Debian-based (e.g., Ubuntu, Linux Mint):

1)  Open a terminal and update the package lists:

sudo apt update

2)  Install Node**.**js and npm:

sudo apt install nodejs npm

3)  Verify the installation:

node \--version

npm \--version

## Arch-based (e.g., Arch Linux, Manjaro):

1)  Open a terminal and update the package lists:

sudo pacman -Syu

2)  Install Node**.**js and npm:

sudo pacman -S nodejs npm

3)  Verify the installation:

node \--version

npm \--version

## Red Hat-based (e.g., CentOS, RHEL):

1)  Open a terminal and update the package lists:

sudo yum update

2)  Enable the EPEL repository **(**Extra Packages for Enterprise
    Linux**)**:

sudo yum install epel-release

3)  Install Node**.**js and npm:

sudo yum install nodejs npm

4)  Verify the installation:

node \--version

npm \--version

## Fedora-based (e.g., Fedora):

1)  Open a terminal and update the package lists:

sudo dnf update

2)  Install Node**.**js and npm:

sudo dnf install nodejs npm

3)  Verify the installation:

node \--version

npm \--version

These steps should help you install Node**.**js and npm on the
respective Linux distributions**.** After installation, you can start
using Node**.**js and npm for your development needs**.**

![](media/image22.png){width="5.273392388451444in"
height="3.5877777777777777in"}

You can check if they are already installed by running the following
commands in a terminal:

node -v

npm -v

If they are not installed, you can refer to the Node**.**js and npm
documentation for instructions on how to install them**.**

![](media/image23.png){width="4.929396325459318in"
height="1.6823326771653544in"}

2)  Once you have Node**.**js and npm installed, you can
    install penguins**-**eggs by running the following command in a
    terminal:

\$ sudo npm install -g penguins-eggs

This command will install the penguins**-**eggs package globally on your
system**.**

![](media/image24.png){width="4.949583333333333in"
height="1.172998687664042in"}

3)  After installing penguins**-**eggs, you will need to manually handle
    the installation of any dependencies that are required by the
    package**.** You can refer to the documentation or instructions
    provided with penguins**-**eggs to identify and install the
    necessary dependencies**.**

Please note that this method may require more manual effort and may not
be as straightforward as using the distribution**-**specific package
managers like apt, yay, or pamac**.** It is generally recommended to use
the package manager specific to your Linux distribution whenever
possible, as it will handle the dependencies and installation process
more seamlessly**.**

## Method 8: Installing Eggs from npm source

Using penguins**-**eggs from the source code can indeed provide benefits
such as easier debugging and the ability to review the code running on
your machine**.** It can also offer greater security and the potential
for collaboration on the project**.** Here are the steps to install and
use penguins**-**eggs from the source code:

1)  Install the required dependencies, including Node**.**js and
    the pnpm package manager**.** On Manjaro, you can run the following
    command to install them:

sudo pamac install nodejs pnpm devel-base

On Debian**/**Devuan**/**Ubuntu, it is recommended to use the NodeSource
repository to install Node**.**js version 16**.**x**.**

2)  Once Node**.**js and npm are installed, you can
    install pnpm globally by running the following command:

sudo npm i pnpm -g

3)  Clone the penguins**-**eggs source code repository by running the
    following command:

git clone https://github.com/pieroproietti/penguins-eggs

4)  Change your current directory to the penguins**-**eggs directory:

cd penguins-eggs

5)  Install the project dependencies using pnpm by running the following
    command:

\$ sudo pnpm install

Note that pnpm is used instead of the traditional npm command, which
allows for faster compilation**.**

Once the installation is complete, you can
use penguins**-**eggs directly from the source code**.** For example, to
run the produce command with verbose output, you can use the following
command:

\$ sudo ./eggs produce \--verbose

Please note that when using the source code, you need to specify the
path to start eggs as **./**eggs, and you should launch it from
the \~**/**penguins**-**eggs directory**.** The functionality remains
the same as when using precompiled packages, but you have the advantage
of being able to interact with the code directly**.**

Keep in mind that using the source code requires some technical
knowledge and may involve additional steps compared to using precompiled
packages**.**

# Updating the eggs

Once the package is installed, you can use the command eggs tools ppa
--add to add the repository penguins**-**eggs**-**ppa and get all the
updates to eggs via the command apt**.** To do this simply issue the
command:

sudo eggs tools ppa --add

![](media/image25.png){width="5.173255686789151in"
height="1.9550579615048118in"}

![](media/image17.png){width="5.06507874015748in"
height="1.9863582677165355in"}

The eggs tools ppa command is used to add or remove PPA **(**Personal
Package Archive**)** repositories in the Debian family of operating
systems**.** Here is a breakdown of its usage:

![](media/image26.png){width="5.09423009623797in"
height="3.7283114610673667in"}

In the EXAMPLES: section, you can find two usage EXAMPLES::

\$ sudo eggs tools ppa \--add

This command adds the penguins**-**eggs PPA repository to the
system**.** PPAs are commonly used in Debian**-**based systems to
provide additional software packages that are not available in the
official repositories**.**

\$ sudo eggs tools ppa \--remove

This command removes the penguins**-**eggs PPA repository from the
system**.** Removing a PPA repository can be useful if you no longer
need the packages provided by that repository or if you want to clean up
your system**.** Please note that adding or removing PPA repositories
can have implications for your system, such as introducing new software
sources or removing access to certain packages**.** Exercise caution and
ensure that you are familiar with the PPA and its contents before adding
or removing it**.**

Here\'s a more detailed description of each flag used in the eggs tools
ppa command:

-   **-**a, **\--**add: This flag adds the penguins**-**eggs PPA
    repository to the system**.** PPAs are additional software
    repositories commonly used in Debian**-**based systems to provide
    access to packages not available in the official repositories**.**
    Adding a PPA allows you to install software from that
    repository**.**

-   **-**h, **\--**help: This flag displays the help message for
    the eggs tools ppa command**.** It provides information about the
    command\'s usage, flags, and EXAMPLES:**.**

-   **-**n, **\--**nointeractive: This flag allows the operation to be
    performed without any user interaction**.** When this flag is used,
    the command will not prompt for any confirmation or additional
    input**.** It can be useful when you want to automate the process of
    adding or removing a PPA repository**.**

-   **-**r, **\--**remove: This flag removes the penguins**-**eggs PPA
    repository from the system**.** Removing a PPA repository can be
    useful if you no longer need the packages provided by that
    repository or if you want to clean up your system**.**

-   **-**v, **\--**verbose: This flag enables verbose output, providing
    more detailed information during the execution of the eggs tools
    ppa command**.** It can be helpful for understanding the progress
    and actions taken during the operation**.**

The eggs tools ppa command is used to add or remove PPA repositories in
the Debian family of operating systems**.** Adding a PPA allows you to
access additional software packages, while removing a PPA removes access
to those packages**.**

Here are a couple of EXAMPLES::

\$ sudo eggs tools ppa \--add

This command adds the penguins**-**eggs PPA repository to the system,
allowing you to install software packages from that repository**.**

\$ sudo eggs tools ppa \--remove

This command removes the penguins**-**eggs PPA repository from the
system, preventing further installations or updates from that
repository**.** Please note that adding or removing PPA repositories can
have implications for your system, such as introducing new software
sources or removing access to certain packages**.** Exercise caution and
ensure that you are familiar with the PPA and its contents before adding
or removing it**.**

**More details in source code:**

https://github.com/pieroproietti/penguins-eggs/blob/master/src/commands/tools/ppa.ts

# eggs version 

The eggs version command is used to display information about the
version of the **"**eggs**"** command**-**line interface **(**CLI**)**
tool**.** Here is a breakdown of its usage:

**USAGE**

\$ eggs version \[\--json\] \[\--verbose\]

![](media/image27.png){width="5.198173665791776in"
height="0.9246205161854768in"}

The command has the following flags:

**FLAGS**

\--verbose Shows additional information about the CLI.

\--json Formats the output as JSON.

By running the eggs version command without any flags, you will get the
version of the **"**eggs**"** CLI tool**.** It will display the version
number of the tool**.**

Note:

If you want more detailed information, you can use the \--verbose flag.
This will show additional information about the CLI, including the
architecture, Node.js version, operating system, and versions of any
plugins being used.

![](media/image28.png){width="4.263176946631671in"
height="3.601175634295713in"}

If you prefer the output to be in JSON format, you can use
the **\--**json flag**.** This will format the output as JSON, which can
be useful if you want to programmatically parse the version
information**.** []{dir="rtl"}Remember to include the eggs command
before the version subcommand when running the command**.**

![](media/image29.png){width="4.549653324584427in"
height="1.6859120734908137in"}

![](media/image30.jpg){width="7.103583770778653in"
height="9.05511811023622in"}
