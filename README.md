# Recursive-Search

Search(Recursive)

Search for a key in a Linked List. Return the position where it is found. If not found, return -1.

public int helper(Node head, int key) {
        if (head == null) {
            return -1;
        }

        if (head.data == key) {
            return 0;
        }
        int idx = helper(head.next, key);
        if (idx == -1) {
            return -1;
        }

        return idx + 1;
    }

    public int recSearch(int key) {
        return helper(head, key);
    }