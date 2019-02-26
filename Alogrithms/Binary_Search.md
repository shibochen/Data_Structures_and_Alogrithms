# Binary Search (二分法)

`二分法查找`：给定数组是有序的，给定一个key值。每次查找最中间的值，如果相等，就返回对应下标，如果key大于最中间的值，则在数组的右半边继续查找，
如果小于，则在数组左半边查找。最终有两种结果，一种是找到并返回下标，第二种是没找到。

1. 判断条件
    - 有序排列
2. 两种写法
    - 递归写法
    - 迭代写法
3. Rotate
4. 子数组
5. 二维数组

## Implemenation

递归：

```java
public static int binarySearch(int[] nums, int low, int high, int target) {
    if (high <= low) {
        return -1;
    }
    int mid = low + (high - low) / 2;
    if (nums[mid] > target) {
        return binarySearch(nums, low, mid + 1, target);
    } else if (nums[mid] < target) {
        return binarySearch(nums, mid + 1, high, target);
    } else {
        return mid;
    }
}
```

迭代：

```java
public static int binarySearch(int[] nums, int target) {
    int left = 0;
    int right = nums.length - 1; //[left, right]

    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] > target) {  //[left, mid - 1]
            right = mid - 1;
        } else if (nums[mid] < target) { //[mid + 1, right]
            left = mid + 1;
        } else {
            return mid;
        }
    }
    return -1;
}
/*以上方法终止条件：right + 1 = left
 *三个值的大小分别为：right < target < left
 *当心越界问题
*/
```

```java
public static int binarySearch(int[] nums, int target) {
    int left = 0;
    int right = nums.length; //[left, right)

    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] > target) {  //[left, mid)
            right = mid;
        } else if (nums[mid] < target) { //[mid + 1, right)
            left = mid + 1;
        } else {
            return mid;
        }
    }
    return -1;
}
/*以上方法终止条件：left = right
 *三个值的大小分别为: target < left || right
*/
```

```java
public static int binarySearch(int[] nums, int target) {
    int left = 0;
    int right = nums.length - 1; //[left, right]

    while (left + 1 < right) { //
        int mid = left + (right - left) / 2;
        if (nums[mid] > target) { //[left, mid]
            right = mid;
        } else if (nums[mid] < target) { //[mid, right]
            left = mid;
        } else {
            return mid;
        }
    }
    if (target == nums[left]) {
        return left;
    } else if (target == nums[right]) {
        return right;
    } else {
        return -1;
    }
}
/*终止条件： left + 1 = right
 *当left和right仅靠时，while loop 不会执行
 *当个值大小: left < target < right
*/
```