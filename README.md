# numix-brave

This is fork of Numix theme with changes from abandoned shiki-colors-revival theme.

Relevant license files can be found underneath the folders. (Numix is
GPL-3, Xfwm4 and Metacity are GPL-2, Plank themes and build system are ISC)

## Included
- GTK 2 and 3 themes
- Metacity themes
- Xfwm4 themes
- Openbox themes

## Build It

First, you need to compile the theme using the [Sass](http://sass-lang.com/) compiler.

To install Sass, install Ruby and the gem command using your distribution's package manager. Then install `sass` with the `gem` command,

`gem install sass` (not needed for Ubuntu/Debian)

You'll also need the ```glib-compile-schemas``` and  ```gdk-pixbuf-pixdata``` commands in your path to generate the gresource binary. Install them using your distribution's package manager.

|Distro|Commands|
|:----:|:----:|
|![arch][arch] &nbsp;![antergos][antergos]|`sudo pacman -S glib2 gdk-pixbuf2`|
|![opensuse][opensuse]|`sudo zipper install glib2-devel gdk-pixbuf-devel`|
|![fedora][fedora]|`sudo dnf install glib2-devel gdk-pixbuf2-devel`|
|![debian][debian] &nbsp;![ubuntu][ubuntu]|`sudo apt-get install ruby-sass libglib2.0-dev libgdk-pixbuf2.0-dev libxml2-utils`|

After installing all the dependencies, change to the cloned directory and, run the following in Terminal,

```sh
sudo make install
```

To set the theme in GNOME, run the following commands in Terminal,

```sh
gsettings set org.gnome.desktop.interface gtk-theme "Numix-Brave"
gsettings set org.gnome.desktop.wm.preferences theme "Numix-Brave"
```

To set the theme in Xfce, run the following commands in Terminal,

```sh
xfconf-query -c xsettings -p /Net/ThemeName -s "Numix-Brave"
xfconf-query -c xfwm4 -p /general/theme -s "Numix-Brave"
```

## Screenshots

This is screenshot of the theme running on Xfce desktop.

![Numix-Brave](https://raw.githubusercontent.com/Somasis/shiki-colors-revival/master/screenshots/Shiki-Brave-Revival.png)

## Credits
- [Numix] by [shimmerproject]
- [GNOME Colors] project for the initial theme designs, and base for a lot
  of the assets used for the Metacity and Xfwm4 themes.
- [Shiki-Colors-Xfwm] by [fredbird67]
- [Shiki-Colors-Revival] by [somasis]

[gnome-colors-revival]: https://github.com/Somasis/gnome-colors-revival
[arc-colors-revival]: https://github.com/Somasis/arc-colors-revival
[Numix]: https://github.com/shimmerproject/Numix
[Shiki-Colors-Xfwm]: http://xfce-look.org/content/show.php/Zukitwo-Colors+Xfwm+Themes?content=148624
[shimmerproject]: http://github.com/shimmerproject
[fredbird67]: http://xfce-look.org/usermanager/search.php?username=fredbird67
[GNOME Colors palette]: https://github.com/Somasis/gnome-colors-revival/blob/master/Palette.png
[releases]: https://github.com/Somasis/shiki-colors-revival/releases
[GNOME Colors]: https://code.google.com/p/gnome-colors
[Shiki-Colors-Revival]: https://github.com/somasis/shiki-colors-revival
[somasis]: https://github.com/somasis
