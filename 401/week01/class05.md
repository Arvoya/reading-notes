# Big O Quiz

<!--toc:start-->
- [Big O Quiz](#big-o-quiz)
  - [1](#1)
  - [2](#2)
  - [3](#3)
  - [4](#4)
  - [Answers](#answers)
<!--toc:end-->

## 1

``` javascript
function findElement(arr, match) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === match) {
      return true;
    }
  }
  return false;
}
```

## 2

``` javascript
function isFirstElementNull(arr) {
  return arr[0] === null;
}
```

## 3

``` javascript
function printAllPairs(arrs){
  for (let i = 0; i < arrs.length; i++) {
    for (let j = 0; j < arrs.length; j++) {
      console.log(arrs[i], arrs[j]);
    }
  }
}
```

## 4

``` javascript
function binarySearch(arr, target){
  let left = 0;
  let right = arr.length - 1;
  while(left <= right){
    let mid = Math.floor((left + right) / 2);
    if (arr[mid] === target) return true;
    else if (arr[[mid] < target]) left = mid + 1;
    else right = mid - 1;
}
return false;
}
```

## Answers

1. O(n)
2. O(1)
3. O(n^2)
4. O(log n)
