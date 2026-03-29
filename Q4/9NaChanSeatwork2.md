# Seatwork #2 - Getting to know CSS Position and z-index.

**Name:** Hannah Princess G. Chan

---

## Step 1: Static vs Relative
The element moves from its original position to 20px from the top and 20px to the left, but it still occupies its original space in the layout when position: relative is applied.


As compared to Static Positioning, it follows the normal document flow, but it ignores the offset properties (top, bottom, left, right, z-index).
---

## Step 2: Fixed
When you scroll the page, the footer stays fixed (does not move) and at the bottom of the viewport.

The footer behaves differently from position relative since they use different document flows (relative takes up space in normal flow and fixed is removed from normal flow), as well as its positioning context, wherein position relative is positioned relative to its normal position, while fixed position is positioned relative to viewport.

---

 ## Step 3: Absolute
 position: absolute is positioned relative to its nearest pointed ancestor and its element is removed from the normal flow.

 Absolute elements move when the page is scrolled, while fixed elements don't---they stay in place.
 
---

 ## Step 4: Absolute and z-index
 The notice appears on top of the content since it has a higher z-index, with notice having a z-index of 2, and content having a z-index of 1.

 If their z-index values are swapped, content would be on top and notice would be covered by content.
 
---

## Challenge

### 1. Position .notice at the top right corner of .content

```css
.content {
  position: relative;
}

.notice {
  position: absolute;
  right: 0;
  top: 0;
```

### 2. Change position of .content --> relative --> fixed.

```css

```
 
