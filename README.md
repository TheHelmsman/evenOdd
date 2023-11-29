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

JavaScript:

```js
function odd(data) {
  if (!Array.isArray(data)) return [];

  const result = data;

  const sortedOddList = data
    .filter((element) => element % 2)
    .sort((a, b) => b - a);

  if (result !== undefined) {
    for (let i = 0; i < result.length; i++) {
      if (result[i] % 2 > 0) {
        result[i] = sortedOddList.pop();
      }
    }
  }

  return result;
}

console.log(odd([2, 3, 1, 4, 7, 6, 8, 5, 9]));
```

TypeScript:

```ts
export const odd = (data: number[]): number[] => {
  if (!Array.isArray(data)) return [];

  const result = data?.length > 0 ? data : [];

  const sortedOddList = data
    .filter((element) => element % 2)
    .sort((a, b) => b - a);

  if (result !== undefined) {
    for (let i = 0; i < result.length; i++) {
      const tmp: number = result[i] ?? -1;
      if (tmp != -1 && tmp % 2 > 0) {
        result[i] = sortedOddList.pop() ?? -1;
      }
    }
  }

  return result;
};

console.log(odd([2, 3, 1, 4, 7, 6, 8, 5, 9]));
```
