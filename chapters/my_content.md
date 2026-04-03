**Evaluating and replicating studies: A practical guide\**

wolf vanpaemel

KU Leuven

wolf(dot)vanpaemel(at)kuleuven(dot)be

last change: march 4 2025

A. PREFACE

## about this guide

\- This guide is based on a collection of notes, which grew out of doing
replication research with master students as part of their master
thesis, which I started doing erratically in 2013 and somewhat
systematically since 2020. I tried to create something helpful for them
and this guide is a part of that survival package.

\- While the main topic is replication research, an important step when
replicating a study is critically evaluating the study of interest. A
good deal of these notes focuses on these aspects (Sections
\@sec-evaluating to \@sec-reanalysing), and includes topics like
conversions, recreations, and reproductions. As evaluating or appraising
a study is of interest to any researcher, not just to a researcher
wishing to replicate a study, these notes might be useful for you even
if you don't want to replicate. \[Note: These sections will be added
somewhere soon\]

\- This guide grew out of my own hands-on experiences and conversations
with my students, and it shows. It doesn't integrate the different
findings and perspectives from all sorts of papers about replication and
evaluation found in the literature. It doesn't even try to! It just
represents how I advise my students to do replication research and how
to evaluate a study. It doesn't represent (nor does it try to represent)
a consensus of how the field thinks it should be done, or how it is done
by others. That being said, I don't think I am saying much that could be
considered controversial. Not only is nothing in these notes
controversial, nothing is new or original either. Still, my students
have found it valuable to have all things collected in one place, so you
might find that too.

\- This guide is incomplete by design, as it is not intended to be
complete. It, for example, do not contain all possible fine grained
distinctions between types of replications. My main or only criterion
for inclusion was whether it is helpful to my students doing their
replication study. \[FOONOTE: Ok, I admit, I did not always honor the
usefulness criterion in the footnotes.\] Further, it is also just
incomplete by time. It represents what I have collected up till today,
not what I think should ideally be discussed. As long as my students
continue to ask me questions, this guide will be expanded in the future.
So this guide is very much a work in progress. Sometimes, I know what I
want to add, but haven't found the energy or the time to do that. So you
will come across a few things like "TODO: add an example".

Also, things change quickly. Tools come and go, platforms rise and fall,
techniques pop up, insights mature and priorities shift. I can not
possibly keep up.

\- So this guide is supposed to be a living document. This means that

1\) It is a work in progress and incomplete.

2\) It will be regularly updated, sometimes with large overhauls (in
which case I will keep a legacy copy), sometimes by just adding or
deleting a few sentences.

3\) It is very much open to your comments and suggestions, when things
are missing, unclear, or just plain stupid. Send me an email, or leave a
comment in this google doc TODO update when Rmd and git.

#- I often didn't bother writing eloquent or long paragraphs. Again, the
main goal was usefulness, not flex.

#- It's just a loosely organised collection of notes, and it does not
adhere to academic style. For example, I have been deliberately loose on
referencing. I will try to make up for that by extending the Further
Reading part.

