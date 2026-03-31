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

**Relative:** The content element moves to the middle while leaving a space from its original position, it is still reserved and not taken by the other elements since it is part of the normal flow.
**Fixed:** It stays the same as like absolute.

### 3. Effect of z-index
The z-index controls which element appears on top of another element first. Elements with higher values of z-index appears on top, while those with lower values appear behind.

---
## Reflection Questions

### a. Differences between CSS Position Values
- **Static:** Default, follows normal document flow, and ignores offset properties (top, bottom, left, right, z-index).
- **Relative:** Relative to normal position, takes up space in normal flow, and can use offset properties.
- **Absolute:** Relative to nearest positioned ancestor, removed from normal flow, and can use offset properties.
- **Fixed:** Relative to viewport, stays in place during scrolling, removed from normal flow, and can use offset properties.

 ### b. How does absolute positioning depend on its parent element?
 Absolute positioning depend on its parent element, the nearest positioned ancestor, with its position set to relative, absolute, fixed, or sticky. If no parent element is positioned, it positions itself relative to the viewport (the body of the page).

 ### c. Sticky vs Fixed
 - **Sticky:** Stays in place during scroling.
 - **Fixed:** Scrolls with the page until a scroll threshold is reached, then it acts fixed.

### d. Application of positioning in a school event webpage
- **A header with fixed position**: This is where students, faculty, and non-teaching staff can access the menu and serve as navigation.
- **A schedule with sticky position**: This is where the overall schedule will be posted for the days of the event.
- **A description of the event with static position:** This will show the description of the event as part of the homepage.
- **A banner/image with absolute position:** To highlight guests, events, and activities.

Overall, it would serve as a tool to make information more accessible and easier to see.
