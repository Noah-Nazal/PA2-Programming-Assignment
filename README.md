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

# Output (example)
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

# Problem 2: Emoticon Problem
Change specific words into emoticons from user input

Mappings Used:

"smile" → :)

"grin" → :D

"sad" → :((

"mad" → >:(

# Problem 2: EMOTICON PROBLEM
# Input
    def emoticon(sentence):
        # Make dictionary for word-emoticon equivalents
        replacements = {
            "smile": ":)",
            "grin": ":D",
            "sad": ":((",
            "mad": ">:("
        }

        # Temporary storage of characters
        word = ""
        result = ""

        for ch in sentence:
            if ch != " ":
                word += ch
            else:
                # Process word when space is found
                if word in replacements:
                    result += replacements[word]
                else:
                    result += word
                result += " "
                word = ""

        # After loop, process last word
        if word != "":
            if word in replacements:
                result += replacements[word]
            else:
                result += word

        return result

    # Example:
    x = input("Enter a sentence: ")
    print(emoticon(x))

# Output (example)
    I am :(( but I try to :)

# Problem 3: Unpacking List Problem
Unpack a list into first, middle, and last elements

lst = [1, 2, 3, 4, 5, 6]

# Problem 3: UNPACKING LIST PROBLEM
# Input
    # Starting list
    writeyourcodehere = [1, 2, 3, 4, 5, 6]

    # Breaking into segments
    first, *middle, last = writeyourcodehere

    # Output
    print("first:", first)
    print("middle:", middle)
    print("last:", last)

# Output
    first: 1  
    middle: [2, 3, 4, 5]  
    last: 6  
