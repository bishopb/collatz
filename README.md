# bishopb/collatz
Software to investigate the 3n+1 problem, also known as the Collatz Conjecture or Syracuse Problem.

Start with a simple recurrence relationship:

> Choose N<sub>0</sub> ∈ ℕ. Let N<sub>i+1</sub> ≡ { 3×N<sub>i</sub>+1 <i>if N<sub>i</sub> is odd</i>; N<sub>i</sub>÷2 <i>otherwise</i> }. 

For example:

   * N=1: 4, 2, 1
   * N=2: 1
   * N=3: 10, 5, 16, 8, 4, 2, 1
   * N=4: 4, 2, 1
   * N=5: 16, 8, 4, 2, 1
   * N=6: 3, 10, 5, 16, 8, 4, 2, 1
   
You're probably starting to see a pattern: no matter the starting number, the recurrence relation *seems* to converge to 1. Despite years of investigation, no one has *proven* this convergence. Some have [claimed proof](http://www-personal.ksu.edu/~kconrow/newpapr2.pdf). Others have claimed it's [unprovable](https://www.youtube.com/watch?v=iALl05kUgy4). Even eminent mathematician Paul Erdős had a go and declared: "Mathematics is not yet ready for such problems."

https://xkcd.com/710/




var collatz = (n) => (n%2 : 3*n+1 : n/2);
