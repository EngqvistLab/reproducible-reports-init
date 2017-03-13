Reproducible Reports Project Initialization
======================

A template library for use in making research reports/grant proposals follow standard guidelines


Overview
--------

    project
    |- final_report/    # Text and pdf files used for the final report
    |  |- instructions/ # Documents issued by grand funding body outlining final report requirements
    |  +- figures/      # Figures used in final report
    |
    |- literature/      # Any literature collected specifically for this proposal
    |
    |- proposal/        # Text and pdf files used for the proposal
    |  +- instructions/ # Documents issued by grand funding body outlining proposal requirements
    |  +- figures/      # Figures used in proposal
    |
    |- README.md        # The top level description of content
    |- Makefile         # Executable Makefile for this propoal, if applicable



Requirements
------------
If using [Pandoc Markdown](http://pandoc.org/MANUAL.html) you will need to install [Pandoc](http://johnmacfarlane.net/pandoc/) And [Tex Live](https://www.tug.org/texlive/).

`apt-get install pandoc`

`apt-get install texlive`

You will also need citeproc for citations.


How to use
--------
* Create a new directory for your project.
* Download the [latest version](https://github.com/EngqvistLab/reproducible-reports-init) of this repository, and unzip it in the directory you just created.
* Open this document in an editor. Change the first line to reflect the title of your research study.
* Write your proposal/report keeping all files in their appropriate place.
* Preferably use [Pandoc Markdown](http://pandoc.org/MANUAL.html) for writing your proposal/report and use [Semantic Versioning](http://semver.org/) to keep track of file versions.
* If using Pandoc Markdown, compile the final report document(s) with [Pandoc](http://johnmacfarlane.net/pandoc/). Output format can vary (html, doc, rtf, tex) and does not have to be pdf.

Generate pdf using the command line as such:

`pandoc xyz_file_version_1.0.1.md -o xyz_file.pdf`

To the extent possible under law, the author(s) of this template have dedicated all copyright and related and neighboring rights to it to the public domain worldwide under the [CC0 Public Domain Dedication](http://creativecommons.org/publicdomain/zero/1.0/). The template and all other content in the [reproducible-reports-init repository](https://github.com/EngqvistLab/reproducible-reports-init) is distributed without any warranty.

