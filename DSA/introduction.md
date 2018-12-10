# Introduction to Algorithms

## Topics

- Vocabulary for design and analysis of algorithms
  - e.g. "Big-O" notation
  - "sweet spot" for high-level reasoning about algorithms
    - Ignore constants and lower-level terms and focus on how well algorithmic performance scales with large input sizes
    - Big-O notation is the mathematical representation of this sweet spot.

- Divide and conquer algorithm design paradigm
  - Break down a problem into smaller components.  Solve them recursively and combine solutions into one overall solution.
  - There is no silver bullet in algorithm design.
    - There are a few general algorithm design techniques that are useful across a range of domains
  - Divide and conquer (DnC) applies to the following:
    - Integer multiplication
    - Sorting
    - Matrix multiplication
    - Closest pair

- Randomization in algorithm design
  - Allowing randomization inside an algorithm can often lead to simple, elegant, and practical solutions.
    - e.g.
  - Applies to the following:
    - QuickSort
    - Primality testing
    - Graph partitioning
    - Hash functions and hash maps

- Primitives for reasoning about graphs
  - Primitives are operations that can be performed on data that is so fast, it's essentially free
    - They are a tool that should be used whenever there's an opportunity
    - e.g. sorting numbers
  - Applies to the following:
    - Connectivity information
    - Shortest paths
    - Structure of information in social networks

- Use and implementation of data structures
  - Data structures are responsible for organizing data to enable fast queries.
    - Different data types support different types of queries.
  - Includes:
    - Heaps
    - Balanced binary search trees
    - Hash tables/maps
    - Variants (e.g. bloom filters)

---

## General

- Why Study Algorithms
  - Important for all branches of computer science
  - Plays a key role in modern technological innovation
    - Moore's law states that the density of transistors in integrated circuitswould double every 1-2 years.
    - In many areas, performance gains due to algorithms have vastly exceeded gains due to increased processor speed.
  - Provides novel "lens" on processes outside of CS and tech
    - e.g. quantum mechanics, economic markets, evolutionary biology
  - Challenging (i.e. good for the brain) and "fun"

- Algorithm Designer's Mantra
  - The most important principle for the good algorithm designer is to refuse to be content.
    - i.e. Can we do better?
  - There is usually a simple, "naive" brute-force approach that tests every single possibility
    - These are often inefficient and time-consuming.
    - There is usually at least one better method.