\- Because I have a bad memory and I suspect my students do too, I ask
them to write quite a few reports throughout the replication process.
Most of these reports come with a template, which you may find here
[[https://docs.google.com/document/d/1V0m4x6pDVFaDSu5_AWa6SiNCqI3wc9V-\_SiyqXuZC7s/edit?tab=t.0]{.underline}](https://docs.google.com/document/d/1V0m4x6pDVFaDSu5_AWa6SiNCqI3wc9V-_SiyqXuZC7s/edit?tab=t.0),
in case they would be useful to you. TODO update

## who this guide for

\- This guide heavily focuses on quantitative research, solely
reflecting my own bias, interest and experience.

\- It is written with an inexperienced audience in mind. It, for
example, includes an elaborate section explaining where to look for info
related to a paper. If you are a seasoned researcher but have never done
a replication, this section is probably not that useful to you, but I
found it was being appreciated by my inexperienced students.

\- There is another sense in which this guide is written with an very
experienced audience in mind, or at least an audience that is willing to
find information elsewhere. These notes strictly focus on evaluation and
replication research. As replication research is of course just a type
of empirical research, a more complete description of how replication
research works should, in principle, discuss how to design a study, how
to collect empirical data, how to analyze the data, and so on. This
guide does *not* do that, so if you are looking for that, this guide
will not be (sufficient) for you. I only included stuff that is specific
for doing replication research in particular, not for doing empirical
research in general. Also, I assume familiarity with basic statistical
concepts.

\- However. An excellent source to learn about these general empirical
and experimental methods is
[[Experimentology]{.underline}](https://experimentology.io/) (pdf here
[[https://experimentology.io/Experimentology.pdf]{.underline}](https://experimentology.io/Experimentology.pdf)).
A true gem when it comes down to statistics is
[[https://learningstatisticswithr.com/book/]{.underline}](https://learningstatisticswithr.com/book/)
(pdf here
[[https://learningstatisticswithr.com/lsr-0.6.pdf]{.underline}](https://learningstatisticswithr.com/lsr-0.6.pdf)).
I will refer to it as LSR. Despite its name, this book comes in several
versions beyond R, including JASP, all linked on
[[https://learningstatisticswithr.com/]{.underline}](https://learningstatisticswithr.com/).

## software

\- In the part about evaluating a study (Section \@sec-evaluating to
\@sec-reanalysing), I sometimes provide R code. I don't give a lot of
explanation there, because I assume you already know R, or will not
bother learning R just for this goal. To make up for that, I will try to
give user friendly alternatives on external websites when available.
Further, I will point out if and how these analyses can be done using
the open source, intuitive and free statistical software program JASP,
which is freely available here
[[https://jasp-stats.org/]{.underline}](https://jasp-stats.org/).

## similar works

\- To avoid having to replicate stuff that other people have written
earlier and well, I will sometimes refer to or literally quote from
similar sources. In particular, when needed I will refer to and quote
from from

- the [[Handbook for Reproduction and Replication
  Studies]{.underline}](https://forrt.org/replication_handbook/) (pdf
  here
  [[https://forrt.org/replication_handbook/Handbook-for-Reproduction-and-Replication-Studies.pdf]{.underline}](https://forrt.org/replication_handbook/Handbook-for-Reproduction-and-Replication-Studies.pdf)),
  which focuses on replication and reproduction (which is a part of
  evaluation). I will refer to it as HRRS.

- the [[Guide for Accelerating Computational Reproducibility in the
  Social Sciences \| Guide for Accelerating Computational
  Reproducibility in the Social
  Sciences]{.underline}](https://bitss.github.io/ACRE/) (pdf here
  [[https://bitss.github.io/ACRE/ACRE_book.pdf]{.underline}](https://bitss.github.io/ACRE/ACRE_book.pdf)),
  which focuses on reproduction (which is a part of evalaution). I will
  refer to it as ACRE.

- The currently best reference I know about checking the numerical
  conformity of a study of Section \@sec-checkingconformity (which is
  one of the steps in the evaluation process) is
  [[forensicmetascience.com]{.underline}](http://forensicmetascience.com)
  (pdf here
  [[https://zenodo.org/records/14871843/files/Heathers%20J%20An%20Introduction%20to%20Forensic%20Metascience%20(2025).pdf?download=1]{.underline}](https://zenodo.org/records/14871843/files/Heathers%20J%20An%20Introduction%20to%20Forensic%20Metascience%20(2025).pdf?download=1)).
  I will refer to it as AITFM.

## citation

Vanpaemel, W. (2026) Evaluating and replicating studies: A practical
guide**\**
Retrieved from [[earsguide.io]{.underline}](http://earsguide.io). doi
TODO

## acknowledgements

\^ Most of what is included in this guide was written in response to
questions that were asked by my, sometimes enthusiastic and at other
times frustrated, students when doing a replication study, or have
originated as remarks I thought of when I was reading their work.
Without my students, I wouldn't have written any of this, so I have them
to thank.

## table of contents

> [about this guide 2](#about-this-guide)
>
> [who this guide for 3](#who-this-guide-for)
>
> [software 4](#software)
>
> [similar works 5](#similar-works)
>
> [citation 5](#citation)
>
> [acknowledgements 5](#acknowledgements)
>
> [table of contents 6](#table-of-contents)

[**A replication? {#areplication} 8**](#a-replication-areplication)

[**The same? {#thesame} 9**](#the-same-thesame)

> [doing the same is impossible or infeasible {#impossible}
> 9](#doing-the-same-is-impossible-or-infeasible-impossible)
>
> [doing the same is ambiguous {#ambiguous}
> 11](#doing-the-same-is-ambiguous-ambiguous)
>
> [doing the same is not ideal or undesired {#undesired}
> 15](#doing-the-same-is-not-ideal-or-undesired-undesired)
>
> [doing the same is not your current interest {#nointerest}
> 17](#doing-the-same-is-not-your-current-interest-nointerest)
>
> [ok, i get it. can we wrap up, please?
> 19](#ok-i-get-it.-can-we-wrap-up-please)

[**Are we replicating still? {#still}
20**](#are-we-replicating-still-still)

[Some criteria for selecting a replication study {#somecriteria}
25](#some-criteria-for-selecting-a-replication-study-somecriteria)

> [feasibility{#feasibility} 26](#feasibilityfeasibility)
>
> [questionability{#questionability}
> 27](#questionabilityquestionability)
>
> [impact{#impact} 28](#impactimpact)
>
> [other practical considerations{#other}
> 29](#other-practical-considerationsother)

[Finding information about published research {#findinginformation}
30](#finding-information-about-published-research-findinginformation)

[Contacting the original authors {#contacting}
33](#contacting-the-original-authors-contacting)

[CRITICALLY EVALUATING THE ORIGINAL STUDY {#evaluating}
36](#critically-evaluating-the-original-study-evaluating)

[POST PUBLICATION AND OTHER DISCUSSIONS {#postpublication}
37](#post-publication-and-other-discussions-postpublication)

[**CHECKING THE REPORTING INTEGRITY OF THE ORIGINAL STUDY
{#checkingprereg}
39**](#checking-the-reporting-integrity-of-the-original-study-checkingprereg)

[**CHECKING THE QUALITY OF THE ORIGINAL STUDY {#checkingquality}
41**](#checking-the-quality-of-the-original-study-checkingquality)

[VISUALISATION CHECKS {#checkingvisuals}
46](#visualisation-checks-checkingvisuals)

[CHECKING THE NUMERICAL CONFORMITY OF THE ORIGINAL STUDY (WITHOUT THE
ORIGINAL RAW DATA) {#checkingconformity}
47](#checking-the-numerical-conformitydata-integrity-xxx-of-the-original-study-without-the-original-raw-data-checkingconformity)

> [common sense and logic{#commonsense}
> 50](#common-sense-and-logiccommonsense)
>
> [internal conversion: general idea{#internalgeneral}
> 52](#internal-conversion-general-ideainternalgeneral)
>
> [internal conversion: the equality edition (no p-values from
> summaries){#internalequality}
> 53](#internal-conversion-the-equality-edition-no-p-values-from-summariesinternalequality)
>
> [internal conversion: the p-value from summary statistics
> edition{#internalpvalue}
> 64](#internal-conversion-the-p-value-from-summary-statistics-editioninternalpvalue)
>
> [internal conversion: the inequality edition{#internalinequality}
> 79](#internal-conversion-the-inequality-editioninternalinequality)
>
> [external conversion{#external} 81](#external-conversionexternal)
>
> [recreation{#recreation} 83](#recreationrecreation)
>
> [rounding beware{#rounding} 91](#rounding-bewarerounding)
>
> [rules of thumb{#rules} 103](#rules-of-thumbrules)

[**REANALYSING THE ORIGINAL RAW DATA {#reanalysing}
106**](#reanalysing-the-original-raw-data-reanalysing)

> [reproducibility analysis{#reproducibility}
> 106](#reproducibility-analysisreproducibility)
>
> [alternative analyses{#alternative}
> 111](#alternative-analysesalternative)
>
> [data fabrication{#fabrication} 112](#data-fabricationfabrication)

[DESIGNING YOUR STUDY {#designingstudy}
114](#designing-your-study-designingstudy)

[DESIGNING YOUR ANALYSES {#designinganalysis}
116](#designing-your-analyses-designinganalysis)

[PREREGISTERING YOUR STUDY{#prereg}
119](#preregistering-your-studyprereg)

[**COLLECTING YOUR DATA{#datcoll} 120**](#collecting-your-datadatcoll)

[**INTERPRETING YOUR RESULT 121**](#interpreting-your-result)

[WRITING UP YOUR EVALUATION AND REPLICATION STUDY{#writing}
122](#writing-up-your-evaluation-and-replication-studywriting)

> [GENERAL 122](#general)
>
> [INTRODUCTION 122](#introduction)
>
> [EVALUATION 123](#evaluation)
>
> [REPLICATION 125](#replication)

[**PUBLISHING {#publishing} 127**](#publishing-publishing)

[**SHARING {#sharing} 128**](#sharing-sharing)

> [BOOKS ON REPLICATION, CONFORMITY AND REPRODUCTION
> 129](#books-on-replication-conformity-and-reproduction)
>
> [ON REPLICATION 129](#on-replication)
>
> [ON REPRODUCTION 130](#on-reproduction)
>
> [ON MULTIVERSE 130](#on-multiverse)
>
> [STUDIES USED IN THE EXAMPLES 130](#studies-used-in-the-examples)
>
> [STATISTICAL FALLACIES 132](#statistical-fallacies)
>
> [TOOLS AND CHECKLISTS FOR STUDY EVALUATION
> 132](#tools-and-checklists-for-study-evaluation)
>
> [TOOLS AND TECHNIQUES FOR CHECKING NUMERICAL CONFORMITY
> 132](#tools-and-techniques-for-checking-numerical-conformity)
>
> [OTHER 132](#other)

B. GETTING STARTED

# A replication? {#areplication}

\^ Let's start by discussing some terminology

- A **replication** of a result involves collecting new data in the same
  design and running the same analyses on the **newly collected data**
  (i.e. different data) to test the same hypothesis (or more broadly: to
  answer the same research question) as someone else did already.
  Typically, this is done by different researchers than the ones that
  came up with the result in the first place. If researchers replicate
  their own work, this is called a self-replication.

- A replication is related to but different from a **reproduction** of
  someone's work (which we will discuss in more detail in Section
  \@sec-reproducibility). This involves someone else running the same
  analyses on the **already collected data** (i.e., the same data; with
  code either self-written or provided by the original researchers, or
  something in between).

\^ Not that this is the terminology I will stick to in these notes, but
keep in mind that conventions differ across fields, disciplines, time,
researchers and vibes. For example, when in 2105 200 researchers
(inlcuding myself) replicated 100 studies, they collectively thought
they were [Estimating the reproducibility of psychological science
[[https://www.science.org/doi/10.1126/science.aac4716]{.underline}](https://www.science.org/doi/10.1126/science.aac4716)]{.mark}

\^ Another terminological confusion relates to the sentence "Study X has
been replicated". Typically, it just means that someone has tried to do
the study again. It doesn't say anything about the results that someone
has found. When that someone found the same results (by whatever
criterion; see Section XXX), you would read "Study X was successfully
replicated", and if the results were different, you would read "Study X
failed to replicate". Somehow, i would interpret "Study X has been
reproduced" as "Study X has been successfully reproduced" but it might
be just me.

\^ So, basically, when you do a replication, you will be doing an
earlier study again. Let\'s introduce some more terminology. The study
you will do again aka replicate will be referred to as *the original
study (OS)*, and its authors as, wait for it, *the original authors
(OAs)*. I have tried to suppress my gangsta desire to use O.G. study and
O.G. authors, but I can\'t promise I\'ve always succeeded.

# The same? {#thesame}

xxx a bit like correcting bugs vs adding features in software
development

\^ While the idea of *doing everything the same way the original
authors* *did* seems ideal (at least in terms of deciding what to do),
in practice, it is guaranteed to turn out to be much more muddy. A lot
of work in the definition of a replication is done by the word *same*.
There\'s a lot to say about that. Below, I\'ll try to say a few bits. As
I explain below, 1) it can be very hard if not impossible to do things
the same; 2) it can be hard to judge whether or not you actually do the
same 3) it can be plain stupid to do the same!

## doing the same is impossible or infeasible {#impossible}

\^ First, doing everything the same is sometimes infeasible or even
downright impossible. Even if you would like to do everything the OAs
did exactly again, your study inevitably *will* differ from the original
one!

\^ You, for example, will have different participants in your sample.
The people that participated in the OS are typically untraceable. There
will inevitably be a difference in the sample you use.

\^ What's worse, you might live in a different **place** than the OAs.
So if the OS did not involve click workers and unless you are up for
academic travel, your sample will come from a different place and as a
result may have different characteristics like theirs, in terms of age,
gender, religion, culture, nationality and so on. You might live in a
different country than the OAs of the study you are replicating, where
the inhabitants might have different characteristics (such as
religiosity, level of conservatism, etc). your "general population"
might differ from their "general population". Or the OAs might have
studied the influence of xxx on social media use with students living in
dorms, but your local students population is not living in dorms. So
this means you might be sampling from a different **population**.

\^ As Bawb had told us, times, they are a-changin'. So another
difference you can not avoid unless you are Doc and drive a DeLorean, is
**time**.

\^ A similar reasoning relates to the **context** of the study. Some
studies focus on something that is very context dependent for which the
context is hard to recreate. Take, for example, a study on the mental
health during the March 2020 lockdown in Belgium. It will be hard to
recreate the exact circumstances in Belgium in March 2020. Even if you
are "lucky" to live through another lockdown, and study mental health
again in Belgium, your study will probably not be the same. Each
lockdown is different, in terms of build-up, severity of the disease,
groups of people being most affected, regulations, measures and policies
etc.

\^ Finally, maybe you don't have the same **means** as the OAs, which
could be due to the passage of time, or to the division of wealth, or
just other practical stuff getting in the ways. That makes doing the
same not impossible in general, but at least impossible for you. For
example, you do a study again but, for some technical reason, you use
pictures instead of film clips to invoke trauma. Or the OAs might have
collected their data over summer, but the practicalities of your data
collection makes it impossible for you to do so and you will have you do
your data collection during winter.

\^ There's a sadder reason than geography and physics why doing things
exactly the same might be impossible. These reasons are psychology and
sociology. It is often surprisingly hard to find out exactly what the
OAs did in all its glory **details**, as they tend to under-report what
exactly they did. Often, authors keep their readers in the dark about
lots of stuff, both big and small. Things have gotten slightly better
recently, but no one is adding this info retroactively to their
imprecisely reported studies! And of course, if you don't know what the
OAs did, how can you do it again? Do you want an example? I have more
than you wished for!

- If the OAs included a subscale of measure D in their analyses, did
  they only present the relevant items to the participants, or did they
  present the full set of items and only analysed the data for the
  subscale?

- When doing an independent samples t-test, did the OAs use the Student
  version (assuming equal variances) of the Welch version (not assuming
  equal variances)? When doing a Pearson's Chi-squared test, did they
  use a continuity correction or not? Which type of ANOVA (I, II or III)
  was done?

- How were missing data treated? How were outliers treated? How were
  they defined?

- Which exact inclusion or exclusion criteria did the OA use?

- What were the exact test instructions?

- Did the model include an interaction? Which estimator was being used?

- The OAs know, but they won't tell you! Or more likely, they won't
  know. They won't tell you and you will need to guess! TODO add more
  examples from Artner et al. (2021).

- etc

\^ So because authors are often terribly unspecific in their methods
description, it will often be unclear what the OAs did. So the default
"do as they did" doesn't work here. We could ask them, but still, and
shockingly, it often remains unclear! If the OAs were unspecific in
their reporting at the time of their reporting, and they are now
non-communicative when prompted for details or simply don't remember the
details themselves, your glorious road to sameness abruptly ends.

## doing the same is ambiguous {#ambiguous}

\^ The same and the same are not the same. Even if you ignore the
inevitable differences between now and then, and you go full Nancy Drew
and you do find out exactly what the OAs have been doing, it is often
simply unclear what *doing the same* exactly means. This has to do with
the fact that "the same" can have two different meanings: you can either
make the same *choice* as the OAs made, or you can follow the same
*decision* *strategy* as the OAs did. Those both routes do not
necessarily lead to the identical steps! Here are some examples I
encountered when doing replications, just to give you a feel:

- The OAs make weird choices in data collection without justification,
  such as rewording items or instructions compared to the "official"
  source, or add an item of their own making, or inexplicably dropped an
  item. Do you make the same weird choice or do you follow the same
  strategy of assessing construct X with tool Y and thus follow the
  manual?

- Back in the 80s, the OAs paid their participants \$20 for a short
  task, which was quite a sizeable sum at the time. Do you make the same
  choice and pay the same amount (in your local currency) or do you
  follow the same strategy and pay "a lot" too (whatever that currently
  means) and xxx incentives remuneration if the effect depends on it, it
  should be equally high. moet lager. dit is over dat het een verschil
  kan zijn. en dat het mss chice vs stratey xxx

- The OAs make weird choices in data processing without proper
  justification, such not including the answer to a specific item when
  constructing the sum score, contrary to what the manual for the
  questionnaire tells prescribes. Do you make the same weird choice or
  do you follow the same strategy of assessing construct X with tool Y
  and thus follow the manual?

- The OAs report that, at the time of the OS, there was a better (in
  whatever sense) version of the questionnaire than the one they used,
  but the OAs didn't include the superior version because it was too
  long and the OS was part of a larger data collection which couldn't
  afford to include the long version. If time is not such an issue for
  your study, do you use the short, inferior version or the long
  superior version?

- The OAs include a measure C in their data collection, but do not
  report the analyses about C, citing low reliability in their sample as
  the reason. Should you make the same choice and also not include C in
  your data analysis, and hence not even in your collection? Or should
  you follow the same strategy, and include it in the data collection
  and inspect its reliability? And what should you do if you include it
  but reliability is high?

- The OAs remove an item from their scale because doing so increases the
  Cronbach's alpha. Do you make the same choice and remove the item as
  well, or do you follow the same strategy, and only remove it when
  doing so increases alpha? And what if the gain when an item was
  deleted was high in the OS (say, from .49 to .77) but small in yours
  (from .63 to .65)?

- The OAs combine two subscales into a total score because of the high
  correlation between them. In your study, correlation is low. Do you
  combine (same choice) or not (same strategy). And what exactly counts
  as high?

- The OAs split their sample in a high and a low group using a mean
  split. Do you use their mean (same choice) or your mean (same
  strategy)?

- The OAs use two measures, each of which are a subscale, with the
  scores on each subscale being determined using a factor analysis. Do
  you use the scale structure as revealed by the OA factor analysis
  (same choice) or rather the scale structure as revealed by doing a
  factor analysis on your own data (same strategy)?

- The OAs only include variables as a covariate in their model based on
  a significant correlation with some other variable. Do you include
  only those covariates the OAs included (so you make the same choice as
  the OA did) or do you only include covariates that were significantly
  correlated in your data set (so you follow the same strategy as the OA
  did)?

<!-- -->

- The OAs only include covariates in their model if they have a
  significant correlation with the outcome variable. Do you use the
  exact same covariates as the OAs, regardless of significance (same
  choice), or do you use the same procedure as the OA, meaning you only
  include the variables with a significant correlation in your data
  (same strategy)? TODO merge with previous

<!-- -->

- The OAs derived four clusters of participants, based on their data. Do
  you make the same choice and use the same number of clusters and the
  same cutoff, or do you follow the same strategy and make a possible
  different number of clusters of your own, based on your own data?

- etc

\^ The *the same is not the same as the same* problem is further
amplified by what we tend to celebrate: **scientific progress**. There
is a good chance that since the OS the state of the art about data
collection, data processing and data analysis has changed. Science
progresses, you know. Especially for older papers, it makes sense to use
different materials or analyses altogether.

- Maybe there is now an updated, better version of the stimulus set or
  questionnaire the OAs used. Do you make the same choice and use the
  old version, or the same strategy and use the updated version?

- Maybe there is a new (and possibly better) questionnaire assessing the
  same construct or concept altogether, so not just an updated version
  of the questionnaire the OAs used. Do you make the same choice and use
  the questionnaire used but the OAs (using questionnaire X), or the
  same strategy and use the new questionnaire (assessing construct Y)?
  If the OAs measured depression with questionnaire A, but now, years
  later, questionnaire B for measuring depression turns out to be better
  in some sense, is using A the same (using the same choice of
  questionnaire) or is using B the same (using the same strategy of
  assessing the depression using a questionnaire)? TODO merge with
  previous

- Maybe the OAs did an analysis which is ok but could be improved upon,
  either because you just had a better education, or new tools have been
  developed since the OS. Do you stick to the ok analyses (making the
  same choices) or do you go for the new and improved ones (following
  the same strategy of testing the hypotheses using appropriate tools)?
  TODO add example

\^ Another reason why *doing the same* can be ambiguous is that there is
sometimes, embarrassingly, more of the same. Some OAs underreport,
others overreport.

- The OAs report in their paper a few examples items of their survey.
  They also shared their study materials with the world. Great! But what
  if the reported items are not identical to the shared items? Which
  ones should you use if you want to do the same?

- The OAs report in their paper using a Welch t-test. They also shared
  their code with the world. That's awfully nice! But what if the code
  shows they used a Student t-test, and you don't have the raw data to
  check which version they actually uses? Which version should you use
  if you want to do the same?

\^ To be clear, I don't have the answers to these questions raised when
discussing ambiguity. Sometimes the answer will be: do several things,
all of which implement the idea of *the same* to some extent. But these
are things that you will come across and will need to make decisions
about. So often, it might be interesting to do the main analyses several
times (see also Section \@sec-designanalysis).

## doing the same is not ideal or undesired {#undesired}

\^ The previous examples focused on cases where something better is
available, but the original approach was not terrible. Sometimes,
however, scientific **progress** is so clear that doing the same as in
making the same choice is simply undesired. Which is what I discuss
next. In these cases, doing exactly the same as the OAs is perfectly
possible, but doing so would actually be bad form! xxx

\^ You might have decided to use a different population, such as
nationality (which, as per above, might or might not mean you are still
doing a replication). Clearly, replicating an OS which was done in
Portugal with Portuguese materials with your Dutch speaking participants
will give you a very high score on sameness, but would be a very bad
idea. This means that you might need to do things in a different
language than the OAs, which means you will have to find translated
materials or possibly do the translation yourself.

\^ xxx A final instantation of the ambiguity of *same* is a result of
the OS (probably) being set in a different time and place. In some
situations, there is again the option of using the literal original
material (same choice) or you might need to "translate" the study to a
current, local context (same strategy).

Even is the measure is perfectly fine, you might still not be off the
hook. In some situations, you might need to "translate" the study to a
current, local context

- Say you want to assess interests in sports in general and use a
  Flemish population. The OAs did their study in the 80s in the US. If
  the OS used a dropdown menu with popular sports and asked the
  participants to select which they like (to assess interests in sports
  in general), that list might represent popular US sports in the 80s.
  You might want to use popular sports in current-day Flanders!

- One of my students attempted to replicate a study from 1999 on the
  relationship between attachment styles and parasocial behavior. To
  assess parasocial behavior, the OAs made use of a questionnaire
  published in 1992 with items like "I think my favorite TV personality
  is like an old friend". To a 2023 audience, this sentence probably
  reads like a question about your favourite gladiator, so the outdated
  term "TV personality" should be updated to current day celebrities and
  media personalities like influencers.

\^ These sorts of problems call for the use of positive or negative
controls, or piloting.

\^ Also, there is a non-negligible chance that the OAs did something
wrong or stupid (I should watch my language. Maybe I should go and read
Section \@sec-writing) when designing their study and analyzing their
data so the OS suffers from serious methodologcal shortcomings. After
all, they are human too!

- The OAs might have overlooked a confound.

- The OAs might have not used an appropriate measure

- The OAs did not include an important control variable they really
  should have

- The measures used by the OAs could, for example, be of questionable
  psychometric quality (such a reliability of validity)

- They could not correspond to the construct of interest

- They could not be appropriate for the population under study

- TODO: add example birthe

- In Sections \@sec-reproducibility and \@sec-checkingquality, I list
  some common statistical fallacies and mistakes, but obviously the
  catalogue is much larger.

If this happened, it would be unwise to make the same mistake,
especially if a better option is available. *They* may have done stupid
things that are deeply flawed, but *you* are not making these **errors**
that again.

\^ But even when the OAs didn't do something wrong or stupid, there is
no reason to just relax. Remember how I told you science progresses? I
still stand behind that statement! Maybe, and more generously, what they
did made perfect sense at the time of their study, but now we realize
they were flawed.Not because what they did was good, you shouldn't aim
for better. Don't let the good be the enemy of the better! So even if
their design, materials, and analysis was appropriate, you migh want to
look further so that your study reflects current best practices. For
example, TODO: add example.

- For example, maybe the OS was done in a time where attention and

> manipulation checks weren't customary. This does not mean your study
> should not include some (there are reasons, though, to not include it
> xxx)

- There are better stimuli, questionnaires, tools, techniques and
  statistical approaches available now.

## doing the same is not your current interest {#nointerest}

\^ Everybody is unique and, somewhat contradicting to that claim, you
are no exception to that. So you might have slightly different interests
than the OAs. Sometimes, you don't want to do the same, because you are
interested in something different than the OAs. Or, you might feel
forced, by whatever academic pressure, to not "just" do a replication
study because that is taken to mean by some people you have a boring,
uncreative, nasty and kleptomanic personality. So maybe in your study,
you *want* things to be different. As per above, the difference might be
relevant enough to no longer count as a replication study.

\^ You might be interested in a different population. You could end up
doing a study again (with the same research questions, materials,
experimental design and analytic plan) but in a different population
(e.g., with Europeans or Belgians instead of with Americans; or with
golf players instead of with soccer players; and so on) or in a
different field (e.g., in math education instead of in language
education xxx; visual memory to auditory memory; from face-to-face
impressions to online impressions xxx).

- The OAs investigated the mental health among professional soccer
  players and made their conclusion about soccer players (and not about
  sportsmen in general). You, on the other hand, might be interested to
  do the same study again with professional golf players and your
  conclusion will be about golfers (and not about sportsmen in general).
  That's not replicating, despite doing most of the things exactly the
  same. xxx

- The OAs investigated the impact of various types of sex education in
  Portugal. You might be very interested in doing the same study in
  Belgium. Since at least the formal sex education in Portugal is
  organised differently than in Belgium, if you do the study again in
  Belgium, that's not replicating, despite doing most of the things
  exactly the same. xxx

- The OAs studied young adults and found a relationship between social
  media use and loneliness. You do the same study again but in a general
  population or an elderly population or with kids. This might no longer
  count as a replication, depending on the extent to which the OAs
  stressed that their conclusion is limited to young adults. xxx

\^ Of course, changing the population of interest might mean you need to
change other stuff. A survey targeted at soccer players most likely
contains slightly different items than at golf players; doing a study
with kids that invoked trauma using film clips should probably use
different film clips to invoke trauma if it involves adults; etc

\^ You might be interested in a different approach: Does xxx only work
with film clips or also with text xxx? Or does the crowd within effect
gets bigger when the delay is longer?

\^ Maybe you want your study to be more informative than theirs. For
example, you might want to include additional factors or variables that
the OAs did not consider.

- For example, if the OA [showed that self-compassion significantly
  predicted changes in depression symptoms, you might want to test that
  relation again using the same materials, procedure, and analyses, but
  additionally want to include stress as an additional predictor. In
  your analyses, however, you could also just do the original analysis
  with just self-compassion as a predictor. If you do so, your study
  will both be a replication and an extension. xxx]{.mark}

## ok, i get it. can we wrap up, please?

\^ So say you do a replication and the OAs were kind enough to share all
their study materials and all their analysis code. This might sound like
you have hit the replication jackpot! Your first instinct might be to
just use all of that and call it a day. After all, the point is to do
the same as what they did, right? I hope to have shown you that this is
not always the best course of action, and that there might be reasons to
do things differently.

- You might want to go and look for the "official" version of the
  stimulus set, survey or questionnaire (because the OAs might have
  deviated from this version, for no good or no justified reason).

- You might want to look for different existing materials than the
  materials shared by the OAs (because there might be better materials
  available by now, or they were constrained by practical reasons for
  using a lesser version and you are not).

- You still might need to create your own materials (because their
  materials might be sub par or you might not have the machines or
  expertise to use it or you need to translate it or adapt it to current
  place and time and population).

- You might still want to think for yourself about a good research
  design (because there might be a confound in theirs).

- You still might wish to write your own code (because the OAs might
  have made a mistake in theirs or might not have used the best analysis
  available).

So much for "just doing the same". So while in an ideal world, you can
simply do *everything just like the original authors did*, I hope to
have warned you by now that often, it won't be that simple.

\^ Also, note that there are many aspects to a study. Your study might
be the exact same in the materials used, but not in the design. Or you
might test the same hypothesis, but using different analyses. All this
leads to a vast array of types of replications. But these fine grained
distinctions are not only hard to make but also relatively
uninteresting. The most important take-away is 1) that you should not
panic if you can't do things the same 2) that doing the same is not
always a good, let alone the best, idea

\^ Since we are on the topic of warnings, here's another warning you
didn't know you needed. As HRSS writes, "Ideally, being replicated would
be an honor for authors since other researchers deem their findings
important but a failed replication could potentially harm the reputation
of the original and increase distrust towards them among their peers".
So while you think you are doing a service to science, not everybody
will agree. Some people might consider you a nagging, rude, wasteful
creature lacking any creativity. There's not much that can be done about
it, but it's good to keep that in the back of your mind.

# Are we replicating still? {#still}

\^ So, as per above, there are many reasons why you would end up not
doing the same as the OAs. Does this mean you will never ever be able to
do a replication study? Well, here is where things get a bit weird.
Despite things not being exactly the same in your study, it could still
be same enough to count as a replication study. The prerequisite is that
the differences that exist between your study and the OS should not
influence the result.

\^ Basically, what you need to ask yourself is: Do I try to answer the
same question as the OA? Or, put differently, imagine you have an answer
to your question, will this answer speak to, positively or negatively,
the conclusion of the OS?

\^ Well, that's a relief. But how do you know whether these differences
will influence the result? Simple, you don't! Ideally the OAs have
included a Constraint on Generality (CoG) statement, and clearly
indicated whether their result is, for example, only expected to hold in
Catholic countries (and not in Islamic ones) and with verbal stimuli
(and not with text stimuli). Alternatively or additionally, their work
might be informed by a theory which delineates those boundaries. Often,
however, there is neither a CoG nor clear theory, so you should go by
your own reasoning and gut feeling. With a bit of luck read the title,
abstract and conclusion of the OS very carefully should reveal what
*they* find important. Barring all that, you will need to rely on your
one judgement.

\^ The guiding principle is as follows: If (as dictated by a CoG, a
theory or a conclusion) the claim you can (potentially) make based on
your study is different than the conclusion from the OS, or, put
differently, if your result has the potential to speak against the
result of the OS, the difference between your study and the OS is
important and your study no longer counts as a replication. If finding a
different conclusion than the OS would speak (badly) to the OS, you are
doing a replication. If finding a different result would not say
anything at all about the correctness, truthfulness, trustworthiness,
veracity or another fancy word you are not doing a replication but
something else.

\^ Let's look at some examples

\^ You might also be sampling from a different **population**. The
question is whether this difference is relevant, for which you can,
ideally, consult CoG, theory, or whatever the OA concluded.

- For some studies (say, Stroop), you don't expect population or
  nationality to matter. So if, say, the original participants come from
  the US and you intend to collect a Belgian sample, you are still doing
  a replication study.

- For other studies, population or nationality might be an important
  aspect of the original study. For example, with a study on attitudes
  towards controversial ethical topics, you might expect to find a
  different result in the US compared to Belgium. If you do the same US
  study in a new, say, Belgian, sample, you are no longer doing a
  replication study. xxx or with students in dorms only xxx liesl

- A study that investigated the relationship between religiosity and
  fertility status, and sampled participants in a predominantly Catholic
  population might conclude that "[women become more religious when
  ovulating]{.mark}" or it might conclude that "[women become more
  religious when ovulating]{.mark} among Catholics". If you do the study
  again in a mostly Islamic population, it will be a replication with
  the former but it will not be a replication with the latter
  conclusion. The reason is that if you find no evidence for a relation
  between religiosity and ovulation in your sample, you would question
  the first conclusion but not the second conclusion of the OS.

\^ If the conclusion contains (or should contain!) a limiting statement
like "among US university students living in dorms", and you do the same
study again at home which is not the US, your study no longer counts as
a replication. Instead, you are doing an **extension** study or a
**generalizability** study.

\^ So if the conclusion is crucially dependent on a population you don't
have reasonable access to, doing a replication might be infeasible at
best and impossible at worst. Even if you live in Belgium and it is
important that your population consists of US students in dorms or women
in Islamic country, it is possible to travel, it is probably not so
efficient way of spending time and money.

\^ What about **time**? Again, whether or not that difference is
important depends. Replication studies make the tacit assumption that
the world we study is relatively stable. If you do a study again in a
new time period where things might have reasonably changed, it is no
longer a replication study. Again, the trick is to look at the CoG, the
underlying theory (if any), or to carefully read the conclusion. While
you would hope that the population, if important, will be part of the
conclusion (e.g. "among young religious women"), time restrictions are
seldom made explicit in a conclusion, even if it is clear that the OAs
are just taking a snapshot of a state of affairs. Some conclusions are,
by design, time specific, even if they are not explicitly specified as
such.

- When Stroop (1935) TODO add ref concluded that "the interference of
  conflicting word stimuli upon the time for naming 100 colors \...
  caused an increase of \... the normal time for naming colors", he did
  not just forget to add "in 1935" to this conclusion. The reason he
  didn't add it to his conclusion was because he assumed that the Stroop
  effect in the near future should not be different than when it was
  originally tested in 1935. Since the original conclusion did not have
  nor need "in 1935", doing the study again today would count as a
  replication.

- In 2015, we replicated a study done by Wicherts et al. in 2006 TODO
  add ref, who studied the willingness of researchers to share their
  data and found a rather low willingness. Our study TODO add ref was
  done roughly 10 years after the original one, and I was hoping that we
  would *not* find the same result, but that the sharing rate has
  increased since the OS. The fact that we found a higher sharing rate
  does not invalidate the conclusion of the OS at all! Rather, it just
  means that things are different at the time of our study than at the
  time of the OS. That is because although the conclusion of the OS was
  "that 73% of the authors did not share their data", tacitly, the
  conclusion was "that 73% of the authors did not share their data *in
  2016*". Our study had no capacity to change that original conclusion,
  so our study was not a replication study.

\^ If you reasonably think the conclusion should be augmented with "in
1999", and you do the same study again at a (inevitably) later time,
your study again no longer counts as a replication. It is more useful to
think of the study as a **follow-up** study rather than as a replication
study.

\^ As explained above, some studies focus on something that is very
context dependent for which the **context** is hard to recreate.

- Take, for example, a study on the mental health during the March 2020
  lockdown in Belgium. It will be hard to recreate the exact
  circumstances in Belgium in March 2020. Even if you are "lucky" to
  live through another lockdown, and study mental health again in
  Belgium, your study will probably not be a replication. Each lockdown
  is different, in terms of build-up, severity of the disease, groups of
  people being most affected, regulations, measures and policies etc. If
  you are interested in doing this study again, you are probably doing a
  follow-up or an extension study or a generalization study.

\^ So when population, time and context are an important aspect of the
study (and you don't have access to the original population because of,
for example, geography), it might be impossible (for you) to do a
replication study.

\^ What if you can't use the same equipment as the OAs? Again, whether
your study is a replication or or not depends again on the same
reasoning as discussed above.

- If you do a study again but, for some technical reason, you use
  pictures instead of film clips to invoke trauma, and 1) the conclusion
  of the OAs did not mention film clips and 2) the theoretical framework
  used by the OAs does not mention film clips, your study still counts
  as a replication (provided that you can show that the pictures did
  invoke trauma).

- If, on the other hand, the OAs have clearly indicated (in their CoG,
  or their conclusion, or by the theory that they use) that their
  finding is restricted to film clips, you are doing not doing a
  replication when you use pictures.

\^ If the conclusion contains (or should contain!) a limiting statement
like "using Tetris (Version 1.2.1; Blue Planet Software, 2007)", and you
do the same study again but you no longer have access to that version of
Tetris, your study no longer counts as a replication but rather is an
**extension** study or a **generalizability** study. If it does not
contain the statement, and you find a version of Tetris with the same
characteristics as Version 1.2.1, you are still doing a replication,
which could be called a **conceptual replication**.

\^ What if the OAs collected data during summer and you do a winter data
collection, this might or might not count as a replication. As HRRS
notes, if your study is on color perception, you are replicating but if
it is about tea preferences, it is not nut rather a xxxx xxx goeie plek
xxx Again, this would depend on COG, theory, writing xxx

\^ Remember that you will often be confronted with the problem of making
the same choice vs following the same strategy? The good news is that,
whatever you do, you will probably be replicating. If you (mostly) make
the same choices, your study is a **direct** or **close** or **exact
replication**. If you follow the same strategy as the OAs, but do not
make the same exact choices, and if the resulting differences are not
expected to be relevant to the conclusion, you are doing a **conceptual
replication** (see LeBel et al. 2018, especially their Figure 1) TODO
add ref. How many differences there should be to jump from a direct to a
conceptual replication (e.g., if the authors forgot to include an item
of a 12 item questionnaire, and you use all 12 items instead of their
11) is a debate I rather not go into, because it doesn't really matter
all that much.

xxx vb van TV personality xxx wat is het als je het niet aanpast? xxx

\^ Correcting stuff also means you can still do a replication, despite
not doing everything the same. If you have in the same sense improved
the original study, you might want to pat yourself on the back and buzz
around that you did a **constructive replication**.

\^ If you do everything the same except e.g. the population (e.g golf
players instead of soccer players), it is reasonable to assume this
change of population might make the results different, your study is no
longer a replication but an extension of generalizability, or might just
end up being a **new study** altogether (which was heavily inspired by
the OS).

\^ Imagine you do everything the same but add a covariate. [In your
analyses, however, you could also just do the original analysis with
just original covariate as a predictor. If you do so, your study will
both be a replication and an extension.]{.mark}

# Some criteria for selecting a replication study {#somecriteria}

\^ As each study result is just a single data point for a future
meta-analysis, every study is worthy of replication. Further, even if
there would be absolutely no scientific benefit of doing a replication
(for example, because there has already been a significant amount of
replication studies, or the finding is clearly bogus), you will
hopefully learn a thing or two while doing a replication. That means
that basically any study serves as a good candidate study for
replication, especially for a student project.

\^ That being said, some studies are better candidates for replication
than others. In this section, I list some criteria for choosing useful
candidate studies.

\^ Don't let this list confuse you: a good replication study does *not*
need to meet *all* of these criteria. These are just some things to keep
in mind when searching for good candidate studies to replicate. Hell,
sometimes these criteria might even *contradict* each other: high impact
studies are in need of replication, and studies with limited evidence
are in need of replication as well. But high impact studies (hopefully)
are high in evidentiary values, so there's that.

\^ All these criteria aside, you should make sure to choose something
that interests *you*. What would you like to tell your family, friends,
dates, and cats when they ask you what you are doing research about?

\^ While not strictly necessary, it is advised to find something that
has been published in a decent scientific journal. In general,
preprints, white papers, master theses, internal reports, and so on are
typically not good candidates. Also, try to avoid papers published in
journals that feature on [[Beall\'s List -- of Potential Predatory
Journals and Publishers]{.underline}](https://beallslist.net/). It might
also be good to check whether it is retracted. Ideally, this should be
clear from the online version, but it might be wise to double check in
the retraction watch database [[Retraction Watch
Database]{.underline}](https://retractiondatabase.org/RetractionSearch.aspx?).
Whether or not a retracted study is worthy of replication depends on the
reason for retraction. If it was retracted because of plagiarism, it
might still make for a good replication candidate.

## feasibility{#feasibility}

\^ Obviously, if you want to do a replication it should of course be
something that is possible to do a replication study on.

- As explained above, some effects are very contextual and
  time-dependent. Doing this kind of studies again probably means you
  are not doing a replication study, but rather a follow-up or extension
  study instead (see above).

- Further, as per above, some studies might be impossible to replicate
  because it is too unclear from the report what the OAs did

\^ The study should of course be feasible within the context of your
research (such as a master thesis)

\^ in terms of experimental setup and design: e.g., eye-tracking
requires a lot of technical expertise and longitudinal studies a lot of
time, so both are hard to do.

\^ in terms of participant pool: e.g., clinical, developmental,
cross-cultural samples are harder to collect than general population
samples. Per above (Section XXX), the nationality of the participants in
the OS might or might not be a feasibility concern, depending on whether
the nationality of the participants in the sample of the OS was a
crucial aspect in the study and its conclusion (and on whether you
really want to do a replication and not an extension).

> \^ in terms of sample size: as your replication study is ideally
> informative, you will probably need a large sample size to reach
> either high power or high precision. This is either easy (if you are
> interested in a general population and your study involves a short,
> simple, survey) or hard (e.g., children from a single parent diagnosed
> with ADHD) to come by.
>
> \^ in terms of expertise and available technical equipment. e.g.,
> don't start just doing an MRI study if you don't know how and don't
> have the machines. Really.
>
> \^ in terms of time. like, obvi.

## questionability{#questionability}

\^ The result of the OS is uncertain, questionable or controversial

> \^ studies with low evidentiary value/strength of evidence/degree of
> evience/for which there is limited evidence xxx are more in need of
> replication than others

\^ replicating the Stroop effect is (by now) a waste of time from a
scientific point of view (though could be fun and a good learning
experience) given there is solid evidence for it.

> \^ here are a few red flags pointing to low evidentiary value: it
> hasn't been (succesfully) replicated before; it contradicts other
> findings; it is based on a small sample size; it includes post-hoc
> sub-group analyses; the OAs have a COI (see also Part C in general and
> Section \@sec-checkingquality in particular); etc

\^ However, they shouldn't be too questionable either!

> \^ something that is scientifically and methodologically valid, is
> well designed and correctly reported (reproducibility; see below)

\^ it's a waste of time to redo a bad experiment or to try to redo a
study for which the effect was a clear fluke

\^ it will impair publication chances. even the best replication of a
bad study will have a hard time to get published

\^ unless, of course, you fix all of this and you do a constructive
replication (see Section \@sec-areplication). If you can think you can
improve the flaws (e.g., using better measures, doing better analyses,
removing confounds etc), you can use a bad study as an inspiration (but
it might no longer be a replication study).

> \^ but still, whether it is worth doing a constructive
> replicationdepends a bit on the hypothesis. If the hypothesis is
> clearly silly, and the support for the silly hypothesis was based on
> scientific mistakes, just pointing out these mistakes is enough to
> kill the study and a costly replication is not needed. However, if the
> hypothesis is not silly, and the original result was due to a mistake,
> it is worthwhile to do the study again (and fixing the mistake).

## impact{#impact}

\^ The result of the OS is important and has been shown to be impactful,
important, relevant or influential;

\^ is foundational to theory

> \^ is foundational to (clinical) practice or policy
>
> \^ is taught in courses or has made it into textbooks
>
> \^ is published in a prestigious journal (such as *Science*, *Nature*,
> *PNAS*, *Psychological Science*, *Journal of Personality and Social
> Psychology*, etc)
>
> \^ has gained a lot of (international) press coverage
>
> \^ is the topic of a recent dispute
>
> \^ is highly cited
>
> \^ has high online impact (e.g., see altmetric)
>
> \^ has a lot of impact on e.g. policy or in other applied settings
> (e.g. therapy)
>
> \^ etc

## other practical considerations{#other}

\^ At some point, you might need to contact the OAs. If the OS is fairly
recent, the OAs are more likely to be alive or active, which I heard
considerably facilitates communication.

\^ Further, you might want to choose a study that has open data. This
will be useful for many reasons, such as checking reproducibility (see
Section \@sec-reproducibility), for testing your own analyses, and for
doing a power analysis (see Section \@sec-desingingstudy).

\^ If the OS has open materials (i.e., stimuli, survey items, etc), part
of the *doing the same* problem is solved (or can be, at least, per the
caveats of Section \@sec-areplication).

\^ However, both these criteria go both ways. If the OS meets these
criteria, it will make your life as a replicator easy, or at least
easier. On the other hand, from a broader, field-wide perspective,
replications are more useful and informative when the above criteria
have *not* been met. For example, if a study does not have open
material, you will need to find or create your own, which sucks, but the
net result is that, if you then share the materials with the world,
there are now open materials for the study. It is up to you if you want
to take one for Team Science or not.

#  

# Finding information about published research {#findinginformation}

\^ A large part of doing a replication study involves finding resources
about the study you decided to replicate.

\^ The first thing you need to find if you want to replicate a study is
of course the paper describing the research process and results. Your
first go-to for finding a paper will be google, google scholar, and your
university (online) library. If you can't find the pdf of a paper in the
online library, and if you want to avoid illegal sites, take extra care
to avoid sci-hub, because you will find a lot of illegal papers there
and who would want that?

\^ Now that you have the paper, you would hope that you now have access
to all the information about the OS, such as info about the experimental
procedure, the exact research materials (e.g., stimuli, questionnaires)
used, the data processing steps, etc. I am sorry to have to crush your
hopes. As you will soon see, academic reporting is shockingly and
embarrassingly bad, scattered and incomplete. Sadly, not all information
about a study is neatly contained in the published paper. *If* the info
you need is even reported (and you should consider yourself lucky if
that is the case!), it will most likely be scattered around the academic
universe.

\^ Here is a non-exhaustive traveler's guide to places where you might
or might not find the info you are looking for. Note that not all these
associated resources are available for all papers. In these spots, you
might find code shared by the original authors, their preregistration
protocol, their research materials, their data, results of any
additional analyses, etc

- the appendix of the paper

- the supporting information/supplemental materials of the paper (often
  found with the electronic version of the paper, such as
  [[https://journals.sagepub.com/doi/10.1111/j.1467-9280.2008.02136.x]{.underline}](https://journals.sagepub.com/doi/10.1111/j.1467-9280.2008.02136.x))

- the journal's website

- ideally (but very seldomly), the authors share (part of) their
  materials, data, etc on a third-party platform or repository.

  - for example, the open science framework, osf.io. osf.io is one of
    the many platforms that researchers use to share e.g., data,
    materials etc. if there is an associated osf project page, there
    will be a link in the paper if there is an associated osf project
    page. keep an eye out for in paper osf.io links, such as
    [[https://osf.io/ivfu6/]{.underline}](https://osf.io/ivfu6/).

  - keep in mind that there are many others (e.g., figshare; zenodo). so
    read the paper carefully looking for clues

  - github/gitlab accounts of the OAs

- the personal websites of the OAs or the websites of their research
  groups or labs

- some studies come with a pre-registration plan, which might provide
  additional cues. If they do, it will most likely be advertised in the
  paper, with a link to a [[osf.io]{.underline}](http://osf.io) project
  or [[aspredicted.org]{.underline}](http://aspredicted.org) project.

\^ In some cases, the same data set is used in several papers by the
same authors. You would think that the description of the study would be
the same in both papers, but you should stop thinking really. You might
hope (you can still hope!) that when this happens, the authors would
just copy their earlier text when reusing it, but there is surprisingly
little cross-paper-consistency, and if your OS is lacking in detail, you
might get lucky that another paper using the same data set is a bit more
loose-lipped in exactly how the data were collected and processed.

\^ Of course, when seaching for these additional sources, google is your
friend (though evil). Be creative!

\^ A last resort for finding info about the OA is asking them. You
should thread lightly though, which is why there is a full section for
that (see Section \@sec-contacting).

\^ Fully understanding how the study was performed probably involves
piecing together several sources of information. For example, the OAs
might not have mentioned in the paper they deleted cases with missing
data, so you only realize that when you inspect their code; or the OAs
might not have mentioned anything about attention checks in the paper,
and only by inspecting the raw data, you find out that they included 3
attention check items. Since sources are scattered, I advise to keep
track of all details of the original study in a separate document and to
add the source for each aspect you are discussing.

#  

# Contacting the original authors {#contacting}

\^ Sometimes, it will prove necessary or helpful to contact the authors
of the original study. Here's the why, what, who, when and how.

\^ Why? There are several reasons.

- You might need access to their materials (which they might or might
  not want to share with you), their data (which they might or might not
  want to share with you), more detailed information about the exact
  experimental procedure, clarifications about the data analytical
  choices made, and so on.

- If you write a preregistration, you might want to ask their comments
  and feedback on your plan before you start collecting the data.

- You might even want to consider including them in your study, possibly
  as an adversarial collaboration.

- When all is said and done, probably more can be said. You might wish
  to share your results with the OAs once you did your study and ask for
  their comments and feedback on the results.

- Or you just want to feel less alone and want to talk to somebody who
  actually cares about the topic you are studying!

\^ What? It is extremely impolite to ask the OAs (or anybody else, for
that matter) to do your work for you. Be respectful of their time and
only ask their input for stuff you can not do yourself and their input
is strictly needed.

- Here are some examples of unreasonable questions because you typically
  should be able to answer these yourself without asking their input

<!-- -->

- Where can I find the survey you used? (when they are commonly used and
  publicly available surveys)

- Which analyses did you do? (when they are described in full detail in
  the paper)

- Can you send me your data? (when they clearly say in the paper where
  their data are publicly available)

> \- Here are some examples of reasonable questions, assuming that you
> did your very best to find the answers yourself by carefully sifting
> through the paper, the supplementary materials, the shared code, the
> osf project page etc, and did not find the answer

- Which effect size did you use in your power calculations?

- I found a version of the survey that seems better than the one you
  used, for these and these reasons (see attached). It was already
  available when you did your study. You don't mention it in your study.
  Did you consider using this version, and do you remember the reasons
  you decided against it?

- You mention that you collected data from 187 participants, but the
  reported degrees of freedom seem consistent with 164 participants.
  Does that mean you have excluded participants? If so, do you remember
  on which criteria these exclusions were based?

- etc

\^ Who? The best person to contact is the corresponding author. If the
corresponding author does not seem to be very good at corresponding, the
next step is to contact the first or the last author.

\^ When? As the questions you want to ask the OAs will probably show up
gradually, and it is impolite to just send an email any time something
pops up, it is probably a good idea to collect all the questions you
have and send them all in one (or a few) giant batch(es).

\^ How? Here are some examples for initial contact with the OAs. Of
course, you should turn it into your own! But some phrases might apply
and could be literally copied:
[[https://docs.google.com/document/d/11in0iAUqy3_RpGn2tndMpTCBD2oD0ZQOHYAHf1UFmQI/edit?usp=sharing]{.underline}](https://docs.google.com/document/d/11in0iAUqy3_RpGn2tndMpTCBD2oD0ZQOHYAHf1UFmQI/edit?usp=sharing)

\^ How? ACRE has a full chapter on guidance for constructive
communication:
[[https://bitss.github.io/ACRE/comunications.html]{.underline}](https://bitss.github.io/ACRE/comunications.html)

\^ More? An overview of relevant literature on the effect of the
involvement of OAs can be found in Section 6.4.1 of HRRS

#  

C. EVALUATING

# CRITICALLY EVALUATING THE ORIGINAL STUDY {#evaluating}

\^ After finding the study and all that comes with it, the next step is
to critically evaluate or appraise it. Your observations during these
activities might help you design your replication study. There are many
angles to it, and they will be discussed separately in the next 5 xxx
sections. Only the last section requires access to the raw data.

\^ Humans, including researchers, are fallible and prone to biases. As a
corollary of this thesis, there is a good chance there is something
wrong with the study, despite it being peer reviewed. Before you start
on your own study, it's advised to have a deep look at the original
study first. This will not only help to correctly interpret the results
from the original study, but will also help doing your own study well.

xxx iets over the quality xxx correctness of the original report xxx.
maar daar valt alternative analysis niet onder xxx

\^ For example, in one replication study I participated in, we wanted to
test the crowd-within effect (more on this in Section XXX), a study
which garnered almost 500 citations (now; I can't remember the citation
count at the time of our replication study). The OAs are very rigorous,
well-educated, experienced and well-respected researchers. During the
process of our replication, it turned out that they had a mistake in
their analyses (which did not affect their conclusion). Shockingly,
their main analysis was nothing but a simple t-test! Similarly, I will
discuss an example soon (see Section XXX) of another replication I was
involved in where we did exactly that, and messed up a t-test by somehow
mixing two variants of it (it did not affect our conclusion). So if even
well-meaning, rigorous researchers (to be clear, I am referring to the
first example here) can bottle an ordinary t-test, you don't need a lot
of fantasy to imagine what lesser educated and lesser well meaning
researchers make of less basic stuff like complicated cross-lagged panel
hierarchical stepwise moderation analyses.

\^ I tend to fall asleep during podcasts, so I didn't listen to them
yet, but these podcasts are at least on topic and maybe even
interesting:
[[https://www.podbean.com/ep/pb-ref7x-16ae964]{.underline}](https://www.podbean.com/ep/pb-ref7x-16ae964)
and
[[https://everythinghertz.com/110]{.underline}](https://everythinghertz.com/110).

# POST PUBLICATION AND OTHER DISCUSSIONS {#postpublication}

\^ Some people might have done some of the evaluative work you are about
to do. They might even have shared their findings. So one part of the
critical examination involves reading up about what other people have
been saying about it.

\^ Sometimes, the reviews of the paper are available (but keep in mind
that they will be about an earlier version of the paper, not the one you
are currently looking at). If these are available, they will most likely
be found with the electronic version of the paper.

\^ What is absolutely crucial is that you look for other replication
efforts of the same effect or finding. You need to find all studies that
attempt to replicate your original study. Don't panic, though, since
typically, there will be none. The FORRT Replication Database
[[https://forrt-replications.shinyapps.io/fred_explorer/]{.underline}](https://forrt-replications.shinyapps.io/fred_explorer/)
TODO add, which is the successor of now deprecated
[[https://curatescience.org/]{.underline}](https://curatescience.org/)
TODO add ref Lebel et al. (2018), might be helpful in this regard, but
if you don't find anything there, it does not mean there have been no
replication attempts. In the somewhat distant future, you should be able
to find a lot of replication studies in the newly founded Replication
Research
[[replicationresearch.org]{.underline}](http://replicationresearch.org).
Other journals that are dedicated to publishing replications can be
found in Table 8.2 of HRRS.

\^ Another source are post publication discussions, which includes
(published) comments, criticisms, reviews, and extensions of the OS.

\^ The recently founded Journal of Robustness Reports
[[https://scipost.org/JRobustRep]{.underline}](https://scipost.org/JRobustRep)
published robustness analyses (see Section \@sec-alternative) of paper,
and you might get lucky and find one about your OS there. Other journals
that are dedicated to publishing reproductions can be found in Table 8.2
of HRRS.

\^ However, not all academic post publication discussions come in
papers! Lots of interesting discussions take place on blog posts and on
social media. Or you can have a look on the many platforms that allow
post or prepublication review and comment, such as
[[pubpeer.com]{.underline}](http://pubpeer.com). So it is probably a
good idea to check whether your OS has received some comments on those
platforms.

\^ Another useful platform with possible post publication discussion
about your OS, brought to you by the people who brought you ACRE:
[[socialsciencereproduction.org]{.underline}](http://socialsciencereproduction.org).
I 100% guarantee I have missed others.

\^ A longer list of platforms used to critically discuss the result,
identify errors, suggest different interpretations, etc. is provided in
Table 1 of [[OSF \| Preprint review services: Disrupting the scholarly
communication
landscape?]{.underline}](https://osf.io/preprints/socarxiv/8c6xm_v3)
TODO add ref

#  

# CHECKING THE REPORTING INTEGRITY OF THE ORIGINAL STUDY {#checkingprereg}

\^ You should not always trust what you read, especially if you are
reading an academic paper. If the OAs shared more than just their paper
(see Section XXX for hunting tips), you could check whether what is
being reported is at least consistent with what else is being shared.

\^ Finding an inconcistenty between the paper and other shared stuff is
not necessarily bad news, but does raise eyebrows. Also, it makes
understanding what the OAs did exactly harder.

\^ The OAs might have shared their study materials. In that case, you
might need to check whether what they shared is consistent with what
they reported! They might report using a 22 item questionnaire, but
sharing 23 items. Or they might report a few examples items, and these
items are not identical to the shared items.

\^ If the OAs shared their code, you might need to check whether what
they shared is consistent with what they reported! They might report
using a Welch t-test, but when you look at the code find that they did a
Student t-test. Or they might not mention the removal of outliers in
their report, but the code shows they did (or at least have a line that
does it).

\^ Maybe the OAs pre-registered their study. There are many reasons why
people would do something different than they said they would do in
their pre-registration plan (see aline xxx TODO add ref xxx). It might
be interesting to see the extent to which they did.

\+ Non-adherence can go in two ways: either authors promised to do
something, but did not do it, or did it differently (outcome switching
would be an important example here); or they did more than they
promised.

\+ For each deviation you encounter, it is important to understand

> 1\) which of the above types the deviation is and what the deviation
> exactly entails
>
> 2\) whether the non-adherence was disclosed (with, e.g., sentences
> like "contrary to what was pre-registered")
>
> 3\) the justification used for the deviations (which can be, and often
> will be "none")
>
> 4\) what is impact of the deviation (i.e., would the result have been
> different without deviating)

\+ This will again turn out to be a very frustrating experience, riddled
with under reporting, under specification, changes in terminology, and
more of that K-pop.

#  

# CHECKING THE QUALITY OF THE ORIGINAL STUDY {#checkingquality}

\^ I hate the word quality in this context but for lack of an
alternative I will keep it here as a placeholder. xxx maybe validity xxx
inferential evidential methodological xxx epistemic integrity

\^ There are many interesting questions you could or maybe should ask to
speak to the quality of a study and its conclusion which are not
necessarily numerical in nature. It is impossible to list them all, but
here are some:

TODO add examples

TODO add more items

TODO map this with same is not ideal/undesired

- If the OAs shared their materials, you want to double check their
  material, as they might have butchered the exact wording of items
  and/or the instructions, or added some of their own, or dropped some,
  or used different scoring instructions than described in the
  "official" manual.

- Do the OAs use a measure of questionable psychometric quality? For
  example, are they reliable?

- Do the measures/scales correspond to the construct of interest? Do the
  measures used (e.g., CES-D) assess the construct of interest (e.g.,
  depression)?

- Are the measures used appropriate for the population under study?

- Do the OAs overlook a confound?

- Do the OAs report a clear stopping rule?

- Is there any protection against exploiting researcher degrees of
  freedom (like preregistration, blind analysis, 21 word solution,
  multiverse analysis, etc)?

- Is the experimental design sufficient (e.g. was there proper
  randomization; was there a control group; etc)

- Can the manipulation realistically work? Is there any evidence it did
  work?

- Have outliers been treated correctly?

- Have missing data been treated correctly?

- Did the processing of the raw to processed data happen correctly (e.g.
  reverse scoring)

- Is the power analysis appropriate, i.e., based on a reasonable and
  justified sample size and using the method/model/test that is
  appropriate for the main result in the paper?

- Is the study high powered for the effect of interest?

- Is there a clear link between the statistical result and the
  scientific result (i.e., the conclusion)?

- Do the OAs overstate their conclusions or oversell their results (in
  terms of population, manipulations, conditions, etc)?

<!-- -->

- Is the statistical model/test appropriate for the data at hand
  (including the measurement level)? Are the model assumptions tested?

- Is the statistical model/test appropriate for the questions at hand?

- Do the OAs fall prey to a **statistical fallacy**? This topic is
  another list of itself, but here are some common statistical
  fallacies: \[TODO maybe move this to an appendix\]

  - "The difference between significant and not-significant is not
    itself significant" fallacy (when authors are finding an effect in
    one group but not in another, they conclude the groups differ
    without having tested whether the groups differ; "a comparison of
    two experimental effects requires a statistical test on their
    difference"; solution: don't compare p-values but compare effects;
    e.g. using interactions)
    [[signif3.dvi]{.underline}](https://sites.stat.columbia.edu/gelman/research/unpublished/signif3.pdf)
    and [[Erroneous analyses of interactions in neuroscience: a problem
    of
    significance]{.underline}](https://www.ejwagenmakers.com/2011/NieuwenhuisEtAl2011.pdf))
    TODO add ref

  - The U-shape fallacy (when authors are testing a curvilinear
    relation; solution: use two lines) TODO add ref
    [[https://urisohn.com/sohn_files/wp/wordpress/wp-content/uploads/2019/01/two-lines-u-shape-published.pdf]{.underline}](https://urisohn.com/sohn_files/wp/wordpress/wp-content/uploads/2019/01/two-lines-u-shape-published.pdf)

  - Treating clustered or nested data (e.g., students in school; or
    repeated measures in a person as independent: solution: use
    multilevel model or repeated measures approaches)

  - Collider bias: Not adjusting for covariates that matter or adjusting
    for covariates that shouldn't be adjusted for (solution: TODO) TODO
    add ref
    [[https://journals.sagepub.com/doi/pdf/10.1177/2515245917745629]{.underline}](https://journals.sagepub.com/doi/pdf/10.1177/2515245917745629)

<!-- -->

- If there are subgroup analyses, do they seem reasonable and justified
  or ad hoc/post hoc (and possibly conceived after analyzing the data)?
  If the OAs perform sub group analyses (e.g., restricting the sample of
  men over 40), are these choices justified or do they seem contrived?

- Is there sufficient justification for important data analytical
  decisions (exclusion, transformation, model building and choice, etc)?

<!-- -->

- All sorts of stuff about validity. TODO expand

<!-- -->

- \...

\^ There are many, many more interesting questions you could ask,
including questions zooming in on the larger context of the study (such
as, do the OAs have a COI?). Here is a hopelessly incomplete overview of
sources to get some more inspiration if you just can't get enough.

- Some people have collected stuff like this in **checklists**. Some
  examples include.

> \+ [[https://www.seaboat.io/]{.underline}](https://www.seaboat.io/)
> (see also
> [[https://osf.io/preprints/psyarxiv/fc8v3_v1]{.underline}](https://osf.io/preprints/psyarxiv/fc8v3_v1))
>
> \+ SEES
> [[https://osf.io/jk674/files/sp5y9]{.underline}](https://osf.io/jk674/files/sp5y9)
>
> \+ [[VALID Checklist
> 2024]{.underline}](https://www.validchecklist.com/)
>
> \+ REAPPRAISED
> [[https://resource-cms.springernature.com/springer-cms/rest/v1/content/17589730/data/v1]{.underline}](https://resource-cms.springernature.com/springer-cms/rest/v1/content/17589730/data/v1),
>
> \+ INSPECT-SR (in development)
>
> \+ several risk of bias checklists, such as the supplemental files
> here
> [[https://link.springer.com/article/10.1186/S40779-020-00238-8]{.underline}](https://link.springer.com/article/10.1186/S40779-020-00238-8)
>
> \+ [<https://casp-uk.net/casp-tools-checklists/>]{.underline} and
> [[FAIRsharing \| Home]{.underline}](https://fairsharing.org/) collect
> many other standards and checklists, sometimes for very specific types
> of research.

\+ Here are a few other **posters/flyers** with handy overviews

- [[https://www.ucy.ac.cy/sinnopsis/wp-content/uploads/sites/167/2024/04/Red-Flags-of-scientific-studies_v1-2.pdf]{.underline}](https://www.ucy.ac.cy/sinnopsis/wp-content/uploads/sites/167/2024/04/Red-Flags-of-scientific-studies_v1-2.pdf)

- [[https://static1.squarespace.com/static/5ecdd7e2f328710ed4c16901/t/627b52c97e6e4004623bd6a2/1652249289507/\_CRABS+illustration+%28Infographic%29+%28A4+Document%29.pdf]{.underline}](https://static1.squarespace.com/static/5ecdd7e2f328710ed4c16901/t/627b52c97e6e4004623bd6a2/1652249289507/_CRABS+illustration+%28Infographic%29+%28A4+Document%29.pdf)

- [[https://www.compoundchem.com/2014/04/02/a-rough-guide-to-spotting-bad-science/]{.underline}](https://www.compoundchem.com/2014/04/02/a-rough-guide-to-spotting-bad-science/)

<!-- -->

- Of course, many people have been writing papers, books, chapters and
  blogposts about it. Here are some examples I found useful

> \+ On the
> [[callingbullshit.org]{.underline}](http://callingbullshit.org)
> website (or the
> [[callingbull.org]{.underline}](http://callingbull.org) website for
> the faint of heart), you can find an interesting collection of
> questions to ask when evaluating a paper that are not strictly
> numerical, but definitely important and informative [[Tools - How do
> you know a paper is
> legit?]{.underline}](https://www.callingbullshit.org/tools/tools_legit.html)
>
> \+ The appendix of this book is fun, but I can't find a version of
> just the appendix online [[Book - by Stuart Ritchie - Science
> Fictions]{.underline}](https://www.sciencefictions.org/p/book)

#  

# VISUALISATION CHECKS {#checkingvisuals}

There are several visual checks you can do. The brevity of this section
does not indicate that it is of lesser importance. It merely reflects my
own personal lack of experience with this approach. I hope to use it
more and to be able to devote a full section to it in future editions.
For now, I refer you to Chapter 7 of AITFM, [[Tools - Misleading axes on
graphs]{.underline}](https://www.callingbullshit.org/tools/tools_misleading_axes.html),
and the Inference by Eye paper, explaining seven "rules of eye"
[[https://psycnet.apa.org/record/2005-01817-003]{.underline}](https://psycnet.apa.org/record/2005-01817-003)

#  

# CHECKING THE NUMERICAL CONFORMITY/DATA INTEGRITY xxx OF THE ORIGINAL STUDY (WITHOUT THE ORIGINAL RAW DATA) {#checkingconformity}

\^ If the raw data are available, you can do a lot. More about that in
Section XXX. But for now, let's just pretend we don't have access to the
raw data.

\^ In the more likely case that the original data are not available,
there is some stuff you can do even in the absence of the raw data. In
particular, if you don't have access to the underlying data, you can
still ask: do the reported numbers (number of participants, means,
p-values, etc) make any sense? It is hard to put a name on all of this,
but let's call the absence of numerical
anomalies/abnormalities/ongerijmdheid xxx numerical integrity/conformity
xxx. There are tons of ways in which you can play "capture the flags".
Below, I list a few.

\^ An important point is that if you find numerical anomalies, this does
not necessarily mean the findings can't be trusted. For example, if the
OAs report to have used use 20 items of a 25-item test without
explanation or justification, this could be the result of a simple typo
(and the 20 should have been 25); Or maybe there was a good reason to
drop the 5 items, such as them belonging to an irrelevant subscale.

\^ Another point I will discuss in more in depth but is so important I
want to foreshadow here is that you are necessarily working with
mutilated numbers, which in the format you see them did not underlie the
reported number. Rounding issues should always be the first explanation
you entertain when encountering a numerical anomaly!

\^ More generally, seeing *that* something is off is considerably much
easier than understanding *why* something is off. The most benign
explanation of a number anomaly is always a typographical error or
sloppy reporting practices more generally. The most evil one is
deliberate fraud as a step towards world dominion. The full range
between an honest, innocuous mistake and outright fraud, really. Again,
explanation is hard.

\^ I organized the different numerical conformity xxx checks into five
convenient categories. Note that these are labels I came up with to
organize these notes, but that others sources might use the same labels
to mean different things or different labels to mean the same thing.
Life is messy, I know.

- One is common sense.

- The other one banks on the fact that many statistical stuff is deeply
  related, and is asking: are all reported summary statistics consistent
  with each other? If a study reports numbers A, B and C, and C can be
  computed from A and B, does the C computed-by-conversion (roughly)
  match the reported C? Checking for a mismatch or discrepancy between
  the reported number and the computed one could be called the *internal
  consistency/coherence/congruity* or *internal conversion* approach.
  This category is by far the largest and will be split up to keep
  things organised.

- A third one is a slight tweak on the conversion approach. Like the
  conversion approach, you take several reported statistics and wrangle
  them around. But instead of checking whether your result matches
  another reported statistic, you compare your result to something else
  that is not reported. To what, you might ask? Just have some patience,
  I will explain below. This can be called the *external conversion*
  approach.

- A fourth one is asking: can we find a raw data set that would give
  rise to the reported summary stats (such as means, ranges, standard
  deviations)? If a study reports a number A, can I come up with raw
  data so that if I would compute A from these recreated data, the
  recreated A matches the reported A? This can be called the
  *reconstruction*, *recovery*, or *recreation* approach.

- A fifth is a (for now, short) list of some imperfect, but still highly
  useful, rules of thumb.

\^ Note that this is all based on the most common situation that the
results associated with a data set are all reported in a single paper.
In the more unlikely case that the same data set is used in other papers
(see Section XXX), you can of course combine info from all papers.

xxx sometimes they report difference siin mean. recpoimute that.

do figre and numerical reports align xxxx

\^ If possible or helpful, I will use R code, either extensive or using
a single line, using a dedicated function from a package. Besides
several functions included in base R, I will use the following functions
from the following R packages. The functions grim(), grimmer() and
debit() functions come from the scrutiny package (Note that it also
comes with a somewhat less intuitive shiny app
[[https://errors.shinyapps.io/scrutiny/]{.underline}](https://errors.shinyapps.io/scrutiny/)).
The GRIMMER_test() and GRIM_test() functions come from the rsprite2
package. I will also use the statcheck() and checkPDF() functions from
the statcheck package. Next, there are the tsum.test() function from the
BSDA package, the anovaMean() and aovSuccifient() functions from the HH
package, and the r.test() function from the psych package. Several
related functions are included in the rpsychi package, but it seems to
have been removed from CRAN [[cran/rpsychi: :exclamation: This is a
read-only mirror of the CRAN R package repository. rpsychi ---
Statistics for psychiatric research.
Homepage:]{.underline}](https://github.com/cran/rpsychi)
[[http://blue.zero.jp/yokumura/]{.underline}](http://blue.zero.jp/yokumura/)
xxx [[rpsychi package -
RDocumentation]{.underline}](https://www.rdocumentation.org/packages/rpsychi/versions/0.8)
alles met .second
[[https://www.rdocumentation.org/packages/rpsychi/versions/0.8]{.underline}](https://www.rdocumentation.org/packages/rpsychi/versions/0.8)

\^ I will also direct you to websites where you can do the necessary
computations in your browser. These are often very handy, but also
typically don't report detailed output (e.g., in terms of number of
significant digits), make your workflow hard to archive and reproduce,
and might keep you in the dark of what *exactly* is being computed. If
you want to do something that is not listed in the resources I provided,
you might wish to try your luck here
[[https://statpages.info/]{.underline}](https://statpages.info/)

\^ Finally, when the analysis is possible in JASP, I will show you how.

\^ There is probably a lot that I missed in the overview I provide
below. The current plan is to include more about this in a future
version of these notes. Among others:

\+ Some tools and techniques exist that do conversions for Bayesian
analyses. It is, for example, possible to compute Bayes factors based on
p-values, using R or JASP. For example, for some analyses in the Summary
Statistics module from JASP, you can input a t-statistic and sample size
to compute a Bayes factor. The JASP Bayes Factor Functions module does
something similar. I am still in the process of getting the lay of the
land here, mostly due to the fact that my students never replicated a
study reporting a Bayesian analysis. This only works of course if the
OAs have used the same priors as the ones underlying these conversions.

\+ Also, there is
[[betterpapers.org]{.underline}](http://betterpapers.org) This seems
promising but is not functional yet, so I don't know what it will do.

## common sense and logic{#commonsense}

\^ One source of information is just common sense, logic, and gut
feeling.

\^ Some numbers are simply impossible. Here are a few things to look out
for:

- if the range of number of hours slept in a day is -3 to 33, something
  went horribly wrong somewhere

- means, median and modes can not be outside the range

- as you can not unread a book, the reported number of books read in a
  year can not be a negative number

- correlations should be between -1 and 1

- the minimum can not be larger than the maximum

- most common reliability coefficients, such as Cronbach's alpha, can
  not exceed 1

- all percentages within a category should add up to (roughly, because
  of rounding) 100%

- etc

\^ Beyond the impossible, you should ask yourself: are the reported
numbers realistic? Some numbers are simply implausible. A nice trick is
to think generatively, which contrasts favorably with thinking
retroactively. That is, *before* you see any reported numbers, ask
yourself this: based on the description of the methods alone, what kind
of numbers do I expect to see? Which numbers are unusual or excessive?

- if the mean self-reported number of hours slept is 16, there might be
  something off. if the reported mean number of hours slept in a day is
  16, there must be a typo or a conspiracy xxx merge

- when you spot an age range of 18 to 123, the authors must have done
  something very, very special

- can a person really smoke 74 cigarettes in a day?

- an intervention that can reduce the prevalence of people with mental
  health problems from say 38% to just 4% is probably more magic not
  science

- a cohen's d of 5 is very large and quite unlikely for a common
  manipulation

- it is unlikely that a correlation between a depression score and the
  number of hours of sleep is as high as .87

- reading a study with as much as 547291043 participants is impressive
  but probably a typo or a lie, especially when the population was
  children from divorced parents with ASD

- a prevalence of 90% of depressions symptoms among PhD students is
  probably (hopefully) incorrect

- is it really true that in a general population of students more than
  95% have never drank a sip of alcohol in their entire life?

- etc

\^ Some numbers are impossible, unrealistic or suspicious *within the
context of the study*.

- You can check whether the inclusion/eligibility and exclusion criteria
  have been followed, using summary stats, plots, tables, etc.

  - If the OAs, for example, report they only focus on 18-21 year olds
    as their population (either by an exclusion criterion or an
    inclusions criterion) but report an age range of 16-43 in their
    sample, something is off.

  - If the sample is reported to be restricted to people with a
    depression score above 16, the reported range of the depression
    score should respect these boundaries.

- You can check whether the answer format and the summary data make
  sense. For example, if the OAs say the answer options for each item
  for a scale were between 1 and 7, but the reported minimum and maximum
  of their data, averaged over items, are 0 and 6, respectively, this
  suggests there is something wrong. One possible explanation is that
  the answer options were between 0 and 6, really. TODO add example from
  Liesl

- Similar to above, but with a mean of 8. Not possible, Sir.

- You can always use more background knowledge to spot wrong numbers.
  Maybe the "official" scale the OAs use has 29 items, but they say they
  only use 20 (without explaining why). Or the OAs report using a scale
  of 20 items, but in their shared materials, there are 25 items. That's
  a numerical anomaly.

\^ It's not just your guts that should tell you whether the numbers you
see are plausible. There are (summary) data for that! Check whether the
statistical conclusions agree with what you would eyeball from just
looking at the data, if such a plot or table is available.

## internal conversion: general idea{#internalgeneral}

\^ The starting point is that in typical statistical reporting there is
a lot of redundant information. The reason is that there are often very
intricate interrelationships between the various numbers being computed
and reported, and they can be converted into each other, sometimes
straightforwardly, sometimes with a little bit of work. Some things can
not be simultaneously true. You can find out using where
inconsistency/incongruence/incongruity checks xxx.

\^ Here is an appealingly easy example: It can not be simultaneously
true that there are 20 participants in the experimental condition, 24 in
the control, and the total sample size is 45. One of those should be
wrong! So the basic idea is to exploit the redundancy between
statistical information, try out different sorts of conversions, and see
if any inconsistencies can be spotted.

\^ Below, I list a few useful conversions. I am sure, however, there are
many more of these relationships floating around, waiting to be
unearthed and put to use.

\^ The biggest use case (I really wanted to ever find a good spot to use
that word, and I think I nailed it!) for the internal conversion
approach involves converting summary statistics, such as means, standard
deviations and sample sizes, into p-values/One category of this approach
involves recomputing p-values from other summary info such as means and
standard deviations xxx. Because this category is so big, I gave it its
own subsection/is so extended I collected it in a separate subsection,
but it is just an application of the same principle xxx. Also, the
internal conversions that are inequalities are given their own section.
So this means I will start out with the equalities that are not p-values
based on summary statistics.

## internal conversion: the equality edition (no p-values from summaries){#internalequality}

\^ This one is not really a conversion, unless you are Big Words Person
and want to be on record for calling things an identity-conversion, but
it is close enough to be included. Often sample sizes and summary
statistics are reported several times, such as in the text (the sample
size is often mentioned repeatedly, such as in the abstract and in the
methods section), in a table, and a figure. Of course, the values should
be identical across means of presentation.

\^ conclusion from p-value: It pains me to have to say this, but you
should [check whether the reported p-value is below the significance
level when significance is concluded. If the authors conclude there is a
significant difference but back this up with a p-value of .12, something
is amiss. They might, for example, have forgotten a *not* in their
conclusion, or a 0 in the p-value.]{.mark}

\^ Everybody can count and so should you! It is always easy to check
stuff that is easy to count. for example:

- total number of items from the separate number of items. Often OAs
  report the total number of items used in their study. They also often
  list the number of items each scale contains. The total should match
  the sum of its parts.

- final sample size from collected sample sizes: sometimes, OAs report
  how many participants they collected, how many they discarded or how
  many dropped out, and how many they ended up using. The sum (well,
  subtraction) should check out.

- total sample size from subgroup sample size: if the OAs report there
  are N participants, and then later on they split up the data in
  subgroups (e.g., males and females; control vs experimental; etc), of
  course the sum of all the sample sizes from all the subgroups should
  be equal to N.

\^ overall summary statistics from subgroup summary statistics: There
are more relations between subgroup-level statistics and overall
statistics than just the sample size. Here is how: TODO EXPLAIN THE
EQUATION AND GENERALIZE TO N\>2

\\bar{x} = \\frac{\\sum\_{i=1}\^k n_i \\bar{x}\_i}{\\sum\_{i=1}\^k n_i}

s\^2 =

\\frac{

\\sum\_{i=1}\^k (n_i - 1)s_i\^2

\+

\\sum\_{i=1}\^k n_i(\\bar{x}\_i - \\bar{x})\^2

}{

\\sum\_{i=1}\^k n_i - 1

}

This makes it possible to check whether the overall mean and standard
deviation are compatible with the reported means, standard deviations,
and sample sizes on the subgroup level.

As an example, let's look at another replication study I was part of
TODO add ref
[[https://ppw.kuleuven.be/okp/\_pdf/Rutten2018DSACL.pdf]{.underline}](https://ppw.kuleuven.be/okp/_pdf/Rutten2018DSACL.pdf).
The main focus was on the relation between depression (assessed using
the CES-D) and category learning. The exact details don't matter, but at
some point, we wanted to make two groups, one with participants scoring
high on a depression score, and the other group scoring low. We reported
that we ended up with a "usable sample of 238 participants on which the
analyses were conducted" and that "\[t\]o determine above average and
below average depressive symptoms groups, a split at the CES-D sample
mean was applied. A split at the \[overall CES-D\] mean (14.60; SD =
11.59) resulted in an above average depressive symptoms group of 101
participants (mean CES-D score = 25.61), and a below average depressive
symptoms group of 137 participants (mean CES-D score = 6.47)." We did
not report the subgroup standard deviations, but for the sake of this
example, I will tell you they are 9.09 and 4.14 for the above average
and below average groups, respectively. \[FOOTNOTE I computed these from
the raw data available at
[[https://osf.io/auzgp/files/5kpv7]{.underline}](https://osf.io/auzgp/files/5kpv7).
When the raw data are available, there is not much point in doing this
kind of analyses, but I do report them here because they make for a nice
illustration.\]. Let's see if we can convert all the subgroup statistics
into the overall statistics. This can be done by hand or using a simple
calculator. Here is how to do it in R.

\`\`\`{r, opts.label=\'code\'}

n_o \<- 238 #overall

m_o \<- 14.60 #overall

s_o \<- 11.59 #overall

n1 \<- 101

m1 \<- 25.61

n2 \<- 137

m2 \<- 6.47

s1 \<- 9.09

s2 \<- 4.14

#conversions

n_computed \<- n1 + n2

n_computed

m_computed \<- (n1 \* m1 + n2 \* m2)/(n1 + n2)

m_computed

var_computed \<- ((n1 - 1) \* s1\^2 + (n2 - 1) \* s2\^2 + n1 \* (m1 -
m_computed)\^2 + n2 \* (m2 - m_computed)\^2)/(n1 + n2 - 1)

sd_computed \<- sqrt(var_computed)

sd_computed

\`\`\`

Hurray! The overall sample size and the mean can be computed from the
subgroup level information. The overall standard deviation, however, can
not. So something is off. Without access to the raw data (which would
typically be the case when you do this kind of analyses), you can't do
much more to find what exactly is wrong. In this case, we do have the
raw data. It turns out that in our paper we made a mistake in reporting
the overall standard deviation. Reinspecting the raw data tells me that
the overall standard deviation should have been reported as 11.60
instead of as 11.59, exactly the value our conversion suggests.

As another example, consider this study
[[https://ppw.kuleuven.be/okp/\_pdf/Voorspoels2014CRRBE.pdf]{.underline}](https://ppw.kuleuven.be/okp/_pdf/Voorspoels2014CRRBE.pdf),
where we replicated a famous finding TODO add ref that "race encoding is
not automatic and inevitable, but rather a byproduct of categorization
in terms of coalitions". A total of 463 participants completed the
study, in one of two conditions (visual cue vs no visual cue). In Table
2 we find that the 225 participants in the first condition had a mean
age of 33.25 with a standard deviation of 10.92, whereas the 238
participants in the second condition had a mean age of 33.47 with a
standard deviation of 10.58. In the full group, the mean age was 33.36
with a standard deviation of 10.73. Can we convert the condition-based
values to the overall? Well, almost:

\`\`\`{r, opts.label=\'code\'}

n_o \<- 463 #overall

m_o \<- 33.36 #overall

s_o \<- 10.73 #overall

n1 \<- 225

m1 \<- 33.25

s1 \<- 10.92

n2 \<- 238

m2 \<- 33.47

s2 \<- 10.58

n_computed \<- n1 + n2

n_computed

m_computed \<- (n1 \* m1 + n2 \* m2)/(n1 + n2)

m_computed

var_computed \<- ((n1 - 1) \* s1\^2 + (n2 - 1) \* s2\^2 + n1 \* (m1 -
m_computed)\^2 + n2 \* (m2 - m_computed)\^2)/(n1 + n2 - 1)

sd_computed \<- sqrt(var_computed)

sd_computed

\`\`\`

Everything checks out, except for, again, the standard deviation. There
is a very small difference between the recomputed one (10.73548 rounded
to 10.74) and the reported one (10.73). Is this evidence for another
mistake like in the depression and category learning example above? No.
This time, the observed discrepancy is due to rounding. If I recompute
the summary statistics based on the raw data, available here
[[https://osf.io/9n62e/overview]{.underline}](https://osf.io/9n62e/overview),
and report them with more decimal places, all is well. The recomputed
standard deviation is now 10.73236, which rounds to 10.73, identical to
the reported one. \[FOOTNOTE: Of course, if I had access to the raw
data, I would not be doing these checks at all but would move to the
stuff discussed in Section XXX\]:

\`\`\`{r, opts.label=\'code\'}

m_o \<- 33.36069

s_o \<- 10.73236

m1 \<- 33.24889

s1 \<- 10.91732

m2 \<- 33.46639

s2 \<- 10.57647

\`\`\`

There is a very important lesson here: A mismatch should not necessarily
mean something is off. Given that the reported numbers that you use in
your conversion are typically rounded, this loss of precision is almost
guaranteed to lead to a mismatch. This means that it would be severely
misguided or downright evil to expect perfection, because you are
feeding it approximations to the real summary statistics! Still, you
would not want to see a large discrepancy. I will say more about dealing
with rounding in Section \@sec-rounding.

\^ percentages/proportions from counts/frequencies and sample size: If
both frequencies (or counts) and proportions (or percentages) are
reported, try to recompute the percentages/proportions from the
counts/frequencies and the sample size. TODO add example camille.

\^ degrees of freedom from sample size and design: the degrees of
freedom are often closely related to the sample size or to other
information that is readily available (like number of groups or number
of parameters). It might be worthwhile to check whether the reported
degrees of freedom make sense in the light of the reported sample size
and design choices. TODO add example; tegenvb: [chikwadraattest op
onafhankelijkheid van 2 kwalitatieve variabelen]{.mark} (maar nog wel
steeds checkbaar want based on table dimensions) TODO cleanup welch is
nog moeilijker: ook variances. TODO make overview with examples and APP
dfcheck

\^ standard error from mean and sample size: authors often numerically
report standard deviations and sample sizes, and visually report
standard errors. The standard error of the mean is a simple conversion
of the reported numbers: SE = SD/sqrt(n).

\^ error bars for the mean from xxx: error bars are either SE based or
CI based or SD based [[Error bar charts - IBM
Documentation]{.underline}](https://www.ibm.com/docs/en/spss-modeler/18.6.0?topic=types-error-bar-charts).
xxx

Consider again, the race erased example. You can easily check whether
the errors bars reported in their Figure 1 make sense. We will focus on
the coalitional encoding variable, indicating the extent participants
encoded team membership of basket players shown in photographs in the
visual cue condition (where there was visual help to signal team
membership)/ The summary statistics are reported in their Table 3 and
the mean and standard errors are shown on the far right side of their
Figure 1. TODO add figure xxx You can use the summary statistics to
compute the lower and upper bounds of the error bar, and compare them to
what you see on the plot (the other standard errors can of course be
checked similarly). You could use a simple calculator or R:

\`\`\`{r, opts.label=\'code\'}

n2 \<- 238

m2 \<- 3.50

s2 \<- 4.10

se_computed_hi1 \<- m2 + s2/sqrt(n2)

se_computed_lo1 \<- m2 - s2/sqrt(n2)

\`\`\`

Just by the fact it relies on eyeballing, this comparison will be
ballpark only. And ballpark, this example checks out.

\^ effect size from t-statistic and other statistics: There are
straightforward relations between effect size and other reported
statistics, such as means, standard deviations and t-statistics. For
example, for an independent samples t-test, Cohen's d is defined in
terms of the mean, standard deviation and sample size for each group,
or, alternatively as d = t \\sqrt{1/n1​​+1/n2​}. In a future version, this
needs to be expanded. There's probably a lot of good stuff here
[[https://matthewbjane.quarto.pub/]{.underline}](https://matthewbjane.quarto.pub/).
There are probably many R functions to help with this conversion, but I
need to still get a lay of the land. escalc() from the metafor R package
should be a good one to look into.

\^ planned sample size from assumed effect size: Typically, you should
be able to redo the power analysis. There are many tools, websites and R
packages for doing that.

For example, in the race erased example, we wrote that we "reject the
null hypothesis that there is no difference if the p-value is smaller
than 0.05", that we used a "pooled effect size of the effect for H1 \...
0.328" and that we "calculated a planned sample size for achieving a
0.95 power level using a one-sided independent-samples t-test. This
resulted in a sample size of 202 per condition for H1, and thus in total
404 participants." This result can be easily checked using

\`\`\`{r, opts.label=\'code\'}

library(pwr)

pwr.t.test(

d = 0.328,

power = 0.95,

sig.level = 0.05,

type = \"two.sample\",

alternative = \"greater\" \# one-sided (H1: group1 \> group2)

)

\`\`\`

\^ standard deviation from mean (for binary variables): A very well
known relationship is one between the variance and the mean of binary
variables: sigma2 = p q, where p is the proportion of 1s and q is the
proportion of 0s. Because q = 1-p and p is equal to the mean, it follows
that sigma2 = p q = p (1-p) = mean (1-mean)). \[FOOTNOTE You are
probably not here for historical fun facts about reliability
coefficients, but hey, that's the main reason why footnotes were
invented. This relationship is the reason why every researcher in
psychology has heard of the name Cronbach but Kruder and Richardson ring
lesser bells. In 1937, Kruder and Richardson published a reliability
coefficient, now somewhat known as KR20, in which they used pq. They
thought it was bloody obvious that pq was equal to the variance, so they
didn't also provide a version of KR20 where pq was explicitly
substituted by the variance. Besides, everybody was working with binary
variables anyway and pq was a handy shortcut to compute the variance, so
there was nothing to gain with the more general expression. In 1951,
Cronbach published the same equation, but now saying the quite part out
loud and replacing pq with variance. This equation catapulted Cronbach
to psychometric stardom and is the now famous Cronbach's alpha. To be
fair, there are other reasons why alpha is a classic while KR20 is more
underground. A fascinating historical account is provided by Cho TODO
add ref
[[Originators-of-Reliability-Coefficients-A-Historical-Review-of-the-Originators-of-Reliability-Coefficients-Including-Cronbachs-Alpha.pdf]{.underline}](https://www.researchgate.net/profile/Eunseong-Cho-2/publication/326945602_Originators_of_Reliability_Coefficients_A_Historical_Review_of_the_Originators_of_Reliability_Coefficients_Including_Cronbach's_Alpha/links/6131fb8038818c2eaf7aeb9a/Originators-of-Reliability-Coefficients-A-Historical-Review-of-the-Originators-of-Reliability-Coefficients-Including-Cronbachs-Alpha.pdf)\]

Translating this basic result to the sample standard deviation, this
means that the sample standard deviation is given by sqrt(N/(N-1)
sigma2) = sqrt(N/(N-1) mean (1-mean)). So with binary data, the standard
deviation of binary data is determined by the sample size and the mean.
If you don't believe me, you can read an accessible explanation and
derivation of this relation in the Section Binary Items of this book:
[[https://www.google.be/books/edition/Psychometrics/FjQ3VG2cBtgC?hl=nl&gbpv=1&pg=PA53&printsec=frontcover]{.underline}](https://www.google.be/books/edition/Psychometrics/FjQ3VG2cBtgC?hl=nl&gbpv=1&pg=PA53&printsec=frontcover)

For example, if the sample size is 10, the mean is reported to be 0.6,
and the standard deviation is 0.24, you can easily check if these three
numbers can simultaneously be true. This can be done by hand or using a
simple calculator. Here is how to do it in R.

\`\`\`{r, opts.label=\'code\'}

n \<- 10

sd_reported \<- .52

mean_reported \<- .6

sd_computed \<- sqrt(n/(n-1)\*mean_reported\*(1-mean_reported))

sd_computed

#if you want to save yourself a bit of time

library(scrutiny)

[debit(x = \"0.6\", sd = \"0.52\", n = 10)]{.mark}

\`\`\`

The computed standard deviation matches the reported mean, which is
confirmed by the triumphant TRUE from the debit() function.

\^ p values from test statistics and degrees of freedom: To compute a
p-value, you don't always need the raw data. In some cases, summary
statistics, like means and standard deviation suffice, as will be
discussed in the Section \@sec-internalpvalue. But even without those
summary statistics, you can often recompute the p-value based on what is
reported in the paper. In particular, a p-value is a simple conversion
of the reported test statistic (such as t-values) and degrees of
freedom.

- [T]{.mark}here are several websites that can do these, like
  [[https://www.graphpad.com/quickcalcs/pvalue1/]{.underline}](https://www.graphpad.com/quickcalcs/pvalue1/)
  or a bit more advanced
  [[https://statcheck.steveharoz.com/]{.underline}](https://statcheck.steveharoz.com/)

- In R, these checks can be done by simple code or by using the
  statcheck() function from the statcheck R package. Note that the input
  does not have to be (but can be) just numbers: it is a snippet of text
  with appropriately formatted (i.e., APA style) statistics. xxx not
  tables and only APA style. for others, you are on your own xxx

For example, consider a study from Durante et al. (2013) TODO add ref
focusing on religiosity of women in a 2x2 design: High vs Low Fertility
and Single vs Relationship Relationship Status. They report a
significant Fertility × Relationship Status interaction, F(1, 159) =
6.46, p = .012. Let's see if we can recompute that p-value:

\`\`\`{r, opts.label=\'code\'}

p_reported \<- .012

f_reported \<- 6.46

p_computed \<- 1 - pf(f_reported, df1 = 1, df2 = 159)

p_computed

\# or using statcheck

library(statcheck)

statcheck(\"F(1, 159) = 6.46, p = .012\")

\`\`\`

The conversed p-value is equal to the reported one (as confirmed by the
FALSE under raw error in the statcheck output), so all is good.

Durante et al. (2013) continue to focus on a simple effect: "\[W\]omen
in relationships reported more religiosity if they were in the
high-fertility group \... than if they were in the low-fertility group
\..., F(1, 159) = 2.64, p = .10". Let's see if these numbers are
compatible:

\`\`\`{r, opts.label=\'code\'}

p_reported \<- .10

f_reported \<- 2.64

p_computed \<- 1 - pf(f_reported, df1 = 1, df2 = 159)

p_computed

\# or using statcheck

statcheck(\"F(1, 159) = 2.64, p = .10\")

\`\`\`

Now the computed p-value does not match the reported one, as statcheck
indicates with a big TRUE under raw error. Now there is a mistmatch. The
computed p-value is [0.1061842, which should round to 0.11, not to the
reported 0.10. It is impossible to know what is off. The 2.64? The .10?
Both? Without the raw data, there is no way to know. \[FOOTNOTE In this
particular case, there is access to the raw data, as they are available
here
[[https://osf.io/zj68b/files/hj9gr]{.underline}](https://osf.io/zj68b/files/hj9gr).
Inspection of the data reveals that it is both: Durante et al. (2013)
should have reported]{.mark} F(1, 159) = 2.63, p = .11 instead of F(1,
159) = 2.64, p = .10[, which would have passed the check. But that's of
course cheating because the point here is to not use the raw data.
Without the raw data, we would have only known that something does not
check out.\]]{.mark}

[The other simple effect presents an interesting case. Durante et al.
(2013) report that "\[s\]ingle women reported significantly less
religiosity if they were in the high-fertility group \... than if they
were in the low-fertility group \... *F*(1, 159) = 3.88, *p* = .050".
Let's see for ourselves:]{.mark}

\`\`\`{r, opts.label=\'code\'}

p_reported \<- 3.88

p_computed \<- 1 - pf(p_reported, df1 = 1, df2 = 159)

p_computed

\# or using statcheck

statcheck(\"F(1, 159) = 3.88, p = 0.050\")

\`\`\`

[Our computed p-value is 0.05060182 which rounds to 0.051, which is
again close but not identical to the reported p-value. Was there another
error? For one, statcheck does not think there is an error though, as it
produces FALSE under raw error. Why is that? The reason is simple in
theory, but makes life complicated in practice. The reported value of
3.88 *might* actually be a rounded version of, say, 3.884, This value of
the F statistic is compatible with a reported p-value of 0.050 (code not
shown), so rounding might be an explanation for the observed mismatch.
Luckily, statcheck deals with this nasty rounding problem! FOOTNOTE
\[From the manual: TODO add ref "Correct rounding is taken into account.
For instance, a reported t value of 2.35 could correspond to an actual
value of 2.345 to 2.354 with a range of p values that can slightly
deviate from the recomputed p value. statcheck will not count cases like
this as errors."\]]{.mark}

[\[FOOTNOTE The story is still a bit more complicated: after the
reassuring message that statcheck() takes care of the messy issue of
rounding, I have to bring a less reassuring message. Despite not finding
an error, inspection of the raw data reveals that the numbers are, in
fact, wrong. Again, there is no way to know this from the reported
numbers alone, but in this case the raw data are available, and based on
these data it turns out that Durante et al. (2013) should have reported
*F*(1, 159) = 3.89, *p* = .050\]]{.mark}

[\^ I illustrated the approach and the use of statcheck for an F test,
but the same logic (and code) applies much more generally. statcheck
works for correlations (r) and t, F, χ2, Z tests and Q tests.]{.mark}

\^ Note that statcheck is even more useful than this: conveniently, you
can easily run the full paper through statcheck. It is very easy to use
and it does something very very cool: it automatically extracts all APA
style reported p-values and does the check described above. It takes
just one line of R code checkPDF(\"durante-et-al-2013.pdf\"). If you
don't want to fire up your R engine for that, there is even a handy
website where you can upload the paper,
[[statcheck.io]{.underline}](http://www.statcheck.io).

## internal conversion: the p-value from summary statistics edition{#internalpvalue}

\^ p values from summary statistics: Some tests can be performed using
summary statistics only, which are routinely reported. This allows you
to check the test results, even without having access to the raw data.

\^ With count data, converting summary statistics into p-values and
confidence intervals is painfully easy, so I am almost embarrassed
writing this. Most tools do not even take the raw data (0s and 1s) as
input, but require the summary statistics, in the form of successes,
failures and sample sizes, possibly organized in a contingency table. So
that's almost a free pass.

- In a browser, you can use the website:
  [[https://www.graphpad.com/quickcalcs/catmenu/]{.underline}](https://www.graphpad.com/quickcalcs/catmenu/)
  or (if your contingency table is larger than a 2x2
  [[https://home.ubalt.edu/ntsbarsh/Business-stat/otherapplets/Catego.htm]{.underline}](https://home.ubalt.edu/ntsbarsh/Business-stat/otherapplets/Catego.htm).)

- In JASP, you can as follows:

  - to do a Chi-squared test and a fisher test based on the summary
    (count) data by picking *Contingency Table* from the *Frequencies*
    module. You need to upload the count data first, for example
    organized as follows (based on an example from JASP's data library):
    healthabits TODO

  - To do a Binomial test based on the summary (count) data, go to the
    Summary Statistics module and pick Bayesian Binomial Test. You
    *don't* need to upload the data, but can directly input them in the
    left JASP panel. Despite its name, it will also do a non-Bayesian
    Binomial test for you, although the non-Bayesian output is currently
    limited to just the p-value. FOOTNOTE\[The Binomial option from the
    *Frequencies* module does require the individual data.\]

  - Doing a proportion test is not possible.

- In R, the basic functions to test hypotheses with count data, such as
  chisq.test(), fisher.test(), binom.test(), and prop.test() all require
  summary data (i.e., counts) already.

\^ To do a correlation test and compute the associated confidence
interval, you only need the correlation and the sample size.

- In your browser, you can use
  [[https://www.graphpad.com/quickcalcs/pvalue1/]{.underline}](https://www.graphpad.com/quickcalcs/pvalue1/),
  keeping in mind that DF should be equal to the sample size - 2.

- In JASP, you can go pick the Bayesian Correlation option from the
  Summary Statistics module. This will again give you a non-Bayesian
  answer (i.e., a p-value) based on just the correlation and the sample
  size. Alternatively, you can use the ESCI module (but this is still in
  beta; confusingly, if you want to use the ESCI module with summary
  data, you have to open a data set, but this can be an empty one. This
  might or might not change in the future [[\[Feature Request\]: Expand
  Summary Statistics with (part of) ESCI · Issue #3979 ·
  jasp-stats/jasp-issues]{.underline}](https://github.com/jasp-stats/jasp-issues/issues/3979)).

- In R, you can use the r.test() function from the psych package.

For example, if the observed correlation is .57 in a sample size of 30:
TODO add a more interesting example from real (ideally, replication)
research

\`\`\`{r, opts.label=\'code\'}

> library(psych)
>
> cor.nf \<- 0.57 #the correlation
>
> n \<- 30 #the sample size
>
> library(psych)
>
> r.test(r12 = cor.nf,
>
> n = n,
>
> twotailed = TRUE)

\`\`\`

\^ To do a one-sample t-test, you only need the mean, the standard
deviation, and the group sample sizes to compute the t-statistic,
p-value and confidence interval.

- In your browser you can use
  [[https://www.graphpad.com/quickcalcs/onesamplet1/?format=sd]{.underline}](https://www.graphpad.com/quickcalcs/onesamplet1/?format=sd)
  and
  [[https://www.graphpad.com/quickcalcs/cimean1/?format=sd]{.underline}](https://www.graphpad.com/quickcalcs/cimean1/?format=sd).

- In JASP, pick the Bayesian One Sample T-Test option from the Summary
  Statistics module, select the Input Type to be "Mean, SD and Sample
  Size" and fire away. It will give you your much-desired t-statistic
  and p-value. An alternative is using the ESCI module, with Mean and
  Median Single Group. Don't forget to select the Hypothesis evaluation
  option.

- In R, there is the tsum.test() function from the BSDA package.

TODO Add a more interesting example from real (ideally replication)
research. As an example, let's focus on a fictional data set discussed
in LSR. The data consist of a set of grades of 20 psychology students,
and the question of interest is in whether these grades are different
from 67.5. The conclusion, based on the raw data, is as follows:

\[FOOTNOTE: If you want to check, the raw data are grades \<- c(50, 60,
60, 64, 66, 66, 67, 69, 70, 74, 76, 76, 77, 79, 79, 79, 81, 82, 82,
89).\]

"the psychology students scored slightly higher than the average grade
of 67.5 (t(19) = 2.25, p \< .05); the 95% confidence interval is \[67.8,
76.8\]." You can recompute these results without the raw data, provided
that you know the sample size, mean and standard deviation. Say that
these are the summary statistics (which I computed from the raw data):

\`\`\`{r, opts.label=\'code\'}

n \<- 20

mean \<- 72

sd \<- 9

library(BSDA)

tsum.test(mean.x = mean,

s.x = sd,

n.x = n,

alternative = \"two.sided\",

mu = 67.5)

\`\`\`

Pretty close, but not quite the banger you would hope. But what if I
report the summary statistics with a bit more precision?

\`\`\`{r, opts.label=\'code\'}

n \<- 20

mean \<- 72.3

sd \<- 9.520615

tsum.test(mean.x = mean,

s.x = sd,

n.x = n,

alternative = \"two.sided\",

mu = 67.5)

\`\`\`

Now everything is fine. So there are two bottomlines to this example:
One is that it is possible to convert means, standard deviations to the
t-statistic and p-value of a one sample t-test. The other one is the now
hopefully familiar theme that rounding issues should always be on top of
your mind when encountering a mismatch.

\^ The two-sample independent samples t-test is very similar. To do a
two-sample independent samples t-test, the groups means, group standard
deviations, and the group sample sizes are enough to compute the
t-statistic, p-value and confidence interval (and the exact test type,
of course).

- In a browser, you can use
  [[https://www.graphpad.com/quickcalcs/ttest1/?format=sd]{.underline}](https://www.graphpad.com/quickcalcs/ttest1/?format=sd).

- In JASP, pick the Bayesian Independent Samples T-Test option from the
  Summary Statistics module, select the Input Type to be "Means, SDs and
  Sample Sizes" and fire away. It will give you your much-desired
  t-statistic and p-value. In the current version, this is wrong, but it
  will hopefully be corrected in the next version (see here
  [[https://github.com/jasp-stats/jasp-issues/issues/3968]{.underline}](https://github.com/jasp-stats/jasp-issues/issues/3968)).
  Using the ESCI module, with Means and Medians Two Groups seems to work
  well (again choosing the Hypothesis evaluation option).

- In R, you can again use the tsum.test() function from the BSDA
  package.

Consider for example the replication we did of the crowd within effect
TODO add ref, reported in TODO add ref. Participants had to provide two
answers to a set of trivia questions. One group of participants were
prompted for a second answer immediately after the first answer. Another
group of participants were asked to provide their second answer after a
delay of three 3 weeks. The main interest is in whether the average
answer of the two is better, as in having a lower mean square error,
than the first. The accuracy gain is assessed by the difference between
the MSE of the average answer and the MSE of the first guess.

Let's now compare the accuracy gain in the delayed condition to the
accuracy gain in the immediate condition. Steegen et al. (2014) report
these results: t(609) = 0.18, p = 0.858. Can we convert the summary
statistics to these values? Steegen et al. (2014) report the mean
accuracy gains to be 50 and 48 in the delayed and immediate conditions,
respectively, the standard deviations to be 147 and 119, and the sample
sizes to be 140 and 471.

Let's feed these numbers in the tsum.test() function:

\`\`\`{r, opts.label=\'code\'}

meanx \<- 50

meany \<- 48

sdx \<- 147

sdy \<- 119

nx \<- 140

ny \<- 471

library(BSDA)

tsum.test(mean.x = meanx,

mean.y = meany,

s.x = sdx,

s.y = sdy,

n.x = nx,

n.y = ny,

alternative = \"two.sided\",

var.equal = TRUE)

\`\`\`

This is similar to what Steegen et al. (2014) reported, but not
identical. Did we do something wrong in our replication study? We did
not, except maybe being too imprecise when reporting the summary stats
(To be fair, we made the data publicly available, so please give us some
slack).

What if we had reported the summary statistics in a more precise
fashion? These are the more precise values: 49.97201, 47.79869,
147.0215, and 119.403. \[FOOTNOTE: These values were not reported in the
paper but computed from the raw data available here
[[https://osf.io/arxvg/overview]{.underline}](https://osf.io/arxvg/overview),
which you typically won't see reported in a paper. Again, the whole
point of this section is to not use raw data. The reason that I did use
the raw data to compute the summary statistics at a higher level of
precision is to show you that it, in principle, works, and that rounding
should always be taken into account.\] If you use these values as input,
tsum.test() produces the values reported by Steegen et. al (2014).

As a final example, let's go back to our race erased replication
discussed in Section XXX. We compared a variable called coalitional
encoding across both conditions. The sample sizes, mean and standard
deviations are shown in Table 3 of Voorspoels et al. (2014). We
performed an independent-samples, one-sided t-test, comparing
coalitional encoding across the two conditions, and found that the "test
revealed a significant difference \[t(461) = 9.26, p \< 0.001\]". Can
you convert the summary statistics to these values?

\`\`\`{r, opts.label=\'code\'}

n1 \<- 225

m1 \<- 0.50

s1 \<- 2.78

n2 \<- 238

m2 \<- 3.50

s2 \<- 4.10

tsum.test(mean.x = m1,

> s.x = s1,
>
> n.x = n1,
>
> mean.y = m2,
>
> s.y = s2,
>
> n.y = n2,
>
> var.equal = T,
>
> alternative = \"less\")

tsum.test(mean.x = m1,

> s.x = s1,
>
> n.x = n1,
>
> mean.y = m2,
>
> s.y = s2,
>
> n.y = n2,
>
> var.equal = F,
>
> alternative = \"less\")

\`\`\`

Well, we can, but not at the same time. The fact that the degrees of
freedom is an integer suggests the use of var.equal = T. However, this
option does produce xxx as the t-statistics. So when we assume equal
variances, we find the reported degrees of freedom, but not the reported
t-statistic. Let's try var.equal = F. When we do not assume equal
variances, we find the reported t-statistic, but not the reported
degrees of freedom (which we could have predicted even before running
the code, since assuming unequal variances typically produces
non-integer degrees of freedom). Clearly, in our replication study, we
made an (inconsequential) mistake, and erroneously reported the degrees
of freedom (461) for a t-test assuming equal variances.

\^ To do a one way anova, you only need the groups means and standard
deviations are enough to compute the t-statistic and the p-value (and
the exact test type, of course).

- In your browser, you can use
  [[https://statpages.info/anova1sm.html]{.underline}](https://statpages.info/anova1sm.html)
  or
  [[http://www.prepubmed.org/anova/]{.underline}](http://www.prepubmed.org/anova/).
  Unlike the first link, the second link only reports the F-statistic,
  but is smart enough to take rounding issues (see below) into account.

- As far as I can tell, you can currently not do this in JASP.

- If you want to use R, the anovaMean() function from the HH package is
  there for you.

TODO add an interesting example, preferably from a replication study. As
an example, I will use the fictional clinical trial data from LSR, which
relate to testing the effectiveness of a new antidepressant drug. The
study involves the administration of three drugs: a placebo, an existing
antidepressant, and the new one. In each test group, there are 6
participants. The key outcome is the overall improvement in mood. To
facilitate comparison, let's first perform a one way ANOVA on the raw
data:

#the data can be found here
[[https://github.com/djnavarro/rbook/blob/main/bookdown/data/clinicaltrial.Rdata]{.underline}](https://github.com/djnavarro/rbook/blob/main/bookdown/data/clinicaltrial.Rdata)

load( \"clinicaltrial.Rdata\" )

anova( lm( mood.gain \~ drug, data = clin.trial ))

The summary data look like this.

[condition means SDs n]{.mark}

[1 placebo 0.4500000 0.2810694 6]{.mark}

[2 old 0.7166667 0.3920034 6]{.mark}

[3 new 1.4833333 0.2136976 6]{.mark}

Doing a one way ANOVA with these summary data, we find

\`\`\`{r, opts.label=\'code\'}

d \<- data.frame(

condition = c(\"placebo\", \"old\", \"new\"),

means = c(0.4500000, 0.7166667, 1.4833333),

SDs = c(0.2810694, 0.3920034, 0.2136976),

n = c(6, 6, 6)

)

library(HH)

anovaMean(d\$x,d\$n,d\$means,d\$SDs)

\`\`\`

Sweet!

In many studies, however, summary statistics are not presented up to 7
decimal places. The values you would find in a paper would more look as
follows:

[condition means SDs n]{.mark}

[1 placebo 0.45 0.28 6]{.mark}

[2 old 0.72 0.39 6]{.mark}

[3 new 1.48 0.21 6]{.mark}

With these summary statistics, we find

\`\`\`{r, opts.label=\'code\'}

d \<- data.frame(

condition = c(\"placebo\", \"old\", \"new\"),

means = c(0.45, 0.72, 1.48),

SDs = c(0.28, 0.39, 0.21),

n = c(6, 6, 6)

)

d

library(HH)

anovaMean(d\$x,d\$n,d\$means,d\$SDs)

\`\`\`

The values are close, but not identical to the ones we would find using
the raw data.

\^ To do a 2×2 between-subjects factorial ANOVA with balanced,
independent groups, you only need the cell means, standard deviations,
and sample sizes.

> \+ There is no website that I know of where you can do this in full
> detail. On this website, you can at least compute the F-statistic
> [[http://www.prepubmed.org/anova_2way/]{.underline}](http://www.prepubmed.org/anova_2way/)
> This website is sophisticated enough to take rounding issues (see
> below) into account.
>
> \+ In JASP, you can use the 2x2 factorial Means and Medians analysis
> of the ESCI module.
>
> \+ Note that, for the main effects, both the website and JASP do not
> return the results of the omnibus test but rather the estimated
> marginal mean contrasts. \[FOOTNOTE Let's unpack this rather cryptic
> statement. It means that for the main effect, it returns the result
> equivalent to the following R code, if you would start from the raw
> data of the study discussed in the example below

#the data can be found here TODO add link

\`\`\`{r, opts.label=\'code\'}

load( \"durante.Rdata\" )

durante_lm \<- lm(RelComp\~Fertility\*RelationshipStatus, mydata.proc)

library(emmeans)

emmeans(durante_lm, pairwise \~ RelationshipStatus)

emmeans(durante_lm, pairwise \~ Fertility)

#but it does not return the result of the R code (for the main effects)

anova(durante_lm)

\`\`\` \]

\+ In R, you can make use of the aovSufficient() function from the HH
package.

[As an example, let's focus again on the Durante et al. (2013) paper I
discussed when talking about statcheck in Section XXX. As a
reminder,]{.mark} they report a significant Fertility x Relationship
Status interaction, F(1, 159) = 6.46, p = .012[. Can we compute them
from the reported summary statistics? Well, no. Sadly enough, even the
summary statistics were not fully reported in the paper, as the reader
is only given the means, not the standard deviations and sample sizes.
But what if they had been reported? Let's have a look. \[FOOTNOTE I
computed some of them from the raw data. So when the data are available
and the summary statistics are not fully reported, obviously you
wouldn't take the conversions approach, but rather move on to reproduce
the raw data (see Section]{.mark} \@sec-reproducibility[).\]]{.mark}

[Fertility RelationshipStatus RelComp s n]{.mark}

[1 High Relationship 5.953611 2.978209 36]{.mark}

[2 Low Relationship 4.876957 3.136663 46]{.mark}

[3 High Single 4.316905 2.914928 42]{.mark}

[4 Low Single 5.623846 2.862675 39]{.mark}

[\`\`\`{r, opts.label=\'code\'}]{.mark}

[d \<- data.frame(]{.mark}

[Fertility = c(\"High\", \"Low\", \"High\", \"Low\"),]{.mark}

[RelationshipStatus = c(\"Relationship\", \"Relationship\", \"Single\",
\"Single\"),]{.mark}

[RelComp = c(5.953611, 4.876957, 4.316905, 5.623846),]{.mark}

[s = c(2.978209, 3.136663, 2.914928, 2.862675),]{.mark}

[n = c(36, 46, 42, 39)]{.mark}

[)]{.mark}

durante_suf \<- aovSufficient(RelComp\~Fertility\*RelationshipStatus,

> data = d,
>
> weights = d\$n,
>
> sd = d\$s)

summary(durante_suf)

\`\`\`

This neatly reproduces the reported F and p values. \[FOOTNOTE and the
values you would get when using the raw data and anova(durantel_lm)).\]
That's pretty cool.

FOOTNOTE\[There is one quirk I need to mention. The aovSufficient()
produces residuals, because R kind of expects it to. You can check them
using resid(durante_suf). However, t[he documentation]{.mark}
aovSufficient() [warns that these residuals are fake. This is not a
problem for our current purposes, because we don't use the residuals
whatsoever, but it does mean that if you would want to use the
residuals, for example to do a test on their normality, doing so would
be totally meaningless.\]]{.mark}

Don't get too excited, though. Remember, I have been cheating. I did not
use the reported summary statistics, but rather computed the summary
statistics based on the raw data. This means I had the summary
statistics in a very precise form. Summary statistics, when reported,
are often reported much less precise. Had Durante et al. (2013) reported
their summary stats, it would probably have looked something like this:

[Fertility RelationshipStatus RelComp s n]{.mark}

[1 High Relationship 5.95 2.98 36]{.mark}

[2 Low Relationship 4.88 3.14 46]{.mark}

[3 High Single 4.32 2.91 42]{.mark}

[4 Low Single 5.62 2.86 39]{.mark}

Using the aovSufficient() magic with *these* summary statistics, I get
an F value of [6.389]{.mark} and a p value of [0.0125. There is a small
but clear mismatch with the F and p values reported in the paper, but
there is absolutely nothing wrong with their analysis or
reporting.]{.mark}

[\`\`\`{r, opts.label=\'code\'}]{.mark}

[\# create the data frame]{.mark}

[d_r \<- data.frame(]{.mark}

[Fertility = c(\"High\", \"Low\", \"High\", \"Low\"),]{.mark}

[RelationshipStatus = c(\"Relationship\", \"Relationship\", \"Single\",
\"Single\"),]{.mark}

[RelComp = c(5.95, 4.88, 4.32, 5.62),]{.mark}

[s = c(2.98, 3.14, 2.91, 2.86),]{.mark}

[n = c(36, 46, 42, 39)]{.mark}

[)]{.mark}

durante_suf_r \<- aovSufficient(RelComp\~Fertility\*RelationshipStatus,

> data = d_r,
>
> weights = d_r\$n,
>
> sd = d_r\$s)

summary(durante_suf_r)

\`\`\`

This example again [illustrates two things: using aovSuffcient() to do a
2x2 ANOVA based on summary statistics and the dangers of
rounding.]{.mark}

\^ Simple effects. Many authors will follow up on this analysis by
looking at simple effects, and so can you!

- If you want to do this in your browser, go here
  [[https://www.graphpad.com/quickcalcs/posttest1/]{.underline}](https://www.graphpad.com/quickcalcs/posttest1/).
  You will need to input from the previous analysis, in particular the
  mean square and the degrees of freedom of the residuals.

- In JASP, you can again use the 2x2 factorial Means and Medians
  analysis of the ESCI module.

- In R, you can use the emmeans() and contrast() functions from the
  emmeans package, building on the output of the previous analysis.

In the statcheck example, we already encountered the simple effect
analyses Durante et al. (2013) performed to follow up on their
interaction analysis. They find that "women in relationships reported
more religiosity if they were in the high-fertility group than if they
were in the low-fertility group \... and that single women reported
significantly less religiosity if they were in the high-fertility group
than if they were in the low-fertility group".

V1 XXX The relevant statistical results are F(1, 159) = 2.63, p = .11
and F(1,159) = 3.89, p = .050, respectively. \[FOOTNOTE: Note that these
are not identical to the values reported by Durante et al. (2013), but I
have corrected the values, so these values differ slightly from the
values reported by Durante et al. (2013) See footnotes XXX and XXX for
more information. Also note that, by the dominant criteria for
statistical significance, the p-value of .11 would not be taken as
indicating a significant difference.\] Doing these analyses using just
the summary statistics would go something like this using R, using the
data from Table XXX (which are the summary data which are way more
precise then typically reported):

\`\`\`{r, opts.label=\'code\'}

> library(emmeans)
>
> emm_durante \<- emmeans(durante_suf, \~ Fertility \|
> RelationshipStatus)
>
> contrast(emm_durante, method = \"pairwise\")

\`\`\`

[This leads to F statistics of 2.634317 and 3.886958 and p-values of
0.10655806 and 0.05039779, so there is a perfect match (to the corrected
values, that is).]{.mark} When, in contrast, using the data from Table
XXX (which are the summary data as they probably would appear in the
paper had they been reported), w[e find F statistics 2.602668 and
3.846983 and p values 0.10866696 and 0.05158211.]{.mark} Again, the
mismatch between the recomputed value and the reported values is no
reason to think Durante et al. (2013) did something wrong, but is just a
result of imprecise reporting due to rounding.

V2 XXX The relevant statistical results are F(1, 159) = 2.64, p = .10
and F(1,159) = 3.88, p = .050, respectively. Doing these analyses using
just the summary statistics would go something like this using R, using
the data from Table XXX (which are the summary data as they probably
would appear in the paper had they been reported).

\`\`\`{r, opts.label=\'code\'}

> library(emmeans)
>
> emm_durante_r \<- emmeans(durante_suf_r, \~ Fertility \|
> RelationshipStatus)
>
> contrast(emm_durante, method = \"pairwise\")

\`\`\`

w[e find F statistics 2.602668 and 3.846983 and p values 0.10866696 and
0.05158211. For the first simple effect, we know from our statcheck
analysis is SectionXXX that something is wrong, and the mismatch is not
just due to rounding. For the second simple effect, howeer,]{.mark} we
can not know that the mismatch between the recomputed value and the
reported values is a reason to think Durante et al. (2013) did something
wrong, or is just a result of imprecise reporting due to rounding.
\[FOOTNOTE: Readers of footnote XXX will know the answer, because the
values are wrong, but these footnotes have relied on access to the raw
data, which we pretend not to have.\]

\^ Regression: The simplest case is to compute t from b/SE, but more
advanced options, starting from rougher summaries are possible. It is,
for example, possible to recompute the regression coefficients from
summary statistics such as the (co)variances. I am currently playing
around with R code and a website to make those more advanced cases easy
for you, and I hope to be able to include them in a future version of
these notes.

\^ In a future version, I plan to extend this section to include the
computation of effect sizes (and confidence intervals, to the extent
they are not yet included in the tools discussed above) based on summary
statistics. If you can't wait and want to have a go already, you will
probably need to look into the various functions starting with ci. from
the MBESS and statpsych packages and various effect size packages (see
also
https://dgbonett.sites.ucsc.edu/statistical-methods-for-psychologists/).

\^ This is a much recommended website with some more of this type of
conversions for a bit more exotic and less frequently used analyses
[[https://www.graphpad.com/quickcalcs/]{.underline}](https://www.graphpad.com/quickcalcs/).

## internal conversion: the inequality edition{#internalinequality}

Unlike the other internal conversions, the next ones involve an
inequality.

\^ standard deviation vs range: The next little nugget of wisdom is
almost 100 years old, but I first read about it in AITFM. It is called
Popviciu's inequality on variances ( []{.mark}[[Popoviciu\'s inequality
on variances -
Wikipedia]{.underline}](https://en.wikipedia.org/wiki/Popoviciu%27s_inequality_on_variances);
see also section 4.1.5 of AITFM): the maximum of the sample standard
deviation is (roughly) half the range. Formally, while Popoviciu found
that sigma\^2 \<= 1/4 R\^2 or sigma \<= 1/2 R, where R is the range,
translating this to the sample standard deviation (i.e., that one that
you are looking at), we have s \<- sqrt(n/(n-1)) R/2 xxx. So if the
range of some score is 0 to 32, finding a standard deviation much larger
than 16 would be very suspect. range in methods section material xxx

\^ standard deviation vs range for binary data: This expression is
merely a special case of the above but deserves a special mention. Since
for binary data, the maximum and minimum are 1 and 0, R = 1, so the
above inequality reduces to s \<= sqrt(n/(n-1)​ 1/2. This means that when
n is large, the maximum of the sample standard deviation is always
approximately . 5.​

\^ correlation vs reliability: A well known result in psychometrics
(related to the adage that reliability is an upper bound to validity;
see e.g. macdonald TODO add ref) holds that when you have two measure X
and Y, r(X,Y) \<= sqrt(rXX') sqrt(rYY'), where rXX' is the reliability
of X. This result has inspired people
[[https://journals.sagepub.com/doi/10.1111/j.1745-6924.2009.01125.x]{.underline}](https://journals.sagepub.com/doi/10.1111/j.1745-6924.2009.01125.x)
\[Brought to you by the people who brought you the crowd within effect
discussed in Section XXX and someone who did a replication study on the
single women and religiosity study discussed in Section XXX. Don't you
just love it when things click?\] to claim that "the reliabilities of
two measures provide an upper bound on the possible correlation that can
be observed between the two measures". While this is true algebraically,
I am less sure about how useful it is in practice, for several reasons.

- One is that it is only true if the assumptions of Classical Test
  Theory (CTT) hold. One of these assumptions is the independence of
  errors, and this is very unlikely to hold.

- Another is that it requires the computation of reliability. While
  there are more reliability coefficients than anyone actually asked
  for, there is a difference between a reliability coefficient and
  reliability. These coefficients are only equal to reliability if
  another set of assumptions is met, which is again often not the case.
  For example, the test-retest reliability coefficient and the
  Spearman-Brown split-half coefficient only equal reliability if
  parallelism can be assumed, and Cronach's alpha is only equal to
  reliability if all items are equivalent (and it is a lower bound to
  reliability if not).

Consider for example a situation where both measures have a reliability
of .7 and an alpha of .6. Suppose now you observe a correlation of .65
between both measures. If you would mistakenly think that alpha equals
reliability, this correlation seems puzzlingly high (as anything above
.6 is) but it is not! Only a reliability higher than .7 is suspect
(given all the other caveats).

- But even if all assumptions are for the relation to hold, your
  troubles are still not over. All these relations do not consider
  sampling errors and are therefore only correct at the population
  level. At the sample level, which you inevitably are at when
  evaluating a paper, these relationships may no longer hold, even when
  all CTT and additional assumptions hold. Applying an expression that
  holds at the population level but not at the sample level at that very
  sample level seems misguided. \[FOOTNOTE Psychometricians are partly
  to blame for the misapplication of this expression. Cronbach notes
  that (in Cronbach & Shavelson, 2004, p. 401 TODO add ref) that in
  "'the history of psychometric theory, there was virtually no attention
  to \... \[the\] distinction \[between results for the sample and
  results for the population\] prior to 1951, save in the writings of
  British-trained theorists." and Cho TODO add ref, insightfully as
  always, continues to remark that "\[w\]e have not yet abandoned this
  legacy, and much of the psychometric literature still does not
  distinguish well between population and sample levels."\]
  [[https://www.researchgate.net/profile/Eunseong-Cho-2/publication/356726483_The_Accuracy_of_Reliability_Coefficients_A_Reanalysis_of_Existing_Simulations/links/61f6a52b007fb5044726069d/The-Accuracy-of-Reliability-Coefficients-A-Reanalysis-of-Existing-Simulations.pdf]{.underline}](https://www.researchgate.net/profile/Eunseong-Cho-2/publication/356726483_The_Accuracy_of_Reliability_Coefficients_A_Reanalysis_of_Existing_Simulations/links/61f6a52b007fb5044726069d/The-Accuracy-of-Reliability-Coefficients-A-Reanalysis-of-Existing-Simulations.pdf)

## external conversion{#external}

\^ We continue to convert the reported numbers into something else, but
instead of comparing the result of our conversion to a number reported
in the paper, we compare it to something that is not in the paper.

\^ the mean, the variance, and the sample size for integers vs an
integer: Another insight which holds for integers is from
[[https://aurelienallard.netlify.app/post/anaytic-grimmer-possibility-standard-deviations/]{.underline}](https://aurelienallard.netlify.app/post/anaytic-grimmer-possibility-standard-deviations/)
The idea is to compute (n-1)\*s\^2 + n\*xbar\^2, where n is the sample
size, s is the sample standard deviation and xbar is the sample mean.
This somewhat odd looking combo of summary statistics should not be
compared to another published statistic (if that was the case, it would
be in the internal conversion approach). Rather, it can be shown that
this result is an integer. What's more, if the parity of that integer
(i.e., whether it is even or odd), should be the same as the parity of
the rounded value of n\*mean.

- In your browser, you can go to
  [[http://www.prepubmed.org/grimmer_sd]{.underline}](http://www.prepubmed.org/grimmer_sd)
  or
  [[http://www.prepubmed.org/grimmer_se]{.underline}](http://www.prepubmed.org/grimmer_se)
  or
  [[http://www.prepubmed.org/grimmer_var]{.underline}](http://www.prepubmed.org/grimmer_var)
  (depending on whether the exact input is a standard deviation, a
  variance or a standard error xxx se can even be done without mean)

- Doing it in R is relatively simple using your own code or using the
  grimmer() or GRIMMER_test() functions.

As an example, let's say you come across these data: A sample size of 22
participants, with a reported mean of 2.59 and a reported standard
deviation of 1.14[.]{.mark}

\`\`\`{r, opts.label=\'code\'}

n \<- 22

mean \<- 2.59

sd \<- 1.14

int_computed \<- (n-1)\*sd\^2 + n\*mean\^2

\`\`\`

The simple code yields [174.8698]{.mark} for int_computed which is most
emphatically not an integer. So this seems to suggest that something is
wrong. However, there is more clever code that tells us to just relax

\`\`\`{r, opts.label=\'code\'}

GRIMMER_test(mean = mean, sd = SD, n_obs = n) or
grimmer(x=\"2.59\",sd=\"1.14\",n=n)

\`\`\`

The reason we can relax is that we are dealing with rounded numbers. The
reported numbers could actually just be approximations to more precise
values.

To see this, just imagine that the numbers used above are just the
rounded, imprecise versions of these numbers?

\`\`\`{r, opts.label=\'code\'}

mean \<- 2.590909

sd \<- 1.140555

int_computed \<- (n-1)\*sd\^2 + n\*mean\^2

\`\`\`

With these values we find int_computed to be equal to 175. Additionally,
this number is odd just like round(n \* mean), so it means the parity
requirement is met. \[FOOTNOTE Further, note that 2.590909 is still a
possible mean, as per Section XXX below\]. So despite n= 22, sd \<- 1.14
and mean \<- 2.59 not yielding an integer value for (n-1)\*sd\^2 +
n\*mean\^2, all is just fine since the reported mean and standard
deviation could be approximations to values for the mean and standard
deviation that do yield and integer (n-1)\*SD\^2 + n\*mean\^2.
Thankfully, the grimmer() and GRIMMER_test() functions take this
important consideration into account.

\^ effect size vs implausible or impossible values: Effect sizes 1) are
not as often reported as they should be and 2) can often be computed
based on summary statistics. While effect sizes are seldom reported, it
will not often be useful for a conversion check (does the converted
effect size match the reported one?), but it can lead to uncovering
anomalies. The underreporting of effect sizes makes checking the
mismatch hard, but there is often a sense to evaluate whether a
standardized effect size is plausible or, for these effect sizes that
have mathematical bounds (correlations, R2, Cramer's V, and the likes)
whether the values are even possible at all. So this strategy is a bit
of a blend of strategies 1 (common sense) and 2 (internal conversion),
and it will involve an inequality. See above for literature and R code
for converting effect sizes.

> \+ Correlation vs bounds: An interesting application of this general
> idea can be found in Section 4.2.2 in AITFM. They convert summary
> statistics into an (unreported) correlation and find a converted
> correlation bigger than 1, which is of course impossible.
> [[https://matthewbjane.quarto.pub/pre-post-correlations/]{.underline}](https://matthewbjane.quarto.pub/pre-post-correlations/)
> gives a delightfully detailed account of how to compute correlations
> from several statistics for repeated measures designs.

## recreation{#recreation}

TODO nog vb met recreation and rounding xxx

\^ The basic idea of the recreation approach is asking: can raw data
exist that give rise to the reported summary data? Your job is to find
these data. This does not necessarily mean you will be able to recreate
the exact raw data that underlie the reported statistics, but *a* data
set that could have given rise to the summary statistics \-\-- which is
not necessarily identical to *the* data set the OAs have used. This is
where most things are starting to become harder to do. Luckily, there
are often tools to help you out! I will list the ones I know, but I will
surely have overlooked some. Or a lot.

\^ Percentages/proportions. The easiest example is about recreating the
frequencies or counts that underlie the reported percentages or
proportions. If you see percentages being reported, you can always ask
yourself whether there is a corresponding integer underlying it. For
example, when the sample size is 67, a percentage of 75% is possible
(when the number of cases was 50), and a percentage of 73% is possible
(when the number of cases was 49), but there is no integer that could
give rise to a percentage of 74%. So if you see 74% in combination with
a sample size of 67 something is off.

- In your browser, you can go to
  [[http://www.prepubmed.org/grim_test/]{.underline}](http://www.prepubmed.org/grim_test/)

<!-- -->

- Here is the R code for that:

\`\`\`{r, opts.label=\'code\'}

n \<- 67

prop_reported \<- .74 #or .75 or .73

prop_rec \<- round(round(n \* prop_reported)/n, 2)

prop_rec #should match prop_reported

#if you want to use a function

grim(\".74\", n = n) #or .75 or .73

GRIM_test(prop_reported, n)

\`\`\`

Using the code above, the proportion based on the recreated data
(prop_rec) matches the reported proportion (prop_reported) when
prop_reported = .75 or .73 but not when prop_reported = .74. Both grim()
and GRIM_test() agree, by returning TRUE, FALSE or TRUE when
prop_reported = .73, .74 or .75, respectively.

\^ Means of integers. A very useful insight from TODO add ref
[[https://journals.sagepub.com/doi/abs/10.1177/1948550616673876]{.underline}](https://journals.sagepub.com/doi/abs/10.1177/1948550616673876)
is that the logic used when thinking about percentages/proportions is
more generally applicable and also applies to means of integers. Which
is good, since we have a lot of integers in psychology, given the
abundance of Likert testing on a 5 or 7 point scale. What they have in
common is that the reported result (a proportion/percentage or a mean of
integers) is the result of the division of one integer (the
frequencies/count or the sum of integers) by another. Again, you can ask
yourself whether the data underlying the reported mean can even exist.

For example, take a scale with response options 1, 2 and 3, and the
reported mean is 2.83. If two persons take the test, the only means that
are possible are 1, 1.5, 2, 2.5, or 3, so 2 is clearly not a sample size
that is compatible with this reported mean. In fact, there are only a
few sample sizes below a certain maximum that are compatible with a mean
of 2.83. One of those is 6, if, for example, the individual data points
are 3,3,3,3,3, and 2 so that the mean = 17/6= 2.833333333

- In your browser, you can use
  [[http://www.prepubmed.org/grim_test/]{.underline}](http://www.prepubmed.org/grim_test/)

- In R, we can do the same as before

\`\`\`{r, opts.label=\'code\'}

> n \<- 6
>
> mean_reported \<- 2.83
>
> mean_rec \<- round(round(n \* mean_reported)/n, 2)
>
> mean_rec
>
> #if you want to use a function
>
> grim(\"2.83\", n = n)
>
> GRIM_test(mean_rep, n)

\`\`\`

Using the code above, the mean based on the recreated data (mean_rec)
matched the reported mean (mean_reported) when n=6 but not when n=2.
Both grim() and GRIM_test() agree, by returning TRUE and FALSE when n=6
and n=2, respectively.

\^ Back to percentages/proportions. A related but slightly different
question is: for which sample sizes could .74 be observed?

- There is no website that I know of that actually does this. However,
  there is one that comes close. In particular, if you use
  [[http://www.prepubmed.org/grim_test]{.underline}](http://www.prepubmed.org/grim_test),
  press Calculate, and on the next page you will be given the option to
  make a plot which shows which sample sizes are possible.

- This is how to do it brute force using R (code taken from AITFM)

\`\`\`{r, opts.label=\'code\'}

maxn=100

results \<- sapply(1:maxn, function(x) grim(\"0.74\",x))

n_rec \<- which(results == TRUE)

n_rec

\`\`\`

It turns out that 67 is not among the possible sample sizes, but there
are sample sizes (such as 66 or 68) for which .74 is possible. Finding
the sample size for a single percentage is typically not directly
useful, but it will turn out useful in the next bit.

\^ Proportions in a 2x2 contingency table. A cute extension of this idea
is described in Section 4.4.3 of AITFM, and involves testing whether
*two* proportions can occur simultaneously, like they do in a 2x2
contingency table.

Suppose a study reports an experimental procedure with a total sample
size of 99, but does not mention the sample sizes in the control and
experimental conditions. (For a fuller explanation, see Section 4.4.3 of
AITFM). The percentage of cases is .342 and .629 in the experimental and
control conditions, respectively. The following R code can be used to
check whether the two percentages can not occur together.

\`\`\`{r, opts.label=\'code\'}

totalN \<- 99

maxn \<- totalN-1

resultsAC \<- sapply(1:maxn, function(x) grim(\"0.342\",x))

true_valuesAC \<- which(resultsAC == TRUE)

#true_valuesAC

#OPTION 1

resultsBD \<- sapply(1:maxn, function(x) grim(\"0.629\",x))

true_valuesBD \<- which(resultsBD == TRUE)

true_valuesBD

true_valuesBDbyAC \<- totalN-true_valuesAC

true_valuesBDbyAC \<- sort(true_valuesBDbyAC\[true_valuesBDbyAC\>0\])

true_valuesBDbyAC

intersect(true_valuesBDbyAC, true_valuesBD)

#OPTION 2

sort(totalN-unname(true_valuesAC)\[grim(\"0.629\",totalN-unname(true_valuesAC))\])

\`\`\`

Running this code tells us there are sample sizes in the experimental
group that could give rise to the reported .342. And that there are
sample sizes in the control group that could give rise to the reported
.629. But we have more information: Because we know the total sample
size, the sample sizes in the experimental group imply a sample size in
the control group. And these implied sample sizes can *not* give rise to
.629. So it turns out there are no sample sizes that simultaneously
could give rise to both reported numbers. This means that something in
the contingency table does not check out.

What if the numbers would have been rounded to .34 and .63? Running the
same code but with updated numbers (not shown) shows that the two
percentages can occur together.

\^ The most direct take on the recreation approach is to randomly
generate data using the summary statistics provided, compute any
statistic of interest from this generated data that was not directly
used to generate the data, repeat this process, say, a 100000 times, and
use these repetitions to get a sense how likely it was to observe the
actually reported summary statistic. This is relatively easy to do, but
relatively hard to interpret, which is a deadly combination, so it
should be used very carefully. \[[Dit proces begrijp ik niet goed. Als
je datasets creëert die allemaal voldoen aan de gegeven summary
statistics, hoe ga je dan een idee krijgen van de waarschijnlijkheid dat
die summary statistics optreden? (want in je samples is dat toch 100%?)
xxx]{.mark}\]

An example of this is provided by TODO add ref
[[https://journals.sagepub.com/doi/10.1177/0956797613480366]{.underline}](https://journals.sagepub.com/doi/10.1177/0956797613480366).
The (first) example focuses on a study with three conditions, for which
the sample sizes, means, ranges, and standard deviations are reported.
The interest is in the similarity of the three ranges. Similarity is
quantified by computing the standard deviation across the three values.
As the ranges for the three conditions in one of the studies are 76, 76
and 74, their dissimilarity score (which is just the standard deviation
of these three numbers) is 1.15. So the question becomes, how likely is
it to observe three standard deviations that are that similar or even
more similar, or, formally, what is the probability that a study with
three conditions produces data with a similarity score for the standard
deviations equal to smaller than 1.15? The following simulation gives an
approximate answer to this probability, using two different ways to
construct the covariance matrix Sigma based on the reported standard
deviations.

\`\`\`{r, opts.label=\'code\'}

library(MASS)

nsim \<- 100000 \# number of simulations

m \<- 15

mean_vec \<- c(39.74, 85.74, 65.73) \# mean1 mean2 mean3

sd_vec \<- c(25.09, 24.58, 25.65)

#option 1 all the same

Sigma\<- mean(sd_vec\^2)\*diag(length(sd_vec))

#Sigma

#option 2 all different

Sigma \<- diag(sd_vec\^2) \# diagonal covariance matrix

res \<- numeric(nsim)

for(i in 1:nsim){

X \<- mvrnorm(n = m, mu = mean_vec, Sigma = Sigma)

res1 \<- round(diff(range(X\[,1\])))

res2 \<- round(diff(range(X\[,2\])))

res3 \<- round(diff(range(X\[,3\])))

res\[i\] \<- sd(c(res1, res2, res3)) #compute similarity score

}

\# the reported ranges

range_vec \<- c(76, 76, 74)

#the similarity score of the reported summary statistics of interest
(ranges)

rep \<- sd(range_vec)

mean(res \< rep) \* 100

#a very basic histogram for quick checking

hist(res)

abline(v = rep, col = \"red\", lwd = 2)

\`\`\`

Both options for the construction of Sigma lead to a similarly small
probability of less than a half percent.

Note that the similarity (of the ranges, the means or the standard
deviations) is just one example you could consider. The simulation-based
recreation technique applies to any aspect of the reported summary
statistics you may find interesting in a paper, and is by no means
restricted to just similarity. However, similarity is often a good thing
to check, because it is a priori unlikely that summary statistics are
identical or very similar across conditions.

Let's now look at the same but this time with standard deviations
instead of ranges. The code is very similar. I round up to two decimal
places to match the precision of the reported standard deviations.

\`\`\`{r, opts.label=\'code\'}

dp \<- 2 #decimal places of the statistic of interest

res \<- numeric(nsim)

for(i in 1:nsim){

X \<- mvrnorm(n = m, mu = mean_vec, Sigma = Sigma)

res1 \<- round(sd(X\[,1\]),dp)

res2 \<- round(sd(X\[,2\]),dp)

res3 \<- round(sd(X\[,3\]),dp)

res\[i\] \<- sd(c(res1, res2, res3)) #compute similarity score

}

#the similarity score of the reported summary statistics of interest
(standard deviations)

rep \<- sd(sd_vec)

mean(res \< rep) \* 100

hist(res)

abline(v = rep, col = \"red\", lwd = 2)

\`\`\`

Again, the probability of observing a set of standard deviations that
are this similar (or more similar) is very small. Typically, you would
see standard deviations that are farther apart.

The obvious dangers of this simulation based-recreation approach are
twofold. First, the probability is conditional on the reasonableness of
the assumptions made when generating the data. In this example, we
assumed the data were normally distributed, but maybe they were not.
Second, even rare things happen, so you might have just witnessed
something very very special! For these reasons, the strongest conclusion
that can come from this approach is that the probability is small enough
to warrant contacting the OAs asking for the raw data. Without raw data,
compelling conclusions are impossible from this approach.

\^ SPRITE (by random walk)
[[https://peerj.com/preprints/26968/]{.underline}](https://peerj.com/preprints/26968/)
TODO add ref, CORVIDS (by exhaustion) TODO add ref
[[katherinemwood/corvids: Source code for the CORVIDS data
reconstruction
system]{.underline}](https://github.com/katherinemwood/corvids) and an
unnamed method by Morey TODO add ref
[[https://bayesfactor.blogspot.com/2016/03/how-to-check-likert-scale-summaries-for.html]{.underline}](https://bayesfactor.blogspot.com/2016/03/how-to-check-likert-scale-summaries-for.html)
bring the data recreation idea to next level, and search through
plausible set of values that underlie a reported mean, standard
deviation and sample size of integer-style data. This allows users to
inspect the distribution of possible underlying raw data that give rise
to the reported summary stats. Whether or not those recreated data look
sus or chill is still up to you, though. See Section XXX of AITFM if you
want to know more. SPRITE is implemented in the rsprite2 package [[CRAN:
Package
rsprite2]{.underline}](https://cran.r-project.org/web/packages/rsprite2/index.html)
(also see here [[rSPRITE beta
0.18]{.underline}](https://shiny.ieis.tue.nl/sprite/) and here
[[http://www.prepubmed.org/sprite/]{.underline}](http://www.prepubmed.org/sprite/)
). For CORVIDS, there is no R package that I know of.

## rounding beware{#rounding}

\^ None of the conversion techniques discussed above are very
complicated. Or, at least, not very complicated to understand. Using
them in practice is a bit more of a challenge. The reason is that the
numbers we want to convert and the numbers we want to recompute have
been rounded.

\^ When converting numbers based on other reported numbers the goal
should never be to convert the numbers to provide a perfect match to
another number. A perfect match is often not possible, but for other,
less interesting, reasons than that the OAs make a mistake in their
analysis or in their reporting. As demonstrated in several examples
above, a mismatch can often be explained by rounding: the numbers
reported in the papers are rounded and are therefore not the numbers
that have been used to compute the other numbers. When not perfect is
good enough is a terribly difficult question to answer, both when
investigating research and in real life.

\^ We have come across several examples where the conversion did not
yield the reported statistics exactly, but still the OAs made no error
at all in their analysis or reporting! The reason was always the same:
when numbers are being reported in a paper, they are rounded, which
means we are dealing with approximations to the numbers that were
actually used in the computations.

Take a reported number rounded to two decimal places, like 2.93. Before
rounding, it could have been anything ranging from 2.925 to
2.9349999\... . We don't even know the precision, so it might correspond
to an actual value of 2.926, 2.9261, 2.92619, and so on. The rounded
numbers are not identical to the numbers that really went into the
computation of the, say, a p-value, but they are only approximations to
the numbers that were really used.

\^ Some functions (e.g., GRIMMER_test()) and websites (like
[[http://www.prepubmed.org/data_thugging/]{.underline}](http://www.prepubmed.org/data_thugging/))
are clever enough to deal with the curse of rounding. Others (e.g.,
tsum_test()) do not. So be aware when failing to recompute a statistic
by conversion. Because of the precision loss introduced by rounding, the
mismatch between recomputed and reported numbers might not mean what you
think it means.

\^ When the code does not, you will need to do a **range analysis**
before jumping to conclusion. This means that if you convert the number
2.93 to another number, you should really consider a range of numbers,
all of which would yield 2.93 when rounding, implying a range of
computed values. Rounding implies that conversion does not generate a
single recomputed p-value or standard deviation. Rather, it yields a
range of recomputed values, based on a range of potential input numbers.
So if you want to draw any firmer conclusion than "the conversions lead
to numbers that are ballpark similar than the reported number", you will
need to explicitly investigate this range of potentials means and
standard deviations, all compatible with the reported rounded versions,
implying a range of recomputed p-values. All these values are possible
since they all are compatible with the rounded reported statistics and
are therefore consistent conversions.

\^ One way to do this is by making use of simulations. The basic idea is
sample: do whatever analysis you did with the reported statistics, but
instead of using the reported statistics, use a version that, when
rounded, becomes the reported statistics. Repeat that process a lot. For
example, if a mean is 0.46, the underlying number could be anything
between 0.455 and 0.465. Generating a value like this can be done as
follows:

mean1 \<- .46

mean1_r \<- runif(1, mean1-0.005, mean1+0.005)

Using the procedure, round(mean1_r,2) will yield .46.

Of course, if the mean is reported as .463, you have the change the code
as follows

mean1 \<- .463

mean1_r \<- runif(1, mean1-0.0005, mean1+0.0005)

The more generic version is as follows:

mean1 \<- .463

dp \<- 3 #decimal places

eps \<- [10\^(-dp)/2]{.mark}

mean1_r \<- runif(1, mean1-eps, mean1+eps)

Using this procedure, round(mean1, dp) will yield .463.

\^ To illustrate this approach, we will focus again on computing the
overall mean and standard deviation from the subgroup means, standard
deviations, and sample sizes (see Section XXX). Let's first do it for
the strange standard deviation encountered in the race erased example
(see Section XXX). In that example, we could not convert the group level
standard deviations to the overall standard deviation. I already spoiled
that the fact that we could not recompute the convert the summary
statistics to the overall standard deviation was due to rounding, but I
could only tell you that because I have access to the raw data. With the
following straightforward simulation code, you can find it whether it is
possible that the mismatch is a result of rounding.

\`\`\`{r, opts.label=\'code\'}

n1 \<- 225

mean1 \<- 33.25

sd1 \<- 10.92

n2 \<- 238

mean2 \<- 33.47

sd2 \<- 10.58

nsim \<- 100000

results \<- matrix(NA, nrow = nsim, ncol = 6)

for (i in 1:nsim) {

mean1_r \<- runif(1, mean1-0.005, mean1+0.005)

mean2_r \<- runif(1, mean2-0.005, mean2+0.005)

sd1_r \<- runif(1, sd1-0.005, sd1+0.005)

sd2_r \<- runif(1, sd2-0.005, sd2+0.005)

mt_com \<- (n1 \* mean1_r + n2 \* mean2_r)/(n1 + n2)

var_com \<- ((n1 - 1) \* sd1_r\^2 + (n2 - 1) \* sd2_r\^2 + n1 \*
(mean1_r - mt_com)\^2 + n2 \* (mean2_r - mt_com)\^2)/(n1 + n2 - 1)

sd_com=sqrt(var_com)

sd_com

results\[i,1\] \<- mean1_r

results\[i,2\] \<- mean2_r

results\[i,3\] \<- sd1_r

results\[i,4\] \<- sd2_r

results\[i,5\] \<- mt_com

results\[i,6\] \<- sd_com

}

n_o \<- 463 #overall

mean_o \<- 33.36 #overall

sd_o \<- 10.73 #overall

discrepancy \<- abs(round(results\[, 5\],2) - mean_o) +
abs(round(results\[, 6\],2) - sd_o)

m_sorted \<- results\[order(discrepancy), \]

#m_sorted \<- results\[order(abs(round(results\[,6\],2) - sd_o)), \]

head(m_sorted)

round(head(m_sorted),2)

mean(discrepancy==0)

\`\`\`

As it turns out, there are quite a lot of values of the summary
statistics that produce the correct result. In fact, we don't care that
there are many. Even one would have been enough to explain away the
discrepancy as due to rounding! These values for the means and standard
deviations 33.24959, 33.47244, 10.91628 and 10.57754, for example,
produce both the reported subgroup level means and standard deviations
when rounded, and also produce the correct overall mean and standard
deviation when rounded. This means that, instead of concluding that the
mismatch between the computed standard deviation (based on rounded
summary statistics) and the reported standard deviation should raise
eyebrows, we should conclude that, *when rounding is taken into
account*, the conversion from group level to overall level provides a
match.

\^ In the depression and category learning example, we could also not
convert the overall standard deviation, and I have told you, while
cheating by looking at the raw data, that this was a real error, not a
rounding issue. Could I have told you the same without having access to
the raw data? Let's see!

\`\`\`{r, opts.label=\'code\'}

n1 \<- 101

mean1 \<- 25.61

n2 \<- 137

mean2 \<- 6.47

sd1 \<- 9.09

sd2 \<- 4.14

nsim \<- 100000

results \<- matrix(NA, nrow = nsim, ncol = 6)

for (i in 1:nsim) {

mean1_r \<- runif(1, mean1-0.005, mean1+0.005)

mean2_r \<- runif(1, mean2-0.005, mean2+0.005)

sd1_r \<- runif(1, sd1-0.005, sd1+0.005)

sd2_r \<- runif(1, sd2-0.005, sd2+0.005)

mt_com \<- (n1 \* mean1_r + n2 \* mean2_r)/(n1 + n2)

var_com \<- ((n1 - 1) \* sd1_r\^2 + (n2 - 1) \* sd2_r\^2 + n1 \*
(mean1_r - mt_com)\^2 + n2 \* (mean2_r - mt_com)\^2)/(n1 + n2 - 1)

sd_com=sqrt(var_com)

sd_com

results\[i,1\] \<- mean1_r

results\[i,2\] \<- mean2_r

results\[i,3\] \<- sd1_r

results\[i,4\] \<- sd2_r

results\[i,5\] \<- mt_com

results\[i,6\] \<- sd_com

}

n_o \<- 238 #overall

mean_o \<- 14.60 #overall

sd_o \<- 11.59 #overall

discrepancy \<- abs(round(results\[, 5\],2) - mean_o) +
abs(round(results\[, 6\],2) - sd_o)

m_sorted \<- results\[order(discrepancy), \]

#m_sorted \<- results\[order(abs(round(results\[,6\],2) - sd_o)), \]

head(m_sorted)

round(head(m_sorted),2)

mean(discrepancy==0)

\`\`\`

Now, despite XXX tries, we could not find a subgroup level statistics
(assuming the sample sizes are correct) that, when rounded, can convert
the the correct, rounded overall mean and standard deviation, suggesting
(well, confirming in this case) that the mismatch is not due to
rounding.

\^ With similar code, you can do the same for the crowd within
replication we encountered when discussing the two samples independent
samples t test. Remember from Section XXX that, based on the summary
statistics reported by Steegen et al. (2014), we could not match the
reported results, t(609) = 0.18, p = 0.858. Because we have the raw
data, we have been able to explain this discrepancy as being the result
of rounding, but if we don't have access to the data, we will need
simulations to check if something is wrong.

\`\`\`{r, opts.label=\'code\'}

meanx \<- 50

meany \<- 48

sdx \<- 147

sdy \<- 119

nx \<- 140

ny \<- 471

nsim \<- 100000

results \<- matrix(NA, nrow = nsim, ncol = 6)

for (i in 1:nsim) {

meanx_r \<- runif(1, meanx-0.5, meanx+0.5)

meany_r \<- runif(1, meany-0.5, meany+0.5)

sdx_r \<- runif(1, sdx-0.5, sdx+0.5)

sdy_r \<- runif(1, sdy-0.5, sdy+0.5)

t=tsum.test(mean.x = meanx_r,

mean.y = meany_r,

s.x = sdx_r,

s.y = sdy_r,

n.x = nx,

n.y = ny,

alternative = \"two.sided\",

var.equal = TRUE)

results\[i,1\] \<- meanx_r

results\[i,2\] \<- meany_r

results\[i,3\] \<- sdx_r

results\[i,4\] \<- sdy_r

results\[i,5\] \<- t\$statistic

results\[i,6\] \<- t\$p.value

}

p_reported \<- 0.858

m_sorted \<- results\[order(abs(round(results\[,6\],3) - p_reported)),
\]

head(m_sorted)

#only look at scenarios that yield the p_reported

results_c \<- results\[round(results\[,6\],3)==p_reported,\]

reported_t \<- 0.18

mc_sorted \<- results_c\[order(abs(round(results_c\[,5\],2) -
reported_t)), \]

head(mc_sorted)

dim(results_c)\[1\]/nsim

mean(round(results\[,6\],3)==p_reported)

\`\`\`

It turns out that more than 1% of the generated data sets 1) yield the
reported summary statistics when rounded and 2) yield the reported
p-values when not rounded. So there are quite a lot of values of the
summary statistics that produce the correct result (and even 1 would
have been enough to explain away the discrepancy as due to rounding!)
This means that, instead of concluding that the mismatch between the
computed p-value (based on rounded summary statistics) and the reported
p-value should raise eyebrows, we should conclude that, *when rounding
is taken into account*, the conversion from summary statistics to
p-value provides a match.

\^ What about the other strange t statistic we encountered, in the race
erased replication example? Remember that when var.equal = F, we could
find the reported t-statistic from the summary data, but not the
reported degrees of freedom. With var.equal = T, we could find the
reported degrees of freedom but found a t-statistics of 9.16 instead of
the reported 9.26. Because we have the raw data, we know that the
mismatch was not due to rounding but by a clear and unprovoked error.
But what if we did not have the data? Can we use simulations to rule out
rounding as an explanation for the mismatch? Let's see, using very
similar code as in the previous example. We will try to find out whether
the 9.16 (the t-statistic we found when setting var.equal = T) could be
a 9.26 in disguise (the reported one) because of rounding issues.
FOOTNOTE \[Alternatively, we could try to find whether the 418.77 (the
degrees of freedom we found when setting var.equal = F) could be a 461
in disguise (the reported one) because of rounding issues, but this
scenario is less likely because setting var.equal = F is unlikely to
produce an integer like 461.\]

\`\`\`{r, opts.label=\'code\'}

n1 \<- 225

m1 \<- 0.50

s1 \<- 2.78

n2 \<- 238

m2 \<- 3.50

s2 \<- 4.10

nsim \<- 100000

results \<- matrix(NA, nrow = nsim, ncol = 6)

for (i in 1:nsim) {

meanx_r \<- runif(1, m2-0.005, m2+0.005)

meany_r \<- runif(1, m1-0.005, m1+0.005)

sdx_r \<- runif(1, s2-0.005, s2+0.005)

sdy_r \<- runif(1, s1-0.005, s1+0.005)

t=tsum.test(mean.x = meanx_r,

mean.y = meany_r,

s.x = sdx_r,

s.y = sdy_r,

n.x = n2,

n.y = n1,

alternative = \"greater\",

var.equal = T)

results\[i,1\] \<- meanx_r

results\[i,2\] \<- meany_r

results\[i,3\] \<- sdx_r

results\[i,4\] \<- sdy_r

results\[i,5\] \<- t\$statistic

results\[i,6\] \<- t\$p.value

}

reported_t \<- 9.26

hist(results\[,5\])

mean(round(results\[,5\],3)==reported_t)

\`\`\`

The simulation reveals that, this time, rounding is *not* a sufficient
explanation of why in the race erased example we found a t-statistic of
9.16 instead of the reported 9.26. Out of our 1000000 xxx veel hoger
xxxtries, we could not generate a single data set that produced the
exact t-value as reported! Even if we allow for rounding, 9.26 is way
outside the range of t-statistics that can be generated. This finding is
of course compatible with our above observation that the mismatch is not
due to rounding but due to a reporting error.

FOOTNOTE\[ Above, we focused on the question of whether there is one (or
more, but one is enough) data set that yields a p-value (or t-statistic)
identical to the reported one. [[OSF \| Rounded Input Variables, Exact
Test Statistics
(RIVETS)]{.underline}](https://osf.io/preprints/psyarxiv/ctu9z_v1) TODO
add ref argue that it is also insightful to look at the proportion of
simulated data sets that yield a p-value (or t-statistic) identical to
the reported one (i.e, mean(round(results\[,6\],3)==p_reported) ). The
argument is that if this proportion is sufficiently low, there is some
evidence that the summary statistics are not a result of the "normal
process of allowing a statistical package to calculate everything in one
run starting with the raw data points" but are indicative that "the test
statistic may have been calculated "by hand"---for whatever
reason---from the rounded

descriptive statistics". The idea is to use simulations like the ones
shown above to check whether truncation has occurred at some point
during the statistical process (which suggests data meddling, since
software packages typically only round at the very end). This has been
called RIVETS TODO and is discussed in Section 4.5 of AITFM. While the
basic observation is true, finding a justified threshold of what should
count as "too low" is needed before this method can be used in any
serious application. Above, we have found that for the perfectly fine
crowd-within example, this proportion was slightly above 1%.\]

\^ The previous examples focused on the independent samples t-test, but
the same approach applies to other examples as well, like for example
anova. xxx TODO check range from
[[http://www.prepubmed.org/anova/]{.underline}](http://www.prepubmed.org/anova/)
TODO: check the other examples where we know the discrepancy is due to
rounding

Remember how, in Section XXX, we could not find the f and p values for
the two simple effects in Durante et al. (2013) based on the reported
summary statistics? Let's see if rounding can be an explanation for
these mismatches.

\`\`\`{r, opts.label=\'code\'}

nsim \<- 1000

results \<- matrix(NA, nrow = nsim, ncol = 12)

eps \<- 0.005

for (i in 1:nsim) {

data\$RelComp_r \<- runif(nrow(data), data\$RelComp - eps,
data\$RelComp + eps)

data\$s_r \<- runif(nrow(data), data\$s - eps, data\$s + eps)

fit_durante \<- aovSufficient(RelComp_r\~Fertility\*RelationshipStatus,

data = data,

weights = data\$n,

sd = data\$s_r)

#simple effect

emm_durante \<- emmeans(fit_durante, \~ Fertility \| RelationshipStatus)

con_durante_d \<- contrast(emm_durante, method = \"pairwise\")

f \<- (summary(con_durante_d)\$t.ratio)\^2 #F

p \<- (summary(con_durante_d)\$p.value)

results\[i,1:4\] \<- data\$RelComp_r

results\[i,5:8\] \<- data\$s_r

\# results\[i,3\] \<- sdx_r

\# results\[i,4\] \<- sdy_r

results\[i,9:10\] \<- f #\$t\$statistic

results\[i,11:12\] \<- p #t\$p.value

}

p_reported1 \<- 0.10

f_reported1 \<- 2.64

discrepancy1 \<- abs(round(results\[, 9\],2) - f_reported1) +
abs(round(results\[, 11\],2) - p_reported1)

m_sorted \<- results\[order(discrepancy1), \]

head(m_sorted)

mean(discrepancy1==0)

p_reported2 \<- 0.050

f_reported2 \<- 3.88

discrepancy2 \<- abs(round(results\[, 10\],2) - f_reported2) +
abs(round(results\[, 12\],3) - p_reported2)

m_sorted \<- results\[order(discrepancy2), \]

head(m_sorted)

mean(discrepancy2==0)

results\[discrepancy2==0, \]

\`\`\`

The first simple effect held that "women in relationships reported more
religiosity if they were in the high-fertility group \... than if they
were in the low-fertility group \..., F(1, 159) = 2.64, p = .10". No
summary statistics have been found that lead to the reported, rounded
summary statistics and to the reported, rounded f statistic and p-value,
confirming the findings by statcheck and by our cheat-peek at the raw
data (see Section XXX) that there is something more going on then
rounding.

The second simple effect held that "\[s\]ingle women reported
significantly less religiosity if they were in the high-fertility group
\... than if they were in the low-fertility group \... F(1, 159) = 3.88,
p = .050". Our simulation finds summary statistics that lead to the
reported, rounded summary statistics and to the reported, rounded f
statistic and p-value, confirming the findings by statcheck that all is
good and that the observed mismatch could be due to rounding. You might
remember from footnote XXX that inspection of the raw data revealed
t/hat something is wrong with these numbers (in particular, 3.88 should
have been 3.89), underscoring that passing a check does not necessarily
mean all is good!

\^ In the simulation based recreation approach (see Section
\@sec-recreation), we compared the similarity of the reported standard
deviations to the similarity of the generated standard deviations. The
similarity of the reported standard deviations, however, can be
misleading for the reason I by now hopefully don't have to explain: the
reported standard deviations are rounded. The values 1, 1 and 1 are
maximally similar (standard deviation of 0), but if they are rounded
versions of .9500, 1.000, and 1.049, they are not (standard deviation of
.05)! So a better approach is to factor in the possibility that the
similarity of the reported numbers might be tainted by rounding.
Luckily, it's very easy to get a better similarity measure, much like we
did in the previous example. (You need to run the code from Section XXX
again first)

\`\`\`{r, opts.label=\'code\'}

sd(sd_vec)

eps \<- [10\^(-dp)/2]{.mark}

sds \<- NULL

for(i in 1:nsim){

sd1 \<- runif(1, sd_vec\[1\]-eps, sd_vec\[1\]+eps)

sd2 \<- runif(1, sd_vec\[2\]-eps, sd_vec\[2\]+eps)

sd3 \<- runif(1, sd_vec\[3\]-eps, sd_vec\[3\]+eps)

sds\[i\] \<- sd(c(sd1,sd2,sd3))

}

\# compute common breaks so bins align

brks \<- pretty(range(c(res, sds)), n = 20)

hist(res, breaks = brks, col = rgb(1, 0, 0, 0.5),

freq = FALSE, xlim = range(brks),

main = \"Overlayed histograms\", xlab = \"value\")

hist(sds, breaks = brks, col = rgb(0, 0, 1, 0.5),

freq = FALSE, add = TRUE)

mean(res \< max(sds)) \* 100

\`\`\`

Even when the level of precision is taken into account, observing such a
small similarity between the standard deviations is still very unlikely.

\^ When recreating numbers, based on imagined numbers the goal should
never be to convert or the numbers perfectly. xxx is dat zo xxx

## rules of thumb{#rules}

\^ There are a couple of useful **rules of thumb** or **heuristics**
that can be checked without any, or with at most back-of-the envelope,
computations. They do not always hold, but they hold often enough to
check if they do, and if they are violated, investigate if this
violation is expected in the given circumstances \[TODO maybe give this
a separate section\]

- Typically, a statistically significant p-value corresponds to a
  confidence interval (CI) that does not include 0. The p-value - CI
  **equivalence rule** only holds if 1) the p-value corresponds to a
  two-sided test is used, 2) the value used in the hypothesis test is
  0, 3) the confidence level (e.g., 95% confidence interval) matches the
  test significance level (e.g. p \< 0.05) and 4) the CI is constructed
  in a traditional way. This should hold for the mean, difference in
  means, linear regression coefficient, proportion, and correlation
  coefficient. It, for example, does not hold for odds ratios or hazard
  ratios, where the null value is 1, not 0, and for e.g. bootstrap
  confidence intervals or profile likelihood intervals. It might also
  not hold for bounded parameters for which the estimates are near that
  bound, such as proportions near 0 or 1.

- Typically, the point estimate lies at the center of the confidence
  interval, with the interval width determined by the standard error and
  the confidence level. For example, if the estimate = 0.20 and the
  standard error is 0.06, the 95% CI is approximately: 0.20 \\pm 1.96
  \\times 0.06 \\approx \[0.08; 0.32\]. So that the estimate lies at the
  midpoint of the interval. The **symmetry rule** does not hold for, for
  example, odds ratios or hazard ratios, for e.g. bootstrap confidence
  intervals, or for bounded parameters with estimates near that bound.

#  

#  

# REANALYSING THE ORIGINAL RAW DATA {#reanalysing}

\^ If the raw data are available and you want to put in the work, there
is a lot of interesting stuff you can do with them. There are many
interesting angles to re-analyzing the raw data. You can do a full blown
reproducibility analysis. You can do an improved analysis. You can do a
robustness analysis. Or you can do a multiverse analysis.

\^ Note that sometimes data are being shared in-paper, such as in a
table, appendix or figure. So "having the raw data" doesn't necessarily
mean you should have them in, say, .xls or .csv format. There are even
tools to extract data from figures (see Section 7.1 of AITFM for some
pointers).

## reproducibility analysis{#reproducibility}

\^ Redoing the analyses on the original data (i.e., a reproduction or
**reproducibility analysis**) is useful for at least three things: not
only will you learn about the credibility of the original study, you
will also check whether you know how to do and practice doing the data
processing and analyses in your own study (because that will likely be
similar to the processing and analyses in the original study), and you
might get ideas of how to do things better (in your study).

\^ In a reproducibility check, you ask yourself: if I use the raw data
underlying the OS, and do the analyses performed by the OAs (possibly
using different software), do I find (roughly) the same results as
reported in the OS?

\^ Reproducibility can be checked on two levels: from processed data
(e.g., sum scores) to statistical results (e.g., p-values) and from raw
data (e.g., item scores) to processed data (e.g., sum scores). If the
data set you found contains both raw data (e.g., answers to individual
items on a questionnaire) and processed data (e.g., the sum scores of
the answers to these items; or transformations of data), try to
reproduce both (the statistical results starting from the processed
data, and the processed data starting from the raw data).

\^ First, if possible, check whether the data cleaning occurred as
advertised. e.g., if the authors claim in their paper to exclude
everybody under 18, and the data contain age as a variable, check
whether there are indeed no data from people below 18. Do keep in mind
though that some data cleaning could have occurred in the analysis code.

\^ If available, start by focusing on the processed data (for example,
the scores on scales instead of the individual item scores). From the
original processed data, try to recreate as many of the published
numbers as possible, including sample sizes, degrees of freedom, test
statistics, p-values and so on. This can be very difficult, but also
very simple. It's a good idea to start simple, and try to, e.g.,
reproduce means and other summary stats (e.g., percentage of male
participants), before diving into reproducing the p-values of e.g.
mediation analyses.

\^ Next, try to reproduce the processing from raw to processed.

\- Doing so might involve having to look up and read the
manuals/associated papers and scoring instructions of the
questionnaires.

\- When doing so, keep in mind that for many questionnaires, some items
require *reverse scoring*. To know when this applies, you might need to
look up the manual/associated paper of the scales used. Keep in mind
that the reversing might already have taken place in the raw data.
Ideally this should be explained in the codebook of the OS.

\^ Reproduction has a good chance of being annoying. The reason is
twofold. In most papers, analyses are underspecified, in the sense that
often important details are left implicit or being left out when
reporting about the analysis. There is a good chance nothing about
important steps is mentioned, or, if at all, being described vaguely.
For example, "Cases with outliers were deleted" is only really helpful
in so far it is also made clear how exactly outliers are being defined.
I gave some additional examples about this pervasive vagueness in
Section \@sec-impossible. Further, OAs are humans (for now), and humans
make mistakes, so you might need to actively make mistakes yourself.

\^ You will see you will probably need to **fill in** many **details**
(see Section \@sec-impossible). If you can't reproduce the result by
just following what the OAs describe in their report, these are things
you could try:

- Authors sometimes exclude outliers without reporting the rule used
  (e.g., ±3 SD, leverage, Cook's distance). They might even just exclude
  them (maybe post hoc to obtain significance) without even mentioning
  it at all. To reproduce their results, you may need to guess which (if
  any) observations were removed.

- Maybe the OAs restricted their analyses to complete cases only without
  mentioning, because that's what people do, right?

- You might need to guess whether the test was one-tailed or two-tailed.

- Variables may have been log-transformed, standardized, reverse-coded,
  or dichotomized at some point, but this step might be omitted or
  misreported. Trying common transformations may help reproducing the
  results

- Even if no interactions are mentioned in the paper, you might need to
  add one to be able to arrive at a successful reproduction.

- Often, there are several estimators possible when fitting a model. For
  example TODO add example. Don't expect the OAs to tell you which one
  they used, let alone why. Do expect a lot of guessing.

- Sometimes "basic" covariates (like age or gender) are included in a
  model without this being made explicit. That's wild, don't you think?

- Many tests come in different versions. For example, a t-test comes in
  a Welch and a Student variant. A chi-squared test can be done with or
  without a continuity correction. ANOVA comes in types I, II and III.
  [[R: Confidence Intervals for Binomial
  Proportions]{.underline}](https://search.r-project.org/CRAN/refmans/DescTools/html/BinomCI.html)
  lists no less than 16 variants to computing confidence intervals for
  binomial proportions, and I am pretty sure they left out some. And so
  on. Sometimes authors use one of those variants without telling you
  which one (probably because it is the default of their software
  program, without them realizing), leaving you guessing.

- etc xxx see richard xxx

\^ When doing this guess work when filling in the details, there is a
good chance the OAs just used the default settings of whatever
statistical software (be wary of the version, as defaults can change
over time!) the OAs have been using, so trying to find out about these
might be a good start in your guessing game.

\^ As a scientist, you probably try to avoid making mistakes and
confusions. While reproducing, however, you might be required to let go
of that desire, and actively do things wrong! \[FOOTNOTE: It is very
important here to not read this sentence out of context. You are not
Sabrina Carpenter after all.\] The reason you might need to get rid of
your good boy or good girl attire and go rogue is that the OAs might
have made mistakes, so if you want to arrive at the same results as they
did, you will have to make the same mistake again.

\^ In general, it is very hard to predict which mistakes they will have
made, but here is a short list of mistakes I have seen made more than
once. So if you can't reproduce the result, try to **make** some of
these common **mistakes** when analyzing their data: \[TODO maybe move
this to an appendix\]

> \- Keep a close eye on how missing data were handled. Often, in data
> processing, NA (i.e., missing) data are assigned a number (often 0).
> But this 0 has of course a very different meaning than a participant
> saying they smoked 0 cigarettes last month, or had 0 fights with their
> romantic partner. Treating these two 0s as the same will leads to
> distortion of the data. As the OAs might have made this mistake, you
> might have to make that mistake if you want to reproduce the reported
> results. TODO add example birthe
>
> \- Many authors are deeply confused by the difference between the
> standard deviation and the standard error of the mean. So if you want
> to reproduce their standard errors and fail to do so, you might wish
> to try to compute the standard deviation instead (see also Section
> \@sec-internalequality).
>
> \- Many authors confuse mediation and moderation analysis.
>
> \- Remember that you should treat categorical variables as factors.
> For example, if gender is "female", "male", "other", and this is coded
> in the data as 1, 2 and 3, treating these 1, 2 and 3 as meaningful
> quantities rather than labels might lead to (sadly very common)
> errors! (A related mistake is treating nominal data as being metric
> xxxx the same xxx.) To do a successful reproduction, you might need to
> make that mistake, since the authors might have to commit this sin!
>
> \- This list will be updated if my ~~frustration~~ experience grows!

\^ This step will probably involve a lot of trial-and error. You will
have to try a lot of different things, both doing guess work when
details are being left out, and making reasonable mistakes the OAs could
have made, before you succeed or decide to give up.

\^ Classifying a reproduction as successful or failed is hard xxx see
richard xxx. Some failures are worse than others and might or might not
have an impact on the conclusion of the OS. see artner ankel-peters
dreber johannesson

\^ Also, it is not just a question about the extent to which you have
been able to recreate the reported numbers. Even if you have been able
to find the exact numbers based on the raw data, it is not over. What is
at least as important is *how* you achieved that. Maybe you had to
introduce mistakes, because the authors did. Maybe you had to delete
outliers or incomplete cases, without the authors mentioning anything
about that at all. Maybe you had to include an interaction term in your
model, without this being mentioned in the paper.

\^ There are at least two ways of defining reproduction success.
Obviously, if you can not reproduce the numbers, that is not a success.
Also obviously, if you can reproduce the numbers based on whatever the
OAs provided (their paper and possibly code), that is a success. But
what if to reproduce the numbers you needed more than what the OAs
provide, like guess work or contacting the OAs? xxx Further, there are
many numerical results, at at least two levels (from raw data to
processed data and from processed data to statistical results), so .
There is no clear consensus of what is a success and a failure, but that
shouldn't be a problem, as long as you make clear to your readers what
you did and found.

\^ Again, finding that some results are not or only partially
reproducible does not necessarily mean the findings can't be trusted.
For example, if you can only reproduce a coefficient by adding an
interaction to the model (without the OAs having specified the
interaction), the result is not strictly reproduced, but still is, to
some extent. The OAs have just been sloppy in how they report on their
model.

\^ Things might get so bad that you might need to contact the OA to ask
for clarification and mental support.

\^ I know doing a reproduction analysis is very hard. What's worse, it
feels like it should be easy, if only the OAs had described everything
they did and did so in a clear enough way. There is a good chance you
will be frustrated if reproducing is difficult. You shouldn't, though. I
assure you it is them, not you.

## alternative analyses{#alternative}

\^ It can make sense to do the analysis again in a way that is at least
as reasonable. In the course of a study, many data processing and data
analytical decisions are made, and for many, there are several
reasonable options, out of which the OAs just chose one. Do the results
still hold up when you make a different, reasonable choice and slight
changes to these decisions? Remember how I reminded you above how many
tests come in different flavors (Welch and Student t-test; corrected and
uncorrected chi-squared test; Wilson and Wald (and may other) Binomial
confidence intervals; etc)? If the OAs choose option A without clear
justification, check what the result would be using option B, unless
that option is clearly inferior in the current context. And if the OAs
removed outliers, what would the result be if you don't, or adopt a
different operationalisation of outliers? TODO: add an example from a
real robustness report. This is called a **robustness** or **sensitivity
analysis**.

xxx eg Bayesian xxx

\^ A special case of this is when your adherence to the prereg plan (see
Section XXX) revealed that the plan was to do a different analysis.
Especially if there is no clear justification why the pre-registered
analysis is bad, it make sense to do the pre-registered analyses on the
raw data.

\^ A **multiverse analysis** is basically a robustness analysis on
steroids, and you try to consider a combination of all (compatible)
reasonable choices. An example of a multiverse analysis on the fertility
and religiosity study discussed in Section XXX can be found in Steegen
et al. (2016) TODO add ref. They made several other choices in data
processing that the OAs did, including using different cutoffs for when
a person is classified as being High vs Low in fertility, whether or not
women who were unsure about the data they provided should be included in
the data set, and so on. Combining all the compatible choices leads to
120 different reasonable data sets, all of which can be reasonably
derived from the same raw data set. There's quite a lot of coding
experience required, but there are some R packages to help you out, such
as milliways, specr, boba, multiverse and counting. \[FOONOTE: Don't go
looking for the R package counting. It does not exist. Or maybe it does,
but it won't do multiverse analysis. Or maybe it does, but that would be
an insane coincidence.\]

\^ It can make sense to do the analysis again in a way that you think is
better, especially if during your reproducibility analysis, you found
mistakes the OAs made, for example one of the small list of common
mistakes I collected in Section \@sec-reproducibility or one of the
statistical fallacies I listed in Section \@sec-checkingquality.
Remember science progresses, and the current state of the art might have
changed. Are there analyses available for the same construct that are
more appropriate and have e.g. better statistical properties? For
example, if the data from the OS are nested (e.g. repeated measures),
but the OAs ignored this dependence and used for example single
level/ordinary regression in their analysis, re-analyse their data using
a multilevel regression model. TODO add example birthe This is called an
**improved analysis**.

## data fabrication{#fabrication}

\^ With the raw data, you can check for irrealistic data patterns, which
might indicate the data have been fabricated instead of collected, which
is no longer just an error but downright fraud. Data fabrication has
happened, is happening, and will happen, but as far as i know it is
rather rare, so if you are not actively looking for a study where it is
reasonable that the OAs fabricated their data, your OS probably won't
have. Which means that, unless you have good reasons to be very
suspicious about the OAs, you shouldn't necessarily do these checks, but
I want to mention it anyway. But still, it is good to keep in the back
of your head that these things can happen.

Here is an interesting example from
[[https://pubmed.ncbi.nlm.nih.gov/23982243/]{.underline}](https://pubmed.ncbi.nlm.nih.gov/23982243/)
(focusing on another study than in Section XXX) TODO add ref, just to
give you a feel of what is possible. It involves an experiment where
people are asked what prices they were willing to pay for two items.

- Simonsohn's experience was that people tend to answer these questions
  by multiples of 5. This hunch was then backed up by looking at the raw
  data of this type of other papers. Data where the proportion of cases
  where a multiple of 5 is used is at baseline (20%, as of the 10 digits
  0,1,2,\...9, only 0 and 5 would yield a multiple of 5) are at least
  unusual and probably fabricated.

- Further, it would make sense that if these two items were similar,
  there would be a positive correlation between both prices. Finding no
  such correlation or a negative one would certainly raise the
  possibility of data fabrication.

\^ You can read about many more inspiring examples here,
[[https://datacolada.org/archives/category/fake-data]{.underline}](https://datacolada.org/archives/category/fake-data)

D. REPLICATING

\^ While you won't easily find someone saying this in print, replication
studies are less attractive to journal to novel studies. That means
that, if your desire is to get published, to bar is often a bit higher
for doung a replication study. This translates to, for example, tacit
expectations about being high powered, being pre-registered, etc

# DESIGNING YOUR STUDY {#designingstudy}

\^ Even if the OAs were transparent and kind enough to share their
materials, don't just assume the best course of action is to use just
this shared material. It might still make sense to do something
different than the OAs and go beyond the exact same materials as used by
the OAs.

- They might have done something weird or wrong. See Section
  \@sec-undesired, \@sec-ambiguous and \@sec-checkingquality for
  examples.

- You currently don't have the means to do exactly the same (see Section
  \@sec-impossible).

<!-- -->

- And even if all the answers to the questions asking "was so-and-so
  done correctly?" are "yeah, sure", now is the time to ask, can
  so-and-so be done better? Are there measures available for the same
  construct that are more appropriate and have e.g. better psychometric
  qualities? TODO add example

- So, in light of the fact that people do stuff that is weird and wrong,
  and that science progresses, you should consider using alternative or
  improved materials compared to the OAs (constructive replication).

- (Of course, doing an extended study with e.g. an additional covariate
  is reason enough already why you can not just blindly redo the
  analyses from the OAs.)

\^ You probably want to keep a document with a list of the **known
differences** between your study and the original study (I promise you
will forget about those if you don't keep track!), where "known" signals
the fact that you knew about this in the design face, before your
results came in. Also, keep in mind that whenever you were not sure what
the OAs exactly did (see Section \@sec-impossible and Section
\@sec-reproducibility), whatever you did is a potential known
difference, and you should list it as such.

\^ When designing your study, remember that sometimes the OAs were given
"free" bonus data without them asking, so you could consider collecting
that info. For example, if they collected data from students at American
universities, they knew the country of residence and the occupation of
all their participants without having to ask for it. You, on the other
hand, might be using prolific, so your participants can be from anywhere
over the world, so asking their country of residence and occupation
might be interesting, despite the OAs not having done so, or at least
not explicitly!

\^ There is a sense in which doing a replication is just doing things
the same (but by Section \@sec-areplication, I hope I got you thinkin'
non-sense). Even if you are an "I want to do things exactly the same"
hard core type, there is one thing where you will have to give in: there
is no good reason to use the same sample size as the OA did. You might
want a higher power or more precision than in the OS. **Determining your
sample size** is an important step about which I don't have anything
interesting to say. Luckily, HRRS has an interesting section about this
(6.2), which I am not going to repeat, so I will just keep quiet for a
while.

\^ xxxx Also, if you focus on one specific result as your main target of
replication, justify why you choose this xxx moet dat ook niet bij
desging ergens xxx what is the main claim? needed for power analysis and
for some metrics of replication success

#  

# DESIGNING YOUR ANALYSES {#designinganalysis}

\^ Even if the OAs were transparent or kind enough to share their
detailed processing analysis steps or code, don't just assume the best
course of action is to use just this exact processing and analytical
approach and shared code. It might still makes sense to do something
different than the OAs and go beyond the exact same processing analysis
steps or code as used by the OAs.

- Your quality check from Section \@sec-checkingquality, your visual
  check from Section \@sec-checkingvisuals, your numerical conformity
  check from Section \@sec-checkingconformity, and your re-analysis from
  Section \@sec-reanalyzing might have revealed the need to do things
  differently, because the OAs did something weird or wrong.

- And even if all the answers to the questions asking "was so-and-so
  done correctly?" are "hell, yeah", now is the time to ask, can
  so-and-so be done better (see also Section \@sec-alternative)? Are
  there analyses available for the same test that are more appropriate
  and have e.g. better statistical properties? xxx current state of the
  art xxx TODO add example

- So, in light of the fact that people do stuff that is weird and wrong,
  and that the field has matured (or you are just better educated than
  the OAs are), you should consider doing an alternative or improved
  analysis compared to the OAs (constructive replication).

- (Of course, doing an extended study with e.g. an additional covariate
  is reason enough already why you can not just blindly redo the
  analyses from the OAs.)

\^ If your analysis will be different from the original ones and the
original raw data are available, it make sense to do your analysis and
their old data as well to facilitate comparison (see Section XXX)

\^ Similarly, it might be a good idea to perform the analyses as done by
the OAs on your data, next to your analysis and your data, explaining
the differences and why they are justified

\^ You still have the document with a list of the **known differences**
between your study and the original study I suggested you'd keep? Good!
Make sure to update it when thinking about your analyses.

\^ A big question is whether your tests should be one tailed or two
tailed. If you believe the OAs have provided some credible evidence for
the effect you are investigating, one-sided tests would make sense, I
guess. But I don't have any solid advice on this one. Maybe I should do
some reading up about it. In the absence of that, you should do that
yourself.

\^ Remember all the nagging questions I raised in Section
\@sec-ambiguous talking about how doing the same is often ambiguous and
can have at least two meanings, the same choice vs the same strategy? To
be clear, I don't have the answers to these questions raised. But these
are things that you will come across and will need to make decisions
about. Sometimes the answer will be: do several things, all of which
implement the idea of *the same* to some extent (i.e., the choice-same
and the strategy-same). So often, it might be interesting to do the main
analyses several times.

\+ Consider for example this scenario: the OAs correlate two measures,
each of which are a subscale. The scores on each subscale are determined
using a factor analysis, in which the items load on different factors
than the authors of the scale proposed/intended. This means there are at
least three plausible ways to compute the subscale for your data .

1)  use the scale structure as proposed by the scale developers

2)  use the scale structure as revealed by the OAs factor analysis

3)  use the scale structure as revealed by doing a factor analysis on
    your data

You can do these 3 options for both subscales. You could then look at 9
correlations, combining all 3 approaches. Or you could look at 3
correlations (approach 1 for subscale 1 and approach 1 for subscale 2;
approach 2 for subscale 1 and approach 2 for subscale 2; approach 3 for
subscale 3 and approach 1 for subscale 2). It's up to you how far you
want to go (between 1 and 9 analyses).

\^ If you take a different analytical strategy than the OAs, it often
makes sense to do the analyses of the OAs as well, as this facilitates
comparability.

\^ A big question to consider is how you will **evaluate replication
success**. When it is money time, you will need to answer the question:
was the replication attempt a success or a failure? Broadly speaking,
you want to compare your result to the original results and assess
whether your result either supports/confirms/converges/is consistent
with xxx or contradicts/diverges from the original result (or is
inconclusive).

\^ Well, like with everything, it depends how you measure and define
success.

Here is an overwhelmingly large bunch of ways you could do that
[[http://rachelheyard.com/reproducibility_metrics/#table]{.underline}](http://rachelheyard.com/reproducibility_metrics/#table).
Among all of these variants, these two stand out:

- p-value based: Do you find a significant result when the OAs did, in
  the same direction?

- effect size based: Is your effect size inside the confidence interval
  of the effect size in the OS?

\^ Most of the above metrics concern a single
hypothesis/effect/test/research question. The study you replicated
probably contained many, such as an interaction effect followed up by a
simple effect. That means that your overall conclusion about the
replication study can (or most likely, often will be) mixed, in the
sense that some results converged but others did not.

#  

# PREREGISTERING YOUR STUDY{#prereg}

\^ Again, I don't have much to say here (yet). Pre-registration is hard,
but there is not much that is specific to pre registering a replication
that I can think of.

\^ The only real difference from a preregistration of a non-replication
study is that it is advised to include a section with known differences
with the OS, including a justification of why these differences are
reasonable or needed, and a discussion on whether you think these will
impact the result compared to the OS.

\^ Ideally, the pre-analysis plan includes a definition of what
constitutes replication success vs failure, but that's a tough nut (a
bit more in Section \@sec-designinganalysis) for some ideas.

\^ Optionally, you can contact the OAs and ask them to read through the
preregistration. This is especially when there were a lot of changes to
their study.

#  

# COLLECTING YOUR DATA{#datcoll}

\^ There is nothing I can think of really where collecting data for a
replication study is any different from collecting data for a
non-replication study.

#  

# INTERPRETING YOUR RESULT

\^ What if your replication failed, by whatever the metric you prefer?
If you don't find the same results as the original authors, what now?
Think of what might have caused or contributed to this. There are many
possible explanations or reasons for why your results may differ from
theirs.

- The original effect was a false positive

- Your result is a false negative

- The different result might be caused by the inevitable differences
  between the OS and your study. When discussing this, it makes sens to
  make a distinction between differences that are known before data
  collection and analysis (i.e., by design) or unknown (e.g.,
  differences in gender distribution; differences in attrition rate)
  differences with the OS.

- If you come up with a hidden moderator to explain the different
  result, try to turn it into a testable hypothesis that you then
  recommend as a suggestion for future research. If possible, discuss
  how the known and surprising differences with the original study might
  have influenced the results. How important are the (inevitable)
  differences between your study and the original one? And is it
  possible, feasible, and interesting to test this?

- fig 4.2 en 7.1 xxxx

E. WRITING UP AND WRAPPING UP

# WRITING UP YOUR EVALUATION AND REPLICATION STUDY{#writing}

\^ To some extent, a replication study is just an empirical study like
any other. General strategies, good practices, tips and tools that are
useful for writing up an empirical study are still applicable to a
replication study. A few aspects are special, though, and I highlight
the ones I could think of below.

## GENERAL

\^ Here's a piece of solid advice I found in HRRS. They ask you to be
mindful of your language when writing up your replication study. In
particular, they "recommend a descriptive and impersonal language. When
criticizing bad documentation, no access to data, or brevity in methods
replication authors should keep in mind the historical context of the
original publication. For example, sharing data was much more diﬀicult
in the 1990s and not required in many areas until recently."

\^ In evaluation and replication studies (where you to a large extent
re-write what the others have done, for example in the intro and methods
section), the risk of plagiarism is very high. Make sure you say
everything in your own words as much as possible!

xxx do better structure xxx like aline wicherts xxx

\^ If the OAs were somehow involved in your evaluation or replication
study, be sure to describe that in the relevant section of your paper.

## INTRODUCTION

\^ You will need to discuss the OS in considerable detail.

\^ When discussing the OS, give a lot of detail about their
participants, as their background might be an important factor to
understand any differences in the results of your study and the OS (if
there are any). This could go on in the introduction, or possibly in
METHODS/DISCUSSION).

\^ Also, make very clear what, besides the paper itself, you have found
(such as data and materials) and where and whether you have used it (and
if not why not).

\^ This should go without saying but still: make very clear what exactly
you are evaluating and replicating. Just sharing the title of the paper,
the authors and the journal will often not be enough, as a paper
typically contains many studies, studies often contain many research
questions or hypotheses and so on. So you need to be very specific about
which paper, studies, results/hypotheses.

\^ Explain or justify why you chose the OS as your target study (at
least if it is more interesting to your readers than just your own
private interests) and the claims you focus on. Include your reasoning
of why your OS is worthy or in need of evaluation and/or replication.
Also, if you focus on one specific result as your main target of
replication, justify why you choose this xxx moet dat ook niet bij
desging ergens xxx

\^ When there are many previous replication attempts, consider providing
a meta-analytic estimate for the effect.

\^ you might or might not want to include a specific section talking
about (the need for) evaluation and replication studies in general (what
it is; the importance; etc). Further, you might want to offer general
reflections on the value of and pitfalls associated with doing
replications in general (in introduction or possibly in the DISCUSSION).

## EVALUATION

\^ Discuss the results of the sleuthing you've been doing earlier:

- A summary of the post publication discussion you have found (see
  Section \@sec-postpublication), giving of course proper credit,
  restricting yourself to the parts of this discussion that don't come
  up in the next bullets.

- The results of your quality check (see Section \@sec-checkingquality).

- Discuss the reporting integrity (see Section \@sec-checkingprereg).
  For example, when the original study had been pre-registered, include
  an evaluation of the extent to which they adhered to their
  preregistration protocol.

- The results of your visual checks (see Section \@sec-checkingvisuals).

- The results of your checks on numerical conformity (see Section
  \@sec-checkingconformity).

- The results of your reproducibility check of the original study (see
  Section \@sec-reproducibility). Make sure to include many details when
  doing that. Here are a few things to keep in mind:

  - The nature of all the materials you used.

    - Did you have access to the full raw data or just to the processed
      data? Indicate whether you started from the raw data or from the
      processed data or from both.

    - Did you have access to the code or data analytical protocol used
      by the OAs? Make clear whether you wrote your own code (for
      processing, for analysis or for both), just ran the code (for
      processing, for analysis or gor both) provided by the OAs, or
      started from the code (for processing, for analysis, of for both)
      provided by the OAs and adapted it.

    - If there was no code, or partial code only, you had to go by
      whatever the OAs described. Where did you find these descriptions?
      Just the paper or also e.g., the pre-registration plan?

  - The exact location/source of all the materials (data and code) you
    used, such as from a public platform like osf, shared by the authors
    on request; extracted from tables; etc

  - whether you got input from the OAs and if so what kind of input.

  - which software 'n' version you and the OAs used.

  - for each numerical result that you managed to reproduce: whether you
    needed to do something different, or more detailed, than what was
    reported by the OAs (or found in their shared code) to reproduce the
    results.

    - Which details were omitted in the report and did you need to fill
      in to be able to reproduce the results, based on logic, common
      sense, or inspecting the code shared by the OAs?

      - For example, did the OAs just report they used a t-test, and did
        you have to find out by trial-and-error or by inspecting the
        shared code they used a Welch t-test?

    - Which deviations to what is reported by the OAs (or found in their
      shared code) were needed to reproduce the results? Why? What were
      the results without these changes?

      - For example, did the OAs just report they used a Student t-test,
        but can you only reproduce their results with a Welch t-test?
        Does their conclusion change when you do use a Student t-test?

  - for each numerical result that you could not reproduce: what is the
    impact on the conclusions? Does it change any of the conclusions?

- If any of these checks are only done for a selection of numerical
  results, justify your selection xxx

- The results of your robustness/improved/multiverse analysis of the
  OS's raw data (see Section \@sec-alternative), again reporting many of
  the aspects listed above (source, software, involvement of the OAs,
  etc).

- If you did not do any of these checks, it might be good to briefly
  explain why (e.g., because of the fact that no data were available)

## REPLICATION

\^ Include a subsection called *Differences from original study* or
something along these terms, for example in the Methods section. In this
subsection, discuss any inevitable differences between the original and
replication study, especially those that might undermine/could have
undermined the probability of a successful replication. xxx rewrite xxx

- try to make a distinction between differences that are known before
  data collection and analysis (i.e., by design) or unknown (e.g.,
  differences in gender distribution) differences with the OS.

- if these differences are the results of a decision on your part (some
  things are beyond your decision capacities, like time and your sample
  but others, like design, materials, and analyses are not), discuss why
  (i.e., provide a justification) you decided to change stuff.

- if possible, discuss the expected impact these differences could have
  on the replication results.

\^ When writing the results, it might or might not be a good idea to
present your results (both descriptive and inferential) next to the OS's
results directly, to facilitate comparison. You could consider adding a
table comparing the results of the OS and the results of your
replication study.

#  

# PUBLISHING {#publishing}

\^ Here are some potential outlet options for your paper about your
replication study: TODO: add links

- the journal where the OS was published (but check the info on their
  website to see if they accept replication studies)

- [[replicationresearch.org]{.underline}](http://replicationresearch.org)

- plos one

- scientific reports

- meta-psychology

- collabra

- peer j

- [[https://www.jsr.org/]{.underline}](https://www.jsr.org/)

- see also
  [[https://rr.peercommunityin.org/about/pci_rr_friendly_journals]{.underline}](https://rr.peercommunityin.org/about/pci_rr_friendly_journals)

- see also Table 8.1 of HRRS

- etc

#  

# SHARING {#sharing}

\^ Consider sharing your findings on the post publication platforms
mentioned in Section \@sec-postpublication, especially if you don't seek
to publish your work.

\^ If you have been in touch with the OAs and they have been interested
and/or helpful, it is polite to let them know the results, and
potentially ask for their comments, especially if the replication
failed. You might even wish to alert them if you haven't been in touch
with them. You could, for example, send them a one-paragraph summary
(did it replicate or not or is it complicated?) email with your results,
thanking them again, and send your report as an attachment (or add a
link to the osf project if you have uploaded your report there).

F. FURTHER READING

## BOOKS ON REPLICATION, CONFORMITY AND REPRODUCTION

Röseler, L.\*, Wallrich, L.\*, Hartmann, H., Hüffmeier, J., Goltermann,
J., Pennington, C. R., Boyce, V., Field, S. M., Pittelkow, M.-M.,
Silverstein, P., van Ravenzwaaij, D., Azevedo, F. (2025). Handbook for
Reproduction and Replication Studies. Retrieved from
https://forrt.org/replication_handbook,
[[https://doi.org/10.5281/zenodo.16990114]{.underline}](https://doi.org/10.5281/zenodo.16990114)
[[Handbook for Reproduction and Replication
Studies]{.underline}](https://forrt.org/replication_handbook/) This is
currently somewhat superficial and not always as hands-on-y as it could
be, but it has a few interesting bits and might have more meat in the
future.

Berkeley Initiative for Transparency in the Social Sciences. (2022).
Guide for Accelerating Computational Reproducibility in the Social
Sciences

[[Guide for Accelerating Computational Reproducibility in the Social
Sciences \| Guide for Accelerating Computational Reproducibility in the
Social Sciences]{.underline}](https://bitss.github.io/ACRE/)

Heathers, J. (2025) An Introduction to Forensic Metascience.

[[www.forensicmetascience.com]{.underline}](http://www.forensicmetascience.com)
There is a large overlap with Section \@sec-checkingconformity, but it
has some different examples, and includes several first hand experiences
and some noteworthy suggestions for future developments.

## ON REPLICATION

xxx
[[https://link.springer.com/article/10.1186/s41073-018-0060-4]{.underline}](https://link.springer.com/article/10.1186/s41073-018-0060-4)

LeBel, E. P., McCarthy, R. J., Earp, B. D., Elson, M., & Vanpaemel, W.
(2018). A unified framework to quantify the credibility of scientific
findings. Advances in Methods and Practices in Psychological Science, 1,
389-402.
[[https://doi.org/10.1177/2515245918787489]{.underline}](https://doi.org/10.1177/2515245918787489)
[[https://ppw.kuleuven.be/okp/\_pdf/LeBel2018AUFTQ.pdf]{.underline}](https://ppw.kuleuven.be/okp/_pdf/LeBel2018AUFTQ.pdf)

Block, J., & Kuckertz, A. (2018). Seven principles of effective
replication studies:

Strengthening the evidence base of management research. Management
Review

Quarterly, 68(4), 355--359.
[[https://doi.org/10.1007/s11301-018-0149-3]{.underline}](https://doi.org/10.1007/s11301-018-0149-3)
xxx

[Zwaan, R. A., Etz, A., Lucas, R. E., & Donnellan, M. B. (2018). Making
replication mainstream. *Behavioral and Brain Sciences*, *41*,
e120]{.mark}
[[https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/making-replication-mainstream/2E3D8805BF34927A76B963C7BBE36AC7]{.underline}](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/making-replication-mainstream/2E3D8805BF34927A76B963C7BBE36AC7)

[Nosek, B. A., Hardwicke, T. E., Moshontz, H., Allard, A., Corker, K.
S., Dreber, A., \... & Vazire, S. (2022). Replicability, robustness, and
reproducibility in psychological science. *Annual review of psychology*,
*73*(1), 719-748.]{.mark}

[[https://www.annualreviews.org/doi/full/10.1146/annurev-psych-020821-114157]{.underline}](https://www.annualreviews.org/doi/full/10.1146/annurev-psych-020821-114157)

## ON REPRODUCTION

Artner, R., Verliefde, T., Steegen, S., Gomes, S., Traets, F.,
Tuerlinckx, F., & Vanpaemel, W. (2021). The reproducibility of
statistical results in psychological research: An investigation using
unpublished raw data. Psychological Methods, 26, 527-546.
[[https://doi.org/10.1037/met0000365]{.underline}](https://doi.org/10.1037/met0000365)
[[https://ppw.kuleuven.be/okp/\_pdf/Artner2021TROSR.pdf]{.underline}](https://ppw.kuleuven.be/okp/_pdf/Artner2021TROSR.pdf)

## ON MULTIVERSE

Steegen, S., Tuerlinckx, F., Gelman, A., & Vanpaemel, W. (2016).
Increasing transparency through a multiverse analysis. Perspectives on
Psychological Science, 11, 702-712.
[[https://doi.org/10.1177/1745691616658637]{.underline}](https://doi.org/10.1177/1745691616658637)
[[https://ppw.kuleuven.be/okp/\_pdf/Steegen2016ITTAM.pdf]{.underline}](https://ppw.kuleuven.be/okp/_pdf/Steegen2016ITTAM.pdf)

## STUDIES USED IN THE EXAMPLES

Steegen, S., Dewitte, L., Tuerlinckx, F., & Vanpaemel, W. (2014).
Measuring the crowd within again: A pre-registered replication study.
Frontiers in Psychology, 5, 786, 1-8.
[[https://doi.org/10.3389/fpsyg.2014.00786]{.underline}](https://doi.org/10.3389/fpsyg.2014.00786)
replicating

Vul, E., and Pashler, H. (2008). Measuring the crowd within:
probabilistic representations within individuals. Psychological Science
19, 645--647. doi:
[[https://doi.org/10.1111/j.14679280.2008.02136.x]{.underline}](https://doi.org/10.1111/j.14679280.2008.02136.x)

Rutten, I., Voorspoels, W., Steegen, S., Kuppens, P., & Vanpaemel, W.
(2018). Depressive symptoms and category learning: A preregistered
conceptual replication study. Journal of Cognition, 1, 34, 1-7.
[[https://doi.org/10.5334/joc.35]{.underline}](https://doi.org/10.5334/joc.35)
replicating

Smith, J. D., Tracy, J. I., & Murray, J. M. (1993). Depression and
category learning. Journal of ExperimentalPsychology: General, 122(3),
331--346. DOI:
[[https://doi.org/10.1037/0096-3445.122.3.331]{.underline}](https://doi.org/10.1037/0096-3445.122.3.331)

[Voorspoels, W., [Bartlema,
A.](https://ppw.kuleuven.be/okp/team/Annelies_Bartlema/), & [Vanpaemel,
W.](https://ppw.kuleuven.be/okp/team/Wolf_Vanpaemel/) (2014). Can race
really be erased? A pre-registered replication study. *Frontiers in
Psychology*, *5*, 1035, 1-7.
[[https://doi.org/10.3389/fpsyg.2014.01035]{.underline}](https://doi.org/10.3389/fpsyg.2014.01035)]{.mark}
replicating

Kurzban, R., Tooby, J., and Cosmides, L. (2001). Can race be erased?
Coalitional

computation and social categorization. Proc. Natl. Acad. Sci. U.S.A. 98,

15387--15392.
[[https://doi.org/10.1073/pnas.251541498]{.underline}](https://doi.org/10.1073/pnas.251541498)

Vanpaemel, W., Vermorgen, M., Deriemaecker, L., & Storms, G. (2015). Are
we wasting a good crisis? The availability of psychological research
data after the storm. Collabra, 1, 1-5.
[[https://doi.org/10.1525/collabra.13]{.underline}](https://doi.org/10.1525/collabra.13)
following up on

Wicherts, JM, Borsboom, D Kats, J & Molenaar, D. The poor availability
of psychological research data for reanalysis. American Psychologist.
2006; 61: 726--728.
[[http://dx.doi.org/10.1037/0003-066X.61.7.726]{.underline}](http://dx.doi.org/10.1037/0003-066X.61.7.726)

Steegen, S., Tuerlinckx, F., Gelman, A., & Vanpaemel, W. (2016).
Increasing transparency through a multiverse analysis. Perspectives on
Psychological Science, 11, 702-712.
[[https://doi.org/10.1177/1745691616658637]{.underline}](https://doi.org/10.1177/1745691616658637)
multiversing

Durante, K. M., Rae, A., & Griskevicius, V. (2013). The fluctuating
female vote: Politics, religion, and the ovulatory cycle. Psychological
Science, 24, 1007--1016.
[[[https://doi.org/10.1177/0956797612466416]{.underline}]{.mark}](https://doi.org/10.1177/0956797612466416)

[Navarro, D. (2013). *Learning statistics with R*.
[[https://learningstatisticswithr.com/]{.underline}](https://learningstatisticswithr.com/)]{.mark}
was used for some examples using fictional data.

## STATISTICAL FALLACIES

## TOOLS AND CHECKLISTS FOR STUDY EVALUATION

## TOOLS AND TECHNIQUES FOR CHECKING NUMERICAL CONFORMITY

## OTHER
