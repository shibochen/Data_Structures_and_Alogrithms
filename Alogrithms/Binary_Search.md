# Binary Search (二分法)

`二分法查找`：给定数组是有序的，给定一个key值。每次查找最中间的值，如果相等，就返回对应下标，如果key大于最中间的值，则在数组的右半边继续查找，
如果小于，则在数组左半边查找，。最终有两种结果，一种是找到并返回下标，第二种是没找到。
- 必须是有序的

# Implementation 
1. Recursive
```java
public int binarySearch(int[] arr, int l, int r, int key) {
		if (l <= r) {
			int mid = l + (r - l) / 2;
			
			if (arr[mid] == key) {
				return mid;
			} else if (arr[mid] < key) {
				return binarySearch(arr, mid + 1, r, key);
			} else {
				return binarySearch(arr, l, mid - 1, key);
			}
		}
		return -1;
	}
```
2. Iterative
```java
public static int binarySearch(int[] arr, int key) {
		int l = 0, r = arr.length - 1;
    
		while (l <= r) {
			int mid = l + (r - l) / 2;
			
			if (arr[mid] == key) {
				return mid;
			} else if (arr[mid] < key) {
				l = mid + 1;
			} else {
				r = mid - 1;
			}
		}
		return -1;
	}
```

## Reference
- [Binary Search](https://www.geeksforgeeks.org/binary-search/)
- [二分法的查找图解](https://www.cnblogs.com/wanglog/p/6650695.html)
