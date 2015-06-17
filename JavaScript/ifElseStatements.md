# JavaScript : If-Else Statements
Below you will find examples of JavaScript using If-Else Statements.


### Example 1
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

Then, once the loop is done doing its thing, join the newly created array into a string stored in the str variable that is then returned.