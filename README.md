# Surf
**My custom surf browser (and tabbed) fork.**

## Requirements
Arch GNU/Linux:
```bash
sudo pacman -S webkit2gtk gcr 
```
Gentoo GNU/Linux (Note the versions):
```bash
doas emerge =net-libs/libsoup-2.74.3 =net-libs/webkit-gtk-2.38.2
```

## Compiling
#### Surf
```bash
git clone https://github.com/r4v10l1/surf
cd surf/surf
sudo make clean install

# Or if you edit config.def.h instead of config.h
sudo make cleaner install
```

#### Tabbed
I personally use tabbed for surf, but you can use it for other stuff like st.
```bash
git clone https://github.com/r4v10l1/surf
cd surf/tabbed
sudo make clean install

# Or if you edit config.def.h instead of config.h
sudo make cleaner install
```
Then you can run surf + tabbed using:
```bash
tabbed surf -e

# Or if you want to pass arguments you can add an alias to your bashrc

tsurf() {
    # tabbed: close tabbed when we exit the program and pass tabbed's window id as 2nd arg for surf
    # surf: Use the 2nd arg as window id and open the tsurf args as website
    tabbed -c -r 2 surf -e '' "$@"
}
```

## Customizing
Edit [`surf/config.def.h`](surf/config.def.h) and change the `HOMEPAGE` define. If you want to have a look at a good homepage check out [r4v10l1/browser-homepage](https://github.com/r4v10l1/browser-homepage).
