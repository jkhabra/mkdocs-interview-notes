# mkdocs-interview-notes

This is a simple static site to display Javascript interview questions, it is build in [mkdocs.org](https://www.mkdocs.org). It is hosted on github pages [here](https://jkhabra.github.io/mkdocs-interview-notes/).

## Commands to run on local

* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Setup virtualenv
```zsh
➜ python3 -m venv venv            
➜ source venv/bin/activate        
```
## Setup on local systme
- Clone the project then cd into the project
- Hit the `pip3 install -r req.txt` command