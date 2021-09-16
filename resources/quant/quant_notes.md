# Conducting Research With Theoretical and Quantitative CS Research Strategies

## Learning Objectives

* Understand the landscape of CS research
* Learn a bit more about how folks in databases, systems, networks, and experimentally-dominated disciplines do their thing.
* Learn a bit about theory and formal proof techniques in the context of research. (How do you approach a problem? What do you do if you get stuck)

## Notes

[CS Research overview](https://dl.acm.org/doi/pdf/10.1145/1189136.1189180)

We will have Sean Chester and Bruce Kapron help us out.

Three types of quantitative study: **lab** experiments or field experiments with users, often called controlled experiments. And the most dominant one, **simulations** or data experiments, conventionally using some measure of accuracy on a set of sample data. Think Imagenet, Network traces, Github commits. 

### Statistical experiments

![MRNA study XKCD](https://imgs.xkcd.com/comics/statistics.png)

These are experiments that use statistical techniques - Bayesian or frequentist - to draw inferences from a sample to a population. In these types of studies, we aim for *control* over the phenomena of interest. We get control in two ways:

1. Being strict and specific about our hypotheses. We must precisely as possible define the constructs and associated measures we care about. Consider [the following study](https://slate.com/technology/2013/07/statistics-and-psychology-multiple-comparisons-give-spurious-results.html) that looked at fertility and women's clothing. Central to that paper is the notion of fertility. In the paper, peak fertility is defined as 10-17 days post ovulation. When did ovulation happen? Why 10-17, and not 10-16?

2. Randomizing the assignment of subjects to pools, in order to ensure balance between the groups. 

A "quasi-experiment" is a study where there is less control and (usually) no randomization. 

#### Sampling

If you are using statistics, your goal is inference from your sample to a population. Therefore, precisely defining your sampling frame and eventual sample is essential. Often harder than it seems!

A great reference is Baltes and Ralph: https://arxiv.org/pdf/2002.07764.pdf

#### Statistical Analysis

There are a variety of statistical approaches and usually this is pretty specific to a particular area. I would just say 

1. Not all studies need to try and generalize to a population. Exploratory research is pretty useful, even if you cannot conclude anything for a wider group. Not every study needs to report a p-value! Maybe you just want to say "hmm, here's something interesting".  
2. You should be very clear about the assumptions baked into a given analysis approach. Cookie-cutter stats is a bad idea. For example, [Cohen's D categories are probably not right for your domain](https://www.sciencedirect.com/science/article/abs/pii/S1364661319302979). 
3. I personally find Bayesian analysis to be much closer to the way I like to think about my data and analysis. It also gives a much richer notion of posterior distribution that can be used in many useful ways, esp for practical significance. A great book on [getting started with Bayesian inference is by McIlreath](https://xcelab.net/rm/statistical-rethinking/). The example I showed is from [Furia, Torkar, and Feldt](https://arxiv.org/abs/2101.12591)
4. Probably type-S error (sign) and type-M error (magnitude) are more important than Type 1 and Type 2 errors.

#### Replication and Open Science

In my view the thing that best lends evidence to the effect being true, and important, is more people doing studies that confirm something is happening. Replication is the act of conducting a close parallel to the existing study (strict) or similar in nature to test the hypothesis (conceptual). A meta-study can then be done on multiple individual studies to confirm an effect exists. However, **replications depend on open science**. If you don't make your data or analysis or study protocols available, others can't confirm your results. 

1. Publish an artifact if possible
2. Keep the artifact on a long-term repository, such as Zenodo or FigShare.
3. Licence the artifact.
4. Put everything you can into the artifact: protocol, data, analysis code, visualizations. 
5. Consider registering your study first, if your journals support pre-registration. 

#### Bad Practices in Statistical Research

I direct you to the smells paper for more information. [Gelman's blog](https://statmodeling.stat.columbia.edu) is a fun survey of various issues. But broadly speaking, in experiments (in particular!) we need to worry about researcher bias:

- Not publishing bad results
- Suspiciously many results close to \alpha = 0.05
- Hypothesizing after results are known (HARK)
- Multiple comparisons problems
- Forking path problems
- Low power and small effect sizes. See the [G*Power](https://stats.idre.ucla.edu/other/gpower/) tool.
  - Your pilot study analyzed with a Student *t*-test reveals that group 1 (N  =  29) has a mean score of 30.1 (SD, 2.8) and that group 2 (N  =  30) has a mean score of 28.5 (SD, 3.5). The calculated *P* value  =  .06, and on the surface, the difference appears not significantly different. However, the calculated effect size is 0.5, which is considered “medium” according to Cohen. In order to test your hypothesis and determine if this finding is real or due to chance (ie, to find a *significant* difference), with an effect size of 0.5 and *P* of <.05, the power will be too low unless you expand the sample size to approximately N  =  60 in each group, in which case, power will reach .80. For smaller effect sizes, to avoid a Type II error, you would need to further increase the sample size. Online resources are available to help with these calculations.

#### Describing Limitations

If you do empirical research you should report on possible threats to the validity of your conclusions. Conventionally, one reports:

- External validity - about the generalizability of the results

- Internal validity - how well the tools chosen allow us to test the hypothesis.

- Construct validity - how well the constructs measure the phenomena of interest (e.g. fertility)

But there are others as well. The best approach is to seriously reflect on the paper and identify possible problems critically. Chances are the reviewers will find them anyway! Better to head them off at the pass. [See Martin Robillard's post on this.](https://www.cs.mcgill.ca/~martin/blog/2015-04-29.html)

### Simulations

**Computational simulation studies** are studies that analyze data in a controlled, highly precise way. There are **data** simulations and model simulations. 

In a model simulation, we define a model about how we think the world ought to work, then use simulation techniques - usually something probabilistic like Monte Carlo - to see how our model works. We then try to validate the model outputs against what we think should, or could, happen. Simulating the impact of virus spread on hospitalization is one example. Climate models are another. There's work at Facebook to simulate the social network, in order to test new features. Simulating a new network intrusion detection tool is another example: here, the new tool is our "theory" or model, and the 

Here's Brandon:

>  So in simulations, we have a number of problems, like: 1) not having a baseline or ground truth to validate the simulation itself, 2) not being able to reproduce data even when we have it (crowds are semi-chaotic and ill-conditioned, ie *very* sensitive to initial conditions and context), 3) choosing the right model when there are hundreds and few are validated in any real way or have extremely limited scope. (Haworth)

The other type of simulation is one where we run a precise data experiment, which accounts for a vast number of CS research papers. 

Again, the specifics - such as which measures of accuracy to use - are highly specific to your field. A few best practices I know:

- Be clear what the gold set is. If you are lucky the field defines one, such as ImageNet (in which case, look for problems with bias and variance). 
- Optimize the hyper parameters
- Account for data imbalance
- Use the train/test/validate split
- Run the tests multiple times to get an average
- [Other bad smells listed here.](https://arxiv.org/abs/1803.05518)

### Formal Proof Approaches

Bruce mentioned a lot of these the other day. Commonly used approaches include 

- Explicit definitions of assumptions, problem statements, axioms;
- taking existing techniques and applying them to new problems; 
- doing limited simulation to convince yourself of the approach; 
- Learning and leveraging mathematical approaches. 
- Solving restricted versions of the problem.
- Nearly every theory contribution comes with a proof

I think every CS student should have a good understanding of theoretical CS tools such as proof by induction, contradiction, formal logic, etc.

## Readings (before class)

### Optional and Recommended

* [Doing good KDD research](https://www.cs.ucr.edu/~eamonn/Keogh_SIGKDD09_tutorial.pdf)
* http://www.jfsowa.com/ikl/Stonebraker.pdf
* [V&V of crowd models](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=5679166)
* [Manuel Blum - theory research tips](http://www.cs.cmu.edu/~mblum/research/pdf/grad.html)
* [History of Complexity](https://people.cs.uchicago.edu/~fortnow/papers/history.pdf)
* [importance of effect size](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3444174/)
* [Empirical Standards in SE](https://github.com/acmsigsoft/EmpiricalStandards)
