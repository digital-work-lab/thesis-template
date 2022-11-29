# Markdown template for theses and seminar papers

This repository contains a markdown template for theses and seminar papers. For simplicity, we refer to theses exclusively, but the guidelines also apply to seminar papers. Below you can find guidelines related to the different aspects of a thesis.

We recommend using the markdown template, but a Word template can also be made available upon request.

# Markdown: Why and how?

**Q:** Why use markdown?

**A:** Because it is super easy and powerful. The future of academic publishing.

- You can focus on contents and format automatically at the end (save effort)
- Pandoc and templates easily convert your work into multiple formats (e.g., docx, pdf)
- Based on csl, giving you access to more than 9,000 citation styles
- Compatible with all reference managers (e.g., Zotero, Endnote, Jabref, ...)
- Works with git, allowing you to keep transparent versions and to collaborate
- Cross-platform, available on Windows (via [WSL](https://learn.microsoft.com/de-de/training/modules/get-started-with-windows-subsystem-for-linux/2-enable-and-install)), Mac, Linux
- There are no lock-in issues like in proprietary tools

**Q:** How to setup markdown?

**A:** Install and build Docker, use a markdown editor and this template repository.

1.  Download this repository: `git clone https://gitlab.rz.uni-bamberg.de/gerit.wagner/thesis-template && cd thesis-template`
2.  Install docker from <https://hub.docker.com/search/?type=edition&offering=community>
3.  Build docker image containing all dependencies, e.g. pandoc and TeX Live: `make docker`
4.  Use a markdown editor:

    - [Panwriter](https://panwriter.com/) is the easiest cross-platform option. Please make sure to install pandoc (as stated on the panwriter website).
    - Of course, you can use any other markdown editor, including [visual code](https://code.visualstudio.com/) (e.g., with the [citer plugin](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter)), or even [manubot](https://manubot.org/) ([1](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007128)).

**Q:** How to write your thesis with markdown?

**A:** Follow these steps:

1.  Maintain your references in [`references.bib`](references.bib)
2.  Put the title of your thesis, your name and other meta information in [`md/metadata.yaml`](md/metadata.yaml)
3.  Adjust optional definitions in [`md/metadata.yaml`](md/metadata.yaml) to your needs
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

# Structure of a thesis

The default structure outlined below may need to be adapted to the thesis. It is recommended to use "We" instead of passive voice (commonly used in German).

## Abstract

The abstract acts as a point-of-entry for the reader, providing a first overview of the research study, namely, the motivation for the study, the methodological approach taken and a summary of the main results. In addition, the purpose of the research study should be clearly defined. Typically, an abstract consists of around 200 words.

## Introduction

The introduction should precisely outline the purpose of the study as well as the research question that is sought to be answered. By briefly outlining the context of the study in terms of content and time, the reader acquires a quick overview. A key aspect of the introduction is the presentation of the motivation for conducting the study. This gives the reader a basic understanding of the topic and underpins the relevance and importance of the study. The relevance as well as the purpose can further be highlighted by using an appropriate quotation.

The final paragraph of the introduction gives an outline of the structure of the study, that is, the approaches taken in each step of conducting the research study are briefly described. This gives the reader a clear picture of the composition of the study, i.e., what can and what cannot be expected of the study.

## Background

This section (could also be named Literature Review or Conceptual Framework) sets the theoretical and conceptual context of the study and grounds the leading assumptions in theories. This is done by outlining and citing pertinent work. Here, the author can present the acquired background knowledge that is relevant for the following sections of the study. This background knowledge also helps in building the conceptual framework of the study.

The literature review should focus on concepts as opposed to authors and historical development (cf. Webster and Watson, 2002). It is also possible to use a conceptual framework to structure the literature synthesis. Provide precise definitions of those concepts that are central to your work, emphasize concepts rather than authors, and do not include your own judgment in the background section. Use established definitions and concepts and provide a justification when adapting them.

A graphical representation of the framework helps to illustrate complex theoretical constructs as well as the boundaries of the research study. The explicit statement of the conceptual framework not just informs the reader, it also guides the author in conducting the research.

Relevant background literature can be found in journals such as those listed in
- the [AIS Senior Scholars' Basket of Journals](https://aisnet.org/general/custom.asp?page=SeniorScholarBasket)
- the [VHB Jourqual Ranking](http://vhbonline.org/VHB4you/jourqual/vhb-jourqual-3/teilrating-wi/)
- or conferences such as [ICIS](http://aisel.aisnet.org/icis/) and [ECIS](https://aisel.aisnet.org/ecis).

Papers can be accessed through the [EZB](http://ezb.uni-regensburg.de/), a search on [Researchgate](https://www.researchgate.net), a search on Google, or by contacting the authors.

Guidelines on searching the literature are provided by Webster and Watson (2002).

## Methodology

The methodology section describes a systematic and goal-oriented approach to answer the research question. Hence, the selection of the research method needs to be consistent with the research questions. The approach may be, for example, empirical, analytical, comparative, systematic, historic, or hermeneutic ([Goethe Universität](https://www.uni-muenster.de/imperia/md/content/didaktik_der_chemie/wissenschaftlichesarbeiten/leitfaden.pdf)). The methodological approach needs to be described in detail; appropriate reporting standards for the research method should be considered (such as PRISMA for literature reviews); it should be possible to understand the methodological procedures based on the thesis. For example, it is necessary to provide the formulas of regression models.

## Results

In this section, the author presents the results of the study. In case they are presented by means of figures and/or tables, the results should be clearly legible. Furthermore, in the case of figures, it is recommended to use vector graphics as this ensures good readability without the need to pre-specify the font size within the figures. An example figure and table can be found in the template contained in this repository.

## Discussion

In this section, the author provides a discussion of the results and is thus able to draw an informed conclusion. More precisely, the discussion is an evaluative summary of the research study in relation to the research question. In general, the discussion can be divided in three parts. First, the results should be tied to the research question, thus presenting the reader a solution or improvement to the identified problem space. Here, for example, the author can draw on empirical findings introduced in the Results section to support his or her argument. Next, the author should outline the limitations of the research study by critically examining the used research approach. Limitations might comprise, for example, a limited time frame considered in the research study, or the individual refinement of a specific research method due to time constraints. Finally, suggestions for future research avenues should be provided. These suggestions may be in line with the limitations, as this allows other researchers to build on the present work by extending or analyzing it. In summary, the Discussion section presents the results in relation to the research question as well as restrictions of the study and suggestions for future research in the respective domain.

## Conclusion

The conclusion contains a summary of the research study. In contrast to the Discussion section, in which the main results are presented, here the key contributions of the work are showcased. A well-crafted conclusion answers the research question stated in the Introduction. By so doing, the author clarifies to what extent the research study has presented a solution or improvement to the examined problem space.

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

