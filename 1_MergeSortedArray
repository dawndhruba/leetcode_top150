package _1mergeSortedArray;

import java.util.Arrays;

/*
 * 88. Merge Sorted Array
 * 
 * You are given two integer arrays nums1 and nums2, sorted in non-decreasing order, and two integers m and n, representing the number of elements in nums1 and nums2 respectively.
 * Merge nums1 and nums2 into a single array sorted in non-decreasing order.
 * The final sorted array should not be returned by the function, but instead be stored inside the array nums1. To accommodate this, nums1 has a length of m + n, where the first m elements denote the elements that should be merged, and the last n elements are set to 0 and should be ignored. nums2 has a length of n.
 */
public class Solution {

	public static void main(String[] args) {
		int[] nums1 = new int[6];
		int[] nums2 = new int[3];
		nums1[0] = 1;
		nums1[1] = 2;
		nums1[2] = 3;
		nums2[0] = 2;
		nums2[1] = 5;
		nums2[2] = 6;
		
		merge(nums1, 3, nums2, 3);
		
		for (int i = 0; i < nums1.length; i++) {
			System.out.println(nums1[i]);
		}
	}
	
	public static void merge(int[] nums1, int m, int[] nums2, int n) {
        int[] nums1Copy = Arrays.copyOf(nums1, m+n);

        if (m == 1 && n == 0) {
            // do nothing
        } else if (m == 0 && n == 1) {
            nums1[0] = nums2[0];
        } else {
            // iterate nums2
            for(int i=0,j=0,k=0; i<(m+n); i++) {
                if(j == m) {
                    nums1[i] = nums2[k];
                    k++;
                } else if (k == n) {
                    nums1[i] = nums1Copy[j];
                    j++;
                } else {
                    int nums1elem = nums1Copy[j];
                    int nums2elem = nums2[k];

                    if(nums1elem <= nums2elem) {
                        // if both are equal or first array element is smaller than second array element
                        nums1[i] = nums1elem;
                        j++;
                    } else {
                        // if second array element is smaller than first array element
                        nums1[i] = nums2elem;
                        k++;
                    }
                }
            }
        }
    }

}
