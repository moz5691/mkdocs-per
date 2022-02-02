# MkDocs for tech notes


## Usage

I have struggled to get Poetry working on Python 3.10.x.
I think the reason was I have installed Poetry with Python 3.9.x and upgraded to 3.10.x

Run the following in Python virtual environment if you run into a trouble to run ```poetry```.
```shell
pip install cleo tomlkit poetry.core requests cachecontrol cachy html5lib pkginfo virtualenv lockfile
```

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## GitHub Actions

Note that you need to enable GitHub Pates site and source branch as "None", never choose "Main" branch.
MkDocs build creates ```site``` directory and push compiled HTML/CSS/JavaScript in "gh-pages" branch.

- Step 1. Enabled GitHub Pages and choose source branch as ```none```.  Please refer the following (important!!!)
[Configuring a publishing source for your GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

- Step 2. After first GitHub Actions deploy, you should see GitHub page is unreachable.
    You need to go to ```Settings``` for GitHub pages again and switch source branch to ```gh-pages``` which was created automatically.  

- Step 3. Push/merge to ```main``` branch.  You should see it works perfectly.  No more tweaking of branch needed.
