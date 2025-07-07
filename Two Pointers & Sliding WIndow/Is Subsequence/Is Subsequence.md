###

---

### 🧠 Problem: Is Subsequence (LeetCode #392)

**Given:** Two strings `s` and `t`.

**Task:** Check whether string `s` is a subsequence of string `t`.

---

### 🔑 Key Observations:

- A subsequence keeps characters in the same order but may skip some.
- We need to verify if `s` can be formed by deleting characters from `t` without reordering.

---

### ⏭️ Approach: Two Pointers

- Use two pointers `i` for `s` and `j` for `t`.
- Traverse `t` and check if characters match `s[i]`.
- Increment `i` only when there's a match.
- If `i` reaches the end of `s`, it means all characters of `s` are found in order.

**Logic:**

> Walk through `t`, collecting matching characters for `s` using two pointers.

- ✅ Time: **O(n)** where n = length of `t`
- ✅ Space: **O(1)**

---

### ⚠️ Edge Cases:

- `s` is empty → always true.
- `t` is empty but `s` is not → always false.

---

