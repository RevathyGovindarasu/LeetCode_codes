class Solution {
    public boolean canReach(String s, int minJump, int maxJump) {
        Queue<Integer> queue = new LinkedList<>();
        queue.offer(0);
        for(int i=1;i<s.length();i++)
        {
            if(s.charAt(i)=='0')
            {
                while(!queue.isEmpty() && queue.peek()<i-maxJump)
                    queue.poll();
                
                if(queue.isEmpty()) return false;
                int prev = queue.peek();
                if(prev+maxJump>=i && prev+minJump<=i)
                {
                    queue.offer(i);
                    if(i==s.length()-1) return true;
                }
            }
        }
        return false;
    }
}
