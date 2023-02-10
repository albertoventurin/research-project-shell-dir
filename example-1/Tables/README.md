Put your tables here. As for the other folders, my advice is to __use subdirectories__ and sensible naming conventions. 

Given that the idea is to use dynamic documents, you can save tables in `.tex` or `.html` (or any other format you like) and embed them in the document later and/or save `.csv` (or `.rds`,`.dta`) files which you can make into tables within the dynamic document (using, for example, the [KableExtra package](https://cran.r-project.org/web/packages/kableExtra/vignettes/awesome_table_in_html.html)). 

If you want to do both, keep the already formatted tables __separated__ from the datasets! 