### 🧠 Problem: Two Sum II - Input Array is Sorted (LeetCode #167)

**Given:** A sorted array of integers `numbers` (1-indexed) and a target sum.

**Task:** Find two numbers such that they add up to `target` and return their **1-based indices**.

---

### 🔑 Key Observations:

- The input array is already **sorted in non-decreasing order**.
- Indexes should be **1-based** in the output.

---

### 🔀 Approach: Two Pointers

- Start with two pointers: `i = 0`, `j = arr.length - 1`
- Move pointers based on the sum:
  - If sum is too small → move `i` right.
  - If sum is too large → move `j` left.
  - If equal → return `[i+1, j+1]`

**Logic:**

> Use sorted property to close in on the target by adjusting start/end based on sum comparison.

- ✅ Time: **O(n)**
- ✅ Space: **O(1)**

---

### ⚠️ Edge Cases:

- Return values should be **1-based indexing**.
- Assumes **exactly one valid solution exists**.

---

