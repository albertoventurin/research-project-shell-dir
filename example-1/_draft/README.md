This is the directory that contains the `.qmd` files for each section of your paper: it is a [Quarto project](https://quarto.org/docs/projects/quarto-projects.html). 

The main idea is to write each section in a different file (e.g. `data.qmd`) using Markdown syntax and possibly inserting dynamically generated figures/tables and then compiling a single document that joins all of the sections.

## The `_draft.qmd` file

This is the file that takes all the sections of your paper and puts them together: it does so using [Includes](https://quarto.org/docs/authoring/includes.html). 
You can specify the title, author, section title and other options which can also be related to how the file is compiled (i.e. `number-sections` for section numbering)

## The `_quarto.yml` file

This file contains a YAML header that gives Quarto instructions on how to compile the project: in this case, for example, there are options for both pdf rendering (which uses Latex) and html rendering. You can control a wide variety of parameters governing how your document is put together: refer to the [Quarto docs](https://quarto.org/docs/guide/) to know more.

## How to generate the paper

You can do so in one of the following ways:

- Click the `Render` button on the `_draft.qmd` document
- Use the `Ctrl+Shit+K` keyboard shortcut while `_draft.qmd` is open
- run `quarto render` from terminal __within this directory__
- From R: install the [quarto](https://cran.r-project.org/web/packages/quarto/index.html) package and use `quarto_render()`

> Note: The first two methods will just render a .pdf. If you want to render both a .pdf and an .html file you should use either `quarto render` from terminal or `quarto::quarto_render(output_format="all")`

Refer to the Quarto books documentation to see how to create a project from scratch.

## Note: extensions

In the `summary.qmd` section I am including a `.tex` table which I generated from R, using the [stargazer]() package: it compiles fine in the `.pdf` file but the `.html` file does not show it.


Luckily, there is an [extension](https://quarto.org/docs/extensions/) which allows you to put latex tables in html documents through a call to Pandoc: you can find it [here](https://www.github.com/tarleb/parse-latex). You need to do the following:

- Install the extension __in the directory of the project__ (`quarto install extension tarleb/parse-latex` from terminal)

- Add the instruction to use this extension when compiling to html to your YAML header (see the `_quarto.yml` file)

Moreover, within `_draft.qmd` I am writing the abstract in a section but it appears in the proper place. This is because I also installed (__in this project directory__) the [abstract-section](https://www.github.com/pandoc-ext/abstract-section) extension