# Solution - Reverse a string

### Basic solution - Step by step
```javascript
function reverseString(str) {
  var strSplited = str.split('');
  var arrayReverse = strSplited.reverse();
  var stringReverse = arrayReverse.join('');
  
  return stringReverse;
}

reverseString('javascript');
```

### Small solution
```javascript
function reverseString(str) {
  return str.split('').reverse('').join('');
}

reverseString('javascript');
```

### Code explanation
- Our objective is to take the string and return it in reverse.
- The first step is split the string so we can transform it into array. For this, we use the `split()` function.
- In next, we reverse the array using the `reverse` function.
- At last, we use the `join()` function for join all chars and create our reverse string.