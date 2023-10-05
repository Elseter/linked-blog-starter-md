
---
aliases: [ "20230228115517",  ]
tags: SEC.340, SEC
date_created: 2023-02-28 11:55
---
[[SEC.340 Index]]
# Homework 2 - Riley King
---
## Frequency Analysis Homework
### Assignment
The same plaintext message was enciphered using four different cipher techniques. A
frequency analysis of each of the four resulting ciphertexts was conducted and the results
graphed (see following pages). Match each frequency analysis with the cipher technique that
produced it. Justify your answers.

a. Transposition cipher
>[! done] Transposition Cipher Frequency
>My thought process with this assignment is to work from easiest to most difficult, disregarding the order of in which the questions are presented and using the process of elimination to narrow down the more difficult analyses. Luckily for me, the first question is also the easiest (which would be a remarkably foolish thing for me to say and then proceed to answer it incorrectly. Lets hope that isn't the case :) )
>
>The transposition cipher is a method of encryption that treats the plaintext like an anagram. The same letters are present, but their location is shifted. This results in the length of the message factorial being the number of options. Additionally, it makes basic frequency analysis nigh impossible as the frequency at which the letters appear should be almost exactly the same as traditional English's (with some leeway given as shorter messages won't always return the exact same frequencies).
>
>The Transposition cipher is likely Frequency Analysis 2
>![[FA.jpg]]

b. Shift cipher +6 (the one that replaces “a” with “G”)
>[! done] Shift cipher +6 Frequency
>The Shift cipher +6 replaces each letter of English plaintext with the letter 6 places down from in the alphabet. In regards to frequency analysis, this should result in the frequency graph also undergoing this shift. The frequency that traditionally belongs to a would now belong to g. The frequency that belongs to e (easy to spot) would now belong to k. 
>
>I suspect that the Shift cipher +6 is likely Frequency Analysis 1
>![[FA1.jpg]]


c. Vigenère cipher
>[! done] Vigenère cipher Frequency
>This is likely the most tricky of the ciphers provided as it relies on a series of Caesar ciphers to encrypt the message, where the cipher used is dependent on an unknown key. However, this complexity, in this assignment, is also its weakness. It is the only cipher provided that will not contain the same frequencies as the traditional plaintext English alphabet. While the other ciphers may shuffle the alphabet about, the same frequencies must remain present. That is not the case for the Vigenère cipher.
>
>That, paired with the process of elimination makes it likely that the Vigenère cipher is Frequency Analysis 3
>![[FA3.jpg]]

d. Shift cipher -10 (the one that replaces “a” with “Q”)
>[! done] Shift cipher -10 Frequency
>In a similar case to the previous shift cipher, the frequencies are still present, but shifted back along the alphabet 10 letters. The most common letter, e, has now become u. o has become e and so on. 
>
>I suspect that the Shift cipher -10 is Frequency Analysis 4
>![[FA4.jpg]]
