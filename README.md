# QAdwaitaDecorations
Qt decoration plugin implementing Adwaita-like client-side decorations.

## How to compile
This library uses private Qt headers and will likely not be forward nor
backward compatible. This library will have to be recompiled with every
Qt update. While it can be build using Qt 5, it is recommended to get
backported changes from Qt 6. You can get these [here](https://src.fedoraproject.org/rpms/qt5-qtwayland/blob/rawhide/f/qtwayland-decoration-support-backports-from-qt6.patch).

Build instructions:

```
mkdir build
cd build
cmake [OPTIONS] [-DUSE_QT6=true] [-HAS_QT6_SUPPORT] ..
make && make install
```

## Usage
It can be used by setting the QT_WAYLAND_DECORATION environment variable:

```
export QT_WAYLAND_DECORATION=adwaita-colorful
```

## Configuration
You can customize the colors by creating a configuration file at `$XDG_CONFIG_HOME/QAdwaitaColorfulDecorations.conf` (usually `~/.config/QAdwaitaColorfulDecorations.conf`).

An example configuration file is provided as `QAdwaitaColorfulDecorations.conf.example` in the repository. You can copy it to your config directory and modify it according to your preferences:

```
cp QAdwaitaColorfulDecorations.conf.example ~/.config/QAdwaitaColorfulDecorations.conf
```

The configuration file allows you to customize various colors such as background, foreground, border, and button colors for both active and inactive states, as well as hover and pressed states.

## License
The code is under [LGPL 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html) with the "or any later version" clause.
