# Day 6 – Doubly Linked List (DLL)

## Key Learnings

- Each node has `data`, `prev`, and `next`.
- `head.prev = None`, `tail.next = None`.
- Supports **bidirectional traversal** unlike SLL.

---

## Insertion

- **Append (at tail)**:
  - Empty list → new node becomes head.
  - Non-empty → traverse to tail, link new node.
- **Prepend (at head)**:
  - Empty list → new node becomes head.
  - Non-empty → rewire old head’s prev to new node.
- **Add After Node (key, data)**:
  - Find node with `key`, insert new node between `cur` and `cur.next`.
- **Add Before Node (key, data)**:
  - Find node with `key`, insert new node between `cur.prev` and `cur`.

---

## Deletion

- **Only Node** → head = None.
- **Head Node** → reassign head, set new head.prev = None.
- **Middle Node** → bypass by rewiring `prev.next = cur.next` and `cur.next.prev = prev`.
- **Tail Node** → set second-last node.next = None.

---

## Reversal

- Traverse from head:
  - Swap `next` and `prev` at each node.
- After traversal, assign new head = last node encountered.

---

## Common Exercises

1. **Remove Duplicates**

   - Track visited values using a set/dict.
   - Delete any node whose value already exists in seen.

2. **Find Pairs with Given Sum**
   - Outer loop pointer `p`.
   - Inner loop pointer `q = p.next`.
   - If `p.data + q.data == target`, record pair.

---

## Status

✅ Implemented all insertions.  
✅ Implemented deletions (all 4 cases).  
✅ Reverse works as expected.  
✅ Solved remove duplicates.  
✅ Solved pairs with given sum.

# Doubly Linked List Progress Tracker

## ✅ Covered

- Structure: `data + prev + next` (Easy)
- `append`, `prepend` (Easy)
- `delete_node` (Easy–Medium)
- `len_iterative`, `len_recursive` (Easy–Medium)
- Forward & backward traversal (Easy)

## 🔜 Pending

- Reverse DLL (Medium–Hard)
- Delete at position (Medium)
- Insert at position (Medium)
- Detect & Remove Cycle (Medium–Hard)
- Merge Two DLLs (Medium)
- Flatten a DLL (Medium–Hard)
