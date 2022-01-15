# Contact-Tracing-Simulation
The objective of this project is to design an object-oriented system, implemented with C++ while using classes, standard data structures and unique C++ properties such as the “Rule of 5”. handling memory in C++ and avoid memory leaks.

### Running Example

Consider the following graph, with a single virus in node 0, and a single contact tracer, using MaxRank trees. Blue nodes are healthy, yellow nodes carry a virus, and red nodes are sick.

![](./screenshot.jpg)

In the first iteration, the virus infects node 0, and spreads itself to node 1. The contact tracer, polls the node 0 from the infected queue, and creates a MaxRankTree whose root is the node 0.

![](./screenshot.jpg)

The node 1 is chosen, since it has the maximal rank, and hence all the edges incident to it are removed from the graph. After the first iteration, we obtain the following graph:

![](./screenshot.jpg)

In the second iteration, the first virus spreads itself to node 4. The virus in node 1 infects node 1, but cannot spread itself further, since 1 is disconnected from the graph. Note that in this iteration the contact tracer does nothing, as it appears before the virus (1) in the agents list, and the infection queue is still empty when it's his turn to act.
