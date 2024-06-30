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






