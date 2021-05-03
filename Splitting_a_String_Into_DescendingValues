class Solution {
    public boolean splitString(String s) {
        return helper(s,-1);
    }
    private boolean helper(String s,long parent)
    {
        if(s.length()==0) return true;
        else{
        long current=0;
        for(int i=0;i<s.length();i++)
        {
            current = current*10+s.charAt(i)-'0';
            if((i!=s.length()-1 && parent==-1 || parent-current==1) && helper(s.substring(i+1),current)) return true;
                                    //4321 current =4, 3, 32, 321 ..
        }
        }
        return false;
    }
}
