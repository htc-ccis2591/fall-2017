---
title: Caesar Cipher
summary: "In this exercise we will create a web page to encrypt and decrypt text using the Caesar Cipher. "
---

# {{ page.title }}
{{ page.summary }}

> Note that while there are many ways to implement the Caesar Cipher, you __MUST__ use the method described below for this assignment.

## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [JavaScript Objects]({{ "/readings/js-objects.html" | prepend:site.baseurl }})  
- [JavaScript Document Object]({{ "/readings/js-dom.html" | prepend:site.baseurl }})
- [JavaScript Events]({{ "/readings/js-events.html" | prepend:site.baseurl }})

## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: caesar-cipher]( https://classroom.github.com/a/nQsFaIkh )

Note that once you accept this assignment, you will continue working with the same repository on GitHub for later parts of the assignment and will not need to accept the assignment again.


## Encrypting and Decrypting Text Using a Ciphertext Alphabet
For the purposes of this assignment, we will call unencrypted text “plaintext”, and we will call encrypted text “ciphertext”.

The encryption scheme for this assignment is a simple substitution cipher. The scheme works by replacing each character in the plaintext with the corresponding character in a “ciphertext alphabet”, which is always the same length as the plaintext alphabet.  

For example:  
plaintext alphabet:  ABCDEFGHIJKLMNOPQRSTUVWXYZ  
ciphertext alphabet: KLMNOPQRSTUVWXYZABCDEFGHIJ  

Given the ciphertext alphabet, if we encrypted the string “writing code is cool” it would become “gbsdsxq myno sc myyv”. This is because we replace “w” with “g”, “r” with “b” and so forth. Decryption works exactly the same way, but in reverse. Thus, “myyv” using the above alphabets becomes “cool”.

## Generating a Ciphertext Alphabet from a Key
In your program, rather than having the user specify a ciphertext alphabet directly, you will instead have the user enter a key that will be used to generate the ciphertext alphabet. We will start by setting our ciphertext alphabet equal to the plaintext alphabet. Then, we will move each character to the right by the number of letters specified by the key.  When we get to the end, the letters wrap around.

So for example, if our key is 3, we will start with:  
ciphertext alphabet:  ABCDEFGHIJKLMNOPQRSTUVWXYZ  

Then move each letter to the right 3 positions:  
ciphertext alphabet:  XYZABCDEFGHIJKLMNOPQRSTUVW  

Note that the A is shifted to the right 3 letters, and the last 3 letters of the alphabet (XYZ) have moved to the beginning.

## Program Requirements

### Encrypt & Decrypt Rules
To encrypt or decrypt the text entered by the user, you should use the following rules for each character:

- If it is a letter, replace as described above with a letter of the same case (uppercase or lowercase).
- If it is a space, keep the space.
- If it is anything else, skip it.  It should not appear in the output.

So for example, if we had the alphabets below (key is 16):  
plaintext alphabet:  ABCDEFGHIJKLMNOPQRSTUVWXYZ  
ciphertext alphabet: KLMNOPQRSTUVWXYZABCDEFGHIJ  

And they entered “Writing code is,!;~;;?5555 Cool”, we’d get “Gbsdsxq myno sc Myyv” as output, because we are preserving spaces, but removing any other characters not found in the alphabet.

### HTML Page
Create an HTML page with a simple form to accept input of a key (numeric 1-25) and a text message (of any length). There should be 3 buttons: Encrypt, Decrypt, & Reset. Also add some basic *instruction* text to the page so that anyone browsing to this page will know what it is for and how it works.

Below the form, add a spot for the output. You can use a `div` or another element you feel makes sense, such as a read only text area.

It will be helpful to add id attributes onto the div, buttons, and input controls to easily identify and access them from JavaScript.

### Basic CSS
Use CSS to make the form display nicely. If you want, you can use Bootstrap or another library to help with your display. If not, you will need to write some basic CSS yourself.

### JS Code
Remember to write good ES6 JavaScript code using best practices discussed in class and in the readings. I will expect you to create and use functions with input parameters and return values to structure your code. This problem is *very* complex if you do not break it down into small functions to handle the individual tasks.

#### Get the input values
First, we need to set-up our buttons to get the value of the input controls so that we can use them in the encryption/decryption code. Set up a click handler for each button that will get each of the form fields and log the value to the console.

Tip: Use the String trim() method to remove any whitespace from the beginning & ending of your input values.

#### Form reset
Setup another click handler to clear out the values on the input fields. You can set the value of the controls in much the same way you get the value, just put the expression on the left side of the equal sign.

For example:
`myElement.value = ""`

Note: If you use a form input type of "reset" you do not need to write code to do this. However for this assignment, I want to see that you are able to set the input field values through your JS code.


#### Encrypt & decrypt
Once you are getting your form data, you can work on the code to encrypt or decrypt the message.  To do the encryption or decryption, you will need to use arrays to create the "plaintext" and "ciphertext" alphabets as discussed above.  

I recommend that you begin by creating an array variable for the "plaintext" alphabet, as this should never change. (Be very careful setting this up, as missing a letter or swapping letters will cause incorrect translations!) Then write a function to generate the "ciphertext" alphabet by shifting the letters by the amount specified by the key.

Once you have the plaintext alphabet and the correct ciphertext alphabets, you can start going through the user's message character by character. Find the location of the letter in the plaintext alphabet array, then use the array index to get the appropriate letter from the ciphertext alphabet.


## Helpful Tips
If you need help getting started, try the helpful tips & hints found here: [Tips for Caesar Cipher]({{ "/experiences/caesar-cipher-tips.html" | prepend: site.baseurl }}).
