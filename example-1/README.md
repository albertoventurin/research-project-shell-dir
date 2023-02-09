# Shell directory for research project

This is an attempt to provide a "shell" directory which you can use as a base for your research project. 

The idea is to use of [Quarto](https://quarto.org/) to write the sections of your paper as dynamic documents which are then rendered together in a single file.

__Note:__ it is still a rather brute-force approach, as I am not an expert user of Quarto but it seems to work fine.

# Structure

__Note: R Projects__
- __example-1.Rproj__ : an [R Project](https://support.posit.co/hc/en-us/articles/200526207-Using-RStudio-Projects) file that takes care of relative paths within the folder. It's particularly useful if you use R, but even if you generate your results (plots/tables) with other programs it's here so that the `.qmd` files have no trouble finding plots and tables.



The directory is structured as follows:

## Data

Save your data here, making sure to separate raw data from processed data

## _draft

The directory containing each of the sections of your manuscript and the final rendered file (a .pdf for now)

### __Important files__

- ___draft.qmd__: The Quarto Markdown file that renders all the sections of the paper contained in _draft. The reason I called this shell a brute-force approach is that all it does is using [Includes](https://quarto.org/docs/authoring/includes.html) to render all the sections.
- __quarto.yml__: The common YAML header for all Quarto files in a [Quarto project](https://quarto.org/docs/projects/quarto-projects.html)



## Figures

Save your figures here

## Presentations

You can use Quarto to create [presentations](https://quarto.org/docs/presentations/) as well: I like to keep them in a separate folder.

## Scripts

Save your codes here! My advice is to number each script starting from 00 so that you know in which order they should be run.

## Tables

Save your tables here

