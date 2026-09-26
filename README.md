cat << 'EOF' > README.md
# Web Programming - Assignment 2

This project demonstrates how a single HTML document can adopt two drastically different layouts and behaviors purely through CSS stylesheets (`styleA.css` and `styleB.css`).

## File Organization
- `index.html`: The core HTML structure containing a main container and 6 distinct box elements (`A` through `F`).
- `styleA.css`: Stylesheet implementing a vertical, responsive Flexbox layout with alternating background colors and centered alignments.
- `styleB.css`: Stylesheet implementing an inline horizontal layout that prevents text/box wrapping, features custom hover transitions, and fixes the final element to the bottom-right corner.
- `README.md`: Project documentation and reflections.

## Challenges Faced
1. **Vertical Distribution in Style A:** Ensuring the boxes were vertically distributed evenly across the full viewport height without shrinking or overflowing required setting `height: 100%` on `html`, `body`, and the container, alongside `justify-content: space-between` and `flex-shrink: 0`.
2. **Preventing Line Wrapping in Style B:** To prevent boxes A through E from wrapping onto new lines when the window narrows, `white-space: nowrap` was paired with `display: inline-block`.
3. **Decoupling the 6th Box in Style B:** Isolating the last element while keeping the first five in flow was solved using `position: fixed` targeted via `:last-child`.

## Browser Compatibility
Tested and verified across modern web browsers (Chrome, Safari, Firefox).

## Verification
Validated layout scaling and responsiveness for both Style A and Style B.
