# Surf
**My custom surf browser fork.**

## Requirements
```bash
sudo pacman -S webkit2gtk gcr 
```

## Compiling
```bash
git clone https://github.com/r4v10l1/surf
cd surf/surf
sudo make clean install
```
If you having any problems (stuck loading webpages, etc.) try:
```bash
sudo make move
# Or
sudo mv /usr/local/bin/surf /usr/bin/surf
sudo mv /usr/local/lib/surf /usr/lib/surf
```

## Customizing
Edit [`surf/config.def.h`](surf/config.def.h) and change the `HOMEPAGE` define.
