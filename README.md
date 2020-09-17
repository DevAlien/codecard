NOTICE: The code at the moment is just a prototype made in 10 minutes

<div align="center">

# Codecard

## Share snippets of code as a pretty image
</div>
  

## Introduction
Share snippets of code as a pretty image 
## Dependencies

Ensure you have these dependencies installed

* granite
* gtk+-3.0
* gtksourceview-3.0
* libgee-0.8
* meson
* vala
* ninja

## Install, build and run

Elementary OS

```bash
# install elementary-sdk, meson and ninja 
sudo apt install elementary-sdk meson ninja
# clone repository
git clone git@github.com:DevAlien/codecard.git codecard
# cd to dir
cd codecard
# run meson
meson build --prefix=/usr
# cd to build, build and test
cd build
ninja && ./com.github.devalien.codecard
```

## Generating pot file

```bash
# after setting up meson build
cd build

# generates pot file
ninja com.github.devalien.codecard-pot

# to regenerate and propagate changes to every po file
ninja com.github.devalien.codecard-update-po
```