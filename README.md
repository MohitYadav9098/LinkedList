# LinkedList
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
    public ListNode middleNode(ListNode head) {
        if(head==null||head.next==null){
           return head;
       }
       int count=0;
       ListNode prev=head;
       while(head!=null){
           count++;
           head=head.next;
           }
      int  mid=count/2;
      return helperNode(prev,mid);
    }
    public static ListNode helperNode(ListNode head,int mid){
       int count=-1;
       while(head!=null){
           count++;
           if(count==mid){
              mid++;
              return head; 
           }
           head=head.next;
       }
       return head;
    }
}
