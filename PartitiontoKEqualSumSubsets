class Solution {
    public boolean canPartitionKSubsets(int[] nums, int k) {
        int sum = 0, maxNum = 0;
        for(int i = 0; i < nums.length; i++){
            sum += nums[i];
            maxNum = Math.max(maxNum, nums[i]);
        }
        if(sum % k != 0 || maxNum > sum / k) return false;
        return helper(nums, k, sum / k, 0, new boolean[nums.length], 0);
    }
    
    private boolean helper(int[] nums, int k, int targetSum,
                           int curSum, boolean[] visited, int innerStart){
        if(k == 0) return true;
        if(curSum > targetSum) return false;
        if(curSum == targetSum) return helper(nums, k - 1, targetSum, 0, visited, 0);
        
        for(int i = innerStart; i < nums.length; i++){
            if(!visited[i]){
                visited[i] = true;
                if(helper(nums, k, targetSum, curSum + nums[i], visited, i + 1)) return true;
                visited[i] = false;
            }
        }
        return false;
    }
}
