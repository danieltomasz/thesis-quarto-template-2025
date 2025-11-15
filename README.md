# Ghent University Doctoral Thesis Template

Quarto template for Ghent University (Universiteit Gent) doctoral dissertations. This template is adapted from the [nmfs-opensci/quarto-thesis](https://github.com/nmfs-opensci/quarto-thesis) template and customized to meet UGent formatting requirements and branding guidelines.

## UGent-Specific Features

This template includes:

- **UGent Blue Color Scheme**: Official Ghent University blue (RGB 30, 100, 200) applied to links, citations, and document elements
- **UGent Branding**: Pre-configured with Ghent University name and structure
- **UGent Panno Font**: Configured to use official UGent Panno Text font (requires font files in `include/fonts/`)
- **Typography Enhancements**: Includes paragraph indentation, microtype, and epigraph support
- **A4 Format**: Standard A4 paper size with appropriate margins
- **Biblatex Support**: Compatible with Quarto 1.4+ using biber backend (fixes bibliography rendering issues in Quarto 1.5+)
- **Enhanced Figure Handling**: Improved figure placement using float package

## Requirements

- Quarto 1.4 or higher
- XeLaTeX or LuaLaTeX (for UGent Panno font support)
- Biber (for bibliography processing)
- UGent Panno Text font files (see Font Setup below)

## Font Setup

This template is configured to use the official **UGent Panno Text** font. To use it:

1. Obtain the UGent Panno font files from:
   - UGent Staff Portal (for staff and PhD students)
   - Your faculty's communication department
   - UGent Style Guide: https://styleguide.ugent.be/

2. Place the following font files in the `include/fonts/` directory:
   - `UGentPannoText-Normal.ttf`
   - `UGentPannoText-SemiBold.ttf`

3. Render your thesis using XeLaTeX or LuaLaTeX (default)

**Note**: The UGent Panno fonts are proprietary and require proper authorization. See `include/fonts/README.md` for more details and alternative font options.

## Customizing for Your Thesis

Edit the `_quarto.yml` file to add your personal information:

```yaml
thesis:
  supervisor:
    name: Prof. Dr. Your Supervisor
  university: Ghent University
  department: Your Department Name
  faculty: Your Faculty Name
  group: Your Research Group
```

Based on the Masters/Doctoral Thesis LaTeX Template, Version 2.5 (27 Aug 2017).

## Quick Start!

* Show me how to download a zip and open in RStudio: [Video](https://youtu.be/33l8GhtUfnU)
* Show me how to use this repo as a template and then clone to my computer with RStudio: [Video](https://youtu.be/smzNQtogSaI)
* Show me how to render in Visual Studio Code (see previous videos for how to get the repo onto your computer): [Video](https://youtu.be/IJe3A8-Ee2E)
* Scroll to the bottom for information on customizing the look of your thesis.


## Installing the extension

You will need to do this to get all the folders with tex files. Start in the directory where you will create the directory that will contain your thesis files. Run this from a terminal in that directory.

```bash
quarto use template nmfs-opensci/quarto-thesis
```

It will ask for an empty directory name where to put the files, give it a new directory name.

Once you do that you can cd to the new directory and render from within the directory.

```bash
quarto render
```

## Installation or updating for an existing document

You may also use this format with an existing Quarto project or document. But you will need to have all the tex folders already (see above).

```bash
quarto install extension nmfs-opensci/quarto-thesis
```

## Usage

### Customizing the look

For a LaTeX document, the class file `MasterDoctoralThesis.cls` in the `_extensions/quarto-thesis` determines the look and LaTeX environments available. To make any changes to the layout, change the MasterDoctoralThesis.cls **in the _extensions folder**. The `MastersDoctoralThesis.cls` file in the main folder will be overwritten by the one in the `_extensions` folder when you re-rerender.  To get info on the MasterDoctoralThesis document class, do a web search for `MasterDoctoralThesis.cls`. You'll find some documentation.

### Adding content

* start adding Chapters in qmd format to the Chapters folder.
* then add the chapter (or appendix) to the `_quarto.yml` file

<img width="305" alt="image" src="https://github.com/nmfs-opensci/quarto-thesis/assets/2545978/3cbd21f5-185f-4930-8699-a623af15fd84">


## Getting and giving help

First try the Discussion link because there may be a solution there. Have a solution to post or want to show how you have used this template? Post to the discussion forum too! You'll find links to other Quarto thesis templates there too.

If you think it's a bug, then definitely post an issue and I'll look into it! 

## Contributors

[![Contributors](https://contrib.rocks/image?repo=nmfs-opensci/quarto-thesis)](https://github.com/nmfs-opensci/quarto-thesis/graphs/contributors)

This template is based on the [Masters/Doctoral Thesis, LaTeX Template, Version 2.5 (27 Aug 2017)](https://www.latextemplates.com/template/masters-doctoral-thesis). Other Quarto thesis examples:


## Problems

* All the stuff in Frontmatter is mandatory LaTeX since it is being injected into the tex document after the qmd is processed. Probably need to learn how to write a lua filter to render the Frontmatter qmd to LaTeX via Pandoc.

* I doubt that passing in `classoptions` in your `_quarto.yml` will work. The [elsevier lua filter](https://github.com/quarto-journals/elsevier/blob/main/_extensions/elsevier/elsevier.lua) suggests that the classoptions need to be added on.

* Why does `index-blx.bib` keep appearing?

## Warning. Chapter 1 has R code

Python and Julia users: After you install the extension, search for `{r}` in `Chapters/Chapter1.qmd` and get rid of the R code (for a table and a figure) or replace with Python or Julia code.
