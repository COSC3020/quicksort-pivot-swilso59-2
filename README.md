# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

## Answer 
In slide 34. We can see that using the leftmost element as the pivot. We can see that this has a 50% chance of being a good pivot. 

Since we are picking 3 elements and do not know what they are. We need to consider every permutation. We can do this by assigning our pivots a percentage. A bad pivot can be broken down into two sections high or low. We know that the chance of picking a bad pivot is $\frac{1}{2}$ this give us a $\frac{1}{4}$ chance of picking a pivt that is high or low and a $\frac{1}{2}$ chance of the pivot being good. knowing this we can now go through all the permutations. Then we can determine the probability of if our final pivot will be good or bad. 
permutations of a pivot:
1. LLL
2. LLG
3. LLH
4. LGL
5. LGG*
6. LGH*
7. LHL
8. LHG*
9. LHH
10. GLL
11. GLG*
12. GLH*
13. GGL*
14. GGG*
15. GGH*
16. GHL*
17. GHG*
18. GHH
19. HLL
20. HLG*
21. HLH
22. HGL*
23. HGG*
24. HGH
25. HHL
26. HHG
27. HHH
Taking the selections that result in a good pivot and adding up there probablility will give us the chance we have of selecting a good pivot via the median of three method.
LGG*
LGH*
LHG*
GLG*
GLH*
GGL*
GGG*
GGH*
GHL*
GHG*
HLG*
HGL*
HGG*
This give use the equation
