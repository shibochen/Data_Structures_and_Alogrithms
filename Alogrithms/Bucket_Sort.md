# Bucket Sort

`Bucket sort` is a sorting algorithm thatworks by distributing the elements of an array into a number of buckets. Each bucket is then sorted individually, 
either using a different sorting algorithm, or by recursively applying the bucket sorting algorithm.

Bucket sort works as follows:
1. Set up an array of initially empty "buckets"
2. Scatter: Go over the original array, putting each object in its bucket
3. Sort each non-empty bucket
4. Gather. Visit the buckets in order and put all elements back into the original array

```java
import java.util.Arrays;

public class bucketSort {
	public static void sort(int[] nums, int maxVal) {
		int[] bucket = new int[maxVal + 1];
		
		for (int i = 0; i < bucket.length; i++) {
			bucket[i] = 0;
		}
		
		for (int i = 0; i < nums.length; i++) {
			bucket[nums[i]]++;
		}
		
		int val = 0;
		for (int i = 0; i <bucket.length; i++) {
			for (int j = 0; j < bucket[i]; j++) {
				nums[val++] = i;
			}
		}
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int maxVal = 5;
		int[] data = {5,3,0,2,4,1,0,5,2,3,1,4};
		
		sort(data,maxVal);
		System.out.println(Arrays.toString(data));
	}

}

```
## Reference 
- [wiki](https://en.wikipedia.org/wiki/Bucket_sort)
