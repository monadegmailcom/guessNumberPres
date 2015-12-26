Guess number app
========================================================
author: monade
date: 

Whats it all about
========================================================

This app can guess a number you think of by evaluating
following informations:

- a maximal upper bound for your number 
- a couple of yes/no questions it is asking you

Furthermore, given a maximal upper bound for your number, it will give
you the maximal number of questions it will ask to
guess your number.

The maths behind it
========================================================


Of course there is no rocket science involved. The idea
behind it is a simple interval division algorithm. In
each iteration (question asked) the interval containing
your number will shrink by factor two. So $log_2(max)$ is
an upper bound for the number of iterations (questions).
E.g. to guess your number between 1 and 10000 the app needs
no more than

```r
ceiling(log2(100))
```

```
[1] 7
```
number of guesses. 

Programming techniques
========================================================

It makes use of action buttons and reactive expressions.
The update behaviour of shiny is a bit weird, so some
trial and error was necessary to come up with a more or 
less working solution. 

Acknowledgements
===

My special thanks go to my cat Lili who gave me the calm
and strength to go through this.
Your may play around now with the app a few hours full
of surprises and pleasure:
https://monade.shinyapps.io/shinyApp

