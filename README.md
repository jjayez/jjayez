## Compact annotated corpora 👋


The .zip file contains the results of annotating 5 spoken French corpora, a subtask of the CODIM ANR project (https://www.codim-project.org/).

The annotation targets French *discourse markers* (DM), about 700 in the present state of our dictionary.

The general goal is to distinguish between uses which are genuinely DM and those which are not.
For instance, *bon* in French can be a discourse marker but also an adjective.

The corpora have been explored with a cascade of automata (603 at the time being) created with the Unitex tool (https://unitexgramlab.org/). Each automaton can:
1. isolate an instance as non-DM (e.g. *bon* as an adjective), the corresponding tag being then {DM,.non-DM},
   > {S} qu'est-ce que {c'est ça,.non-DMP}
3. determine that an instance is a DM, either an adverbial connective (DMC), a subordinating conjunction (DMCSUBCONJ) or a discourse particle (DMP),
   > {S} {non,.DMP} en fin de compte j'ai eu {le temps de,.non-DMCSUBCONJ} rien 
5. propose an instance as a *candidate* DM (DMC-CAND or DMP-CAND)
   > {S} {bon,.DMP-CAND} je t'ai fait un petit apéritif 


This is work in progress (bug correction on automata, new corpora, etc.).

Don't hesitate to contact me if you have any question.
