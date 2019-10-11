# Mega GitIgnore

Combine a series of .gitignores into one mega file. Perfect for those of us who want to use multiple gitignores in one project.

## Install

```bash
sudo wget -O /usr/local/bin/mega-gitignore https://raw.githubusercontent.com/samruddhisomani/mega-gitignore/master/mega-gitignore
```

## Usage

From inside the directory you need the gitignore for run mega-gitignore with all the gitignore boilerplates you want separated by spaces. For an example project that involves Node and Python: 

> ```mega-gitignore Node Python```

This will create a brand new .gitignore inside the current directory. Note that this tool will wipe and replace your current .gitignore file. 

All gitignore boilerplates are sourced from [this repo](https://github.com/github/gitignore). Names are case sensitive and must match exactly with the part before ```.gitignore```.

