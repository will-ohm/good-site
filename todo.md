
# 🛠️ Website TODOs & Suggestions

This file collects ideas and suggestions for future improvements.

---

## ✅ Completed
- [x] Use CSS variables for reusable color and font values
- [x] Add dark mode support with `@media (prefers-color-scheme: dark)`

---

## 🚧 In Progress


---

## 🧠 Ideas & Future Improvements
- [ ] Extract :root variables to a separate `colors.css` file
- [ ] Explore `@media` queries for responsive layout (e.g., flex or grid)
- [ ] Add a mobile-first layout with breakpoints
- [ ] Improve site navigation (add nav bar?)
- [ ] Add favicon alternatives for dark/light mode
- [ ] Consider organizing CSS into multiple files (e.g., base.css, layout.css)
- [ ] Add comments to HTML structure for readability

## Implementation Details

### Extract :root variables

separate variables own file, such as: colors.css

Might contain only:

:root {
  --main-bg: #87CEEB;
  --accent-bg: #6495ED;
  --hover-bg: #76ADEF;
  --text-color: #333333;
  ...
}

Then can import file in main stylesheet(s)

@import url("colors.css");

Or in HTML (if separating completely):

<link rel="stylesheet" href="colors.css">
<link rel="stylesheet" href="style.css">

⚠️ Note:
- @import is valid in CSS, but it slows down loading slightly, so <link> is usually preferred for performance.
- This only makes sense once your CSS grows (e.g., 3+ files, reusable modules, or themes).