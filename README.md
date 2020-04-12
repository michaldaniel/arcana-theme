# Arcana Theme

Hight contrast and low vibrance version of Arc theme

## Arcana is available in three variants

##### Arcana

![A screenshot of the Arcana theme](http://i.imgur.com/Ph5ObOa.png)

##### Arcana-Darker

![A screenshot of the Arcana-Darker theme](http://i.imgur.com/NC6dqyl.png)

##### Arcana-Dark

![A screenshot of the Arcana-Dark theme](http://i.imgur.com/5AGlCnA.png)

## Installation

To build the theme the following packages are required
* `autoconf`
* `automake`
* `sassc` 
* `pkg-config` or `pkgconfig` for Fedora
* `git` to clone the source directory
* `optipng` 
* `inkscape`

The following packages are optionally required
* `gnome-shell`
* `libgtk-3-dev` or `gtk3-devel` for Fedora

For the theme to function properly, install the following

* The `gnome-themes-extra` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arcanah Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/michaldaniel/arcana-theme --depth 1 && cd arcana-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency         disable transparency in the GTK3 theme
    --disable-light                disable Arcana Light support
    --disable-darker               disable Arcana Darker support
    --disable-dark                 disable Arcana Dark support
    --disable-cinnamon             disable Cinnamon support
    --disable-gnome-shell          disable GNOME Shell support
    --disable-gtk2                 disable GTK2 support
    --disable-gtk3                 disable GTK3 support
    --disable-metacity             disable Metacity support
    --disable-unity                disable Unity support
    --disable-xfwm                 disable XFWM support
    --disable-plank                disable Plank theme support
    --disable-openbox              disable Openbox support

    --with-gnome-shell=<version>   build the gnome-shell theme for a specific version
    --with-gtk3=<version>          build the GTK3 theme for a specific version
                                   Note: Normally the correct version is detected automatically
                                   and these options should not be needed.
    
After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `Arcana`, `Arcana-Darker` or `Arcana-Dark` as Window/GTK+ theme and `Arcana` or `Arcana-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `Arcana-solid`, `Arcana-Darker-solid` and `Arcana-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{Arcana,Arcana-Darker,Arcana-Dark}

## License

Arcana is available under the terms of the GPL-3.0. See `COPYING` for details.
