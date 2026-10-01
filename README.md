# HackerRank 3rd Semester Algorithm Portfolio

## Student Information

- **Name:** Jyoti Pradeep Netrakar
- **Student ID / USN:** R25EF109
- **Semester:** 3rd Semester
- **Programming Language:** Java
- **HackerRank Profile:** [View my HackerRank Profile](https://www.hackerrank.com/profile/jyotinetrakar201)
- **GitHub Repository:** [HackerRank-3rdSem-Algorithm-Portfolio](https://github.com/pnjyoti/HackerRank-3rdSem-Algorithm-Portfolio)

---

## About This Portfolio

This repository contains five algorithmic problems completed as part of the 3rd Semester HackerRank Algorithms and GitHub Coding Portfolio activity.

The problems cover implementation, arrays, sorting, searching, and greedy algorithm techniques. Each solution is implemented in Java and includes an analysis of the approach, time complexity, and auxiliary space complexity.

---

## Problems Completed

| No. | Problem | Topic | Time Complexity | Auxiliary Space |
|---|---|---|---|---|
| 1 | [Mini-Max Sum](https://www.hackerrank.com/challenges/mini-max-sum/problem) | Arrays / Implementation | O(N) | O(1) |
| 2 | [Birthday Cake Candles](https://www.hackerrank.com/challenges/birthday-cake-candles/problem) | Arrays / Counting | O(N) | O(1) |
| 3 | [Insertion Sort – Part 1](https://www.hackerrank.com/challenges/insertionsort1/problem) | Sorting | O(N) | O(1) |
| 4 | Binary Search | Searching | O(log N) | O(1) |
| 5 | [Mark and Toys](https://www.hackerrank.com/challenges/mark-and-toys/problem) | Greedy / Sorting | O(N log N) | O(N) |

---

# 1. Mini-Max Sum

### Problem Summary

Given five positive integers, calculate the minimum and maximum sums that can be obtained by adding exactly four of the five integers.

### Approach

The solution calculates the total sum of all elements while finding the minimum and maximum values.

- Minimum four-element sum = total sum − maximum value
- Maximum four-element sum = total sum − minimum value

This avoids sorting and requires only one traversal of the array.

### Complexity

- **Time Complexity:** O(N)
- **Auxiliary Space:** O(1)

### Alternative Approach

The array can also be sorted first. After sorting, the sum of the first four elements gives the minimum sum and the sum of the last four gives the maximum sum.

However, sorting requires O(N log N) time, so tracking the minimum and maximum directly is more efficient.

### Solution

[View Mini-Max Sum solution](./01-Mini-Max-Sum/solution.java)

---

# 2. Birthday Cake Candles

### Problem Summary

Given the heights of candles, find how many candles have the maximum height.

### Approach

The solution maintains two variables:

- `max` — the tallest candle found so far
- `count` — number of candles having that maximum height

Whenever a taller candle is found, the maximum is updated and the count is reset to 1. If another candle has the same maximum height, the count is increased.

### Complexity

- **Time Complexity:** O(N)
- **Auxiliary Space:** O(1)

### Alternative Approach

The array can be sorted and the last value can be identified as the maximum, followed by counting occurrences of that value.

The one-pass approach is more efficient because it avoids sorting.

### Solution

[View Birthday Cake Candles solution](./02-Birthday-Cake-Candles/solution.java)

---

# 3. Insertion Sort – Part 1

### Problem Summary

Given an almost-sorted array where the last element is out of position, insert that element into its correct position while shifting larger elements to the right.

### Approach

The last element is stored temporarily.

The algorithm then compares it with the elements to its left. Elements larger than the stored value are shifted one position to the right. Once the correct position is found, the stored value is inserted.

### Complexity

- **Time Complexity:** O(N)
- **Auxiliary Space:** O(1)

### Alternative Approach

A complete insertion sort could be applied to the entire array, but this problem only requires inserting the final element into an already sorted portion. Therefore, processing only the necessary portion avoids unnecessary work.

### Solution

[View Insertion Sort – Part 1 solution](./03-Insertion-Sort-Part-1/solution.java)

---

# 4. Binary Search

### Problem Summary

Binary Search finds a target element in a sorted array by repeatedly dividing the search range into two halves.

### Approach

The solution maintains two boundaries:

- `low` — beginning of the search range
- `high` — end of the search range

The middle element is checked.

- If it matches the target, the search ends.
- If the middle value is smaller than the target, the left half is discarded.
- Otherwise, the right half is discarded.

The process continues until the target is found or the search range becomes empty.

### Complexity

- **Time Complexity:** O(log N)
- **Auxiliary Space:** O(1)

### Alternative Approach

Linear search can check every element one by one. Its time complexity is O(N), whereas binary search reduces the search space by half at every step.

### Solution

[View Binary Search solution](./04-Binary-Search/solution.java)

### Note

Binary Search was implemented and tested locally in Java because this activity permits a suitable coding environment for Problem 4.

---

# 5. Mark and Toys

### Problem Summary

Given prices of toys and a fixed budget, determine the maximum number of toys that can be purchased without exceeding the budget.

### Approach

The prices are sorted in ascending order. The algorithm then purchases the cheapest toys first until adding another toy would exceed the available budget.

This is a greedy approach because choosing the cheapest available toy maximizes the number of toys that can be purchased.

### Complexity

- **Time Complexity:** O(N log N)
- **Auxiliary Space:** O(N)

### Alternative Approach

A brute-force approach could consider different combinations of toys, but this would be much more expensive. Sorting the prices and selecting the cheapest toys provides an efficient greedy solution.

### Solution

[View Mark and Toys solution](./05-Mark-and-Toys/solution.java)

---

# Algorithm Techniques Learned

Through these problems, the following algorithmic techniques were practiced:

- Array traversal
- Minimum and maximum tracking
- Counting occurrences
- Element shifting
- Insertion sort
- Binary search
- Sorting
- Greedy selection
- Big-O time and space complexity analysis

---

# HackerRank Evidence

Screenshots of accepted submissions are maintained as evidence for the completed problems.

### Completed Challenges

- Mini-Max Sum — Accepted
- Birthday Cake Candles — Accepted
- Insertion Sort – Part 1 — Accepted
- Binary Search — Tested locally
- Mark and Toys — Accepted

### Badge Evidence

HackerRank Problem Solving badge progress/evidence will be included in the final activity report.

---

# Repository Structure

```text
HackerRank-3rdSem-Algorithm-Portfolio/
│
├── README.md
│
├── 01-Mini-Max-Sum/
│   └── solution.java
│
├── 02-Birthday-Cake-Candles/
│   └── solution.java
│
├── 03-Insertion-Sort-Part-1/
│   └── solution.java
│
├── 04-Binary-Search/
│   └── solution.java
│
└── 05-Mark-and-Toys/
    └── solution.java
