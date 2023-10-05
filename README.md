# Markdown template for theses and seminar papers

This repository contains a markdown template for theses and seminar papers. For simplicity, we refer to theses exclusively, but the guidelines also apply to seminar papers. Below you can find guidelines related to the different aspects of a thesis.

We recommend using the markdown template, but a Word template can also be made available upon request.

# Markdown: Why and how?

**Q:** Why use markdown?

**A:** Because it is super easy and powerful. The future of academic publishing (see [manubot](https://manubot.org/), [1](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007128)).

- You can focus on contents and format automatically at the end (save effort)
- Pandoc and templates easily convert your work into multiple formats (e.g., docx, pdf)
- Based on csl, giving you access to more than 9,000 citation styles
- Compatible with all reference managers (e.g., Zotero, Endnote, Jabref, ...)
- Works with git, allowing you to keep transparent versions and to collaborate
- Cross-platform, available on Linux, Windows, Mac
- There are no lock-in issues like in proprietary tools

**Q:** How to setup markdown?

**A:** Install and build Docker, use a markdown editor and this template repository.

On Windows, it is recommended to use the [WSL](https://learn.microsoft.com/de-de/training/modules/get-started-with-windows-subsystem-for-linux/2-enable-and-install), e.g., Ubuntu. Run the following commands in the WSL shell. Install make (`apt-get install make`).

1.  Install docker from <https://hub.docker.com/search/?type=edition&offering=community>
2.  Download this repository: `git clone https://github.com/digital-work-lab/thesis-template`
3.  Navigate to the repository (`cd thesis-template`) and build docker image containing all dependencies, e.g. pandoc and TeX Live: `make docker`
4.  Use a markdown editor to edit the markdown documents:

    - You can use any other markdown editor, including [visual code](https://code.visualstudio.com/) (e.g., with the [citer plugin](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter)).

Note: On a Mac, line 9 of the docker/dockerfile.df should be replaced by

```
ARG PANDOCDEB=https://github.com/jgm/pandoc/releases/download/2.11.4/pandoc-2.11.4-1-arm64.deb
```

**Q:** How to write your thesis with markdown?

**A:** Follow these steps:

Note: on Windows/WSL, files are available at [\\wsl$](https://learn.microsoft.com/en-us/windows/wsl/filesystems) in the Windows File explorer.

1.  Add your references to [`references.bib`](references.bib)
2.  Put the title of your thesis, your name and other meta information in [`md/metadata.yaml`](md/metadata.yaml)
3.  Adjust optional definitions in [`md/metadata.yaml`](md/metadata.yaml)
4.  Develop your content in the markdown files under [`md/`](md)
    *   Examples for citations, figures, tables, formulas, and code are in [`md/appendix.md`](md/appendix.md)
    *   If you change filenames, also update them in the Makefile
5.  Build the thesis:
    *   Using the simple layout: `make simple`
6.  Clean up:
    *   To remove temporary (generated) filed: `make clean`
    *   To also remove the generated thesis (PDF): `make distclean`

The above-mentioned files constitute a minimal working example. To start your own project, simply clone this project and customize
the files mentioned above.

# General information

## Submission

When submitting the thesis, make sure to
- include the data and the code for your analyses in a digital appendix
- provide PDFs of the papers you cited (if possible)
- send the source files (markdown, references.bib) and a PDF version of the thesis to your supervisor via e-mail.

## Pre-Submission Checklist

- [ ] For (regression) models, the model formulas are provided.
- [ ] Every figure and table is referenced and described in the text.
- [ ] Choose appropriate formatting of numbers that does not suggest unjustified levels of accuracy (e.g., response times of employees in ms).
- [ ] If feasible, arrange rows/columns/bars in an order of numerical progression; always indicate what numbers are shown, including units (axes, legends).
- [ ] Provide complete reference information in the reference section (e.g., including Authors, Title, Journal, Volume, Issue).
- [ ] Keep in mind that claims of significance require appropriate statistical tests.
- [ ] The writing style should be objective and neutral, in particular in the related work, methodology, and results sections. Clearly indicate when you go beyond the data and develop your own interpretation (e.g., in the form of propositions).

# References

Webster, J., & Watson, R. T. (2002). Analyzing the past to prepare for the future: Writing a literature review. MIS quarterly, xiii-xxiii.


# License

This template is based on [cagix/pandoc-thesis](https://github.com/cagix/pandoc-thesis). Like the original work by [Carsten Gips](https://github.com/cagix) and [contributors](https://github.com/cagix/pandoc-thesis/graphs/contributors), it is licensed under [MIT](https://opensource.org/licenses/MIT).

