# Sequential search

A search technique that iterates over every element in a list and checks if it's the element we're looking for. This technique is useful if the elements are not ordered.

![Sequential search](../pics/sequential-search1.png)

## Cases on an unordered list

| Item presence         | Best case | Worst case | Average case |
| -------------         | --------- | ---------- | ------------ |
| Item is present       | 1         | n          | n/2          |
| Item is not present   | n         | n          | n            |

When a list is ordered, a sequential search becomes more efficient. As we step through the list and make comparisons, as soon as we arrive at an element that is larger than the item that we're looking for, the search can stop. We know that every element after that cannot be the element we're after.

![Sequential search](../pics/sequential-search2.png)

## Cases on an ordered list

| Item presence         | Best case | Worst case | Average case |
| -------------         | --------- | ---------- | ------------ |
| Item is present       | 1         | n          | n/2          |
| Item is not present   | 1         | n          | n/2          |