# Section 2.1 - Binary Numbers

Data values can be stored in variables, lists of items, or standalone constants and can be passed as input to (or output from) procedures.

- We’ve been doing this since the beginning of the year.

Computing devices represent data digitally, meaning that the lowest-level components of any value are bits.

- Everything (numbers, strings, iterables, etc.) on a computer are bits when broken down enough.

Bit is shorthand for binary digit and is either 0 or 1.

- For every bit we add, we double the amount of potential information represented, just like adding a decimal place to one of our normal numbers multiplies the potential values by 10 (i.e. 10 vs. 100 vs. 1,000)

A byte is 8 bits.

- This is a standard size that allows us to store 256 (2^8) unique states (often simply put as the numbers from 0 to 255).

## Abstraction

Abstraction is the process of reducing complexity by focusing on the main idea. By hiding details irrelevant to the question at hand and bringing together related and useful details, abstraction reduces complexity and allows one to focus on the idea.

- When solving problems in Python, we don’t consider reading in the data to be part of the problem, we abstract the problem to be more centered on determining the solution than the minutiae of getting the data accessible.

Bits are grouped to represent abstractions. These abstractions include, but are not limited to, numbers, characters, and color.

- We have abstracted so much away from bits that most of the time when programming we don’t even have to think about them.

The same sequence of bits may represent different types of data in different contexts.

- Given the binary value 01010111. In the context of an integer, this would represent the number 87, but according to the American Standard Code for Information Interchange (ASCII), this would represent the capital letter “W”. Same bits, different information!


## Analog vs. Digital Data

Analog data have values that change smoothly, rather than in discrete intervals, over time.

- Some examples of analog data include pitch and volume of music, colors of a painting, or position of a sprinter during a race.

The use of digital data to approximate real-world analog data is an example of abstraction.

- It would be absurd to measure some weights to the accuracy of milligrams or further, so we accept that weighing to grams is an appropriate approximation for some contexts.

Analog data can be closely approximated digitally using a sampling technique, which means measuring values of the analog signal at regular intervals called samples. The samples are measured to figure out the exact bits required to store each sample.

- In the weight example above, our sampling is limited by how finely we can measure weight. If our scale can only measure to grams, it is less accurate than a scale that measures milligrams, but is more accurate than a scale that measures only to kilograms.


## Bit Storage Limitations

In many programming languages, integers are represented by a fixed number of bits, which limits the range of integer values and mathematical operations on those values. This limitation can result in overflow or other errors.

- This is the case in Java, an integer can hold 4 bytes or 32 bits of information, which limits it to values between -2,147,483,648 (-2^31) and 2,147,483,647 (2^31).

- The number of values a system can store is calculated by taking the base and raising it to the number of digits. For computers this means taking 2 and raising it to the power of the number of bits.

- In these cases, trying to store a value that is too large for the number of bits used would result in a form of overflow error, as there is just not enough bits to store the information.

Other programming languages provide an abstraction through which the size of representable integers is limited only by the size of the computer's memory; this is the case for the language defined in the exam reference sheet.

- This is the case in Python, which will keep allocating more memory for integers until the computer runs out of memory.

In programming languages, the fixed number of bits used to represent real numbers limits the range and mathematical operations on these values; this limitation can result in round-off and other errors. Some real numbers are represented as approximations in computer storage.

- This is true no matter the programming language. For example, if you try to save the value 0.1 in Java or Python, it will actually save as the value 0.100000001490116119384765625, which is very close, but very slightly off (by about a billionth), because we can’t possibly store every decimal value ever.


## Binary-Decimal Conversions

Number bases, including binary and decimal, are used to represent data.

- Binary (base 2) uses only combinations of the digits zero and one, while decimal (base 10) uses only combinations of the digits 0-9.

Both are place-value systems, meaning each position of a given bit/digit represents a certain magnitude/amount.

- In decimal we refer to these as the ones, tens, hundreds, etc. places. This is because they are based on the base raised to the power of the position, starting with 0 (10^0 is 1, 10^1 is 10, 10^2 is 100, etc.).

- This means in binary, it’s the same situation but with the powers of 2 (2^0 is 1, 2^1 is 2, 2^2 is 4, etc.)

To calculate the value of a number in any place-value system, you add up the results of multiplying each bit/digit by its place-value (typically going from right-to-left being smallest-to-largest).

- For example, given the binary number 1010, we can determine its decimal value by doing 0\*(2^0) + 1\*(2^1) + 0\*(2^2) + 1\*(2^3). This simplified to be 0\*1 + 1\*2 + 0\*4 + 1\*8 = 0 + 2 + 0 + 8 = 10.

We can also turn a decimal number into other bases by working backwards. This time, we start by determining the largest power of the given base we can take away from our value, subtract it, then repeat (this goes from left-to-right).

- For example, given the decimal number 28, we can determine its binary equivalent by first determining that the largest power of 2 we can remove from 27 is 16 = 2^4, making our binary number 1 _ _ _ _ (notice the 4 blanks for the powers 3, 2, 1, and 0) and leaving us with 27 - 16 = 11 to work with. Then we can remove 8 = 2^3, making our binary number 11 _ _ _ and leaving us with 11 - 8 = 3. We cannot remove 4 = 2^2, making our binary number 110 _ _ and leaving us still with 3. We can remove 2 = 2^1, making our binary number 1101 _ and leaving us with 3 - 2 = 1. Finally, we can remove 1 = 2^0, making our final binary number 11011 and confirmation that we've done our work correctly since 1 - 1 = 0, leaving us nothing left over.

## Additional Resources

Some useful resources on binary numbers include:

[Maths is Fun - Binary Numbers](https://www.mathsisfun.com/binary-number-system.html)

[Steve's Internet Guide - Binary Numbers](http://www.steves-internet-guide.com/binary-numbers-explained/)

[Khan Academy Computing - Binary Numbers](https://www.youtube.com/watch?v=sXxwr66Y79Y)

[The Organic Chemistry Tutor - ASCII Code and Binary](https://www.youtube.com/watch?v=H4l42nbYmrU)

---

## Work

For each of the following binary (base 2) numbers, convert them to their corresponding values in decimal (base 10):

110 = 

1011 = 

1110 = 

11011 = 

10101010 = 

11001100 = 

10010010 = 

For each of the following decimal (base 10) numbers, convert them to their corresponding values in binary (base 2):

5 = 

12 = 

15 = 

30 = 

75 = 

167 = 

209 = 