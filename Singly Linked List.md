## Implementataion fpr swapping two node in ana singly linked list

````java[]

class ListNode {
    int value;
    ListNode next;
    ListNode(int value) { this.value = value; }
}

public class Main {
    public static boolean areEqual(ListNode headA, ListNode headB) {
        ListNode currentA = headA;
        ListNode currentB = headB;

        while (currentA != null && currentB != null) {
            if (currentA.value != currentB.value) {
                return false; // Data mismatch
            }
            currentA = currentA.next;
            currentB = currentB.next;
        }

        // If both lists have reached the end, they are equal
        return currentA == null && currentB == null;
    }

    public static void main(String[] args) {
        // Create first linked list: 1 -> 2 -> 3
        ListNode node1 = new ListNode(1);
        ListNode node2 = new ListNode(2);
        ListNode node3 = new ListNode(3);
        node1.next = node2;
        node2.next = node3;

        // Create second linked list: 1 -> 2 -> 3
        ListNode node4 = new ListNode(1);
        ListNode node5 = new ListNode(2);
        ListNode node6 = new ListNode(3);
        node4.next = node5;
        node5.next = node6;

        // Check if the two linked lists are equal
        if (areEqual(node1, node4)) {
            System.out.println("The linked lists are equal.");
        } else {
            System.out.println("The linked lists are not equal.");
        }
    }
}

````
