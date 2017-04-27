Reproducible Reports Project Initialization
======================

A template library for use in making research reports/grant proposals follow standard guidelines


Overview
--------

    project
    |- final_report/     # Text and pdf files used for the final report
    |  |- instructions/  # Documents issued by grant funding body outlining final report requirements
    |  +- figures/       # Figures used in final report
    |
    |- literature/       # Any literature collected specifically for this proposal
    |
    |- proposal/         # Text and pdf files used for the proposal
    |  |- styles-master/ # Folder containing citation styles (from https://github.com/citation-style-language/styles)
    |  |- instructions/  # Documents issued by grand funding body outlining proposal requirements
    |  +- figures/       # Figures used in proposal
    |
    |- README.md         # The top level description of content
    |- BibTexCiteKeyForMarkdown.js  # File which enables Zotero to export markdown citation keys
    |- example_bibliography.bib     # An example reference library
    |- example_proposal.md          # An example report markdown file
    +- example_proposal.pdf         # An example output generated with Pandoc from the example_proposal.md file


How to use
--------
* Create a new directory for your project.
* Download the [latest version](https://github.com/EngqvistLab/reproducible-reports-init) of this repository, and unzip it in the directory you just created.
* Open this document in an editor. Change the first line to reflect the title of your research study.
* Write your proposal/report keeping all files in their appropriate place.
* Preferably use [Semantic Versioning](http://semver.org/) to keep track of file versions.


Working with Pandoc
---------------------------------
* [Pandoc Markdown](http://pandoc.org/MANUAL.html) is a great tool for writing your proposal/report. It allows you to focus on the content while adding labels telling Pandoc how to format stuff.
* Ensure that your citation library in .bib format and placed it in the project folder.
* Compile the final report document(s) with [Pandoc](http://johnmacfarlane.net/pandoc/). Output format can be chosen as desired (html, doc, rtf, tex) and does not have to be pdf.


Generate pdf using the command line as such: \
`pandoc --filter pandoc-citeproc example_proposal.md -o example_proposal.pdf`


Requirements
------------
If using [Pandoc Markdown](http://pandoc.org/MANUAL.html) you will need to install [Pandoc](http://johnmacfarlane.net/pandoc/), [Tex Live](https://www.tug.org/texlive/) and pandoc-citeproc (to handle references).

Install [Pandoc](http://johnmacfarlane.net/pandoc/): \
`apt-get install pandoc`

Install texlive (for LaTeX support): \
`apt-get install texlive`

Requires citeproc for citations: \
`apt-get install pandoc-citeproc`


References
----------
* Export your citation library in .bib format and place it in the project folder. This can be an anoying step, but it accomplishes reference manager independence since the library is saved together with the report. It thus ensures reproducibility even in cases where you no longer have access to your reference manager or library.
* The current recommendadtion is to use [Zotero](https://www.zotero.org/) for managing your references. This makes your library portable and backed up.
* To make the Zotero references manager play nice with Pandoc, save the.BibTexCiteKeyForMarkdown.js to your Zotero translator's directory and restart Zotero. If you don't know where your translator's directory is: go to Zotero Preferences. Open the Advanced pane. Click on "Show Data Directory." This will take you to a "zotero" folder. The "zotero" folder will contain a "translators" folder. Save the.BibTexCiteKeyForMarkdown.js file here.
* After you restart Zotero, you can use the drag and drop functionality by going to the "Export" preferences pane and choosing "BibTeX key for Markdown" as the Default Output Format.
* Now, you can select a reference and drag it off the screen into a waiting text editor. Alternatively you can use Cmd+Shift+C to copy the @key to your clipboard.



To the extent possible under law, the author(s) of this template have dedicated all copyright and related and neighboring rights to it to the public domain worldwide under the [CC0 Public Domain Dedication](http://creativecommons.org/publicdomain/zero/1.0/). The template and all other content in the [reproducible-reports-init repository](https://github.com/EngqvistLab/reproducible-reports-init) is distributed without any warranty.
