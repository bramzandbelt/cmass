<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Last-changedate](https://img.shields.io/badge/last%20change-2019--06--26-brightgreen.svg)](https://github.com/bramzandbelt/irmass/commits/master) [![minimal R version](https://img.shields.io/badge/R%3E%3D-3.6.0-brightgreen.svg)](https://cran.r-project.org/) [![DOI](https://zenodo.org/badge/doi/10.5281/zenodo.3257505.svg)](https://zenodo.org/badge/doi/10.5281/zenodo.3257505.svg) [![Licence](https://img.shields.io/github/license/mashape/apistatus.svg)](http://choosealicense.com/licenses/mit/) [![ORCiD](https://img.shields.io/badge/ORCiD-0000--0002--6491--1247-green.svg)](https://orcid.org/0000-0002-6491-1247)

cmass - Data set for computational modeling analysis of selective stopping
==========================================================================

Dataset DOI
-----------

[DOI: 10.5281/zenodo.3257505](https://doi.org/10.5281/zenodo.3257505)

The files at the URL above provide access to a dataset containing task performance data on a action-selective and stimulus-selective stop-signal task (10 participants, 6000 trials per participant). The data were collected for the purpose of developing a computational model of selective stopping, but due to lack of resources (time in particular) and a career switch (leaving academia) the project did not get off the ground.

Authors of this repository
--------------------------

-   Bram Zandbelt (<bramzandbelt@gmail.com>)
-   Ruben van den Bosch (<r.vandenbosch@donders.ru.nl>)

Overview of contents
--------------------

This dataset is closely related to two other research compendia: `irmass` and `cnmss`

The packagae `irmass` is one of two research compendia of the research project *Cognitive and Neurobiological Mechanisms of Selective Stopping* by Bram Zandbelt and Ruben van den Bosch (the other research compendium, `cnmss`, can be found [here](github.com/bramzandbelt/cnmss)<!-- TODO: Check Github URL -->). This project was conducted at the Donders Institute, Radboud University, Nijmegen, the Netherlands, and registered at the Donders Centre for Cognitive Neuroimaging under project number 3017031.05 (DCCN PI: Roshan Cools).

This research compendium contains all relevant data, code, and text and is organized as follows (showing directories in a tree-like format with a maximum depth of two levels):

    .
    ├── analysis
    ├── data
    │   ├── derivatives
    │   └── raw
    └── documents
        ├── content
        └── context

The `analysis/` directory contains:

-   R Markdown notebooks implementing the analyses (`notebooks_and_scripts/` directory), numbered in the order in which they were run;

The `data/` directory contains:

-   the data derived from the raw data (`derivatives/` directory), organized by notebook name.
    -   for meaning of output variables, see the codebooks of the notebook `01_preprocess_log_files` (`documents/content/01_preprocess_log_files/`) and the notebook (`analysis/01_preprocess_log_files.Rmd`).

N.B. The raw data is not shared, because it contains information about date and time on which the session took place, potentially allowing for identification of participants (e.g. by participants themselves). However, the raw data are archived at the Donders Center for Cognitive Neuroimaging under project number 3017031.05

The `documents/` directory contains:

-   documents describing the content of the experimental data (`content/` directory), such as codebooks;
-   documents describing the context of the data (`context/` directory), such as ethics documents and task instructions;

Finally, this research compendium is associated with the following online objects:

<table>
<colgroup>
<col width="9%" />
<col width="45%" />
<col width="45%" />
</colgroup>
<thead>
<tr class="header">
<th>object</th>
<th>archived version</th>
<th>development version</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>stimulus presentation code</td>
<td><a href="https://doi.org/10.5281/zenodo.3243799" class="uri">https://doi.org/10.5281/zenodo.3243799</a></td>
<td><a href="github.com/bramzandbelt/StPy" class="uri">github.com/bramzandbelt/StPy</a></td>
</tr>
</tbody>
</table>

In this experiment, we used the following StPy stimulus presentation configuration files (under `config/` in `StPy`):

-   `expt_3017031-05-Expt01-A.yaml`
-   `expt_3017031-05-Expt01-B.yaml`

Brief overview of methods
-------------------------

### Participants

We recruited a total of 11 participants (for demographics, see: `documents/content/sample_characteristics.csv`) through an online database for subjects interested in participating in research at the Donders Institute and Behavioral Science Institute of Radboud University (Sona Systems Ltd., Tallinn, Estonia). One participants was excluded, because they failed to bring performance in line with pre-set task performance criteria during the practice session. All participants had normal or corrected to normal vision and did report no history of neurological or psychiatric illness or claustrophobia. The study procedures were in accordance with the Declaration of Helsinki \[@WorldMedicalAssociation2013\] and were approved by the local ethics committee (Committee on Research Involving Human Subjects Arnhem-Nijmegen, registered under CMO2014/088). Written informed consent was obtained from all participants before enrollment in the study.

### Task

All stimuli were presented in the center of the screen on a grey background. The fixation stimulus was a white cross, subtending 3 degrees along its vertical axis. The primary stimulus (go stimulus) was a white Hiragana character, subtending 6 degrees along its vertical axis. It was chosen from a set of two; each session, a new set of Hiragana characters was used. The secondary stimulus (signal) was a playing card suit symbol at 80% opacity, subtending 3 degrees along the vertical axis and presented on top of the primary stimulus. It was chosen from a set of four: an orange diamond, a cyan heart, a yellow spade, or a purple club. The same set of secondary stimuli were used across sessions.

Each trial started with the presentation of a fixation stimulus for 200 ms. The fixation cross was immediately followed by the go stimulus and remained on the screen for 1200 ms, regardless of response time. Following go stimulus offset, feedback was presented for 500 ms. The next trial started after a further 200 ms, during which a blank screen was shown.

The primary task was to report the identity of the Hiragana character with a bimanual response. One character was mapped onto the two upper keys of a response pad, the other character was mapped onto the two lower keys. The character-to-key mapping was counterbalanced across participants. Participants controlled the two upper keys with their left and right middle fingers and the lower keys with their left and right index fingers. Participants were instructed to respond as accurate, fast, and simulatenous as possible.

On 40% of trials, one of four secondary stimuli was presented. One stimulus acted as the stop-left (SL) signal; it instructed participants to stop their left-hand response, but not their right-hand response. A second stimulus acted as the stop-right (SR) signal; it instructed participants to stop their right-hand response, but not their left-hand response. A third stimulus acted as the stop-both (SB) signal; it instructed participants to stop both their left-hand response and their right-hand response. A fourth stimulus acted as the ignore (IG) signal; it had to be ignored and the response had to be continued as planned. The stimulus-to-signal mapping was counterbalanced across participants (and did not vary across session). The primary (go) and secondary stimulus were separated by a stimulus onset asynchrony (*t*<sub>*d*</sub>). The stimulus onset asynchronies were 0.066, 0.166, 0.266, 0.366, and 0.466 s, each occurring with equal probability.

### Procedure

The experiment consisted of five sessions that took place on different days (longest interval between first and last session was 24 days). Each session consisted of a practice phase and an experiment phase.

#### Practice phase

The practice phase began with both written and verbal instructions (see `documents/context/StPy_task_instructions.pdf`), followed by experimenter-supervised practice in two stages.

In stage 1, participants performed one block of 50 no-signal trials. The goal of this stage was to acquaint participants with the primary task (Hiragana characters varied across sessions). At the end of this block, a feedback screen was displayed, showing mean no-signal trial RT, mean RT difference between the left- and right hand on no-signal trials, and no-signal choice performance. Task performance had to be in line with the following criteria: (i) mean no-signal response time &lt; 650 ms, (ii) mean difference between the left- and right hand response time on no-signal trials &lt; 50 ms, (iii) no-signal choice performance accuracy &gt; 85%.

If stage 1 task performance was not in line with one or more criteria, participants received additional feedback. If mean no-signal RT was longer than 650 ms, participants saw the following message: “remember to respond as fast as possible”. If mean RT difference between left and right fingers on no-signal trials was greater than 50 ms, participants also received the following feedback: “remember to respond simultaneously with your left and right fingers” If no-signal choice performance fell below 85% %, participants received the following feedback: “remember to be as accurate as possible”. Stage 1 was repeated until all criteria were met. If feedback did not bring performance in line with requirements over five subsequent blocks then the experiment was terminated and the participant was excluded.

In stage 2, participants performed one action-selective stopping block and one stimulus-selective stopping block, the order was counterbalanced across participants. The goal of this stage was to acquaint participants with the action-selective and stimulus-selective stop tasks, while maintaining go task performance. The action-selective stopping block consisted of 60 no-signal trials, 20 stop-left trials, and 20 stop-right trials. The stimulus-selective stopping block consisted of 60 no-signal trials, 20 stop trials, and 20 ignore trials. At the end of this block, a feedback screen was presented with the same descriptive statistics as in stage 1 plus the probability of responding for each of the signals. Task performance had to be in line with the three criteria specified in stage 1 as well as the following: (iv) probability of responding given a stop-left signal &lt; 0.80, (v) probability of responding given a stop-right signal &lt; 0.80, (vi) probability of responding given a stop-both signal &lt; 0.80, (vii) probability of responding given an ignore signal &gt; 0.80,

If stage 2 task performance was not in line with one or more criteria, participants received additional feedback. If overall probability of responding given a stop-signal was greater than 0.80, subjects received the following message: “remember to try to \[stop your left finger/right finger/left and right finger\] when you see a \[color and name of stop stimulus\]”. If overall probability of responding given an ignore-signal is smaller than 0.80, subjects received the following feedback: “remember to try to respond when you see a \[color and name of ignore stimulus\]“. Stage 2 was repeated until all criteria were met. If feedback did not bring performance in line with requirements over five subsequent blocks then the experiment was be terminated and the participant was excluded.

#### Experiment phase

In each session, participants performed 12 blocks of 100 trials, with trials in presented in pseudorandom order. Each block ended with a 10-s feedback screen (identical to the practice session) and participants could take optional breaks between blocks. Action-selective stopping blocks (6) and stimulus-selective stopping blocks (6) were presented in alternating order. All participants completed 5 sessions, hence a total of 6000 trials.

### Data acquisition

The experiment was run in PsychoPy \[@Peirce2007, @Peirce2008, release 1.83.04\] running under Windows 7 on a Dell Precision T3500 computer with two Intel Xeon Quad Core 2.80 GHz processors and 12 GB of RAM. Visual stimuli were projected on a screen positioned approximately 70 cm from the subject. Responses were collected using two MR-compatible fiber-optic response pads (Current Designs, Inc; Philadelphia, PA, USA), one for each hand.

How to use
----------

To download the code and data as you see it on GitHub, for offline browsing, use this line at the shell prompt (assuming you have Git installed on your computer):

Install `cmass` package from Github:

-   From R:

        devtools::install_github("bramzandbelt/cmass")

-   From the command line:

        git clone https://github.com/bramzandbelt/cmass.git

Once the download is complete, open the file `cmass.Rproj` in RStudio to begin the compendium files.

Licenses
--------

Code: MIT <http://opensource.org/licenses/MIT>, year: 2019, copyright holder: Bram B. Zandbelt

Dependencies
------------

Below is the output of `sessionInfo()`, showing version information about R, the OS, and attached or loaded packages:

``` r
devtools::session_info()
#> ─ Session info ──────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 3.6.0 (2019-04-26)
#>  os       macOS Mojave 10.14.5        
#>  system   x86_64, darwin15.6.0        
#>  ui       X11                         
#>  language (EN)                        
#>  collate  en_US.UTF-8                 
#>  ctype    en_US.UTF-8                 
#>  tz       Europe/Amsterdam            
#>  date     2019-06-26                  
#> 
#> ─ Packages ──────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 3.6.0)
#>  backports     1.1.4   2019-04-10 [1] CRAN (R 3.6.0)
#>  callr         3.2.0   2019-03-15 [1] CRAN (R 3.6.0)
#>  cli           1.1.0   2019-03-19 [1] CRAN (R 3.6.0)
#>  crayon        1.3.4   2017-09-16 [1] CRAN (R 3.6.0)
#>  desc          1.2.0   2018-05-01 [1] CRAN (R 3.6.0)
#>  devtools      2.0.2   2019-04-08 [1] CRAN (R 3.6.0)
#>  digest        0.6.18  2018-10-10 [1] CRAN (R 3.6.0)
#>  evaluate      0.13    2019-02-12 [1] CRAN (R 3.6.0)
#>  fs            1.2.7   2019-03-19 [1] CRAN (R 3.6.0)
#>  glue          1.3.1   2019-03-12 [1] CRAN (R 3.6.0)
#>  htmltools     0.3.6   2017-04-28 [1] CRAN (R 3.6.0)
#>  knitr         1.23    2019-05-18 [1] CRAN (R 3.6.0)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 3.6.0)
#>  memoise       1.1.0   2017-04-21 [1] CRAN (R 3.6.0)
#>  pkgbuild      1.0.3   2019-03-20 [1] CRAN (R 3.6.0)
#>  pkgload       1.0.2   2018-10-29 [1] CRAN (R 3.6.0)
#>  prettyunits   1.0.2   2015-07-13 [1] CRAN (R 3.6.0)
#>  processx      3.3.0   2019-03-10 [1] CRAN (R 3.6.0)
#>  ps            1.3.0   2018-12-21 [1] CRAN (R 3.6.0)
#>  R6            2.4.0   2019-02-14 [1] CRAN (R 3.6.0)
#>  Rcpp          1.0.1   2019-03-17 [1] CRAN (R 3.6.0)
#>  remotes       2.0.4   2019-04-10 [1] CRAN (R 3.6.0)
#>  rlang         0.3.4   2019-04-07 [1] CRAN (R 3.6.0)
#>  rmarkdown     1.12    2019-03-14 [1] CRAN (R 3.6.0)
#>  rprojroot     1.3-2   2018-01-03 [1] CRAN (R 3.6.0)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 3.6.0)
#>  stringi       1.4.3   2019-03-12 [1] CRAN (R 3.6.0)
#>  stringr       1.4.0   2019-02-10 [1] CRAN (R 3.6.0)
#>  testthat      2.1.1   2019-04-23 [1] CRAN (R 3.6.0)
#>  usethis       1.5.0   2019-04-07 [1] CRAN (R 3.6.0)
#>  withr         2.1.2   2018-03-15 [1] CRAN (R 3.6.0)
#>  xfun          0.6     2019-04-02 [1] CRAN (R 3.6.0)
#>  yaml          2.2.0   2018-07-25 [1] CRAN (R 3.6.0)
#> 
#> [1] /Library/Frameworks/R.framework/Versions/3.6/Resources/library
```

For a complete list of the packrat Packrat takes care of dependencies.

Acknowledgment
--------------

This research project was funded through a James McDonnell Scholar Award (grant number 220020328) to Roshan Cools. We thank Roshan Cools (RC) for financial support and constructive feedback on conceptualization. We thank Patrick G. Bissett (PGB), Jeffrey D. Schall (JDS), and Gordon D. Logan (GDL) for constructive feedback on on conceptualization. We thank Ben Marwick for inspiration on [how to create, organize, and describe research compendia](https://github.com/benmarwick/researchcompendium).

Contributor roles
-----------------

We specify the contribution of all people involved in the research (contributing non-authors included), according to the [Contributor Role Taxonomy](https://www.casrai.org/credit/).

|                        | BBZ | RvdB | RC  | PGB | JDS | GDL |
|------------------------|-----|------|-----|-----|-----|-----|
| Conceptualization      | X   | -    | -   | X   | X   | X   |
| Methodology            | X   | -    | -   | -   | -   | -   |
| Software               | X   | -    | -   | -   | -   | -   |
| Validation             | X   | -    | -   | -   | -   | -   |
| Formal analysis        | X   | -    | -   | -   | -   | -   |
| Investigation          | -   | X    | -   | -   | -   | -   |
| Resources              | X   | -    | -   | -   | -   | -   |
| Data curation          | X   | -    | -   | -   | -   | -   |
| Supervision            | X   | -    | -   | -   | -   | -   |
| Project administration | -   | X    | -   | -   | -   | -   |
| Funding acquisition    | -   | -    | X   | -   | -   | -   |

Contact
-------

[Bram B. Zandbelt](mailto:bramzandbelt@gmail.com)
