---
marp: true
author: Neil Ernst
---

# M2 - Ways of Knowing, Philosophy of Science

## Learning Objectives

* Characterize different theoretical perspectives on research and epistemology
* Know how little we know about philosophy of science (and who to ask for help!)
* Describe different key developments in epistemology
* Relate phil. of science to your research

## Day 1
- elevator pitch description 
- elevator pitch breakout groups - present pitches to 4 others
- upload your pitch to Brightspace in the assignments

## Day 2
- research paradigms from Easterbrook
	- Is CS an empirical science? A physical science? A social science? What Faculty should we live in? 
	- What is the role of theory in CS?
- the onion model exercise (breakouts)
	- Neil's research in the onion
- ABCs and McGrath's circumplex 

---
## Slides and Notes
- The progress of scientific inquiry. What is the point of science?
- Figuring out where your research fits in these paradigms.

---
# What sort of research questions are you asking:
- **knowledge-seeking** questions:
  - exploratory: understand the problem, surface new insights, generate new hypotheses. Inductive. Often done in data analytics and data mining research. 
  - confirmatory: given a **specific**, **falsifiable** hypothesis, along with some prior beliefs, gather evidence about the phenomenon. Experiments help us control exogenous influences (i.e. colliders in a causal network model).
- **design oriented**: I want to fix a problem in a real setting. Solution-seeking
- **logical deductive**: I want to establish ("prove") some new knowledge based on a set of axioms and proof approaches.

---
We have data (causes), arguments (i.e., theories/explanations), conclusions (or predictions). 

* **Induction**: from the evidence, postulate an explanation. (If I see P, Q, I postulate P→Q). If the sun rises every morning for X days, generalize a rule that the sun always rises.
* **Deduction**: from an argument and data, draw conclusions. (If I know P, P→Q, I can conclude Q). If someone suggests there is a heliocentric orbit, predict when the eclipse might happen.
* **Abduction**: from the predictions and theory, derive the possible explanations (note: infinitely many!) (If I know P→Q, Q, I abduce P). (Abduction is diagnosis). Note that in abduction we might ALSO know R→Q, and so both P and R are valid.

---
Theories: 
	- explain
	- predict
	- organize
	- design

