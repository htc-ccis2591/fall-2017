---
title: Tips for Caesar Cipher
summary: "If you are having trouble getting started, the following tips may help you out. "
---

# {{ page.title }}
{{ page.summary }}

## Don't start with Google
There are many ways to implement the Caesar Cipher and you'll find several options and videos on the internet.  However using those doesn't help you to learn anything.  If you rely on having someone else solve the problem for you, it's not going to be easy to pass tests in this class. It also won't be easy to find a job.  

You __MUST__ use the method described in the assignment instructions to solve this problem.  That almost certainly means you will need to use arrays. You __CANNOT__ use numeric ASCII values of characters to encrypt/decrypt as is shown in numerous example solutions.

You __MUST__ make a separate ciphertext alphabet based on the key value.


## Check your understanding
Before you can even get started writing the code, you need to make sure you understand the problem and how you *as a person* can solve it without needing any code.

If you have the message "Hello World!" and you want to encrypt it to send to me, we first need to decide on a key.  Let's say our key is 5.

To encrypt, we need to shift our letters to the right by 5.  

{% assign q1-text = "What do you think is the correct ciphertext alphabet?" %}
{% assign q1-choices = "ABCDEFGHIJKLMNOPQRSTUVWXYZ | KLMNOPQRSTUVWXYZABCDEFGHIJ | VWXYZABCDEFGHIJKLMNOPQRSTU | XYZABCDEFGHIJKLMNOPQRSTUVW" | split: '|' %}
{% assign q1_feedbacks = "That is the plaintext alphabet, simply A-Z. If we use this to encrypt, our message will not change. The encrypted and decrypted message would be identical. | This is an incorrect ciphertext alphabet as it shifts the letters more than 5 positions to the right; it shifts them 16. | Correct! We have shifted the first letter in the alphabet 5 positions to the right.  | This is an incorrect ciphertext alphabet as it only shifts the letters 3 positions to the right instead of 5." | split: '|' %}
{% include mc-quiz.html header="Question 1" answer=2 text=q1-text choices=q1-choices feedback=q1_feedbacks %}

Now that we have a key and a ciphertext alphabet we can encrypt the message. Remember that we decided our message is "Hello World!".

{% assign q2-text = "What is the first letter of the encrypted message?" %}
{% assign q2-choices = "H | C | R | A" | split: '|' %}
{% assign q2_feedbacks = "That's the first letter of of the message in plaintext, but it hasn't been encrypted yet.  | Correct! H is in position 8 ( or 7 if we start at 0 like an array index) of the plaintext alphabet, and the letter in the same position of the ciphertext alphabet is C. | That is incorrect.  H is in position 8 ( or 7 if we start at 0 like an array index) of the plaintext alphabet. What letter is in the same position of the ciphertext alphabet? | That is incorrect.  H is in position 8 ( or 7 if we start at 0 like an array index) of the plaintext alphabet. What letter is in the same position of the ciphertext alphabet?" | split: '|' %}
{% include mc-quiz.html header="Question 2" answer=1 text=q2-text choices=q2-choices feedback=q2_feedbacks %}

Continue encrypting the message yourself.  

{% assign q3-text = "Is `Czggj rjmgy!` the correct result?" %}
{% assign q3-choices = "Yes | No" | split: '|' %}
{% assign q3_feedbacks = "The letters are mostly encrypted correctly, but the first letter of the second word should be capitalized.  Also, any non-letters should be removed.  | Correct! This is not the correct encrypted result as the capitalization is incorrect and the ! should be removed." | split: '|' %}
{% include mc-quiz.html header="Question 3" answer=1 text=q3-text choices=q3-choices feedback=q3_feedbacks %}

The encrypted message can now be sent to the recipient, but they *must* know the key to decrypt (un-encrypt) the message.  When they decrypt the message, they go through the same process, but in reverse.  They must find the letters in the ciphertext alphabet and then match those to the correct letter in the plaintext alphabet.

{% assign q4-text = "In what position of the ciphertext alphabet do we find the letter r, if we assume the first letter is in position 1?" %}
{% assign q4-choices = "8 | 14 | 18 | 22" | split: '|' %}
{% assign q4_feedbacks = "Sorry, that's not correct.  The correct ciphertext alphabet was shown above. Count off each letter from the beginning starting at 1 until you reach the letter r.  | Sorry, that's not correct.  The correct ciphertext alphabet was shown above. Count off each letter from the beginning starting at 1 until you reach the letter r. | Sorry, that's not correct. That is the position of r in the plaintext alphabet. Use the ciphertext alphabet. | Correct! The letter r is in position 22 of the ciphertext alphabet. " | split: '|' %}
{% include mc-quiz.html header="Question 4" answer=3 text=q4-text choices=q4-choices feedback=q4_feedbacks %}

