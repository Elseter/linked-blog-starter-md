
---
aliases: [ "20230219112716",  ]
tags: SEC.340, SEC, Homework
date_created: 2023-02-19 11:27
---
[[SEC.340 Index]]
# Homework - 1
---
## Homework 1 - Due 8am on Wednesday, Feb 22

### Question 1.)
1. The following cipher texts were encrypted by Rail Fence Transposition with 3 lines. Decipher them and recover the plaintext.
	1. TUEDCEEEINAENMNUHRTIORCTSGIDHAAREGOSVSRSIRNIUNTE
	2. SDTTHIOENEIHERNRMTNNECEFCES

>[! done] Answers for Question 1
>I somewhat struggled with this question, in part due to the expectation that it would output text that would make some form of logical sense. In the end, after running through it multiple times, I ended up checking my results against an online de-cyphering machine, which confirmed that I hadn't made any mistakes in the deciphering process. 
>
>PROCESS:
>I started by doing the second (and smaller) problem by hand to familiarize myself with the process. The result can be seen in the image below
>![[20230219_112619.jpg]]
>This resulted in the plaintext being: SEENDECITHEETRFNHRCMITENONS
>Which could possibly be: SEEN DECIT HEET RFNHRC MITEN ONS
>Or may be another cypher
>
> ADDITIONAL PROCESSES:
> I was curious to see if I could expedite the decryption process, and attempted to wrote some Command Line Java Code. I was successful, although at this time, I have it set to only de-crypt 3 line Rail Fence Transpositions. The code is as follows
> ```java
> public static String decryptRail(String encrypted, int key){  
>        int length = encrypted.length();  
>       char[][] array = new char[key][length];  
>  
>        for (int i = 0; i < key; i++)  
>            for (int k = 0; k < length; k++)  
>               array[i][k] = '-';  
>  
>        for (int i = 0; i < length; i++){  
>            if (i == 0 || i % (key+1) == 0){  
>                    array[0][i] = encrypted.charAt(0);  
>                    encrypted = encrypted.substring(1);  
>            }  
>        }  
>        for (int i =0; i < length; i++){  
>            if (i % 2 == 1){  
>                array[1][i] = encrypted.charAt(0);  
>                encrypted = encrypted.substring(1);  
>            }  
>        }  
>  
>        for (int i =0; i < length; i++){  
>            if ((i+2) % 4 == 0){  
>                array[2][i] = encrypted.charAt(0);  
>                encrypted = encrypted.substring(1);  
>  
>            }  
>        }  
>  
>        int direction = 1;  
>        int k = 0;  
>        int i = 0;  
>        StringBuilder output = new StringBuilder();  
>        while (k < length){  
>            output.append(array[i][k]);  
>            if (i == 2 || (i == 0 && k != 0))  
>                direction *= -1;  
>            i += direction;  
>            k += 1;  
>        }  
>        return output.toString();  
>    }  
>    public static void main(String[] args) {  
>
>        String input1 = "TUEDCEEEINAENMNUHRTIORCTSGIDHAAREGOSVSRSIRNIUNTE";  
>        String input2 = "SDTTHIOENEIHERNRMTNNECEFCES";  
>  
>        // done by hand then checked online due to confusion  
>        // was expecting a readable answer        String answer1 = "TNVMUNSUEHRRDTSICOIRECRTESNGEIIDIHUANANRAETGEOES";  
>        String answer2 = "SEENDECITHEETRFNHRCMITENONS";  
>  
>        System.out.println("Encrypted Message1: " + input1);  
>        System.out.println("Decrypted Message1: " + decryptRail(input1, 3));  
>        System.out.println(answer1.equalsIgnoreCase(decryptRail(input1, 3)));  
>        System.out.println();  
>  
>        System.out.println("Encrypted Message2: " + input2);  
>        System.out.println("Decrypted Message2: " + decryptRail(input2, 3));  
>        System.out.println(answer2.equalsIgnoreCase(decryptRail(input2, 3)));  
>    }  
>}
>```
- It creates a double array with 3 rows, indicating the 3 fences. Each row then has a length equal the length of the input string. The chars from the string are then placed into the array in the same way as it would be done visually by hand, then read from the array in a bouncing diagonal style pattern. It was much easier than I had initially expected. I'm willing to bet the code could be modified to give more control over the number of fences with relative ease.
- It results in the following output
![[Screenshot 2023-02-19 at 11.45.31 AM.png]]

### Question 2.)
1. The following cipher-texts were encrypted by Caesar’s shift cipher. Decipher them and recover the plain-texts. Please keep the spaces between words.
	1. HWDUYTLWFUMD NX YMJ FWY TK XJHWJY BWNYNSL (offset = 5)
	2. FRPSOHALWB LV WKH HQHPB RI HIIHFWLYHQHVV (offset = 3)

>[! done] Answers for Question 2
>I also the coded the solution for this problem using java. The Caesar Cypher shifts plain texts by a set value, offsetting each letter down the alphabet by the provided offset. In my code, I limited the potential characters to lowercase, ascii letters. This limits me to the ascii values 97-122. With java chars, I was able to add/subtract the offset directly from the char ascii values, make sure they were in the 97-122 range and then added them to a string builder before returning the final encrypted string. 

![[Screenshot 2023-02-19 at 11.54.43 AM.png]]
![[Screenshot 2023-02-19 at 11.55.24 AM.png]]
![[Screenshot 2023-02-19 at 11.55.53 AM.png]]
- This results in the cyphers being translated to 
	1. cryptography is the art of secret writing
	2. complexity is the enemy of effectiveness