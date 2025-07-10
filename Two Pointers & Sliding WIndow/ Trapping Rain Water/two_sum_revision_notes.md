### 🧠 Problem: Trapping Rain Water (LeetCode #42)

**Given:** An array `height[]` where each element represents the elevation map’s bar height.

**Task:** Compute how much water can be trapped between the bars after raining.

---

### 🔑 Key Observations:

- Water trapped at index `i` depends on the **min of max height to the left and right** of `i`, minus the current height.
- Brute force is slow due to recomputation of left/right max at every step.

---

### 🐢 Approach 1: Precompute Left and Right Max Arrays

- Create two arrays:
  - `leftMax[i]` = max height from 0 to i
  - `rightMax[i]` = max height from n-1 to i
- Water at `i` = `min(leftMax[i], rightMax[i]) - height[i]`
- Sum up water at all positions.

**Logic:**
> Use precomputed bounds to find how much water each index can hold.

- ✅ Time: **O(n)**
- ✅ Space: **O(n)**

---

### ⚡ Approach 2: Two Pointers (Optimal)

- Use two pointers: `left` and `right`
- Track `leftMax` and `rightMax`
- Move the pointer with the lower height inward
- At each step, if height is less than max, trap water; else update max

**Logic:**
> Use the fact that water is trapped between taller bars; move inward while updating limits.

- ✅ Time: **O(n)**
- ✅ Space: **O(1)**

---

### ⚠️ Edge Cases:

- Array size < 3 → no water can be trapped
- Flat or strictly increasing/decreasing bars → no trapped water

---

