# JavaScript : For Loops
Below you will find examples of JavaScript using For Loops.

### Example 1
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

