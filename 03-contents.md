# Contents

#  {#section .TOC-Heading}

* [What is the Penguins-eggs book?](/01-about.md#what-is-the-penguins-eggs-book)
    * [Introduction](/02-introduction.md#introduction)
    * [Contents at a Glance](/03-contents.md#contents) index
    * [The road map of this book](/04-road-map.md#the-road-map-of-this-book)
* [Chapter 1](/10-chapter-1.md#chapter-1)
    * [What is Penguins-eggs?](/10-chapter-1.md#what-is-penguins-eggs)
    * [Why Penguins-eggs?](/10-chapter-1.md#why-penguins-eggs)
    * [Top Penguins-eggs features](/10-chapter-1.md#top-penguins-eggs-features)
    * [fast and efficient](/10-chapter-1.md#fast-and-efficient)
    * [Supports Compression Algorithm)](/10-chapter-1.md#supports-compression-algorithm)
    * [Supports Clone](/10-chapter-1.md#supports-clone)
    * [Cuckoo and PXE boot](/10-chapter-1.md#cuckoo-and-pxe-boot)
    * [Supports Both TUI/GUI Installer](/10-chapter-1.md#supports-both-tuigui-installer)
    * [Repository lists](/10-chapter-1.md#repository-lists)
    * [Wardrobe](/10-chapter-1.md#wardrobe)
    * [Supporting Multiple Distributions](/10-chapter-1.md#supporting-multiple-distributions)
    * [Supports hardware architectures](/10-chapter-1.md#supports-hardware-architectures)
    * [Supports privacy and security](/10-chapter-1.md#supports-privacy-and-security)

* [Chapter 2)](/20-chapter-2.md)
    * [Pre-build and concept](/20-chapter-2.md#pre-build-and-concept)
    * [Live ISO images](/20-chapter-2.md#live-iso-images)
    * [Understanding Live ISO Images](/20-chapter-2.md#understanding-live-iso-images)
    * [Benefits of Live ISO Images](/20-chapter-2.md#benefits-of-live-iso-images)
    * [Creating Live ISO Images in Linux](/20-chapter-2.md#creating-live-iso-images-in-linux)
    * [Remastering](/20-chapter-2.md#remastering)
    * [Building process](/20-chapter-2.md#building-process)
    * [The ISO image file](/20-chapter-2.md#the-iso-image-file)
    * [UDF - Universal disk format](/20-chapter-2.md#universal-disk-format-udf)
    * [Live system file](/20-chapter-2.md#live-system-file)
    * [Introduction to SquashFS](/20-chapter-2.md#introduction-to-squashfs)
    * [File Compression](/20-chapter-2.md#file-compression)
    * [Structure of SquashFS](/20-chapter-2.md#structure-of-squashfs)
    * [Read-Only Nature](/20-chapter-2.md#read-only-nature)
    * [Use Cases](/20-chapter-2.md#use-cases)
    * [Handling Compression](/20-chapter-2.md#handling-compression)
    * [Customization and Optimization](/20-chapter-2.md#customization-and-optimization)
    * [Compatibility and Performance](/20-chapter-2.md#compatibility-and-performance)
    * [Mksquashfs ](/20-chapter-2.md#mksquashfs)
    * [Introduction to UEFI Boot](/20-chapter-2.md#introduction-to-uefi-boot)
    * [Key Advantages of UEFI Boot](/20-chapter-2.md#key-advantages-of-uefi-boot)
    * [UEFI Boot Process](/20-chapter-2.md#uefi-boot-process)
    * [Compatibility with Legacy BIOS](/20-chapter-2.md#compatibility-with-legacy-bios)
    * [UEFI Boot Components](/20-chapter-2.md#uefi-boot-components)
    * [Secure Boot and UEFI](/20-chapter-2.md#secure-boot-and-uefi)
    * [UEFI Shell](/20-chapter-2.md#uefi-shell)
    * [UEFI Variables](/20-chapter-2.md#uefi-variables)
    * [Vendor-specific UEFI Features](/20-chapter-2.md#vendor-specific-uefi-features)
    * [Legacy BIOS](/20-chapter-2.md#legacy-bios)
    * [Operating Principles of Legacy BIOS](/20-chapter-2.md#operating-principles-of-legacy-bios)
    * [Key Characteristics of Legacy BIOS](/20-chapter-2.md#key-characteristics-of-legacy-bios)
    * [Legacy and Modern Computing Environments](/20-chapter-2.md#legacy-and-modern-computing-environments)
    * [ISOLINUX [40](#isolinux)](/20-chapter-2.md#isolinux)

    * [Syslinux [41](#syslinux)](/20-chapter-2.md#syslinux)
    * [Mkisofs [42](#mkisofs)](/20-chapter-2.md#mkisofs)
    * [Genisoimage [43](#genisoimage)](/20-chapter-2.md#genisoimage)
    * [Isohybrid [45](#isohybrid)](/20-chapter-2.md#isohybrid)
    * [Host.conf [45](#host.conf)](/20-chapter-2.md#host.conf)
    * [language: \'en_US.UTF-8\'](/20-chapter-2.md#language-en_us.utf-8)
    * [Background and Significance](/20-chapter-2.md#background-and-significance)
    * [Implementation and Configuration](/20-chapter-2.md#implementation-and-configuration)
    * [Language Support and Internationalization](/20-chapter-2.md#language-support-and-internationalization)
    * [Impact on Software Development and Localization](/20-chapter-2.md#impact-on-software-development-and-localization)
    * [User Experience and Text Handling](/20-chapter-2.md#user-experience-and-text-handling)
    * [Maintenance and System Administration](/20-chapter-2.md#maintenance-and-system-administration)

[Chapter 3 [49](#chapter-3)](#chapter-3)

[Unnecessary tools and files
[49](#unnecessary-tools-and-files)](#unnecessary-tools-and-files)

[Cleaning [49](#cleaning)](#cleaning)

[how to create a privacy-focused Linux environment?
[50](#how-to-create-a-privacy-focused-linux-environment)](#how-to-create-a-privacy-focused-linux-environment)

[Exclude File and directory
[55](#exclude-file-and-directory)](#exclude-file-and-directory)

[Cleaning Tools [59](#cleaning-tools)](#cleaning-tools)

[BleachBit [60](#bleachbit)](#bleachbit)

[Stacer [60](#stacer)](#stacer)

[Sweeper [60](#sweeper)](#sweeper)

[Chapter 4 [63](#chapter-4)](#chapter-4)

[Necessary file and tools
[63](#necessary-file-and-tools)](#necessary-file-and-tools)

[Filesystem Hierarchy Standard (FHS)
[70](#filesystem-hierarchy-standard-fhs)](#filesystem-hierarchy-standard-fhs)

[Necessary tools and packages
[71](#necessary-tools-and-packages)](#necessary-tools-and-packages)

[Isolinux [71](#isolinux-1)](#isolinux-1)

[Live-boot [72](#live-boot)](#live-boot)

[Live-boot-doc [72](#live-boot-doc)](#live-boot-doc)

[Live-boot-initramfs-tools
[73](#live-boot-initramfs-tools)](#live-boot-initramfs-tools)

[Squashfs-tools [74](#squashfs-tools)](#squashfs-tools)

[Syslinux [74](#syslinux-1)](#syslinux-1)

[Syslinux-common [75](#syslinux-common)](#syslinux-common)

[Cryptsetup [76](#cryptsetup)](#cryptsetup)

[Dosfstools [76](#dosfstools)](#dosfstools)

[Dpkg-dev [77](#dpkg-dev)](#dpkg-dev)

[Coreutils [77](#coreutils)](#coreutils)

[Genisoimage [78](#genisoimage-1)](#genisoimage-1)

[Whoami [79](#whoami)](#whoami)

[Cryptsetup [79](#cryptsetup-1)](#cryptsetup-1)

[Curl [80](#curl)](#curl)

[Dosfstools [81](#dosfstools-1)](#dosfstools-1)

[Dpkg-dev [81](#dpkg-dev-1)](#dpkg-dev-1)

[lsb-release [82](#lsb-release)](#lsb-release)

[lvm2 [83](#lvm2)](#lvm2)

[parted [83](#parted)](#parted)

[pxelinux [84](#pxelinux)](#pxelinux)

[rsync [85](#rsync)](#rsync)

[Squashfs-tools [85](#squashfs-tools-1)](#squashfs-tools-1)

[sshfs [86](#sshfs)](#sshfs)

[syslinux-common [87](#syslinux-common-1)](#syslinux-common-1)

[Genisoimage [87](#genisoimage-2)](#genisoimage-2)

[Chapter 5 [89](#chapter-5)](#chapter-5)

[Installing Eggs [89](#installing-eggs)](#installing-eggs)

[Installing Nodejs [89](#installing-nodejs)](#installing-nodejs)

[DEB Supported Versions
[89](#deb-supported-versions)](#deb-supported-versions)

[Removing Nodejs [93](#removing-nodejs)](#removing-nodejs)

[RPM Installation Instructions
[94](#rpm-installation-instructions)](#rpm-installation-instructions)

[Method1: [98](#method1)](#method1)

[Install from source [98](#install-from-source)](#install-from-source)

[Method2: [101](#method2)](#method2)

[penguins-eggs-ppa [101](#penguins-eggs-ppa)](#penguins-eggs-ppa)

[Method4: eggs package (Debian based)
[103](#method4-eggs-package-debian-based)](#method4-eggs-package-debian-based)

[Method5: installing on Arch Linux
[107](#method5-installing-on-arch-linux)](#method5-installing-on-arch-linux)

[Method6: Installing on Manjaro Linux
[110](#method6-installing-on-manjaro-linux)](#method6-installing-on-manjaro-linux)

[Method7: installing by npm command
[111](#method7-installing-by-npm-command)](#method7-installing-by-npm-command)

[installing node.js [111](#installing-node.js)](#installing-node.js)

[Debian-based (e.g., Ubuntu, Linux Mint):
[111](#debian-based-e.g.-ubuntu-linux-mint)](#debian-based-e.g.-ubuntu-linux-mint)

[Arch-based (e.g., Arch Linux, Manjaro):
[112](#arch-based-e.g.-arch-linux-manjaro)](#arch-based-e.g.-arch-linux-manjaro)

[Red Hat-based (e.g., CentOS, RHEL):
[112](#red-hat-based-e.g.-centos-rhel)](#red-hat-based-e.g.-centos-rhel)

[Fedora-based (e.g., Fedora):
[113](#fedora-based-e.g.-fedora)](#fedora-based-e.g.-fedora)

[Method 8: Installing Eggs from npm source
[115](#method-8-installing-eggs-from-npm-source)](#method-8-installing-eggs-from-npm-source)

[Updating the eggs [116](#updating-the-eggs)](#updating-the-eggs)

[eggs version [120](#eggs-version)](#eggs-version)

[Chapter 6 [124](#chapter-6)](#chapter-6)

[Eggs Installer [124](#eggs-installer)](#eggs-installer)

[1.Calamares Installer (GUI):
[124](#calamares-installer-gui)](#calamares-installer-gui)

[2.Krill Installer (TUI):
[124](#krill-installer-tui)](#krill-installer-tui)

[Method 1. Calamares installer (GUI)
[125](#method-1.-calamares-installer-gui)](#method-1.-calamares-installer-gui)

[What is calamares [125](#what-is-calamares)](#what-is-calamares)

[Calamares modules [125](#calamares-modules)](#calamares-modules)

[Calamares installation
[127](#calamares-installation)](#calamares-installation)

[Step 1:  installing Calamares using the distribution\'s repository
[127](#step-1-installing-calamares-using-the-distributions-repository)](#step-1-installing-calamares-using-the-distributions-repository)

[Step 2: installing calamares with eggs
[130](#step-2-installing-calamares-with-eggs)](#step-2-installing-calamares-with-eggs)

[Calamares settings [132](#calamares-settings)](#calamares-settings)

[settings.conf [133](#settings.conf)](#settings.conf)

[Branding [135](#branding)](#branding)

[modules [140](#modules)](#modules)

[Method2: The Krill installer (TUI)
[142](#method2-the-krill-installer-tui)](#method2-the-krill-installer-tui)

[Config krill manually:
[143](#config-krill-manually)](#config-krill-manually)

[The content of krill.yaml
[144](#the-content-of-krill.yaml)](#the-content-of-krill.yaml)

[Chapter 7 [148](#chapter-7)](#chapter-7)

[Eggs Configuration [148](#eggs-configuration)](#eggs-configuration)

[Part1: configuration automatically
[148](#part1-configuration-automatically)](#part1-configuration-automatically)

[Eggs adaptive resolutions
[152](#eggs-adaptive-resolutions)](#eggs-adaptive-resolutions)

[eggs analyze [155](#eggs-analyze)](#eggs-analyze)

[Eggs Config [156](#eggs-config)](#eggs-config)

[eggs dad [160](#eggs-dad)](#eggs-dad)

[Eggs Configuration [163](#eggs-configuration-1)](#eggs-configuration-1)

[Part2: configuration manually
[163](#part2-configuration-manually)](#part2-configuration-manually)

[Krill config file [165](#krill-config-file)](#krill-config-file)

[Tools.yaml [166](#tools.yaml)](#tools.yaml)

[Exclude.list files [167](#exclude.list-files)](#exclude.list-files)

[Part3: Configuration status
[171](#part3-configuration-status)](#part3-configuration-status)

[eggs status [171](#eggs-status)](#eggs-status)

[Eggs Change log notes
[172](#eggs-change-log-notes)](#eggs-change-log-notes)

[penguins-eggs-9.6.x [172](#penguins-eggs-9.6.x)](#penguins-eggs-9.6.x)

[penguins-eggs-10.0.13
[173](#penguins-eggs-10.0.13)](#penguins-eggs-10.0.13)

[penguins-eggs-10.0.11-2
[173](#penguins-eggs-10.0.11-2)](#penguins-eggs-10.0.11-2)

[penguins-eggs-10.0.11-1
[173](#penguins-eggs-10.0.11-1)](#penguins-eggs-10.0.11-1)

[penguins-eggs-10.0.10-1
[173](#penguins-eggs-10.0.10-1)](#penguins-eggs-10.0.10-1)

[penguins-eggs-10.0.9-1
[174](#penguins-eggs-10.0.9-1)](#penguins-eggs-10.0.9-1)

[penguins-eggs-10.0.8-2
[174](#penguins-eggs-10.0.8-2)](#penguins-eggs-10.0.8-2)

[penguins-eggs-10.0.8-1
[174](#penguins-eggs-10.0.8-1)](#penguins-eggs-10.0.8-1)

[penguins-eggs-10.0.7-1
[174](#penguins-eggs-10.0.7-1)](#penguins-eggs-10.0.7-1)

[penguins-eggs-10.0.6-3
[175](#penguins-eggs-10.0.6-3)](#penguins-eggs-10.0.6-3)

[Note about bionic version
[175](#note-about-bionic-version)](#note-about-bionic-version)

[penguins-eggs-10.0.6-1
[175](#penguins-eggs-10.0.6-1)](#penguins-eggs-10.0.6-1)

[penguins-eggs-10.0.5-2
[175](#penguins-eggs-10.0.5-2)](#penguins-eggs-10.0.5-2)

[penguins-eggs-10.0.4
[176](#penguins-eggs-10.0.4)](#penguins-eggs-10.0.4)

[penguins-eggs-10.0.3
[176](#penguins-eggs-10.0.3)](#penguins-eggs-10.0.3)

[penguins-eggs-10.0.2
[176](#penguins-eggs-10.0.2)](#penguins-eggs-10.0.2)

[penguins-eggs-10.0.0
[176](#penguins-eggs-10.0.0)](#penguins-eggs-10.0.0)

[penguins-eggs-9.8.3 [177](#penguins-eggs-9.8.3)](#penguins-eggs-9.8.3)

[penguins-eggs-9.8.2 [177](#penguins-eggs-9.8.2)](#penguins-eggs-9.8.2)

[penguins-eggs-9.8.1 [177](#penguins-eggs-9.8.1)](#penguins-eggs-9.8.1)

[penguins-eggs-9.8.0 [177](#penguins-eggs-9.8.0)](#penguins-eggs-9.8.0)

[Chapter 8 [179](#chapter-8)](#chapter-8)

[Producing ISO image file
[179](#producing-iso-image-file)](#producing-iso-image-file)

[Step 1: cleaning the system
[180](#step-1-cleaning-the-system)](#step-1-cleaning-the-system)

[Cleaning with eggs [180](#cleaning-with-eggs)](#cleaning-with-eggs)

[sudo eggs tools clean []{dir="rtl"}-v
[180](#sudo-eggs-tools-clean--v)](#sudo-eggs-tools-clean--v)

[Cleaning with bleachbit
[182](#cleaning-with-bleachbit)](#cleaning-with-bleachbit)

[Bleachbit help [186](#bleachbit-help)](#bleachbit-help)

[Step2: show the status
[189](#step2-show-the-status)](#step2-show-the-status)

[Step3: preparing the skel folder
[190](#step3-preparing-the-skel-folder)](#step3-preparing-the-skel-folder)

[eggs tools skel [190](#eggs-tools-skel)](#eggs-tools-skel)

[Step 4: prepare ISO for offline installation
[195](#step-4-prepare-iso-for-offline-installation)](#step-4-prepare-iso-for-offline-installation)

[Step 5: eggs produce [196](#step-5-eggs-produce)](#step-5-eggs-produce)

[eggs produce command
[196](#eggs-produce-command)](#eggs-produce-command)

[Chapter 9 [210](#chapter-9)](#chapter-9)

[After Producing [210](#after-producing)](#after-producing)

[eggs syncto command [210](#eggs-syncto-command)](#eggs-syncto-command)

[eggs syncfrom command
[212](#eggs-syncfrom-command)](#eggs-syncfrom-command)

[Testing the ISO [214](#testing-the-iso)](#testing-the-iso)

[Testing the installation
[215](#testing-the-installation)](#testing-the-installation)

[Test Functionality [216](#test-functionality)](#test-functionality)

[Test Customizations [218](#test-customizations)](#test-customizations)

[Perform Regression Testing
[219](#perform-regression-testing)](#perform-regression-testing)

[Document and Report Issues
[221](#document-and-report-issues)](#document-and-report-issues)

[Eggs tools stat [222](#eggs-tools-stat)](#eggs-tools-stat)

[Wardrobe users\' guide
[226](#wardrobe-users-guide)](#wardrobe-users-guide)

[Appendix 1 [238](#appendix-1)](#appendix-1)

[Penguins Eggs Terms [238](#penguins-eggs-terms)](#penguins-eggs-terms)
