# Section 2.2 - Data Compression

Data compression can reduce the size (number of bits) of transmitted or stored data.

Fewer bits can, but does not necessarily, mean less information.

- Different organizational systems can do different things with the same amount of information, resulting in sometimes being more or less efficient with your information.

The amount of size reduction from compression depends on both the amount of redundancy in the original data representation and the compression algorithm applied.

- Some data naturally has redundancy built as certain values may be guaranteed based on certain criteria, but are saved anyways. Data compression algorithms will try to get rid of these unnecessary values.

## Lossless vs. Lossy Compression

Lossless data compression algorithms can usually reduce the number of bits stored or transmitted while guaranteeing complete reconstruction of the original data.

- This means they really only remove redundant pieces of information, and therefore have to make no guesses when putting everything back together.

Lossy data compression algorithms can significantly reduce the number of bits stored or transmitted but only allow reconstruction of an approximation of the original data.

- They remove more than just redundant pieces of information, and have to make some guesses when putting everything back together.

Lossy data compression algorithms can usually reduce the number of bits stored or transmitted more than lossless compression algorithms.

- Lossy algorithms generally remove more than just redundancy and therefore have more they can remove. Sometimes lossless algorithms can be really clever though!

In situations where quality or ability to reconstruct the original is maximally important, lossless compression algorithms are typically chosen. In situations where minimizing data size or transmission time is maximally important, lossy compression algorithms are typically chosen.

---

## Work

Texting is a great example of simpler data compression, as we often shorten messages without removing much, if any, key meaning from them. Take a look at the sample text messages below and determine if you think they are compressed via lossless or lossy compression and why:

"wait for me" -> "w8 4 me" -

"how are you doing?" -> "whats up" -

"on my way" -> "omw" -

"see you later" -> "l8r" -

Choose three of the following sources (two beginner and one advanced) to learn from about data compression. After going through each source, write 3 sentences about what you thought was interesting about it.

Sample Response:

[Crash Course Computer Science - Data Compression](https://www.youtube.com/watch?v=OtDxDvCpPL4) - I thought it was interesting how you combine three primary colors in proportions to create other colors. The fact that you don't need to save every single pixel's color to recreate an image with a lot of accuracy seems counterintuitive. Comparing frames of videos seems like an intuitive way to determine what information is redundant in a video.

Beginner:

[Crash Course Computer Science - Data Compression](https://www.youtube.com/watch?v=OtDxDvCpPL4) -

[Techlinked - Data Compression as Fast as Possible](https://www.youtube.com/watch?v=guo8if4Yxhw) -

[2BrightSparks - The Basic Principle of Data Compression](https://www.2brightsparks.com/resources/articles/data-compression.html) -

Advanced:

[Computerphile - LZ 77 Text Compression](https://www.youtube.com/watch?v=goOa3DGezUA) -

[3Blue1Brown - Hamming Codes](https://www.youtube.com/watch?v=X8jsijhllIA) -

[Lelewer and Hirschberg - Fundamental Concepts of Data Compression](https://www.ics.uci.edu/~dan/pubs/DC-Sec1.html#Sec_1) -

[Bertolami - Mathematical Fundamentals of Data Compression](https://bertolami.com/index.php?content=posts&detail=fundamentals-of-data-compression&engine=blog) -
