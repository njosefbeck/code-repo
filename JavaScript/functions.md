# JavaScript : Functions
Below you will find examples of functions.

### Example 1
* **Language:** ECMAScript 5 (JavaScript)
* **TOPICS:** Functions, Regular Expressions
* **SOURCE:** Code Wars
* **URL:** [http://www.codewars.com](http://www.codewars.com)

**Code:**
```javascript
function isPalindrome(word) {
    word = word.replace(/[^a-z]/gi, '').toLowerCase();
    return word.split('').reverse().join('') === word;
}
```
**Explanation:**

This function determines if a given string is a palindrome or not, returning true if it is or false if it's not. For example, 'abba' would return true and 'pancake' would return false. 

Using the replace() method, the function accepts a string via 'word' argument and (1) using a Regular Expression, replaces any character NOT found in a-z (ignoring case through use of the /i flag) with '' (which effectively removes the character from the string). (2) Afterwards, converts the string to lowercase.

Then, splits the string into an array of strings, reverses the array, and then joins the array back together into a string. Afterwards, tests to see if this new string is equal to the original 'word' string argument.


### Example 2
* **Language:** ECMAScript 5 (JavaScript)
* **TOPICS:** Functions, For Loops
* **SOURCE:** Code Wars
* **URL:** [http://www.codewars.com](http://www.codewars.com)

**Code:**
```javascript
function squares(x,n) {
    var results = [];
    results.push(x);
    for (var i = 1; i < n; i++) {
        x *= x;
        results.push(x);
    }
    return results;
}
```
**Explanation:**

This function starts with a number x and returns an array of length n with the squares of the previous number. Example:
squares(2,5) = [2,4,16,256,65536]

First we store an empty array in the results variable. Second, using the push method we push the initial x argument onto the end of the array. Third, we intialize a for loop to build the rest of the array. We start the loop at index of 1 (since 0 is where x is already located) with var i = 1. The for loop will run as long as i is less than n (i < n), and each run of the loop will increment i by 1 (i++). 

For each loop iteration, x will be multiplied by itself and given the value of this multiplication (x *= x is the same as x = x * x). Then, this new value of x will be pushed to the end of the results array. 

Once the loop is finished running, we return the newly built array (return results).


### Example 3
* **Language:** ECMAScript 5 (JavaScript)
* **TOPICS:** Functions, For Loops, If-Then Statements
* **SOURCE:** Code Wars
* **URL:** [http://www.codewars.com](http://www.codewars.com)

**Code:**
```javascript
function letterChange(str) {
    str = str.split('');
    for (var i = 0; i < str.length; i++) {
        if(str[i] == 'Z') {
            str[i] = 'A';
        }
        else if(str[i] == 'z') {
            str[i] = 'a';
        }
        else if(str[i] == ' ') {
            str[i] = ' ';
        }
        else {
            str[i] = String.fromCharCode(str[i].charCodeAt() + 1);
        }
    }
    return str.join('');
}
```
**Explanation:**
The spec for this exercise is as follows: You will be given a string. Your task is to replace every character with the letter following it in the alphabet (for example, "b" should be "c", "z" should be "a" and capital "Z" should be "A").

The test cases would not have any special symbols or numbers but it will have spaces. And the upper and lower cases should be retained in your output.

So, split the string into an array of letters, so 'cat' = [c, a, t] using str.split(''). 

Loop through the entire array, starting at index 0 (var i = 0), iterating through the array until the end (i < str.length), and incrementing i by one each time (i++). 

The loop uses a number of if/else if/else statements to replace the characters in the original string. If the character at the index i of the str array is equal to Z or z, it gets replaced with either A or a. Else if the character is a space, it remains a space. 

And for all other cases, denoted by else {}, make the array item into a string by first getting the charCode for the letter at [i] and adding 1; so for example the character c = 63, and 63+1 = 64, which is the unicode for 'd'. Thus, when the String is created using .fromCharCode(64), you get 'd'.

Then, once the loop is done doing its thing, join the newly created string into str variable that is then returned.
