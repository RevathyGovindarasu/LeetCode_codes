/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode reverseBetween(ListNode head, int left, int right) {
        if(head==null) return null;
        
        ListNode cur = head, prev=null;
            while(left>1)
            {
                prev=cur;
                cur=cur.next;
                left--;
                right--;
            }
        
        ListNode start = prev, tail=cur;
        ListNode temp = null;
        while(right>0)
        {
            temp = cur.next;
            cur.next=prev;
            prev=cur;
            cur=temp;
            right--;
        }
        
        if(start!=null){
            start.next=prev;
        }
        else
        {
            head=prev;
        }
        tail.next=cur;
        return head;
    }
}
