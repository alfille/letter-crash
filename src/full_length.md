# Full Alphabet: Length

How many letters, on average, will we go though?


From [our initial analysis](full.html)

\\(Quantity = \left(\frac{1-{p_{win}}^M}{{p_{win}}^M}\right)\left(q_{loss}+\frac{p_{win}}{1-p_{win}}q_{win}\right)+q_{victory}\\)

where
\\(q_{win}=1\\)

\\(q_{loss}=1\\)

\\(q_{victory}=0\\)

since each step counts as *1* but winning doesn't add another letter.

\\(Length = \left(\frac{1-{p_{win}}^M}{{p_{win}}^M}\right)\left(1+\frac{p_{win}}{1-p_{win}}\right) = \left(\frac{1-{p_{win}}^M}{{p_{win}}^M}\right)\left(\frac{1}{1-p_{win}}\right)\\)


----------
Not very well behaved for low probability steps.

![](images/full_length.png)

Cut off at 500 length.