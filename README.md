# Portal-zst

https://youtu.be/Ne82lgXQPFY

Speed: Area 100B-10KB/s

Instruction:
1. Need python 
2. install pip: pip install zstandard
3.

ul; cl; .bin

c2; u2 .bin.bin

Jurijus Pacalovas written program.

4.34 v. zst

0%-99.9949% c.

Cryptography

zst

Lossless data compression

I use Brotli.

LZ77 algorithms achieve compression by replacing repeated occurrences of data with references to a single copy of that data existing earlier in the uncompressed data stream. A match is encoded by a pair of numbers called a length-distance pair, which is equivalent to the statement "each of the next length characters is equal to the characters exactly distance characters behind it in the uncompressed stream". (The distance is sometimes called the offset instead.)

Asymmetric numeral systems

To spot matches, the encoder must keep track of some amount of the most recent data, such as the last 2 kB, 4 kB, or 32 kB. The structure in which this data is held is called a sliding window, which is why LZ77 is sometimes called sliding-window compression. The encoder needs to keep this data to look for matches, and the decoder needs to keep this data to interpret the matches the encoder refers to. The larger the sliding window is, the longer back the encoder may search for creating references.

It is not only acceptable but frequently useful to allow length-distance pairs to specify a length that actually exceeds the distance. As a copy command, this is puzzling: "Go back four characters and copy ten characters from that position into the current position". How can ten characters be copied over when only four of them are actually in the buffer? Tackling one byte at a time, there is no problem serving this request, because as a byte is copied over, it may be fed again as input to the copy command. When the copy-from position makes it to the initial destination position, it is consequently fed data that was pasted from the beginning of the copy-from position. The operation is thus equivalent to the statement "copy the data you were given and repetitively paste it until it fits". As this type of pair repeats a single copy of data multiple times, it can be used to incorporate a flexible and easy form of run-length encoding.

Another way to see things is as follows: While encoding, for the search pointer to continue finding matched pairs past the end of the search window, all characters from the first match at offset D and forward to the end of the search window must have matched input, and these are the (previously seen) characters that comprise a single run unit of length LR, which must equal D. Then as the search pointer proceeds past the search window and forward, as far as the run pattern repeats in the input, the search and input pointers will be in sync and match characters until the run pattern is interrupted. Then L characters have been matched in total, L > D, and the code is [D, L, c].

Upon decoding [D, L, c], again, D = LR. When the first LR characters are read to the output, this corresponds to a single run unit appended to the output buffer. At this point, the read pointer could be thought of as only needing to return int(L/LR) + (1 if L mod LR ≠ 0) times to the start of that single buffered run unit, read LR characters (or maybe fewer on the last return), and repeat until a total of L characters are read. But mirroring the encoding process, since the pattern is repetitive, the read pointer need only trail in sync with the write pointer by a fixed distance equal to the run length LR until L characters have been copied to output in total.

Considering the above, especially if the compression of data runs is expected to predominate, the window search should begin at the end of the window and proceed backwards, since run patterns, if they exist, will be found first and allow the search to terminate, absolutely if the current maximal matching sequence length is met, or judiciously, if a sufficient length is met, and finally for the simple possibility that the data is more recent and may correlate better with the next input.

LZ77 algorithms achieve compression by replacing repeated occurrences of data with references to a single copy of that data existing earlier in the uncompressed data stream. A match is encoded by a pair of numbers called a length-distance pair, which is equivalent to the statement "each of the next length characters is equal to the characters exactly distance characters behind it in the uncompressed stream". (The distance is sometimes called the offset instead.)

To spot matches, the encoder must keep track of some amount of the most recent data, such as the last 2 kB, 4 kB, or 32 kB. The structure in which this data is held is called a sliding window, which is why LZ77 is sometimes called sliding-window compression. The encoder needs to keep this data to look for matches, and the decoder needs to keep this data to interpret the matches the encoder refers to. The larger the sliding window is, the longer back the encoder may search for creating references.

It is not only acceptable but frequently useful to allow length-distance pairs to specify a length that actually exceeds the distance. As a copy command, this is puzzling: "Go back four characters and copy ten characters from that position into the current position". How can ten characters be copied over when only four of them are actually in the buffer? Tackling one byte at a time, there is no problem serving this request, because as a byte is copied over, it may be fed again as input to the copy command. When the copy-from position makes it to the initial destination position, it is consequently fed data that was pasted from the beginning of the copy-from position. The operation is thus equivalent to the statement "copy the data you were given and repetitively paste it until it fits". As this type of pair repeats a single copy of data multiple times, it can be used to incorporate a flexible and easy form of run-length encoding.

This way let to see things is as follows: While encoding, for the search pointer to continue finding matched pairs past the end of the search window, all characters from the first match at offset D and forward to the end of the search window must have matched input, and these are the (previously seen) characters that comprise a single run unit of length LR, which must equal D. Then as the search pointer proceeds past the search window and forward, as far as the run pattern repeats in the input, the search and input pointers will be in sync and match characters until the run pattern is interrupted. Then L characters have been matched in total, L > D, and the code is [D, L, c].

Upon decoding [D, L, c], again, D = LR. When the first LR characters are read to the output, this corresponds to a single run unit appended to the output buffer. At this point, the read pointer could be thought of as only needing to return int(L/LR) + (1 if L mod LR ≠ 0) times to the start of that single buffered run unit, read LR characters (or maybe fewer on the last return), and repeat until a total of L characters are read. But mirroring the encoding process, since the pattern is repetitive, the read pointer need only trail in sync with the write pointer by a fixed distance equal to the run length LR until L characters have been copied to output in total.

Considering the above, especially if the compression of data runs is expected to predominate, the window search should begin at the end of the window and proceed backwards, since run patterns, if they exist, will be found first and allow the search to terminate, absolutely if the current maximal matching sequence length is met, or judiciously, if a sufficient length is met, and finally for the simple possibility that the data is more recent and may correlate better with the next input.

In computer science and information theory, a Huffman code is a particular type of optimal prefix  that is commonly used for lossless data compression. The process of finding or using such a code proceeds by means of Huffman coding, an algorithm developed by David A. Huffman while he was a Sc.D. student at MIT, and published in the 1952 paper "A Method for the Construction of Minimum-Redundancy Codes".

Brotli is a data format specification[2] for data streams compressed with a specific combination of the general-purpose LZ77 lossless compression algorithm, Huffman coding and 2nd order context modelling. Brotli is a compression algorithm developed by Google and works best for text compression. Brotli is primarily used by web servers and content delivery networks to compress HTTP content, making internet websites load faster. A successor to gzip, it is supported by all major web browsers and is becoming increasingly popular, as it provides better compression than gzip

Compression ee-ther.
