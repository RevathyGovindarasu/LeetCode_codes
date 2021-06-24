class Solution {
    private long MOD = 1_000_000_007;
    public int findPaths(int m, int n, int maxMove, int startRow, int startColumn) {
      int[][][] dp = new int[m][n][maxMove+1];
       for(int i=0;i<m;i++){
           for(int j=0;j<n;j++){
               Arrays.fill(dp[i][j],-1);
               dp[i][j][0]=0;
           }
       }
        return find(m,n,startRow, startColumn, maxMove,dp);
    }
    
   private int find(int m,int n,int r,int c,int N,int[][][] dp){
       if(r<0||r>m-1||c<0||c>n-1)
           return 1;
       
       if(dp[r][c][N]!=-1)
           return dp[r][c][N];
       
       long res=0;
       res += find(m,n,r+1,c,N-1,dp)%MOD;
       res += find(m,n,r-1,c,N-1,dp)%MOD;
       res += find(m,n,r,c+1,N-1,dp)%MOD;
       res += find(m,n,r,c-1,N-1,dp)%MOD;
               
       return dp[r][c][N]= (int)(res%MOD);
       
   }

    
}
