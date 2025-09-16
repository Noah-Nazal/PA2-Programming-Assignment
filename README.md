# PA2-Programming-Assignment

Author: Noah Oliver H. Nazal  
Date: 09/16/2025  
Course: ECE2112 – Programming Assignment  

# Software(s) Used:
- Anaconda Navigator  
- Jupyter Notebook  

# Repoistory Information
About: Contains solutions for PA 2 (2 Problems)  

# Languages Used
- Pyhton (100%)

# Version History
V1.0 ([09-14-2025]) – Initial Coding for PA2  

V1.1 ([09-15-2025]) - Creation of Repository Along with Read Me file  

V1.2 ([09-16-2025]) – Finalization of Coding PA2 and Edited Documentation, Code Formatting, and Design in the README File  

# Problem 1: Normalization Problem
Perform normalization on a 5×5 array. Normalization ensures that the dataset has a mean of 0 and a standard deviation of 1, which is useful in machine learning and data preprocessing.

Steps:

1. Create a 5×5 random array using np.random.rand().
2. Compute the mean using .mean() and standard deviation using .std(). 3.Apply normalization using the formula:

X_norm = (X - mean) / std

3. Save the normalized array in a file named X_normalized.npy.

4. Load and print the results to confirm correctness.


# Problem 1: NORMALIZATION PROBLEM
# Input
    # Random 5x5 array
    x = np.random.random ((5, 5))

    # Compute the mean and standard deviation
    x_mean = x.mean()
    x_std = x.std()

    # Normalizing the array
    x_norm = (x - x_mean) / x_std

    # Save normalized array to file
    np.save('x_normalized.npy', x_norm)

    # Output
    print("Original Array (x):", x)
    print("Normalized array:", x_norm)
    print("Mean of normalized array:", x_norm.mean())
    print("Std of normalized array:", x_norm.std())

# Output
    Original Array (x): [[0.13876111 0.82520145 0.44485714 0.71333628 0.31701658]
    [0.93664084 0.40594239 0.98380147 0.29004238 0.65456719]
    [0.93580287 0.31902745 0.66210078 0.69087632 0.71626273]
    [0.01252822 0.22858308 0.69299579 0.23342117 0.32353685]
    [0.82795719 0.1249404  0.52648241 0.95777694 0.38326412]]
    
    Normalized array: [[-1.38090678  1.01845375 -0.31098898  0.62744397 -0.75783859]
    [ 1.40797523 -0.44701029  1.5728189  -0.85212331  0.42202447]
    [ 1.40504624 -0.75080986  0.44835713  0.54893818  0.63767299]
    [-1.82213697 -1.06694608  0.55634649 -1.05003518 -0.73504784]
    [ 1.02808605 -1.4292152  -0.02567877  1.48185363 -0.52627918]]
    
    Mean of normalized array: -9.325873406851315e-17
    Std of normalized array: 1.0

# Problem 2: Divisible by 3 Problem
Using a 10x10 array which are squares of the first 100 positive integers. determine all elements that are divisible by 3.

# Problem 2: DIVISIBLE BY 3 PROBLEM
# Input
    # Create array of squares of first 100 integers
    A = np.arange(1, 101) ** 2

    # Resize to 10x10 array
    A.resize((10, 10))

    # Extract elements divisible by 3
    div_3 = A[A % 3 == 0]

    # Save result
    np.save("div_by_3.npy", div_3)

    # Checking results
    print("10x10 array of squares:\n", A)
    print("Numbers divisible by 3:\n", div_3)

# Output
    10x10 array of squares:
     [[    1     4     9    16    25    36    49    64    81   100]
     [  121   144   169   196   225   256   289   324   361   400]
     [  441   484   529   576   625   676   729   784   841   900]
     [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
     [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
     [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
     [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
     [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
     [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
     [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]

     Numbers divisible by 3:
     [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
     2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
     7569 8100 8649 9216 9801]
