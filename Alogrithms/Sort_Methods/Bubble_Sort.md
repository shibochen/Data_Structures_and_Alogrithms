# Bubble Sort

`Bubble sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order`

```JavaScript
function Bubble_Sort (nums) {
    var n = nums.length;

    for (var i = 0; i < n; i++) {
        for (var j = 0; j < n - i - 1; j++) {
            if (nums[j] > nums[j + 1]) {
                var temp = nums[j];
                nums[j] = nums[j + 1];
                nums[j + 1] = temp;
            }
        }
    }
}
```