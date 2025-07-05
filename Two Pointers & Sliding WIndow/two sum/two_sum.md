### 🧠 Problem: Two Sum (LeetCode #1)
**Given:** An array of integers `nums` and an integer `target`.

**Task:** Find **two distinct indices** `i` and `j` such that `nums[i] + nums[j] == target`.

---

### 🔑 Key Observations:
- We need **exactly one pair** of indices.
- **Order of indices matters**; `i` and `j` must be returned as per array index, not values.
- **Each input has exactly one solution.**

---

### 🔁 Approach 1: Brute Force (Nested Loops)
- Loop over every possible pair `(i, j)` where `i < j`.
- Check if their sum equals `target`.
- ✅ Simple logic, but ❌ time complexity is **O(n²)**.

**Logic:**  
> Compare all pairs until you find the one that adds up to the target.

---

### ⚡ Approach 2: Hash Map
- Use a map to store `value → index`.
- For each element, check if `target - current value` exists in the map.
- Make sure the indices are **not the same**.

**Logic:**  
> Store all elements in a map, then for each element, check if its complement exists in the map.

- ✅ Time: **O(n)**
- ✅ Space: **O(n)**

---

### ⚠️ Edge Cases:
- Avoid using the same element twice (`map[pair] != i`).
- Negative numbers and zero must be handled properly.

---

