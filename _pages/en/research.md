---
page_id: research
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 2
---

This page describes my recent and ongoing work, split across several (often overlapping) projects.

<br>

#### Datasets

---

##### Speech database for phonetic typology

The number and diversity of speech corpora have grown rapidly in recent years, spurred on by massive investments in speech technology. This has helped trigger a new wave in phonetic typology where researchers take ASR corpora and adapt them for phonetic analysis, producing large multilingual databases like [*VoxCommunis*](https://aclanthology.org/2022.lrec-1.566/). These datasets have served as the base for some excellent work, but often come with some limitations: there may be only a few speakers for some languages, or speaker metadata (e.g., speaker labels or gender annotations) may not be present.

This project looks to remedy this issue by creating a new speech database by combining suitable corpora from a variety of sources. The aim is to better be able to tease apart cross-linguistic and inter-speaker variation. So far, I've collated data from 32 languages and more than 4,600 speakers (usually a minimum of ~100 per language). The database includes many (but not only) open corpora like [*LibriSpeech*](https://doi.org/10.1109/ICASSP.2015.7178964) and the various [*NCHLT corpora*](https://www.isca-archive.org/sltu_2014/barnard14_sltu.html). (For a full list of languages, see Table A1 in [this paper](https://doi.org/10.31234/osf.io/m4ksy_v1).) I'm working to make the various scripts and tools (e.g., G2P rulesets, pronunciation dictionaries, and Montreal Forced Aligner acoustic models) available in an easy-to-use way, in hopes that they'll be useful to the wider phonetics community.

<br>

##### *ParlBleu* corpus of Quebec French

Although Quebec French was at the heart of much early variationist research, there are surprisingly few ready-to-use phonetic datasets for the language. To fill this gap, Peter Milne built the *AssNat* corpus from recordings of the National Assembly of Quebec's proceedings (as described in [his 2014 dissertation](https://ruor.uottawa.ca/items/b76e477e-316b-4ee3-b7fd-49463f807248)). While the corpus was originally made publicly available, the website where it was hosted was unfortunately taken down at some point. 

This project is an attempt I've led to resurrect the *AssNat* corpus, wrapping it into an expanded sequel dubbed the *ParlBleu* corpus. Thanks to the help of some research assistants---especially [Laurie Dumont](https://www.linkedin.com/in/laurie-dumont-9690262bb/)---the corpus now includes more than 30 hours of data across 156 speakers, along with as much speaker metadata (gender, year of birth and place of birth) as we've been able to find online. The aim is to continue to grow this resource over the years. The data can be accessed [on OSF](https://osf.io/35fk8/).

<br>

#### Projects

---

##### Mediation analysis of gender variation

The adage "correlation does not imply causation" is often taken to mean that it's impossible to establish causality in observational studies---and thus, in fields like corpus phonetics. This isn't quite true, however: any regression model we fit incorporates certain assumptions about causal relationships between variables. *Causal inference* is the process of making these assumptions explicit and thinking about their plausibility. *Causal mediation analysis* is a causal inference method that helps us solve a common kind of problem in phonetic data. Often, one variable X can affect another Y in two disinct ways that we want to tease apart: either directly (X → Y) or through a *mediating variable* Z (X → Z → Y).

One concrete case is gender variation in speech. We believe speakers use phonetic variables to perform gender, but also that gender (or more accurately, sex) affects things like vocal tract physiology, which in turn affect those same variables. Causal mediation analysis can tell us what the relative contribution of each pathway is to the total effect of gender on the acoustics. In a [2026 Interspeech paper](https://www.isca-archive.org/interspeech_2026/lipari26_interspeech.html) with Morgan Sonderegger and Meghan Clayards, we develop a mediation analysis-based method to disentangle performance and physiology in /s/ acoustics across 12 languages (a subset of the multilingual speech database I built). Here, the mediating variable is speakers' vocal tract length, as estimated from their vowel formants. We find this method produces sensible results across languages: the physiological effect is fairly consistent in size and direction across languages, whereas there's more variation in the performed component.

<br>

##### Spectral dynamics in sibilant fricatives

Fricatives are often treated as if they're fundamentally stationary sounds, showing little variation over the time course of production. But what is lost when we make this simplifying assumption? Recent work (especially Patrick Reidy's [2016 paper](https://doi.org/10.1121/1.4964510)) suggests that patterns of spectral dynamics in (sibilant) fricatives vary across different sibilants in the same language, and also within the same sibilant across different languages. This points to temporal variation in sibilants being linguistically meaningful, and somehow under direct phonological control. Just how much cross-linguistic variation there is remains to be established, however, and the influence of possible confounds like speech rate or coarticulation must be accounted for.

This study, conducted with Morgan Sonderegger and Meghan Clayards, uses my multilingual database to examine the spectral dynamics of /s/ across languages. In a manuscript currently in revision ([preprint here](https://doi.org/10.31234/osf.io/m4ksy_v1)), we replicate previous findings of cross-linguistic variation in temporal dynamics, and show that it survives the inclusion of several control variables.

<br>

##### Articulatory and acoustic variation in English rhotics

Famously, English /r/ can be produced with one of two radically different tongue shapes: it can be bunched or retroflex. In North American varieties, these two articulations are largely in "free" variation, with listeners struggling to hear the difference between them---likely because both variants produce the same key acoustic signature, a very low third formant. But in Scottish English, bunched and retroflex /r/ are audibly distinct and even subject to social stratification: working-class speakers tend to produce a weak, retroflex /r/, whereas middle-class speakers tend to have a strong, bunched /r/. How can these two findings be reconciled? Do formants other than F3 hold a clue to the answer?

These questions are examined in a collaboration with [Eleanor Lawson](https://www.strath.ac.uk/staff/lawsoneleanordr/) and [Jane Stuart-Smith](https://www.gla.ac.uk/schools/critical/staff/janestuart-smith/), which we began while I was at the University of Glasgow in 2024 on a lab visit. We use a corpus of simultaneous ultrasound and audio recordings for 32 speakers of Scottish, Irish, and North American English to investigate how F1--F4 trajectories in vowel + /r/ sequences are affected by tongue shape. Preliminary results are inconclusive: we find small differences in F1, F2, and F4 in the expected direction from [previous work](https://doi.org/10.1121/1.2902168), but the effects are not significant.

<br>

##### Sound change in Quebec French vowels

In [a 2025 paper](https://doi.org/10.16995/labphon.11678) with Morgan Sonderegger, we use an earlier version of the *ParlBleu* corpus to investigate an unusual sound change in Quebec French: the vowels /ø/ (*p**eu***), /œ/ (*c**oeu**r*), and /œ̃/ (***un***) are developing a rhotic quality. This study follows this change across space and apparent time over the second half of the 20th century in order to uncover its underlying cause. We show that contrary to what's expected with rhotacization changes, coarticulation with a following rhotic is not a plausible source. Instead, we argue that the change is driven by a combination of intense contact with English (resulting in many loanwords containing unadapted /ɚ/) and functional pressures (namely the need to enhance contrasts due to vowel space crowding).

<br>


#### Software

---

##### PolyglotDB

I'm a maintainer of the Python package [PolyglotDB](https://polyglotdb.readthedocs.io/en/latest/), a database-centered tool for managing and analyzing large speech corpora. In addition to bug fixes, I've helped contribute a lot of the documentation, especially two case studies working through several options for analyzing [vowel](https://polyglotdb.readthedocs.io/en/latest/case_study_vowel_dynamics.html) and [sibilant](https://polyglotdb.readthedocs.io/en/latest/case_study_sibilants.html) acoustics.
