# Big-O Notation

## General

- Notation Rules
  - Always default to worst-case runtime
  - Remove constants
    - O(2n) becomes O(n)
  - Different inputs should be displayed with different variables
    - Sequential loops (on same indent level): ```O(a + b)```
    - Nested loops: ```O(a * b)```
  - Drop non-dominant terms
    - Lower-level terms are non-dominant
    - ```n^2``` is higher-level than ```n * log(n)```
    
- Operations that increase time-complexity
  - Operations (+, -, *, /)
  - Comparisons (<, >, ==)
  - Looping (for, while)
  - Outside function call
  
- Operations that increase space-complexity
  - Variables
  - Data structures
  - Function call
  - Allocations

