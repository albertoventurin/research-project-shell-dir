# Shell directory for research project

This is an example directory for you to organize a research project. It is ideally self-contained and designed to be a GitHub repository for reproducibility and robustness.

## Main idea

The main idea is to substitute the writing process on Overleaf by using dynamically generated documents by [Quarto](https://quarto.org): the main advantages are the following

-   it is be **a lot** easier to update tables and graphs
-   you always have a **local** (i.e. in your computer) backup of the paper and a backup **on a server** (GitHub)
-   version control keeps track of both the code and the written sections of the paper

## Structure

This directory makes use of [RStudio projects](https://r4ds.had.co.nz/workflow-projects.html) to take care of relative paths and of [Quarto projects](https://quarto.org/docs/reference/quarto-projects.html) to write the paper. Note that while it is certainly convenient to work in R, you can also do your analysis in any language of your choice and it won't impact the functioning of the project.

> Note: Quarto supports R, Julia and Python natively, which means that you can generate plots and tables by writing code directly within the sections of your paper. My advice is to generate plots and tables outside of the documents nevertheless, so that language compatibility won't be an issue and rendering will be faster


