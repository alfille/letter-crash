# Full Alphabet

The game is not just a single letter, but an alphabet of *M* letters, with restarts after any crashes.

To solve, we'll use a general "recurrence" approach:

This means:

* We sum over all the lengths of *wins < M* with then a loss
  * chance is \\(p_{win}\^i\\,p_{loss}\\)
  * contribution to whatever quantity is
    * i * wins
    * 1 loss
    * Game expected quantity (for restart)
* and add the *M* straight wins case
  * chance \\(p_{win}\^M\\)
  * *M* * wins
  
\\(Quantity = \sum_{i=0}\^{M-1}{p_{win}}\^ip_{loss}(i\\,q_{win}+q_{loss}+Quantity)+{p_{win}}\^M(M\\,q_{win})\\)

Here *Quantity* is what we're assessing (like probability, time, ...) and the *q*'s are the quantity of the individual win or loss steps.

----

We can do some simplification using the formula for a [geometric series](https://en.wikipedia.org/wiki/Geometric_series)

\\(\sum_{i=0}\^{M-1}{p_{win}}\^i = \frac{1-{p_{win}}^M}{1-p_{win}} = \frac{1-{p_{win}}^M}{p_{loss}}\\)

So:

\\(Quantity = \sum_{i=0}\^{M-1}{p_{win}}\^ip_{loss}i\\,q_{win}+\sum_{i=0}\^{M-1}{p_{win}}\^ip_{loss}q_{loss}+\sum_{i=0}\^{M-1}{p_{win}}\^ip_{loss}Quantity+{p_{win}}\^M(M\\,q_{win})\\)

Becomes:

\\(Quantity = \sum_{i=0}\^{M-1}{p_{win}}\^ip_{loss}i\\,q_{win}+(1-{p_{win}}^M)q_{loss}+(1-{p_{win}}^M)Quantity+{p_{win}}\^M(M\\,q_{win})\\)

