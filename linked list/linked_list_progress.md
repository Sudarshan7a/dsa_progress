## **DSA Progress Tracker — Day 2>3**

_(Topic: Singly Linked List)_

### ✅ Covered

- **Concept & Structure** _(Easy)_:
  - Nodes with `data` and `next` pointer
  - `head` pointer as entry point
  - Last node points to `None`
- **Comparison with Arrays** _(Easy)_:
  - Linked list faster insertion/deletion at start _(O(1))_
  - Arrays faster random access _(O(1))_
- **Core Operations**:

  - `append(data)` _(Easy)_
  - `prepend(data)` _(Easy)_
  - `insert_after_node(prev_node, data)` _(Easy)_
  - `delete_node(key)` _(Easy–Medium)_
  - `delete_node_at_pos(pos)` _(Easy–Medium)_
  - `len_iterative()` _(Easy)_
  - `len_recursive()` _(Medium)_
  - `swap_nodes(key_1, key_2)` _(Medium–Hard)_ ← **first “hard” moment**

- **Advanced Operations**:
  - **Reverse a Linked List** _(Medium–Hard)_
    - **Iterative**: Used `prev`, `curr`, and `next` pointers to reverse links one by one.
    - **Recursive**: Reversed the rest of the list first, then fixed the link for the current node.
  - **Merge Two Sorted Linked Lists** _(Medium)_
    - Compared nodes from both lists, linked the smaller one, and advanced its pointer until one list was done, then attached the rest.
  - **Remove Duplicates** _(Medium)_
    - Used a hash table to track seen values; skipped nodes with duplicate data by adjusting pointers.
  - **Find Nth-to-Last Node** _(Medium)_
    - **Two-pass**: Found length, then moved to `(length - n)`th node.
    - **One-pass (two pointers)**: Moved `q` ahead by `n`, then moved both pointers until `q` reached the end.
  - **Count Occurrences** _(Easy–Medium)_
    - **Iterative**: Traversed and counted matches.
    - **Recursive**: Checked match at current node, then added result from rest of list.
  - **Rotate a Linked List** _(Medium–Hard)_
    - Made the list circular, moved head to `(k+1)`th node, then broke the loop to form the new end.
  - **Check Palindrome** _(Medium)_
    - **String method**: Built a string and compared with reverse.
    - **Stack method**: Pushed all values to stack, then compared while popping.
    - **Two-pointer method**: Compared nodes from both ends moving inward.

---

### 🔜 Pending for Mastery

- **Implementation Variations**:
  - Circular Singly Linked List _(Medium)_
- **Advanced Operations**:
  - Detect & Remove Cycle (Floyd’s Cycle Detection) _(Medium–Hard)_
  - Find Middle Node _(Easy–Medium)_
  - Delete Linked List _(Easy)_
  - Clone Linked List with Random Pointer _(Hard)_
  - Intersection of Two Linked Lists _(Medium)_
  - Palindrome check using in-place list reversal _(Medium–Hard)_
  - Reverse a Linked List — practice until pointer movements are second nature
- **Applications**:
  - Implement stack/queue using linked list _(Medium)_
  - Polynomial representation _(Medium)_
