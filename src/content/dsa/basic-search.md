---
layout: '../../layouts/PageLayout.astro'
title: Basic Searching
description: Let's learn about Binary and Linear Search
tags:
  - cpp
  - intermediate
  - advanced
  - algorithms
published: true
lang: cpp
course: dsa
order: 5
---

_"Much of the time/effort/energy spent by computer programs involves searching and sorting data"_

\-someone

**Algorithmic Efficiency** - how many resources a computer needs to expend to process an algorithm

## Linear Search:
1. Searches a structure (ex. an array/list) element by element
2. Performs `n` comparisons if searching for a nonexistent value
    - Minimum comparisons: 1
    - Maximum comparisons: `n`
3. Data does not need to be ordered

When searching for a number between 1 and 100:
```cpp
int linear_search(int target, int max) {
  for (int i = 0; i < max; i++)
    if (i == target) return i;
  return -1;
}
```

## Binary Search
1. Searches pre-sorted indexed structure (ex. an array/list)
2. Performs log base 2 `n` comparisons if searching for a nonexistent value
3. Cuts structure in half each time
    - Minimum comparisons: 1
    - Maximum comparisons: log base 2
    - Data must be ordered

When searching for a number between 1 and 100:

```cpp
int binary_search(int target, int low, int high) {
  while (low != high) {
    int mid = (low + high) / 2;
    if (mid > target) high = mid - 1;
    else if (mid < target) low = mid + 1;
    else return mid;
  }
  return -1;
}
```