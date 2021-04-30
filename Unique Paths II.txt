class Solution {
    public int uniquePathsWithObstacles(int[][] obstacleGrid) {
        int size = obstacleGrid[0].length;
        int[] dp = new int[size];
        dp[0]=1;
        for(int[] grid : obstacleGrid)
        {
            for(int j=0;j<size;j++)
            {
                if(grid[j]==1)
                    dp[j]=0;
                else if(j>0)
                    dp[j]+=dp[j-1];
            }
        }
        return dp[size-1];
    }
}