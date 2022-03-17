# Bubble sort

In a given list, bubble sort takes items, two at a time, and decides whether they should be swapped or not. The algorithm metaphorically puts these items in a 'bubble' as it passes through the whole list. As it makes each pass, it tracks whether it has swapped any items. If it has, it needs to run again - if it hasn't, the algorithm can stop as the list is sorted.

The bubble sort is not a very efficient sorting technique, it's cost is $O(n^2)$. The advantage that the bubble sort provides is stopping early if the list is already sorted or if it only takes a few passes to sort.

![Bubble sort](../pics/bubble-sort.png)