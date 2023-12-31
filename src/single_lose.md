# Single letter crash
![](images/graphical_loss.png)

We'll use the same graphical presentation as the win.

* *n* random times from 0 to *T*
* "choose" the first one
* "choose" the second one
* Is the second < 1 second after the first? (a **crash**)
* Are all the others after the second?

### Sorted order (*t1 < T-1*)

Take n times sorted:

\\([t_1,t_2,...t_n]\\)

Chance second is in "crash" interval:

\\(\frac{1}{T}\quad\text{if  }t_1<{T-1}\\)

Chance rest are after second:

\\((\frac{T-t_2}{T})^{n-2}\quad\text{for all  }t_2\\)

### Sorted order (*t1 > T-1*)

Take n times sorted:

\\([t_1,t_2,...t_n]\\)

Chance first is in last second:

\\(\frac{1}{T}\\)

Change rest are after first

\\((\frac{T-x}{T})\^{n-1}\\)

### Unsorted (*t1 < T-1*)

There are *n!* ways to choose the the order, but we only care about the first two, and the rest can be in any order.

Thus \\(\binom{n}{2}=n(n-1)\\)

### Unsorted (*t1 > T-1*)

There are *n!* ways to choose the the order, but we only care about the first one, and the rest can be in any order.

Thus \\(\binom{n}{1}=n\\)
