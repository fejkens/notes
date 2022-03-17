# Hashing

Hash tables are data structures that allow us to search in constant time - $O(n)$. They consist of slots - key-value pairs where the keys are slot numbers and the values are the individual pieces of data. Hashing is done by passing each element of a list through a hash function which determines the correct slot. The idea is that the same piece of data passed through the same hash function will always end up in the same slot. Therefore, when searching for this item, we only need to check the correct slot which means searching in constant time.

![Hashing](../pics/hashing1.png)

## Load factor

The load factor is a measure of how 'full' the hash table is. The calculation is:

λ = \frac {number\  of\ items} {table\ size}

## Hash functions

These are functions that determine placement for each piece of data. There are various techniques for that, most simple ones are:

- **Remainder:** If item is a number, divide it by the number of slots in the hash table and use the remainder as the cell number
- **Folding:** If item is a long number, take two-digit pairs from it, add them together and then perform the remainder method. eg. 07780 764796 ⇒ 07 + 78 + 07 + 64 + 79 + 6 = 241 ⇒ 241 % 11 (size of the table) = 10 - cell number.

## Collisions

Sometimes, a hash function will return the same slot for two different pieces of data. This is known as a collision. Collisions can be resolved in different ways:

- **Linear probing**: The item moves to the next cell, one at a time, until it finds one that is empty. Searching for the item involves checking the correct cell that it was originally assigned to and if that is not empty, following the same movements until we either find the item or reach an empty cell.
- **Chaining**: The cells don't hold the data itself but references to lists of items. This way, multiple items can be in the same cell. This doesn't destroy the purpose of hashing, the lists will be a lot smaller compared to the original ones.

![Hashing](../pics/hashing2.png)