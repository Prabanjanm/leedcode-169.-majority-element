# leedcode-169.-majority-element
leedcode 169. majority element solution

class Solution {
    public int majorityElement(int[] nums) {
        int size= nums.length;

        for(int i=0;i<size;i++){
            int count=1;
            for(int z=i+1;z<size;z++){
                if(nums[i]==nums[z])
                count++;
            }
            if(count>size/2){
                return nums[i];
            }
        }
        return -1;
    }
}
