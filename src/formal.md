# Formal Description

## Each step (letter)

*n* players

*T* time interval

*1* second lockout

Each player chooses a time randomly (and uniformly) in the interval 0 to *T* seconds.

If no other player chooses a time less than 1 second after the first time chosen, the ste is **won**

## Full game

*M* letters in alphabet (e.g. 26 in english)

Keep doing steps until:

* *M* winning steps in a row
* a step is lost. Then start over

## Goal

Which *T* gives the fastest average time to victory?


