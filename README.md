# Mega GitIgnore

Combine a series of .gitignores into one mega file. Perfect for those of us who want to use multiple gitignores in one project.

## Why ?

### Why do we even care about `.gitignore` files?

Sometimes (most of the time?) you don't want to commit every single file in your directory. Common files to exclude include build artifacts and log files. These files are a way to tell git what you want to ignore--that is, not commit to your repo and track changes against.

### Why do I need this tool?

Kind people on the internet have written `.gitignore` files for several languages, operating systems, editors, etc. already. GitHub will even let you choose one when you create a new repository!However, sometimes you need to combine multiple files together to cover all the things you want to exclude.

**This tool automates this collation process so you can spend less time setting up your environment and more time building cool things!**

## Installation

These instructions are written for `bash`. This has been tested on Ubuntu and OSX.

```bash
# Download to usr/local/bin so you can access it from anywhere
sudo wget -O /usr/local/bin/mega-gitignore https://raw.githubusercontent.com/samruddhisomani/mega-gitignore/main/mega-gitignore

# Give the script execute permissions so you can actually run it
sudo chmod +x /usr/local/bin/mega-gitignore
```

## Usage

From inside the directory you need the `.gitignore` for run `mega-gitignore` with all the gitignore boilerplates you want separated by spaces.

If a `.gitignore` file doesn't exist, this command will add one and fill it out as requested. If one already exists, this will append the requested boilerplates to it.

All gitignore boilerplates are sourced from [this repo](https://github.com/github/gitignore). Names are case sensitive and must match exactly with the part before `.gitignore`.

### Examples

**Node and Python:** This might be useful for a project where you have a Python backend and a JavaScript frontend.

```bash
mega-gitignore Node Python
```

**OSX and VSCODE:** This might be useful if you're working with VS Code on an OSX device. \*Note that because these live in the Global folder in the boilerplates repo, we have to put `Global/` before them. While you could choose to instead add these to your personal global or local `.gitignore`, that option runs the risk of collaborators adding those files in by mistake.

```bash
mega-gitignore Global/macOS Global/VisualStudioCode
```

**Jupyter Notebooks and Python:** This might be useful for a project where you're using Jupyter notebooks but you still want to make sure you don't accidentally include common Python exclusions.

```bash
mega-gitignore Python community/Python/JupyterNotebooks
```
