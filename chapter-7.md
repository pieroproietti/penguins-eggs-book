![](/media/chapter-7/chapter-7.jpg)
# chapter-7

# Producing ISO image file

Producing a live image from a system without including any personal data. If you are referring to creating a live image of an operating system (such as a live Linux distribution), this generally does not include personal data unless specifically configured to do so. Live images typically run from a read-only medium like a CD, DVD, or USB drive and don't modify the host system unless explicitly instructed to do so. However, ensuring that personal data is not captured or transmitted is a matter of configuring the live image and the software it runs to avoid such behavior. If you have specific concerns about privacy and data security, it is important to carefully review the settings and documentation of the live image you're using.

°Producing a live image from your system without your data° typically refers to creating a bootable image of an operating system that can be run directly from a USB drive, DVD, or other media without making any changes to the existing system or accessing the user's personal data. In this context, a live image is a snapshot or representation of an operating system that includes all the necessary files and configurations to run the system on a different computer. It allows users to experience and test an operating system without installing it on their own machines.

When creating a live image, the goal is to capture the entire operating system setup, including the necessary system files, applications, and configurations, while excluding any personal data or user-specific information. This ensures that the live image can be used safely and doesn't expose any sensitive or private information. The process of producing a live image typically involves using specialized software or tools that can create an image file from an existing system, compressing it, and making it bootable on different hardware. This allows users to boot into the live image on another computer and experience the operating system without affecting the host system or leaving any traces of personal data. Live images are commonly used for various purposes, such as testing new operating systems, providing a portable environment for troubleshooting or system recovery, or distributing pre-configured systems for educational or demonstration purposes.

## Step 1: cleaning the system

### Cleaning with eggs

The `eggs tools clean` command is used to clean various system logs and apt related files. Here is the breakdown of its usage:

```
sudo eggs tools clean
```

As all the other eggs commands, you can call it with `--help` to have the complete list of flags and a sample.

```
eggs tool clean --help

clean system log, apt, etc

USAGE
  $ eggs tools clean [-h] [-n] [-v]

FLAGS
  -h, --help           Show CLI help.
  -n, --nointeractive  no user interaction
  -v, --verbose        verbose

DESCRIPTION
  clean system log, apt, etc

EXAMPLES
  sudo eggs tools clean
```

### Cleaning with bleachbit

BleachBit is a popular open-source system cleaning and privacy tool for Linux operating systems. It helps you free up disk space, protect your privacy, and improve system performance by removing unnecessary files and data.

Here are some key features of BleachBit:

1. Disk Cleanup: BleachBit can scan and clean up various system and application files, such as temporary files, cache files, log files, and other unnecessary data that can accumulate over time.
2. Privacy Protection: BleachBit can help protect your privacy by securely deleting sensitive files, such as browser history, cookies, and temporary internet files. It can also clear the usage history of many applications, including web browsers, instant messengers, and more.
3. Freeing Disk Space: By removing unnecessary files, BleachBit can free up valuable disk space on your Linux system. This can help improve system performance and make more room for important files and applications.
4. Customizable Cleaning: BleachBit allows you to customize the cleaning process by selecting specific categories or types of files to clean. You can also exclude certain files or folders from being cleaned if desired.
5. Shredding Files: In addition to regular file deletion, BleachBit offers secure file shredding options. This ensures that deleted files cannot be recovered using data recovery tools.
6. Command-Line Interface: BleachBit provides a command-line interface for advanced users who prefer to automate or script cleaning operations.

Run bleachbit with:

```
sudo bleachbit
```

To obtain the latest version of BleachBit, you can download the appropriate package for your Linux distribution from the official BleachBit website. Here are the steps to select the correct package:

