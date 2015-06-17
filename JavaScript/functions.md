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