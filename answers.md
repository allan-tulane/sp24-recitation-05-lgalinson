# CMPS 2200 Reciation 5
## Answers

**Name:** Lakeland Galinson


Place all written answers from `recitation-05.md` here for easier grading.


- **1b.**
In comparing Quicksort variants with TimSort across sorted and shuffled lists, we observe distinct performance patterns:

Quicksort with a Fixed Pivot kind of struggles on sorted lists, showing its worst-case $O(n^2)$ behavior. It performs better on shuffled lists with closer to average-case $O(n \log n)$ efficiency.

Quicksort with a Random Pivot it has consistent performance on both list types, which aligns with its expected $O(n \log n)$ time complexity. It outperforms the fixed-pivot variant on sorted lists.

TimSort excels in all scenarios, especially on sorted lists where its efficiency is best. It operates near $O(n)$ in the best cases and $O(n \log n)$ generally.

Comparing on sorted lists:

|   List Size |   QSort-Fixed-Pivot (ms) |   QSort-Random-Pivot (ms) |   TimSort (ms) |
|-------------|--------------------------|---------------------------|----------------|
|          50 |                    0.286 |                     0.083 |          0.001 |
|         100 |                    0.799 |                     0.167 |          0.001 |
|         150 |                    1.854 |                     0.248 |          0.002 |
|         200 |                    3.091 |                     0.333 |          0.001 |
|         250 |                    5.045 |                     0.386 |          0.002 |
|         300 |                    7.451 |                     0.482 |          0.003 |
|         350 |                    9.991 |                     0.533 |          0.003 |
|         400 |                   13.715 |                     0.621 |          0.002 |
|         450 |                   16.673 |                     0.690 |          0.002 |
|         500 |                   20.320 |                     0.799 |          0.003 |



Comparing on shuffled lists:

|   List Size |   QSort-Fixed-Pivot (ms) |   QSort-Random-Pivot (ms) |   TimSort (ms) |
|-------------|--------------------------|---------------------------|----------------|
|          50 |                    0.067 |                     0.065 |          0.004 |
|         100 |                    0.121 |                     0.129 |          0.007 |
|         150 |                    0.197 |                     0.207 |          0.009 |
|         200 |                    0.285 |                     0.298 |          0.013 |
|         250 |                    0.335 |                     0.417 |          0.016 |
|         300 |                    0.451 |                     0.450 |          0.019 |
|         350 |                    0.472 |                     0.525 |          0.022 |
|         400 |                    0.555 |                     0.611 |          0.026 |
|         450 |                    0.659 |                     0.719 |          0.030 |
|         500 |                    0.735 |                     0.889 |          0.034 |



- **1c.**

Comparing the faster Quicksort variant (which is random pivot) to Python's sorted function (TimSort):

On shuffled lists, both aim for $O(n \log n)$ efficiency, but with TimSort likely will outperform Quicksort due to its code optimizations.

On sorted lists, TimSort's design for exploiting existing order is way more efficent than Quicksort's performance.

