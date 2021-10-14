# Contributing to the Cisneros Research Docs

This website is built with [MkDocs](https://www.mkdocs.org/)
and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

Because GitHub is built for Jekyll, not MkDocs, we kindly ask that you
install MkDocs on your local computer, modify the files, build the site,
and then make a git commit/pull request with any changes.
Issue reports asking for specific documentation improvements are also welcome!

## Installing Mkdocs
You can install it, and the necessary dependencies for this project, with pip.
```
pip install mkdocs
pip install mkdocs-material
pip install mkdocs-material-extensions
pip install fontawesome_markdown
```

> For new projects in the future, you could use:
> ```
> python -m mkdocs new my-project
> cd my-project
> ```
> to set up the project.

## Structure

MkDocs uses `mkdocs.yml` to set up a number of variables, such as the site
name and navigation bar.
[Wikipedia](https://en.wikipedia.org/wiki/YAML) has a solid overview of how
YAML (YAML Ain't Markup Language) files should be written.

Any pages are written in [Markdown](https://www.markdownguide.org/) and
compiled into HTML through MkDocs.

If you're looking for a specific emoji, check the Material for MkDocs
[search](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/)!

The [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/)
also have some really cool tools!

### Project layout

    mkdocs.yml               # The configuration file.
    base/
        index.md             # The documentation homepage.
        amber/               # Subdirectory with pages on AMBER MD
        lichem/              # Subdirectory with pages on LICHEM (QM/MM)
        assets/              # Contains things essential for the pages!
            stylesheets/     # Modified CSS
            images/          # Relevant pictures

### MkDocs Info
* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

If there are specific things you would like to customize, check out the
[material theme documentation](https://squidfunk.github.io/mkdocs-material/).

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Checking the Site

On some systems, you can run:
```
mkdocs serve
```
from the main directory to create a working local example.
If this doesn't work, try:
```
python -m mkdocs serve
```

## Web Accessibility

Before releasing this website into the unknown, **PLEASE** make sure it has
passed an accessibility check.
There are some things in the template that we're working on (all those
empty labels...).
But things like alt text and Aria labels are mandatory.
Also, please consider whether any linked content is appropriately captioned.
- [WebAim Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org/)
- [WAVE Browser Extension (works on `jekyll` test site)](https://wave.webaim.org/extension/)
- [Color Oracle - Color Blindness Simulator](https://colororacle.org/)

You can read more about this on the University of Washington's
[Developing Accessible Websites](https://www.washington.edu/accessibility/web/)
page.


## Preparing for GitHub

When you're satisfied with the site, you can build it for launch by running
```
mkdocs build
```
from the main directory.
Like before, if that doesn't work, try:
```
python -m mkdocs build
```

This will create a new `docs/` directory.
This contains all of the site information, including HTML, images, search, and
sitemap.

After doing this, add and commit your changes.
Then, push to GitHub.
```
git add .
git commit -m "Add/Fix/Modify XYZ"
git push
```
