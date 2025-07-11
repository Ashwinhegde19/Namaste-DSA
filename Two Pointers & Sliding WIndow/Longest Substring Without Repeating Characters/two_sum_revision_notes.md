### 🧠 Problem: Longest Substring Without Repeating Characters (LeetCode #3)

**Given:** A string `s`.

**Task:** Return the length of the longest substring without repeating characters.

---

### 🔑 Key Observations:

- Need to find the maximum length of a substring with no repeating characters.
- A sliding window helps track the current valid substring range.

---

### 🚀 Approach: Sliding Window with Hash Map

- Use a sliding window.
- Move the right index `j` forward character by character.
- If you see a duplicate character:
  - Move the left index `i` forward just past the previous occurrence of that character.
- Keep updating the character's index in a map.
- Ensure the character’s stored index is only considered if it’s ≥ current left index `i`.
- Update the max length each time.

**Logic Summary:**
> Use sliding window: keep expanding the window (`j++`) until you find a duplicate. When found, move left pointer `i` past the duplicate’s last known position using the map.

- ✅ Time: **O(n)**
- ✅ Space: **O(k)**, where *k* is character set size (e.g., ASCII)

---

### ⚠️ Edge Cases:

- Empty string → 0
- All identical characters → 1

---

