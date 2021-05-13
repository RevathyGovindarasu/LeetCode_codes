class Solution {
    public List<String> ambiguousCoordinates(String s) {
        s = s.substring(1, s.length() - 1);
        List<String> result = new LinkedList<>();
        for (int i = 1; i < s.length(); i++) {
            List<String> left = helper(s.substring(0, i));
            List<String> right = helper(s.substring(i));
            for (String llist : left) {
                for (String rlist : right) {
                    result.add("(" + llist + ", " + rlist + ")");
                }
            }
        }
        return result;
    }
    private List<String> helper(String s) {
        int l = s.length();
        char[] cs = s.toCharArray();
        List<String> result = new LinkedList<>();
        if (cs[0] == '0' && cs[l - 1] == '0') { 
            if (l == 1) {
                result.add("0");
            }
            return result;
        }
        if (cs[0] == '0') { 
            result.add("0." + s.substring(1));
            return result;
        }
        if (cs[l - 1] == '0') { 
            result.add(s);
            return result;
        }
        result.add(s); 
        for (int i = 1; i < l; i++) { 
            result.add(s.substring(0, i) + '.' + s.substring(i));
        }
        return result;
    }
}
