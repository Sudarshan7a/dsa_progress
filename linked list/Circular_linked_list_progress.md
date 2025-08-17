# Day 5 – Circular Linked List

## Key Learnings

- Tail node points back to head (forms a circle).
- Traversal requires loop until reaching head again.
- Insertion:
  - Append: connect tail → new node → head.
  - Prepend: new node → old head, tail → new node.
- Deletion:
  - Head removal: rewire tail → new head.
  - Non-head removal: prev.next = cur.next.

## Advanced

- Split into two halves by counting length.
- Josephus Problem can be modeled naturally.
- Detect if a list is circular (check for head re-encounter).

## Status

✅ Implemented all operations in Python.
✅ Solved Josephus problem.
✅ Tested detection logic.
