# 🔗 Maximum Length Chain of Pairs (Greedy Algorithm)

This project implements a Greedy Algorithm to solve the Maximum Length Chain of Pairs problem in Java.

## 📌 Problem Statement

You are given an array of pairs where each pair has two numbers:

(a, b)

A pair (c, d) can follow (a, b) only if:

c > b

Your task is to find the maximum length of chain that can be formed.

## 🧠 Approach (Greedy Strategy)

The idea is similar to the Activity Selection Problem:

Sort the pairs based on their second element (ending value).

Select the first pair.

For each next pair:

If its starting value is greater than the last selected pair’s ending value,

Add it to the chain.

This ensures we always pick the pair that finishes earliest, allowing more pairs to fit later.

💻 Code Logic
🔹 Step 1: Input Pairs
int[][] pairs = {{5,24},{39,60},{5,28},{27,40},{50,90}};
🔹 Step 2: Sort by Second Value
Arrays.sort(pairs, Comparator.comparingDouble(o-> o[1]));

Sorting ensures optimal greedy selection.

🔹 Step 3: Build the Chain
int chainLen = 1;
int chainEnd = pairs[0][1];

Loop through remaining pairs:

if(pairs[i][0] > chainEnd)

If valid:

Increase chain length

Update chain end

## 📊 Time Complexity
Operation	Complexity
Sorting	O(n log n)
Traversal	O(n)
Total	O(n log n)
🏁 Sample Output
Maximum length of chain = 3

# 🚀 Key Concepts Used

Greedy Algorithm

Sorting using Comparator

2D Arrays

Time Complexity Analysis

## 📖 Similar Problems

Activity Selection Problem

Job Scheduling Problem

Interval Scheduling

## ✅ Conclusion

This solution efficiently finds the maximum chain length using a greedy strategy by always selecting the pair with the smallest ending time first.
