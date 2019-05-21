# notes on complexity and computation
* What does it mean to compute something?
* Complexity
  * Classifications of complexity in terms of the time in terms of the time it takes to solve the problem, while scaling the input size of the problem
    * P
      * P stands for polynomial time. A simple problem solved in polynomial time may look like *T = 2x*, where T is time, and x is the size of the problem. 
      * P is a complexity class that describes the set of all problems solveable in P-time. Problems like searching, sorting, and enumerating fall into this category. 
    * Exp
      * Exponential time problems are solveable in *T = 2<sup>n</sup>*.
    * R
      * refers to the set of all solveable problems, under which P and Exp fall.
    * Determinism
      * the notion, generally, that events are determined by causality. In programming, this is the idea that programs are executed one step at a time, and the same input into the same program will result in the same output.  
      * It's inverse, nondeterminism, is the idea that the next steps the program takes are indeterminate. 
    * NP
      * problems sovleable in p time given a non-deterministic algorithm. Problems can be classified this way if they are: 
        * Solveable in exponential time
        * verifiable in polynomial time
        * also solveable in polynomial time by by non deterministic methods
    * Does P=NP?
      * this is an unsolved problem in mathematics, stating that if a nondeterministic algorithm were developed to solve certain problems, those problems would be solveable in p time. 
    * The same problem can be classified different ways. An optimization problem may be reduced to a decision problem, which is a problem that can be posed as a yes or no question to the input values. 
    * NP-complete 
      * decision problems classifiable in NP
    * NP-hard
      * problems that can be reduced to other problems in NP, but are not NP themselves. 
        * The halting problem is an example of such. It asks whether a running computer program will halt. The problem itself is outside R, meaning it is only solveable in an infinite amount of time. However, it can be reduced to a decision problem: Will the program halt? This classifies it as NP hard. 
      * combinitorial optimization problems fall into this category
        * the traveling salesman problem asks, given a list of cities and distances between them, what is the shortest route that visits each city and returns to the first. It reduces to a desicion problem by iterating through every possible path and asking "is there a shorter path?"
          * this can be solved using a greedy algorithm, where the salesman always heads to the city nearest his current city. 
    * Boolean satisfiability problem:
      * ask whether variables in a boolean formula can be replaced by true or false in such a way that the formula will return TRUE.
      * SAT describes problems that can be modeled by a decision tree. 
