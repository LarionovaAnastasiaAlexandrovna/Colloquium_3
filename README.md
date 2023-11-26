# Colloquium 3, Operating Systems
### Task 1
##### TThe directory contains input text files, named as follows: in_<N>.dat, where N is a natural number. Each file consists of two lines. The first line contains a number indicating the action, and the second line contains floating-point numbers separated by a space.
Actions can be as follows:
1 - addition
2 - multiplication
3 - sum of squares
A multithreaded application has been written that performs the required actions on the numbers and writes the sum of the results to the out.dat file. The name of the working directory is passed as an argument of the working line, as well as the number of threads. The code is covered by Unit Tests.

### Task 2
##### A multithreaded application has been developed that computes the product of matrices A (m×n) and B (n×k). The elements cij of the product matrix C = A×B are calculated in parallel p by the same type of flows. If some thread is already calculating the element cij of the matrix C, then the next thread starting the calculation selects the element cij+1 for calculation if j<k, and ci+1k if j=k. After calculating the element of the product matrix, the thread checks whether there is no element that has not yet been calculated. If there is such an element, then proceeds to its calculation. Otherwise, it sends a user message about the completion of its work and suspends its execution. The main thread, having received messages about the completion of calculations from all threads, displays the result on the screen and starts a stream that writes the result to the end of the protocol file. Each thread has a delay in performing calculations (to allow all threads to work). Synchronization of threads among themselves is organized through a critical section or mutex. The code is covered by Unit Tests.