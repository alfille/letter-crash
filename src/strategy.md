# Solution Strategy

We will find a formula for the average total time.

* We'll use *T* as the time interval for each letter
* We have *n* players
* We'll have 1 second as the lockout time (time after the letter is first called out) 
* Each letter is independent, so we can figure out the \\(p_{win}\\) probability as well as \\(t_{win}\\) and \\(t_{loss}\\) times.
* Expected time *E* can be computed knowing the formula from each letter, and the alphabet length *M*

We can leave 1 second as an explicit number, since any other choice would just scale *T* and *E*

