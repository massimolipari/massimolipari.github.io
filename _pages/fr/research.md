---
page_id: research
layout: page
permalink: /research/
title: Recherche
nav: true
nav_order: 2
---

Cette page présente mes travaux récents et en cours, répartis en plusieurs projets qui se chevauchent.

<br>

#### Ensembles de données

---

##### Une base de données pour la typologie phonétique

On assiste depuis plusieurs années à un véritable foisonnement de corpus oraux pour une quantité et une diversité impressionnantes de langues, stimulé par des investissements massifs dans la reconnaissance automatique de la parole. Cette tendance a déclenché une nouvelle vague de travaux en typologie phonétique qui cherche à adapter ces ressources à l'analyse phonétique, faisant émerger de nouvelles bases de données multilingues comme [*VoxCommunis*](https://aclanthology.org/2022.lrec-1.566/). Ces ensembles de données ont rendu possibles des études de grande qualité, mais ils comportent souvent certaines limites : la quantité de données peut être restreinte pour certaines langues, et les métadonnées des locutrices et locuteurs (p. ex., leur identité ou leur genre) peuvent être absentes.

Ce projet vise à mettre sur pied une nouvelle base de données pour pallier certaines de ces limites en réunissant des corpus appropriés tirés de diverses sources. L'objectif est d'arriver à mieux départager la variation interlinguistique et la variation inter-locuteur dans les études typologiques. À ce jour, des données pour 32 langues et plus de 4 600 locutrices et locuteurs (généralement au moins une centaine par langue) ont été colligées. Plusieurs des corpus (mais pas tous), dont [*LibriSpeech*](https://doi.org/10.1109/ICASSP.2015.7178964) et les divers [corpus *NCHLT*](https://www.isca-archive.org/sltu_2014/barnard14_sltu.html), sont entièrement publics. (Pour la liste complète des langues, voir le tableau A1 de [cet article](https://doi.org/10.31234/osf.io/m4ksy_v1).) Je travaille à rendre les divers scripts et outils créés dans le cadre du projet (p. ex., règles de conversion graphème–phonème, dictionnaires de prononciation et modèles acoustiques pour le Montreal Forced Aligner) disponibles, dans l'espoir qu'ils seront utiles à d'autres membres de la communauté phonétique.

<br>

##### Le corpus *ParlBleu* de français québécois

Bien que le français québécois ait été au cœur de nombreux travaux variationnistes pionniers, il existe étonnamment peu de ressources phonétiques prêtes à l'emploi pour cette langue. Afin de combler cette lacune, Peter Milne a constitué le corpus *AssNat* ([décrit dans sa thèse de doctorat de 2014](https://ruor.uottawa.ca/items/b76e477e-316b-4ee3-b7fd-49463f807248)) à partir d'enregistrements des travaux de l'Assemblée nationale du Québec. Bien que le corpus ait d'abord été offert en libre accès, le site Web qui l'hébergeait a malheureusement été mis hors ligne depuis.

J'ai mené un projet visant à relancer le corpus *AssNat* en l'intégrant à une version élargie, rebaptisée corpus *ParlBleu*. Grâce à l'aide de quelques auxiliaires de recherche---surtout [Laurie Dumont](https://www.linkedin.com/in/laurie-dumont-9690262bb/)---le corpus compte dorénavant plus de 30 heures de données provenant de 156 locutrices et locuteurs, ainsi qu'autant d'informations biographiques (genre, année et lieu de naissance) que nous avons pu en trouver en ligne. Il s'agit d'une ressource évolutive que nous comptons bonifier au fil des ans. Les données sont accessibles [sur OSF](https://osf.io/35fk8/).

<br>

#### Projets

---

##### L'analyse de médiation appliquée à la variation de genre

L'adage « corrélation n'implique pas causalité » est souvent compris comme signifiant qu'il est impossible d'établir des liens de causalité dans les études observationnelles---et donc, dans des domaines comme la phonétique de corpus. Ce n'est toutefois pas tout à fait exact : tout modèle de régression que l'on ajuste repose sur certaines hypothèses quant aux liens causaux entre les variables. L'*inférence causale* consiste à rendre ces hypothèses explicites et à en évaluer la plausibilité. L'*analyse de médiation causale* est une méthode d'inférence causale qui permet de résoudre un type de problème courant dans les données phonétiques. Souvent, une variable X peut influer sur une autre variable Y de deux manières distinctes que l'on souhaite départager : soit directement (X → Y), soit par l'entremise d'une *variable médiatrice* Z (X → Z → Y).

La variation de genre dans la parole en offre un exemple concret. Les locutrices et locuteurs se servent de variables phonétiques pour performer leur identité de genre, mais le genre (ou plus exactement, le sexe) influe aussi sur des facteurs comme l'anatomie du conduit vocal, qui affectent à leur tour ces mêmes variables. L'analyse de médiation causale permet de déterminer la contribution relative de chacun de ces mécanismes à l'effet total du genre sur l'acoustique. Dans [une communication présentée à Interspeech 2026](https://www.isca-archive.org/interspeech_2026/lipari26_interspeech.html) avec Morgan Sonderegger et Meghan Clayards, nous élaborons une méthode fondée sur l'analyse de médiation pour démêler la performance et la physiologie dans l'acoustique du /s/ dans 12 langues (un sous-ensemble de la base de données multilingue que j'ai constituée). La variable médiatrice est ici la longueur du conduit vocal de chaque locutrice ou locuteur, estimée à partir des formants de ses voyelles. Nous constatons que la méthode produit des résultats sensés d'une langue à l'autre : l'effet physiologique est relativement constant en ampleur et en direction, alors que la composante performée varie davantage.

<br>

##### La dynamique spectrale des fricatives sibilantes

Les fricatives sont souvent traitées comme des sons fondamentalement stationnaires, qui varient peu au cours de leur émission. Mais que perd-on en adoptant cette hypothèse simplificatrice ? Des travaux récents (notamment [cet article de Patrick Reidy paru en 2016](https://doi.org/10.1121/1.4964510)) suggèrent que la dynamique spectrale varie d'une sibilante à l'autre au sein d'une même langue, mais aussi pour une même sibilante d'une langue à l'autre. La variation temporelle des sibilantes serait donc linguistiquement significative, et d'une manière ou d'une autre sous le contrôle direct des locutrices et locuteurs. L'ampleur de la variation interlinguistique reste toutefois à établir, et l'influence de facteurs confondants potentiels comme le débit de parole ou la coarticulation doit être prise en compte.

Cette étude, menée avec Morgan Sonderegger et Meghan Clayards, s'appuie sur ma base de données multilingue pour examiner la dynamique spectrale du /s/ à travers les langues. Dans un manuscrit en cours de révision ([la prépublication se trouve ici](https://doi.org/10.31234/osf.io/m4ksy_v1)), nous reproduisons les résultats antérieurs quant à la variation interlinguistique dans la dynamique spectrale, et montrons que celle-ci persiste malgré l'inclusion de plusieurs variables de contrôle.

<br>

##### La variation articulatoire et acoustique dans les consonnes rhotiques de l'anglais

Le /r/ anglais connaît deux variantes articulatoires radicalement différentes : une massée (langue bombée sous le palais) et une rétroflexe (pointe de la langue relevée). En anglais nord-américain, ces deux articulations alternent de façon essentiellement « libre », et on peine à les distinguer---probablement parce que les deux variantes produisent la même signature acoustique principale, soit un troisième formant très bas. En anglais écossais, en revanche, les /r/ massé et rétroflexe sont distincts à l'oreille et font même l'objet d'une stratification sociale : les membres de la classe ouvrière tendent à produire un /r/ rétroflexe faible, alors que ceux de la classe moyenne ont plutôt un /r/ massé fort. Comment concilier ces deux constats ? Les formants autres que F3 recèlent-ils la clé de l'énigme ?

Ces questions sont examinées dans le cadre d'une collaboration avec [Eleanor Lawson](https://www.strath.ac.uk/staff/lawsoneleanordr/) et [Jane Stuart-Smith](https://www.gla.ac.uk/schools/critical/staff/janestuart-smith/), entamée lors d'un stage que j'ai effectué à l'Université de Glasgow en 2024. Nous nous servons d'un corpus d'enregistrements audio et échographiques simultanés de 32 locutrices et locuteurs de l'anglais écossais, irlandais et nord-américain afin d'examiner l'effet de la forme de la langue sur les trajectoires des formants (F1--F4) dans les séquences voyelle + /r/. Les résultats préliminaires ne sont pas concluants : nous observons de faibles différences dans F1, F2 et F4 allant dans le sens attendu d'après [des travaux antérieurs](https://doi.org/10.1121/1.2902168), mais ces effets ne sont pas significatifs.

<br>

##### Le changement phonétique dans les voyelles du français québécois

Dans [un article paru en 2025 dans la revue *Laboratory Phonology*](https://doi.org/10.16995/labphon.11678) avec Morgan Sonderegger, nous nous servons d'une version antérieure du corpus *ParlBleu* pour étudier un changement phonétique inusité en français québécois : l'émergence d'une qualité rhotique dans les voyelles /ø/ (*j**eu***), /œ/ (*c**œu**r*) et /œ̃/ (***un***). Cette étude suit le changement dans l'espace et en temps apparent au cours de la seconde moitié du 20<sup>e</sup> siècle afin de déterminer son origine. Nous montrons que, contrairement à ce à quoi on s'attendrait pour ce genre de changement, la coarticulation avec une consonne rhotique subséquente n'en est pas une source plausible. Nous soutenons plutôt que le changement résulte de la conjonction de facteurs externes et internes : un contact intense avec l'anglais (donnant lieu à de nombreux emprunts lexicaux comportant un /ɚ/ non adapté) et des pressions fonctionnelles (à savoir la nécessité d'accentuer les contrastes vocaliques dans un système encombré).

<br>

#### Logiciels

---

##### PolyglotDB

Je suis l'un des mainteneurs de [PolyglotDB](https://polyglotdb.readthedocs.io/en/latest/), un module Python servant à la gestion et à l'analyse de grands corpus oraux à l'aide de bases de données. En plus d'ajouter de nouvelles fonctionnalités et de corriger des bogues, j'ai contribué à une bonne partie de la documentation, notamment deux études de cas qui présentent plusieurs options pour analyser l'acoustique des [voyelles](https://polyglotdb.readthedocs.io/en/latest/case_study_vowel_dynamics.html) et des [sibilantes](https://polyglotdb.readthedocs.io/en/latest/case_study_sibilants.html).