----
Q: Why is astrology not a science? What about [Bem's paper https://slate.com/technology/2013/07/statistics-and-psychology-multiple-comparisons-give-spurious-results.htmlestablishing ESP?](https://slate.com/health-and-science/2017/06/daryl-bem-proved-esp-is-real-showed-science-is-broken.html)
	
	- large sample sizes
	- replication of findings
	- well known statistical analysis

The [garden of forking paths.](https://slate.com/technology/2013/07/statistics-and-psychology-multiple-comparisons-give-spurious-results.html)

[Ghostbusters video.](https://www.youtube.com/watch?v=5ohlA__xABw)

----
### Logical deduction (rationalism)
- the epistemology of theoretical CS
- Euclid and non-Euclidean geometry
	- [Postulates and axioms](https://www.pitt.edu/~jdnorton/teaching/HPS_0410/chapters/non_Euclid_fifth_postulate/index.html#Euclid1): parallel lines never intersect; points may be connected with a straight line, etc.
	- What is the connection to "reality"?
- a system of axioms (Principia Mathematica). The halting problem and computability. 
	- If a (logical or axiomatic formal) system is consistent, it cannot be complete. 2) The consistency of axioms cannot be proved within their own system.

----
- verifying proofs and computer proofs - [the 4 color proof](https://en.wikipedia.org/wiki/Four_color_theorem#Proof_by_computer). Complex proofs.
- Einstein: "Pure logical thinking cannot yield us any knowledge of the empirical world; all knowledge of reality starts from experience and ends in it."
- Kant: mathematics gives us [real knowledge of the world](https://personal.lse.ac.uk/robert49/teaching/ph201/Week02_xtra_Godfrey-Smith.pdf) but does not require experience for its justification

----
### Positivism and Empiricism
I need to measure some effect in the real world. Science is the accumulation of many truths (logical positivism). As I find out more evidence, I add it to the pile of "known facts". Theories then seek to explain these known facts. Claims should be verifiable in principle ("does a feather fall at the same speed as a rock on the Moon"). 
- Define "verifiable" (i.e. confirmatory)
- how do I know X causes Y? Hume.

----
### Falsificationism and modern philosophies of science
- **Popper** - I need to specify a theory that can be falsified. 
- "Intellectual honesty then consists not in trying to entrench, or establish, one's position but in specifying precisely the conditions under which one is willing to give one's position up" (Lakatos summary). Strong ideas weakly held.
- Mayo: statistical inference as severe testing
  
----
- Popper: create theories that might be falsified, rather than general, always true statements (focus on novelty). Einstein and the bending of light.
- Popper: not clear what constitutes "rejection" of a theory (how much evidence is needed?)
- Kuhn - Science is a social enterprise and is about the distinction between gradual and sudden paradigm changes. Revolution is uncommon.  Old scientists dying out. 
 
----
- Story of Copernicus (helio-centricity) and planetary physics: Copernican predictions less accurate (measurement errors). The difficulty (*incommensurability*) of holding incoherent concepts in different paradigms, as anomalies start to accumulate theories are under tension. Can't falsify in different paradigms.
- Perhaps we should look at probability as a guide - how much should we believe something, given the prior knowledge we had and the likelihood of the data.
- Lakatos: think of science as a "research programme" that aspires to constantly explain new evidence (astronomy is a popular one) with new theories. Focus on growth and stagnation of specific "programmes" rather than strict falsification

----
#### Pragmatism 
- C.S. Pierce, Richard Rorty, others: “[What concrete practical](https://iep.utm.edu/pragmati/#:~:text=Pragmatism%20is%20a%20philosophical%20movement,ideas%20are%20to%20be%20rejected) difference would it make if my theory were true and its rival(s) false?” Where there is no such difference, there is no genuine (that is, non-verbal) disagreement, and hence no genuine problem."
- Theories are tools for coping with reality and should be judged by how they solve a problem.

----
#### Critical theorists and constructionists
But knowledge is not an objective thing: it is situated within messy human structures. Data do not appear fully formed but are interpreted and constructed.
It is vital to situate knowledge within a context. Thus ethnographies depend on what we are studying (e.g., homeless populations in Edmonton), but also who is doing the study (the ethnographer). What the ethnographer sees will be coloured by their perspective. "Generalizing" to other situations (Calgary, USA, homeless but not mentally ill populations) is difficult. Rely on replication and triangulation to find general effects. 
Critical theory extends this to specific philosophical perspectives such as gender or class (can we understand homelessness outside of the system of capitalism that Edmonton operates in)

----
- Are there "laws" in social sciences? 
- Feyerabend: science is a social endeavour and human actions such as lies, deception, luck play a big role. There is no single scientific method that makes sense (Against Method is his most well known work). No theory is consistent with all facts.

----
### The Problems with NHST
As I mentioned problems have emerged with the "standard" statistical inferential scientific framework of null-hypothesis significance testing:
- if I know the data I can formulate the hypothesis to look like it explains the data (HARKing)
- I might choose a null that no one agrees is the opposite of the hypothesis of interest
- if I get a negative result I can bury it (file-drawer problem)
- we might call these "Questionable Research Practices"


----
- p-values over 0.05 are hard to publish (Ioannidis, [Why Research Findings...](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.0020124) but ignore his idiotic studies on Covid)
- I might run a study with small N, and not have power to find real (likely small) effects. Big N studies are expensive.
- But the more data I collect, the more likely I am to find an effect. 
- I can run significance tests multiple ways, and probability guarantees I will find something significant (multiple comparisons problem) (see https://xkcd.com/882/)
- I have many research design options when creating my study (sample sizes, experiment setup, ML algorithms) so the results might be biased to my choices and not replicate (forking paths)

----
### Solutions: 
1. Replication
2. Pre-registration
3. Strict or severe testing
	- Meehl and Deborah Mayo. A weak hypothesis test is one where data x agree with a claim C but the method is practically guaranteed to find the agreement, and has no capability of finding any flaws in C (Bad Evidence, No Test)
	- A strong severity requirement is that we have evidence for claim C only to the extent it survives stringent scrutiny, i.e., our test was highly capable of finding flaws in it.

----
### Connecting the ABC circumplex and research onion to your work

## Other resources:
- Uvic [Philosophy of Science course](https://www.uvic.ca/humanities/philosophy/assets/docs/courseoutlines/2019_fall/220-brown.pdf)
- Imre Lakatos - [Criticism and the Methodology Of Scientific Research Programmes](https://personal.lse.ac.uk/robert49/teaching/ph201/week05_xtra_lakatos.pdf) 
- Kuhn - [The Structure of Scientific Revolutions](https://en.wikipedia.org/wiki/The_Structure_of_Scientific_Revolutions)
- Einstein, [“On the Method of Theoretical Physics”](http://www.pitt.edu/~jdnorton/teaching/2590_Einstein_2015/pdfs/Einstein_Method_Physics.pdf)
- False-Positive Psychology: Undisclosed Flexibility in Data Collection and Analysis Allows Presenting Anything as Significant, Joseph P. Simmons, Leif D. Nelson, Uri Simonsohn, 2011.
- [Great set of slides on phil. of science at LSE](https://personal.lse.ac.uk/robert49/teaching/ph201)

----
## Activity

- Design and document your research methodology using https://www.aesanetwork.org/research-onion-a-systematic-approach-to-designing-research-methodology/

----
## Readings (before class)

* [Guide to Advanced Empirical SE - Selecting Research Methods](EmpiricalSEEasterbrook.pdf)
* [ABCs of Research](ABC-SE.pdf)

Optional:

- Our [Who What How framework](https://link.springer.com/article/10.1007%2Fs10664-020-09858-z)