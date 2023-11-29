### Even - Odd

Even odd test assignment in one of the IT companies

## Task:

Function to analyze given array and place all odd numbers in ascending order while odd numbers shall remain in place

## Example:

```js
odd([2, 3, 1, 4, 7, 6, 8, 5, 9]); // [2,1,3,4,5,6,8,7,9]
odd(""); // []
```

### Solution:

```ts
function odd(data: array): array {
  const result = data;

  const sortedOddList = data
    .filter((element) => element % 2)
    .sort((a, b) => b - a);

  for (let i = 0; i < result.length; i++) {
    if (result[i] % 2 > 0) {
      result[i] = sortedOddList.pop();
    }
  }

  return result;
}

console.log(odd([2, 3, 1, 4, 7, 6, 8, 5, 9]));
```
