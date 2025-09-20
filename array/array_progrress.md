# Arrays Progress Tracker

## ✅ Covered

### 1. Array Advance Game (Medium—Hard)

- **Problem statement**: can we reach the last index?
- **Greedy approach** (fails in some cases ❌)
- **Correct approach**: iterate, track `furthest_reached`, check reachability
- **Implementation**: Python (while loop, furthest_reached update, termination check)
- **Status**: ✅ Understood & implemented.

---

### 2. Optimal Task Assignment (Greedy)

- **Idea**: Pair smallest with largest task → balances workload.
- **Steps**:
  1. Sort tasks.
  2. Pair i-th smallest with i-th largest.
- **Complexity**: `O(n log n)` (sort)
- **Status**: ✅ Understood & implemented.

---

### 3. Intersection of Two Sorted Arrays (Two-Pointer)

- **Idea**: Use two pointers to find common elements efficiently.
- **Steps**:
  1. Initialize `i, j = 0`.
  2. Compare `A[i]` and `B[j]`.
     - If `A[i] < B[j]` → advance i.
     - If `A[i] > B[j]` → advance j.
     - If equal → record intersection & advance both.
  3. Skip duplicates if required.
- **Complexity**: `O(m + n)`
- **Status**: ✅ Solid.

---

### 4. Buy and Sell Stock (Single Transaction, Greedy)

- **Idea**: Track min price so far + max profit.
- **Steps**:
  1. Initialize `min_price = ∞`, `max_profit = 0`.
  2. For each price:
     - Update `min_price = min(min_price, price)`.
     - Update `max_profit = max(max_profit, price - min_price)`.
- **Complexity**: `O(n)`
- **Status**: ✅ Mastered.

---

## 🔜 Pending

- Rotate Array (Medium)
- Find Missing Number (Easy)
- Maximum Subarray (Kadane's Algorithm) (Medium)
- Container With Most Water (Medium)
- Trapping Rain Water (Hard)
- Sliding Window Maximum (Hard)
