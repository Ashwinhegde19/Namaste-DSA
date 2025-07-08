### 🧠 Problem: Find the Index of the First Occurrence in a String (LeetCode #28)

**Given:** Two strings `haystack` and `needle`.

**Task:** Return the index of the first occurrence of `needle` in `haystack`, or -1 if it is not found.

---

### 🔑 Key Observations:

- Compare substrings of `haystack` with `needle` starting at each position.
- Stop as soon as a complete match is found.

---

### ▶️ Approach 1: Sliding Window / Brute Force

- Loop from `i = 0` to `n - m` (where `n = haystack.length` and `m = needle.length`).
- At each position, check if the substring of `haystack` starting at `i` matches `needle`.
- Use an inner loop to compare character-by-character.
- If a complete match is found, return `i`.
- If loop ends without a match, return -1.

**Logic:**

> Try matching `needle` starting at every index in `haystack` until it fits.

- ✅ Time: **O(n * m)**
- ✅ Space: **O(1)**

---

### ⚡ Approach 2: KMP Algorithm (Knuth-Morris-Pratt)

- Preprocess `needle` to build the **LPS (Longest Prefix Suffix)** array.
- Use the LPS array to skip unnecessary comparisons in `haystack`.
- Compare `haystack[i]` and `needle[j]`, adjust `i` and `j` accordingly.
- If characters match, increment both.
- If mismatch and `j > 0`, move `j` using `lps[j - 1]`.
- If complete match (`j == m`), return starting index `i - m`.

**Logic:**

> Use pattern knowledge to avoid rechecking known prefixes and speed up search.

- ✅ Time: **O(n + m)**
- ✅ Space: **O(m)** for LPS array

---

### ⚠️ Edge Cases:

- `needle` is an empty string → return 0.
- `haystack` is shorter than `needle` → return -1.

---

