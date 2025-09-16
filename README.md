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
V1.0 ([09-14-2025]) – Initial Coding for PA1  

V1.1 ([09-15-2025]) - Creation of Repository Along with Read Me file  

V1.2 ([09-16-2025]) – Finalization of Coding PA1 and Edited Documentation, Code Formatting, and Design in the README File  

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
    # Input of word
    x = input("Enter a string:")

    # Sorting word alphabetically
    x_sorted = sorted(x)

    # Output of sorted word
    alpha_sorted = "".join(x_sorted)

    print(alphabet("noah"))

# Output (example)
    ahno
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
