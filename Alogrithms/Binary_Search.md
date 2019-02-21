# Binary Search (二分法)

`二分法查找`：给定数组是有序的，给定一个key值。每次查找最中间的值，如果相等，就返回对应下标，如果key大于最中间的值，则在数组的右半边继续查找，
如果小于，则在数组左半边查找，。最终有两种结果，一种是找到并返回下标，第二种是没找到。

1. 判断条件
    - 有序排列
2. 两种写法
    - 递归写法
    - 迭代写法
3. Rotate
4. 子数组
5. 二维数组

## Implemenation

```java
//value: right < target < left
//terminal condition: right + 1 = left
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
        System.out.println("mid: " + nums[mid] + "left: " + nums[left] + "right: " + nums[right]);
    }
    System.out.println("left :" + left + "right :" + right);
    return -1;
}

```

```java
//value: target < left
//terminal condition: left = right
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
        System.out.println("mid: " + nums[mid] + "left: " + nums[left]);
    }
    System.out.println("left :" + left + "right :" + right);
    return -1;
}

```

```java
//two numbers are adjacent, the `while` loop will not execute
//value: left < target < right
//terminal condition: left + 1 = right
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
```