# Chapter 10

# Wardrobe users' guide

The penguins' wardrobe methodology allows for the tracking and reuse of
steps taken during the development of a remastering project. It
provides a way to create customizations starting from a minimal CLI
system that is already installed, referred to as a "naked"
system. You have used this methodology to create various generic
customizations such as colibri, duck, owl, and eagle. Additionally,
you have used it to create Linux systems with waydroids named wagtail,
warbler, and whipbird, based on Gnome, KDE Plasma, and Weston,
respectively.

It's worth noting that while the Penguins' Wardrobe methodology is
useful for remastering projects, it is not necessary to use it in
conjunction with the "eggs" tool. You can still utilize the
"eggs" tool for system customization based on your own
methodologies and original customizations.

Call `eggs wardrobe --help` to get all commands inside:

```
COMMANDS
  wardrobe get   get warorobe
  wardrobe list  list costumes and accessoires in wardrobe
  wardrobe show  show costumes/accessories in wardrobe
  wardrobe wear  wear costume/accessories from wardrobe
```

## eggs wardrobe get

```
eggs wardorbe get
```

clone the default repository: [penguins-wardrobe](https://github.com/piero.proietti/penguins-wardrobe) in a 
folder `./wardorobe` on your home.

You can also, fork [penguins-wardrobe](https://github.com/piero.proietti/penguins-wardrobe) and work on your version:

```
eggs wardrobe get https://github.com/armando/armando-wardrobe
```
## eggs wardrobe list
`eggs wardobe list`
List: costumes, accessories, servers and vendors/themes included on your wardrobe.

## eggs wardrobe show
show a costume or an accessory included in current wardrobe (~.wardrobe`)

## eggs wardrobe wear
`sudo eggs wardrobe wear costume`

# How wardrobe work

Penguins' wardrobe, is not part of eggs and its knowledge and use is not necessary to remaster your own system or to create your own original customizations. Rather, it is a methodology that allows-while developing a remastering project-to keep track of the steps taken and reuse them when needed.

It is a penguins-wardrobe repository consisting mainly of yaml files and simple bash scripts and used by eggs through the wardorobe command to create customizations of Linux systems from a minimal CLI system already installed, in our naked terminology.

I have used this method both for creating some generic customizations: colibri, duck, owl and eagle, and for creating Linux systems with waydroid named: wagtail, warbler and whipbird and based on Gnome, KDE Plasma and Weston respectively.

You can ALWAYS use eggs from your original customizations without using the wardrobe command but following your own methodologies.


## The wardrobe metaphor
The metaphor consists of a `wardrobe` containing `costumes` and `accessories` for dressing systems.

### penguins-wardrobe

[penguins-wardrobe](https://github.com/armando/armando-wardrobe) is a repository, managed with git and organized by directories: `costumes`, `accessories`, `vendors/themes` and `documentation`. 

Its use - preferibility - involves forking it in order to create our own customizations, thus allowing both an easy organization of our work and the consolidation of our experiences, making it easier to search and reuse of work previously done or import work done by third parties.

It is possible to dress up a CLI system with a beautiful GUI interface, but it is also possible to use wardrobe to collect server configurations without necessarily a GUI.

This method has proven useful for development and work organization.

To show a wardrobe sample, I will refere to mine `colibri`, a customization I use to develop penguins-eggs in the version Debian bookworm.


# costumes
A costume essentially consists of a directory named with the name of the costume and a yaml file. eg: [debian.yaml](https://github.com/pieroproietti/penguins-wardrobe/blob/main/costumes/colibri/debian.yml).

`debian.yaml` specifies the composition of the costume, at its definition we find it in [i-materia.ts](https://github.com/pieroproietti/penguins-eggs/blob/master/src/interfaces/i-materia.ts), and it is parsed by the eggs [tailor.ts](https://github.com/pieroproietti/penguins-eggs/blob/master/src/classes/tailor.ts)class. 

Basically, we provide the directions and the tailor sews the suit for us.

In wardrobe, so we just have information specifying mostly repositories and packages in yaml language. This example is from the `debian.yaml` file of my colibri. 

```
# wardrobe: .
# costume: /colibri
---
name: colibri
description: >-
  desktop xfce4 plus all that I need to develop eggs, firmwares and anydesk
  repos
author: artisan
release: 0.9.1
distributions:
  - bookworm
...
  hostname: true
reboot: true
```

The syntax used is yaml, which is fairly easy to read, while for writing you can rely on numerous addons for virtually any editor.

Let's look at how the index.yaml file of a custom is composed.

We can divide it into three parts:

* `header`
* `sequence`
* `customize`


## header

It defines the name, author, description and release of the costume. An important part is distributions if the current distribution is not included the costume will not be applied.

```
name: colibri
description: >-
  desktop xfce4 plus all that I need to develop eggs, firmwares and anydesk
  repos
author: artisan
release: 0.0.3
distributions:
  - bullseye
  - bookworm
```

## sequence
The sequence is the crucial part of both costumes and accessories, it is performed in sequence-hence the name-and the idea was to make it minimal and indivisible. It can contain:

* `repositories`
  * `sources_list`
  * `sources_list_d`
* `preinst`
* `packages`
* `packages_no_install_recommends`
* `try_packages`
* `try_packages_no_install_recommends`
* `debs`
* `packages_python`
* `accessories`
+ `try_accessories`

The idea behind the sequence was to make it as atomic as possible.

Let's see how the sequence is composed in detail.

### `repositories`
It defines what we need both in our `/etc/apt/surces.list` and -- mainly -- in the `/etc/apt/sources.list.d` directory.
repositories, consists of two items:

#### `sources_list`
Specification of components to be used: `main`, `contrib`, `non-free-firmwares`, `non-free`.


#### `sources_list_d`
Specifies commands and scripts to add more repositories within `/etc/apt/sources.list.d`,

### `preinst`
We sometimes need to perform some actions before installing packages, we can add these actions in the form of scripts in this section.

### `packages`
A simple array of packages to install. It is the heart of the system.

```
  packages:
    - adwaita-qt
    - firefox-esr
    - libxfce4ui-utils
    - lightdm
    - lightdm-gtk-greeter
    - network-manager-gnome
    - qt5ct
    - spice-vdagent
    - tango-icon-theme
    - thunar
    - thunar-archive-plugin 
    - xarchiver
    - xfce4-appfinder
    - xfce4-notifyd
    - xfce4-panel
    - xfce4-pulseaudio-plugin
    - xfce4-screenshooter
    - xfce4-session
    - xfce4-settings
    - xfce4-terminal
    - xfce4-whiskermenu-plugin
    - xfconf
    - xfdesktop4
    - xfwm4
    - plymouth
    - plymouth-themes
```


### `packages_no_install_recommends`
A simple array of packages to be installed, however, which are installed with the --no-install-recommends option.

### `try_packages`
It behaves like `packages` but does not fail if it does not find the package.

### `try_packages_no_install_recommends`
It works like `packages_no_install_recommends` but does not fail if it does not find the package.

### `debs`
This is a boolean field, if it is true, the contents of the `./debs` directory - inside the costume - will be installed with the command `dpkg -i ./debs/*.deb`.

### `packages_python`
A simple array of python packages that will be installed with `pip`.

### `accessories`
A list of accessories to be installed to complete the costume. example:

```
accessories:
    base
    eggs-dev # defined in /accessory
    waydroid # defined in /accessory
    ./firmwares # here we will use an accessory defined inside the costume, note ./
```

### `try_accessories`

Equivalent of `accessories` but don't fail.


## `customize`
`costomize` contains variables and scripts to finalize the installation and customize the result. It can contain:

* dirs
* hostname
* script

### `dirs`
`dirs` is a boolean field, if true the directory `./dirs` inside the costume will be copied to the root of the system root.

Example: We need to copy our user desktop customization in `/etc/skel` and our background to `/usr/share/background`.

Simply put all in a directory called `./dirs`, inside our `colibri`:
```
- dirs   + etc   + skel  
         + usr   + backgrounds  + colibri
        
```
You can browse in on the [colibri](https://github.com/pieroproietti/penguins-wardrobe/tree/main/costumes/colibri/dirs) and it's not pratical? I think yes, all our customizations, at the price of a little and light directory structure.

### `hostname`
If `hostname` is `true` file `/etc/hostname` and `/etc/hosts` will be updated to the name of costume, in ourt case `colibri`.

### scripts
`scripts` contains an array of one or more scripts used to customize the resultant system.

You can add other scripts and directories within del costume colibri or use the scripts contained in the scripts folder such as `../../scripts/config_desktop_link.sh`.

Examples:
```
customize:
  dirs: true
  scripts:
    - ../../scripts/config_desktop_link.sh
    - ../../scripts/config_lightdm.sh
```
Scripts are called from customize/scripts and executed in the specific order.

## reboot
If true in system will be rebooted after dressing.


# themes
While `costumes` and `accessories` apply to an installed system, `themes` make it possible to customize the live image. It is possible to both customize the boot of ISO images and the appearance of the calamares GUI installer.
Come per i costumes e gli accessories, i themes sono principalmente costituiti da una directory, dei file yaml, delle icone, sfondi e quant'altro necessario. L'idea è stata presa da calamares e dai suoi file di configurazione ed estesa ad aspetti più specifici di eggs come il boot live.

educaandos-plus was the first external theme created, dozens of themes are currently available.


Let's analyze a theme

A theme consists of a simple directory under themes, named by the name of the vendor. In this example: vendor-theme, which is composed as follows:

```
vendor-name/
    theme
        applications
        artwork
        calamares
            branding
            modules
        livecd
```

# /vendors/[vendor-name]/theme

The [vendors](https://github.com/pieroproietti/penguins-wardrobe/tree/main/vendors) directory contains [vemdors] who can thus include their own themes in the wardrobe structure.

The theme directory is just the container for everything, the root so to speak of the theme itself.

## [vendor-name] contains the following structure:

° `vendor-name`
  * `theme`
    * `appplacetions`
    * `artwork`
    * `calamares`
    * `livecd`

ake a closer look at the contents of these three folders wardrobe.

### `applications`
Just a `.desktop` link that will be copied to `/usr/share/applications/` and the `Desktop` folder to start the calamares graphical installer.

### `artwork`
Contains the icon for your .desktop link, it will be copied to `/usr/share/icons/`.

###  `calamares`
It contains the configuration for calamares and is the most important part of the theme.

`calamares` can have:

° `vendor-name`
  * `theme`
    * `calamares`
      * `branding`
      * `modules`
      * `calamares-modules`
      * `cfs.yml`

The calamares configuration files are always written in yaml and contain documentation for the various options. The main settings.conf configuration file is automatically generated by eggs and only partition, locale and users are currently used by eggs and wardrobe.

Refer to the calamares site for reference information on configuring these files basically.

#### `branding`

° `vendor-name`
  * `theme`
    * `calamares`
      * `branding`

In [branding](https://github.com/pieroproietti/penguins-wardrobe/tree/main/vendors/neon/theme/calamares/branding) are the customizations for calamares. Generally present, but not mandatory, is the `show.qml` file and images that must scroll during installation.

#### `modules`

° `vendor-name`
  * `theme`
    * `calamares`
      * `modules`
        * `locale.yml`
        * `partitions.yml`
        * `users.yml`

(*) In EducaAndOS in order to have administration rights for the user, we need to configure the user in a specific group, so it became necessary to add `users.yml`.


###  `livecd`
° `vendor-name`
  * `theme`
    * `livecd`

[livecd](https://github.com/pieroproietti/penguins-wardrobe/tree/main/vendors/neon/theme/livecd) contain `splash.png` ed i file: `grub.theme,cfg` ed `isolinux.theme.cfg`.

# Others distros

So far we have only discussed Debian bookworn, but wardobe technology is not limited to Debian, it also includes Devuan, Ubuntu and even Arch.

While Devuan uses the same configuration: `debian.yaml` for arch and Ubuntu use their own configurations. So for Ubuntu we have a file: ubuntu.yaml that is evaluated for Ibintu distros. for Arch we have the corresponding `arch.yaml`.

The functionality--except for the package names--is basically the same. Of course in Arch `pacman` will be used and the specified packages will have to exist in the libraries.

# Limits
Of course we are in a flowing river and, as in Chinese proverb, we can never bathe twice in the same river.

Ubuntu, recently with the noble version changed the method of writing components, so the old `repo.lists` are no longer accepted.

This affects the smooth operation of wardorbe, which adds and modifies repositories as needed.

There would thus need to be continuous maintenance, both of the [tailor.ts](https://github.com/pieroproietti/penguins-eggs/blob/master/src/classes/tailor.ts) and the [penguins-wardrobe](https://github.com/pieroproietti/penguins-wardrobe) repository, which also depends on your response and participation in the project.

The `colibru` costume is well tested and continuously updated, but I cannot say the same for other costumes or for Ubuntu noble.