{% assign q5-text = "What letter does r decrypt to?" %}
{% assign q5-choices = "r | o | w | d" | split: '|' %}
{% assign q5_feedbacks = "Sorry, that's not correct.  Letter r was in position 22 of the ciphertext alphabet.  What letter is in the same position of the plaintext alphabet?  | Sorry, that's not correct.  Letter r was in position 22 of the ciphertext alphabet.  What letter is in the same position of the plaintext alphabet? | Correct! The letter r is in position 22 of the ciphertext alphabet, and the corresponding letter in the plaintext alphabet is w. | Sorry, that's not correct.  Letter r was in position 22 of the ciphertext alphabet.  What letter is in the same position of the plaintext alphabet? " | split: '|' %}
{% include mc-quiz.html header="Question 5" answer=2 text=q5-text choices=q5-choices feedback=q5_feedbacks %}

If you are still not sure of how to encrypt or decrypt a message yourself, ask a fellow student, the instructor, a student instructor, or tutor for assistance.

## HTML & DOM Code
### Deal with the user input
Set up the HTML form and write the JavaScript to get the values from the input fields when the buttons are clicked.  You will need two input fields in your HTML, a numeric value for the key and a potentially long string message.  I would suggest an HTML5 number input for the key, and a text area for the message.  Put id attributes on them to make them easy to access in your JavaScript.

You will also need 3 buttons: encrypt, decrypt, and reset.  Each will need their own click even handler function to do the appropriate action.

This can either be done first or last, however it is completely separate from the code needed to actually do the encryption & decryption. It should be relatively easy to do based of the lecture and sample code from module 2. Even if you get no encryption or decryption working, you should be able to do this with minimal effort.


### Deal with the output
Setup the HTML to have an area for your output message.  You have a few options for how you might handle this, for example in class we used a `div`. Here you might also use a text area.

Whatever you choose, you should make sure you can write to it, and if the encrypt or decrypt is clicked multiple times, make sure only the most recent output shows to avoid any confusion.  

Again, this can be done either before or after the encrypt/decrypt code. To do it first, just use dummy text or just echo back the input message. By doing this much, even if you cannot get the Caesar Cipher working, you are showing that you can at least solve this part of the problem.


## Break down the problem
If you don't break this assignment down into smaller pieces it is much more difficult to complete.  There are many options for doing this.  I will suggest *a few* possible ideas here to get you started.

Think about breaking the encryption and decryption into common functions:

- Create a function to generate the ciphertext alphabet from the key.  The function would take the key as an input parameter, then return back an array containing the ciphertext alphabet.

- Create a function to find a letter in an array and find its position. The function would take 2 input parameters, the letter & the array, and then return back the index position of the letter in the array.

- Create a function to determine if a letter is uppercase or capitalized. The function can take 1 input parameter, the letter, and return back true or false.

- Build on the two functions above to create a function to encrypt/decrypt a *letter* (with the proper case). This might take as input the letter, the plaintext alphabet, & the ciphertext alphabet, and return back the encrypted or decrypted letter.

- Build on the above to encrypt/decrypt a *word* by looping through each letter and calling the above function.  

{% include alert.html type="tip"
    content="Why do you think that having the plaintext and ciphertext alphabets both as parameters (even though the plaintext alphabet is always the same A-Z) might be handy?  What is the only difference between encrypting and decrypting?"
%}

These tips should give you some ideas on where to begin and how to break the problem down into smaller pieces.  This not only makes the problem itself easier to solve, but it also makes it easier to discuss the problem with other to get advice or help.  It is also easier to write and troubleshoot the code if you write and test small pieces separately.





## Checking for uppercase
To get this code working correctly, you'll want to know if a letter is uppercase or lowercase. We learned that a string has a `toUpperCase()` method. We can obviously use this to change a letter (or String) to upperCase, but we can also use it to determine if the letter was upper case or not to begin with.

{% highlight JavaScript %}
let letter = "a";
if (letter === letter.toUpperCase()) {
  console.log("That was an upper case letter!");
} else {
  console.log("That was not an upper case letter!");
}
{% endhighlight %}

If the letter in our original message was upper case, we need the encrypted/decrypted letter to also be uppercase.  Likewise if it was not, then we need the encrypted/decrypted letter to be lowercase.  If your plaintext alphabet only contains uppercase letters, as shown in the examples, you will need to make sure you are using toUpperCase before looking for the letter in the array or you will not find a match.  The letter 'r' is not the same as the letter 'R'.  

Then when putting together the encrypted/decrypted message, you will need to convert the letters to the proper case before including them in the output message as well.  
