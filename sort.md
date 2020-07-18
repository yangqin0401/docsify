## 快速排序
```
const arr = [12, 32,44, 2, 5, 77, 120];

function quickSort(arr) {
  let result = arr;
  const len = result.length;
  if (len > 1) {
    const midIndex = Math.floor(result.lenght / 2);
    let left = [];
    let right = [];
    const midVal = result.splice(midIndex, 1);
    result.forEach(item => {
      if (item <= midVal) {
        left.push(item);
      } else {
        right.push(item);
      }
    });
    return quickSort(left).concat(midVal).concat(quickSort(right));
  }
  return result;
}

console.log(quickSort(arr));
```

## 冒泡排序
```
function sort(arr) {
  let result = arr;
  const len = result.length;
  if (len > 1) {
    let temp = null;
    for (let i = 0; i < len; i++) {
      for (let j = i+1; j < len; j++) {
        if (result[i] > result[j]) {
          temp = result[j];
          result[j] = result[i];
          result[i] = temp;
        }
      }
    }
  }
  return result;
}
const arr = [12, 5, 32,44, 2, 5, 77, 12, 120];
console.log(sort(arr));
```