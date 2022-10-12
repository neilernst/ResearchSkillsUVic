---
marp: true
title: Reading Papers
author: Neil Ernst
date: Oct 2022
---

# M4 - Reading Scientific Papers

## Learning Objectives

* Develop knowledge of topic formulation
* Efficiently read a paper
* Characteristics of literature reviews and mapping studies
* Plan a research study with visual abstracts
* Document research plans and turn that into a proposal

----

## Notes

### Choosing a Topic

Generally, being engaged and interested is important. It is very difficult to motivate your work if you aren't excited about the topic! Having said that, working with Professor X does imply that you work on topics that Professor X enjoys (e.g., mind control).

----

My other advice is to aggressively scope your work. It is easy to start out with "make a fully automated car", which isn't well scoped. You probably end up with something more like "LIDAR-based range finding in Volvo SUVs under uneven lighting conditions" or something. That isn't to say you should not have a big goal in mind - you should. But be aware that your results likely won't solve the problem - not immediately anyway. Another rule of thumb is that for a UVic Masters, expect to submit one A*/A conference paper, and for a PhD, 4-5 such papers. VERY rough guideline!

----
To do this, I recommend reading theses of fellow students in your lab. You will be surprised at how little work got in to the thesis. Of course, none of the false starts appear, or boring results, so it can be misleading.

----
**Easy Option 1**

* Your advisor tells you what to do.
* Pro: clear directive
* Con: maybe you don't want to do that!

----
**Slightly Less Easy Option 2**

* Find an old paper of your advisor/someone in their area.
* Look for future work sections or limitations
* Fix or improve on that.
* Pro: clearly a defined problem.
* Con: maybe it is future work because it is really hard!

----
**Hard Option 3**

* Find ongoing work in a conference. E.g., flip through DBLP proceedings in your area.
* Pick a hard problem that is tractable to solve in 1-4 years.
  * Open, Doable, Interesting
* Con: if it was easy to figure out the triplet above, everyone would do that.

----
**Easy Option 4**

* Talk to industry or people with problems
* Solve their problem
* Pro: leads nicely to jobs.
* Pro: obviously relevant 
* Con: industry problems often not important to research. Harder to publish.

----
### Organizing Your Research Plan

[McIlreath's PhD planning template.](https://github.com/rmcelreath/PhD_planning_template/blob/master/PhD_template.pdf)

[The visual abstract and Technological rules presentation](https://docs.google.com/presentation/d/18bOz4OVAQamsBZqk9mMoSq09qbWcg_uTgpGn5CtoUCc/edit?usp=sharing).

Turning the VA into a research plan. 

----
## Systematic Literature Reviews and Reading Papers

- organize a reading group.
- difference between reading for research and reading for reviewing.
- [Dana's slides]()
- doi2bib.org 

----
## Efficiently Reading a Paper

First, decide *why* you need to read the paper:

- As a peer reviewer, to decide if the paper meets conference objectives like significance and validity
- As a replicator, to see how the paper got their results
- As someone who wants to do a thesis in a similar space, as part of a literature review
- As someone who is getting an overview of the field as part of a survey course
- ... 

----
Each of those approaches will change (sometimes subtly) how you approach reading a paper. 

----
### Getting an Overview

My suggestion for getting an *overview* of the field, is to carefully skim the paper but ignore the substantive details, such as tables of data, proofs, pseudo-code and so on. Those tend to be more important for assessing validity (did the numbers they get line up with the stated results) or replications (can I get similar results). 

----
You might look in particular at the following: 

* In the introduction, what are the **research questions** and **claimed contributions** of the paper. Often these are explicit (and it is not a bad idea in papers you write, either). Do they line up with what the title says? How do these RQs build on other papers you have read in the field? 
* If you have never heard of the specifics of the paper before (e.g., "fuzz testing"), take a **look at the background** and maybe inform yourself on some of these items the paper might take as knowledge you should already have. For example, deep learning papers won't explain tensors or dot products. 

----
* In the method section, briefly skim the stated method - I find sketching the process out helps. In data science approaches, these often involve data preparation, tool explanation/alg parameterization, and validation (e.g. cross fold, bootstrap etc). 

----
* Importantly, what *constructs* is the paper defining to assess the RQ? For example, if we want to know the effects of **income** on **intelligence**, we need to operationalize those concepts with constructs we use in our instruments. For example, income might be "gross family income", and intelligence might be "IQ score measured on (some specific IQ test)". Do you agree those constructs represent the theoretical concepts from the RQ? Does the paper have an underlying theory that can explain the concepts further? What colliders/confounders might be confusing the measurements? 

----
* In the Discussion section, we often see authors start to speculate on what the findings imply. Be careful to watch out for "storytelling" where the paper starts drawing conclusions unsupported by their method. However, this *can* be a good place to find places where the authors see the research heading: new implications for research or industry, weird outliers that they can't classify, etc. 

  
----

## Readings (before class)

* none. 

### Optional and Recommended

* [Finding CS Theory problems](https://blog.computationalcomplexity.org/2003/04/finding-problems-to-work-on.html)
* Storey, [Visual Abstracts](https://github.com/margaretstorey/VASE) repo.
* [Writing more accessible theory papers](https://thmatters.files.wordpress.com/2017/05/nature-science-pnas-advice.pdf)
* [Keshav, How To Read a Paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf)
* [Kitchenham, How to Do Systematic Reviews](https://www.inf.ufsc.br/~aldo.vw/kitchenham.pdf
* Creswell's [book on lit reviews and research](https://voyager.library.uvic.ca/vwebv/holdingsInfo?bibId=3081218)