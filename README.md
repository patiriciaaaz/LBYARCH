# LBYARCH

Write the kernel in (1) C program and (2) an x86-64 assembly language. The kernel must calculate the distances between the coordinate points across two vectors.
*Required to use functional scalar SIMD registers
*Required to use functional scalar SIMD floating-point instructions
Input: Scalar variable n (integer) contains the length of the vector; Vectors X1, X2, Y1, Y2, and Z are single-precision float.
Process: Z [i]
=
'(X2 [i] − X1 [i])2 + (Y2 [i] − Y1 [i])2
Example:
X1 -> 1.5, 4.0, 3.5, 2.0
X2 -> 3.0, 2.5, 2.5, 1.0
Y1 -> 4.0, 3.0, 3.5, 3.0
Y2-> 2.0, 2.5, 1.0, 1.5
(answer)
Z-> 2.5, 1.58113883, 2.692582404, 1.802775638
Output: store result in vector Z. Display the result of 1st ten elements of vector Z for all versions of kernel (i.e., C and x86-64).
Note:
1.) Write a C main program to call the kernels of the C version and x86-64 assembly language.
2.) Time the kernel portion only.
3.) For each kernel version, time the process for vector size n = {2^20, 2^24, and 2^30}. If 2^30 is impossible, you may reduce it to the point your machine can support (i.e., 2^28 or 2^29). 
4.) You must run at least 30 times for each version to get the average execution time.
5.) For the data, you may initialize each vector and scalar variable with the same or different random value.
6.) You will need to check the correctness of your output. Thus, if the C version is your "sanity check answer key," then the output of the x86-64 version has to be checked with the C version and output correspondingly (i.e., the x86-64 kernel output is correct, etc.).