1. Visit the BleachBit website at [https://www.bleachbit.org/](https://www.bleachbit.org/).
2. Navigate to the °Download° section of the website.
3. Look for the available package options, which are typically provided in .deb format for Debian-based distributions and .rpm format for RPM-based distributions.
4. Identify your Linux distribution and select the corresponding package. For example, if you are using Ubuntu or a Debian-based distribution, select the .deb package. If you are using Fedora or a Red Hat-based distribution, select the .rpm package.
5. Click on the download link for the selected package to begin downloading it to your system.
6. Once the package is downloaded, you can install it using the appropriate package manager for your distribution. For example, on Debian-based systems, you can use the dpkg command to install the .deb package, and on RPM-based systems, you can use the rpm or dnf command to install the .rpm package.

BleachBit is indeed a feature-rich software designed to help you clean your computer, free up space, and maintain your privacy. Here's a breakdown of its key features and uses:

Privacy and File Deletion:

* BleachBit offers secure file deletion, ensuring that deleted files cannot be recovered. It is designed to delete files so completely that even data recovery tools cannot retrieve them.
* You can easily select the files you want to delete by checking the appropriate boxes and preview the changes before permanently deleting them.

Cross-Platform Compatibility:

* BleachBit is available for both Linux and Windows operating systems, allowing users of different platforms to benefit from its features.

Open Source and Free:

* BleachBit is free of charge and does not have any hidden costs or money trails. It is an open-source software, which means it can be shared, learned, and modified by users.

No Adware or Malware:

* BleachBit is free from adware, spyware, malware, backdoors, browser toolbars, or any °value-added software° that may compromise your system's security.

Multi-Language Support:

* It is translated into 65 languages, making it accessible to users worldwide.

Shredding and Overwriting:

* BleachBit includes features to shred files, hiding their contents and preventing data recovery.
* It can also overwrite free disk space, ensuring that previously deleted files cannot be restored.

Portable and Command-Line Support:

* The Windows version of BleachBit can be run without installation, making it portable and convenient.
* It also provides a command-line interface, allowing advanced users to automate cleaning operations through scripting.

Customization and Updates:

* BleachBit allows users to write their own cleaners using CleanerML, an XML-based markup language.
* It automatically imports and updates winapp2.ini cleaner files, providing access to over 2500 additional cleaners for Windows users.
* BleachBit frequently releases software updates with new features and improvements.

Cleaners:

* BleachBit includes a range of cleaners for popular applications like Google Chrome, Edge, Firefox, VLC, Acrobat Reader, and system logs and temporary files.
* It also provides advanced cleaners for specific tasks, such as clearing memory and swap on Linux, deleting broken shortcuts, cleaning APT for Debian-based distributions, and more.

Overall, BleachBit offers a comprehensive set of features to help you free up disk space, maintain your privacy, improve system performance, and prepare disk images for compression. Its customizable nature, frequent updates, and extensive range of cleaners make it a versatile tool for both Linux and Windows users.

### Bleachbit help

To see the help of cli commands of bleachbit instead of GUI ,Type :

```
bleachbit -h
```

Launch BleachBit: Once BleachBit is installed, you can launch it in either command line or graphical mode.

1.Command Line Mode: Open a terminal and run the bleachbit command followed by any desired options or arguments. For example, to clean the system, you can use the following command:

First: type the following command to list and then clean.

```
sudo bleachbit --l
```

For example:

```
sudo bleachbit --clean apt.clean
```

2.Graphical Mode: If you prefer a graphical interface, simply search for °BleachBit° in your application launcher or menu. Click on the BleachBit icon to launch the graphical interface, where you can select the cleaning options and perform the cleanup.

```
sudo bleachbit
```

Or

```
sudo bleachbit \--gui
```

1. Select Cleaning Options: In the BleachBit interface, you'll find a list of cleaning options for various categories such as system, web browsers, applications, and more. Check the boxes next to the items you want to clean.
2. Start Cleaning: Once you have selected the desired cleaning options, click on the °Delete° or °Clean° button to start the cleaning process. BleachBit will perform the selected cleanup actions, deleting unnecessary files and freeing up disk space.

## Step3: preparing the skel folder

### eggs tools skel&#x20;

The eggs tools skel command is used to update the skeleton directory `/etc/skel/` on a Linux system with the configuration files from a user's home directory. The `/etc/skel` directory is a special directory on Linux systems that serves as a template for new user accounts. When a new user account is created, the contents of the `/etc/skel` directory are copied into the user's home directory. This allows the new user to have a pre-configured set of files and directories.

Here are some key points about the /etc/skel directory:

1. Purpose: The primary purpose of the /etc/skel directory is to provide default configuration files and directories for new user accounts. It ensures that every new user starts with a basic set of files and directories that are commonly needed or desirable.
2. Contents: The /etc/skel directory typically contains a set of default files and directories that are copied into the user's home directory during account creation. This can include configuration files for various applications, default shell profiles (such as .bashrc or .zshrc), example documents, and directories for organizing files.
3. System-wide Changes: Modifying the contents of the /etc/skel directory can have system-wide implications. Any changes made to this directory will be reflected in the home directories of all new user accounts created on the system.
4. Customization: System administrators can customize the /etc/skel directory to suit their needs. By adding or modifying files and directories in this directory, they can establish a consistent environment for new users. This can include pre-configured settings, default document templates, or specific directory structures.
5. User Modifications: It's important to note that the contents of the /etc/skel directory only serve as initial defaults for new user accounts. Once a user account is created, the user has full control over their own home directory and can modify or remove the files and directories provided by /etc/skel.
6. Security Considerations: When customizing the /etc/skel directory, it's essential to ensure that sensitive information or potentially harmful files are not included. The directory should only contain files and directories that are safe and appropriate for all new users.

In summary, the /etc/skel directory acts as a template for new user accounts on Linux systems. It provides default files and directories that are copied into the user's home directory during account creation. By customizing the contents of /etc/skel, system administrators can establish a consistent environment for new users.

Here is a breakdown of its usage:

The command has the following EXAMPLES::

sudo eggs tools skel

and this will be the result:

Final:

you can manually add additional files to the /etc/skel directory by using the cp command. The /etc/skel directory serves as a template directory for creating new user home directories. When a new user is created, the contents of the /etc/skel directory are copied to the user's home directory.

To add files manually, you can use the following command:

sudo cp -r /home/$(whoami). /etc/skel/ -R

Replace /path/to/source/file with the actual path to the file you want to add. This command will copy the specified file to the /etc/skel directory.

By adding files to the /etc/skel directory, any new user created on the system will automatically have those files in their home directory. This can be useful for setting up default configurations or providing specific files for all new users.

This command updates the skeleton directory with the configuration files from the current user's home directory.

$ sudo eggs tools skel --user user-to-be-copied

for example:

```
sudo eggs tools skel --user david
```

This command updates the skeleton directory with the configuration files from the specified user's home directory `user-to-be-copied`, The skeleton directory `/etc/skel` is used as a template when creating new user accounts on Linux systems. By updating it with the configuration files from a user's home directory, any new user accounts created on the system will have the same initial configuration as the specified user. Please note that the /etc/skel directory is typically used as a template for creating new user accounts. The contents of this directory are automatically copied to a new user's home directory when the account is created. Be cautious when modifying or replacing the contents of `/etc/skel` to avoid unintended consequences.

## Step 4: prepare ISO for offline installation

The eggs tools yolk command is used to configure the °eggs° tool to install software packages without requiring an internet connection.

The command has the following example:

```
sudo eggs tools yolk
```

The path of downloaded packages is: `/var/local/yolk`

This command configures calamares or krill to install software packages without relying on an internet connection. By executing this command with administrative privileges (sudo), the necessary configurations are applied to enable offline installations. The exact details of how the eggs tool handles offline installations may depend on its implementation and configuration. It could involve pre-downloading packages, setting up a local package repository, or utilizing other mechanisms to enable installation without internet access.

­~~­~~

## Step 5: eggs produce&#x20;

### eggs produce command

The eggs produce command is used to create a live image of your system without including your personal data. It allows you to generate a snapshot of your system that can be used for various purposes such as creating a bootable USB or testing your system in a virtual environment. Here are the options and flags available for the eggs produce command:

As usual get a look to: `eggs produce --help`

```
produce a live image from your system whithout your data

USAGE
  $ eggs produce [--addons <value>...] [--basename <value>] [-c] [-C]
    [--excludes <value>...] [-h] [--links <value>...] [-m] [-N] [-n] [-p] [-P
    <value>] [--release] [-s] [-f] [--theme <value>] [-u] [-v] [-y]

FLAGS
  -C, --cryptedclone         crypted clone
  -N, --noicon               no icon eggs on desktop
  -P, --prefix=<value>       prefix
  -c, --clone                clone
  -f, --standard             standard compression: xz -b 1M
  -h, --help                 Show CLI help.
  -m, --max                  max compression: xz -Xbcj ...
  -n, --nointeractive        no user interaction
  -p, --pendrive             optimized for pendrive: zstd -b 1M
                             -Xcompression-level 15
  -s, --script               script mode. Generate scripts to manage iso build
  -u, --unsecure             /root contents are included on live
  -v, --verbose              verbose
  -y, --yolk                 force yolk renew
      --addons=<value>...    addons to be used: adapt, ichoice, pve, rsupport
      --basename=<value>     basename
      --excludes=<value>...  use: static, homes, home
      --links=<value>...     desktop links
      --release              release: remove penguins-eggs, calamares and
                             dependencies after installation
      --theme=<value>        theme for livecd, calamares branding and partitions

DESCRIPTION
  produce a live image from your system whithout your data

EXAMPLES
  sudo eggs produce                    # fast compression

  sudo eggs produce --max              # max compression

  sudo eggs produce --pendrive         # compression optomized pendrive

  sudo eggs produce --clone            # clone

  sudo eggs produce --cryptedclone     # crypted clone

  sudo eggs produce --basename=colibri

  sudo eggs produce --theme lastos

  sudo eggs produce --excludes static  # you can customize it

  sudo eggs produce --excludes homes   # exclude /home/*

  sudo eggs produce --excludes home    # exclude ~/*

```

The command allows for various combinations of options and flags, depending on your specific requirements. The provided EXAMPLES: demonstrate different usage scenarios for the eggs produce command.

More details on options:

The \`\`--addons \`

The ``--addons <value>` option allows you to specify additional addons to be used during the image creation process. You can provide multiple addons by separating them with commas. For example, if you want to include the `adapt`, `ichoice`, `pve`, and `rsupport` addons, you would use the`` --addons \` option like this:

`--addons adapt,ichoice,pve,rsupport`

This will ensure that these addons are included when generating the live image of your system. Feel free to customize the list of addons according to your specific needs.

The `--basename <value>` option allows you to set the base name for the generated ISO image file. When creating the live image, you can provide a custom name that will be used as the base for the resulting file. Here's an example:

`--basename colibri-test`

By using this option, the generated image file will have `colibri-test` as its base name. The actual file name may include additional information, such as the image format or extension, but the base name you provide will be used as the starting point for the file name. You can replace °colibri° with any desired name for the image file.

* `--clone`: This option allows you to create a clone of the system. When used during the image creation process, it will generate an full copy of the system, including all files, settings, and configurations.
* `--cryptedclone` option is similar to the `--clone`, but with an added layer of security. When you use this option during the image creation process, it not only creates a clone of the system but also encrypts the resulting image.

By encrypting the image, it ensures that the data within the clone is secure and protected from unauthorized access. This can be particularly useful when dealing with sensitive information or when you want to ensure the privacy and confidentiality of the cloned system.

* `--standard`: This option specifies the use of standard compression: plain `xz` during the image creation. It means that the resulting image file will be compressed using a standard compression algorithm, balancing the trade-off between compression speed and the resulting size of the image.

So, by using the `--standard` option, you can create an image with a compressed file size while maintaining a reasonable compression speed.

* `--max`: This option instructs the system to use maximum compression during the image creation. It applies a more aggressive compression algorithm, which may take more time but can result in a smaller image file size.
* `nointeractive`: When this option is used, the command runs in non-interactive mode, meaning it does not require any user interaction. It allows the command to be executed automatically without any prompts or input required from the user.
* `--prefix`: This option allows you to specify a prefix value for the command. The exact functionality and purpose of this prefix value may depend on the specific command you are referring to. It could be used as a prefix for file names, directories, or other elements involved in the command's execution.
* `--script`: When used, this option enables script mode for the command. In script mode, the command generates scripts that can be used to manage the ISO build. These scripts can be helpful for automating certain tasks or customizing the ISO build process according to specific requirements.
* `unsecure`: Including this option instructs the command to include the contents of `/home/` and the full contents of `/root` on the live system. This option may be useful in certain scenarios where you need to include additional files or configurations from these directories in the resulting live system.
* `--verbose`
* `--yolk`: When you include `--yolk`, it forces the renewal of the yolk. The specific meaning and functionality of the yolk can vary depending on the context of the command you are referring to. In general, forcing a yolk renewal typically implies that a specific component or configuration associated with the yolk will be updated or refreshed. The exact nature of the yolk and the changes made during renewal depend on the command and its specific implementation. The yolk could represent a variety of things depending on the context. It could refer to a software package, a configuration file, a library, or any other relevant component that plays a role in the execution or behavior of the command.

1. \--addons=\<value>...: This option allows you to specify addons to be used. The available addon options are adapt, ichoice, pve, and rsupport. You can include multiple addons by providing them as a comma-separated list.

The --addons=\<value>... option allows you to specify addons to be used with the command. The available addon options are adapt, ichoice, pve, and rsupport. To include multiple addons, you can provide them as a comma-separated list. For example, if you want to include both adapt and pve addons, you would use the option like this:

\--addons=adapt,pve

This will instruct the command to include the specified addons during its execution. The addons you specify can provide additional functionality, features, or configurations to enhance the command's behavior according to your needs. Make sure to consult the command's documentation or help text for more details on how to use the --addons option and the specific effects of each addon.

The --basename=\<value> option allows you to set the basename for the resulting output or file generated by the command. The basename typically refers to the base name or identifier of the file. To set a custom value for the basename, you would replace \<value> with the desired name or identifier you want to assign to the output. For example:

By specifying `--excludes`, you can selectively apply or not same `exludes.list`

* `--release` for final release you can add this tag. It will force calamares or krill to remove penguins-eggs, calamares it'self from the installated system.

1. Maximizing compression: This action aims to optimize the compression of files or data, potentially resulting in smaller file sizes or more efficient storage utilization. By including the --release option, you instruct the command to prioritize compression during the release process.
2. Removing penguins-eggs: This action involves removing or excluding the penguins-eggs component from the release. The specific purpose or functionality of penguins-eggs depends on the context of the command. By using the --release option, you indicate that you want to exclude this component from the final release.
3. Removing calamares after installation: Calamares is a popular open-source installation framework. When you include the --release option, it signifies that you want to remove the Calamares component after the installation process is complete. This action can be useful if you no longer require the installation framework once the system is set up.

The exact implications and effects of using the --release option may vary depending on the specific command and its implementation. It's important to consult the command's documentation or help text for further details on the actions performed during the release process and any additional considerations associated with this option.

\--theme=\<value>: This option allows you to set the theme for the livecd, calamares branding, and partitions. You can provide a custom value to define the desired theme. The --theme=\<value> option enables you to set the theme for various components such as the livecd, calamares branding, and partitions. You can provide a custom value to define the desired theme. To set a custom theme, replace \<value> with the name or identifier of the theme you wish to use. For instance:

\--theme=mytheme

In this example, the theme is set to °mytheme". By specifying a theme, you can customize the appearance, styling, and visual elements of the livecd, calamares branding, and partitions according to your preferences or requirements. The specific effects of the theme option may vary depending on the command and its implementation. It's recommended to consult the command's documentation or help text to understand the available themes, any specific requirements for using custom themes, and how they are applied to the respective components. Remember that the theme option provides an opportunity to personalize the visual aspects of the command's output, making it more aligned with your desired aesthetic or branding. \[]{dir="rtl"}Here are some EXAMPLES: demonstrating the usage of the sudo eggs produce command with different options:

sudo eggs produce

This command will execute the °produce° action without any additional options.

sudo eggs produce --standard

This command will execute the °produce° action with the standard option.

sudo eggs produce --max

This command will execute the °produce° action with the max option.

sudo eggs produce --max --basename=colibri

This command will execute the °produce° action with the max option and set the basename to °colibri".

sudo eggs produce --cryptedclone

This command will execute the °produce° action with the cryptedclone option.

sudo eggs produce --clone

This command will execute the °produce° action with the clone option.

sudo eggs produce --basename=colibri

This command will execute the °produce° action and set the basename to °colibri".

sudo eggs produce --basename=colibri --theme /path/to/theme --addons adapt

This command will execute the °produce° action, set the basename to °colibri°, use a custom theme located at "/path/to/theme°, and include the °adapt° addon. Please note that these EXAMPLES: assume the existence of a valid sudo eggs produce command and may require additional parameters or options depending on the specific context. Make sure to consult the command's documentation or help text for accurate usage instructions. Here are a few more EXAMPLES: showcasing different usage scenarios for the sudo eggs produce command:

sudo eggs produce --addons adapt,debug

This command will execute the °produce° action with the °adapt° and °debug° addons included.

sudo eggs produce --release

This command will execute the °produce° action and apply specific actions during the release process, such as maximizing compression, removing penguins-eggs, and removing calamares after installation.

sudo eggs produce --filters custom,dev

This command will execute the °produce° action and apply the °custom° and °dev° filters.

sudo eggs produce --theme=mytheme

This command will execute the °produce° action and set the theme to °mytheme° for the livecd, calamares branding, and partitions.

sudo eggs produce --basename=colibri --theme /path/to/theme

This command will execute the °produce° action, set the base name to °colibri°, and use a custom theme located at "/path/to/theme".

sudo eggs produce --max --filters custom --theme=default

This command will execute the °produce° action with the max option, apply the °custom° filter, and set the theme to the default theme.

sudo eggs produce --clone --basename=backup

This command will execute the °produce° action with the clone option and set the basename to °backup". Remember to adjust the options and values according to your specific requirements and the available features of the sudo eggs produce command. Additionally, consult the command's documentation or help text for a comprehensive understanding of the available options and their effects.

![](media/image96.png){width="5.12823053368329in" height="2.910598206474191in"}

After creating the ISO file:

![](media/image97.png){width="4.943823272090989in" height="2.1905479002624673in"}

The path of ISO file:

![](media/image98.png){width="4.175096237970254in" height="1.3905653980752406in"}

The default location of the ISO file when mounting it in a Linux system. In some cases, the ISO file may be mounted in the .mnt directory, which is a hidden directory. To access hidden directories in a file manager, you can typically press Ctrl + h to toggle the visibility of hidden files and directories.![](media/image99.png){width="4.3735323709536305in" height="1.2139807524059492in"}

Default grub boot menu:

![](media/image100.png){width="3.612580927384077in" height="1.8858366141732283in"}

![image101.jpg](media/image101.jpg){width="7.103583770778653in" height="9.05511811023622in"}
