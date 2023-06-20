---
layout: post
title: Step 4 - Translate the ANC Pseudocode into Simple English.
---

This week, I completed Step 4 of my [Refactoring Plan](https://cabreraleon.github.io/ANCrefactorplan/).

![ANCpseudocode](https://cabreraleon.github.io/images/ancpseudocode.png) <br>

**Input.** The ANC algorithm requires a connecting vertex q, a set of neighborhood finders (NF), a local planner lp, and a graph G. <br>
<br>

**Output.** The ANC returns a connected graph G with additional edges than it previously had. <br>
<br>

**Require.** Each NF item in the set of NFs is associated with its own probability *p<sub>i</sub>* of being selected by the ANC. *P* is a set of all these probabilities *p<sub>i</sub>*. Therefore, the *i*-th item *nf<sub>i</sub>*  in set NF has a probability equal to the *i-th* item *p<sub>i</sub>* in set P of being selected. The initial value of *p<sub>i</sub>* is 1 over the total size of the set of NFs since each *nf<sub>i</sub>* must have equal probability of being chosen at the start. <br>
<br>

**Step 1.** Since all NFs start with an equal probability of being chosen, an *nf<sub>i</sub>*  has to be randomly picked for the first iteration. In future iterations, the *p<sub>i</sub>*for each *nf<sub>i</sub>* is no longer equal because it is updated by probabilistic formulas that teach the ANC to choose intelligent NF selections. Thus, the next time the ANC selects an *nf<sub>i</sub>*, it will be based according to its *p<sub>i</sub>*in *P*. <br>
<br>

**Step 2.** Let N be a sets of the neighbors of vertex *q*in graph G that have been found by *nf<sub>i</sub>*. <br>
<br>

**Steps 3-7.** For each neighbor n of vertex *q* that is not vertex *q*itself, the local planner lp will check if vertex *q* can be connected to its neighbor n. A local planar takes as input two vertices and defines the connectivity between them. If the local planner determines there is a feasible connection between *q* and n, then an edge is added between the two vertices, connecting *q* and n, and then proceeds to the next iteration of this for-loop. <br>
<br>

**Step 8-10**. The ANC learns a selection probability for each NF based on its prior success rate and cost. Given that the ANC maintains a selection probability *p<sub>i</sub>*for each *nf<sub>i</sub>* , the evaluation of *nf<sub>i</sub>* is done by determining how many of the returned neighbors n resulted in a successful connection with vertex q. Let r be the prior success rate of the local planner over the set of neighbors N. Let c be the cost incurred. Ultimately, P, r, and c are updated according to advanced statistical equations further explained in Ekenna et al (2013). <br>
<br>
