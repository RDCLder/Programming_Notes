# Sorting Algorithms

## Merge Sort

- Integer Multiplication
  - Consider the following: ```1234 x 5678```
    - After several operations, the solution is ```7006652```
    - The number of operations required to find the solution is: ```constant * 2n ** 2```
    - The basic algorithm for performing multiplication is therefore exponential (quadratic).

- Karatsuba Multiplication
  - Consider the previous example: ```1234 x 5678```
    - We can break down both numbers into four blocks and perform the following steps
      - ```a = 56```
      - ```b = 78```
      - ```c = 12```
      - ```d = 34```
    - 1. Compute ```a * c```
      - ```a * c = 672```
    - 2. Compute ```b * d```
      - ```b * d = 2652```
    - 3. Compute ```(a + b)(c + d)```
      - ```(a + b)(c + d) = 134 * 46 = 6164```
    - 4. Compute step 3 - step 2 - step 1 (Gauss's trick)
      - ```6164 - 2652 - 672 = 2840```
    - 5. Combine step 1, 2, and 4 in the following way
      - ```672 * 10000 + 2652 + 284 * 1000 = 7006652```
  - This is fundamentally a recursive algorithm.
  
- Merge Sort
  - Good introduction to divide & conquer
    - Improves over Selection, Insertion, Bubble sorts which all have quadratic (N ^ 2) run times for arrays with N elements.
  - Introduces guiding principles for algorithm analysis
    - Worst-case
    - Asymptotic analysis
  - Generalizes to master method.

- The Sorting Problem
  - Input: An array of N unordered numbers.
  - Output: A sorted array from smallest to largest
  - Merge Sort
    - We divide the array into two halves and sort each half first.
    - We then combine the two sorted halves in some way.
    - Python function:
    ```python
    def mergeSort(arr):
    
      minimum = 4
      n = len(arr)
      if n < minimum:
          return arr
      else:
          subArr1 = sorted([arr[i] for i in range(n // 2)])
          subArr2 = sorted([arr[j] for j in range(n // 2, n)])
          finalArr = []
          i = 0
          j = 0

          for k in range(n):
              if i == n // 2: # Comment 1
                  finalArr.append(subArr2[n // 2 - 1])
              elif j == n // 2:
                  finalArr.append(subArr1[n // 2 - 1])
              else: # Comment 2
                  if subArr1[i] < subArr2[j]:
                      finalArr.append(subArr1[i])
                      i += 1
                  elif subArr1[i] > subArr2[j]:
                      finalArr.append(subArr2[j])
                      j += 1

          return finalArr
    ```
      - Comment 1
        - We must account for end cases when ```subArr[n // 2]``` is out of index.
        - This is the case for the final iteration of k.
        - We simply append the remaining number (which will be in the other subArray).
      
      - Comment 2
        - If neither end case is met, the loop continues iterating to check which subArray has a smaller number to append to the final array.
        - Each time a number is appended, its respective sub array's index is incremented by one to represent moving on to the next biggest number in that array.
  
- Running time analysis
  - Computation speed (runtime) is a direct consequence of how many operations need to be performed to execute all the code.
  - Merge sort has less than or equal ```4n + 2``` operations for an array of n elements.
    - Merge sort is therefore ```constant * log2(n) + constant * n.```
    - Assuming n is greater than or equal to 1, we can "generalize" this into ```6n * logN + 6n``` operations.
  - Traditional sorting algorithms (insertion, selection, bubble) are all quadratic which require many times more operations than logarithmic algorithms.
  - Recursion Tree Model
    - Root:  Entire input.
    - Level 1:  Left, right.
    - Level 2:  Left1, Left2, Right1, Right2.
    - etc.
  - The levels of a recursion tree is a function ```log2(n)``` of the input array.
  - At most, the total amount of work (required operations) can be expressed as ```6n(log2(n) + 1).
    - ```6n``` corresponds to the amount of work per level.
    - ```log2(n) + 1``` corresponds to the amount of levels.
