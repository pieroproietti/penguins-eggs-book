# chapter-7

## Chapter 7

## eggs configuration

### Part1: eggs configuration

You can configure eggs tool automatically using `sudo eggs dad --default`, automatically with your custom values, using `sudo eggs dad --file custom.yaml`, interactive using `sudo eggs dad`.

Of course is possible to configure eggs, editing the two files: `/etc/penguins-eggs.d/eggs.yaml` and `/etc/penguins-eggs.d/tools.yaml`

### Part2: configuration manually

During the installation of the eggs program, three different configuration files are automatically generated. These files can be found in the following directory. The eggs configuration file path is:&#x20;

```
/etc/penguins-eggs.d
```

After installing eggs, the main configuration file can be found at the above mentioned path. This file allows manual configuration of the eggs program.

The used values from `eggs.yaml` file are the follows:

```
force_installer: false
initrd_img: /boot/initrd.img-6.8.8-1-pve
make_efi: true
make_isohybrid: true
make_md5sum: false
root_passwd: evolution
snapshot_basename: father
snapshot_dir: /home/eggs/
snapshot_excludes: /etc/penguins-eggs.d/exclude.list
snapshot_mnt: /home/eggs/.mnt/
snapshot_prefix: egg-of_debian-bookworm-
user_opt: live
user_opt_passwd: evolution
vmlinuz: /boot/vmlinuz-6.8.8-1-pve
```

### /etc/penguins-eggs.d/exclude.list

This file is build from templates inside `/etc/penguins-eggs.d/exclude.list.d/`

### /etc/penguins-eggs.d/exclude.list.d/

Here we have templates for exclude.list, we have templates for:

* master.list
* homes.list
* usr.list
* var.list

When we produce an eggs, this templates are combinated to for an `/etc/penguins-eggs.d/exclude.list`. If for same reasonm you don't want every time rebuild it, you can use flag `--static`.

### eggs status

`eggs status` give a brief explanation on this values on the screen.
