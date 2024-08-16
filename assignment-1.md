
1) Write a simple algorithm for finding the maximum of three numbers using pseudo code.
 
Algorithm FindMaximumOfThree
start
Input: num1, num2, num3
Output: max

max = num1
If num2 > max Then
   max = num2
End If
If num3 > max Then
   max = num3
End If
Return max
stop

2) Compare and contrast two different programming languages, highlighting their strengths and weaknesses.

Java
----
Strengths:
Performance: Java is generally faster than Python due to its compiled nature.

Static Typing: Java uses static typing, which helps catch errors at compile-time

Robustness: Java has strong memory management and exception handling features.

Cross-Platform: Java's "write once, run anywhere" philosophy allows Java applications to run on any device with a JVM.

Weaknesses:

Verbosity: Java code tends to be more verbose compared to Python, leading to longer and more complex code.

Slower Development: Due to its verbosity and stricter syntax, development in Java can be slower and require more boilerplate code.

Memory Consumption: Java applications can consume more memory due to the JVM overhead.

Python
------
Strengths:
Readability and Simplicity: Python's syntax is designed to be readable and straightforward.

Dynamic Typing: Python uses dynamic typing.

Extensive Libraries: Python has a rich standard library and many third-party libraries.

Interpreted Language: Python's interpreted nature makes it suitable for scripting and automating tasks.

Weaknesses:

Performance: Python is generally slower than Java due to its interpreted nature and dynamic typing.

Dynamic Typing: While dynamic typing allows for flexibility, it can also lead to runtime errors .

 
3. Explain the compilation process and how it differs from interpretation.

**Compilation** is like translating a whole book from one language to another all at once, so it can be read and understood by someone who only knows the target language.

Here's how it works step by step:

1. **Preprocessing**: Clean up and prepare the text (like removing comments or including other files).
2. **Lexical Analysis**: Break down the text into small pieces (words and symbols).
3. **Syntax Analysis**: Check the structure of the sentences to make sure they follow the grammar rules of the language.
4. **Semantic Analysis**: Ensure that the sentences make sense (e.g., variables are defined before use).
5. **Optimization**: Make the text better and more efficient (like shortening sentences without losing meaning).
6. **Code Generation**: Translate the cleaned, checked, and optimized text into a different language (machine code).
7. **Linking**: Combine different translated parts into one complete book (an executable program).

### Interpretation Process

**Interpretation** is like translating a book one sentence at a time, on the fly, as someone is reading it, so they understand it immediately.

Here's how it works step by step:

1. **Lexical Analysis**: Break down the current sentence into small pieces (words and symbols).
2. **Syntax Analysis**: Check the structure of the sentence to make sure it follows the grammar rules.
3. **Semantic Analysis**: Ensure the sentence makes sense.
4. **Execution**: Directly do what the sentence says, right away.

### Key Differences

- **Compilation**: The entire book is translated before reading it. This makes reading (execution) faster but requires time to translate first.
- **Interpretation**: Each sentence is translated and understood on the spot while reading. This makes it easier to start reading but can be slower overall.


4. Create a flowchart for a program that calculates the factorial of a given number.
 
5. Write a function in your preferred programming language to calculate the area of a rectangle.
 
def calculate_rectangle_area(width, height):
    area = width * height
    return area

width = 7.5
height = 12.0
area = calculate_rectangle_area(width, height)
print("The area of the rectangle is:", area)



