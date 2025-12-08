# Badge Alignment Demo

This document demonstrates various approaches to align a badge image with surrounding text in GitHub markdown.

**Note:** This is a demonstration file showing different alignment techniques. The original badge image (`.github/assets/screenshots.yellow.pill.stroke.svg`) remains unmodified as per project requirements.

---

## HTML/Markdown Approaches (No Image Modification)

### 1. Current Approach: `align="middle"`

**HTML:**
```html
<img src=".demo/assets/badge-original.svg" alt="screenshots" align="middle">
```

**Rendered:**
- Text before badge <img src=".demo/assets/badge-original.svg" alt="screenshots" align="middle"> text after badge.

**Notes:**
- This is the current implementation
- `align="middle"` aligns the middle of the image with the baseline of the text
- Works in GitHub markdown (not stripped by sanitizer)
- **Best available option without modifying the image**

---

### 2. Using `<sub>` wrapper

**HTML:**
```html
<sub><img src=".demo/assets/badge-original.svg" alt="screenshots"></sub>
```

**Rendered:**
- Text before badge <sub><img src=".demo/assets/badge-original.svg" alt="screenshots"></sub> text after badge.

**Notes:**
- Shifts badge vertically (lower)
- May also shift horizontally
- GitHub's sanitizer might strip this
- Generally not recommended

---

### 3. Table with `valign` (theoretical)

**HTML:**
```html
<table><tr><td valign="middle">Text <img src=".demo/assets/badge-original.svg" alt="screenshots"></td></tr></table>
```

**Rendered:**

<table><tr><td valign="middle">Text <img src=".demo/assets/badge-original.svg" alt="screenshots"></td></tr></table>

**Notes:**
- Complex structure for inline element
- GitHub may strip the `valign` attribute
- Not practical for inline use
- Not recommended

---

## Image Modification Approaches (For Reference Only)

**⚠️ IMPORTANT:** These approaches require modifying the image file, which is **not allowed** per project requirements. They are shown here for educational purposes only.

---

### 4. SVG with Adjusted viewBox (Modified Image)

This approach modifies the SVG's `viewBox` to add transparent padding, shifting the visual center.

**Modified Image:** `badge-with-padding.svg`
- viewBox changed from `"0 0 119 24"` to `"0 -6 119 36"`
- Content shifted down with `transform="translate(0, 6)"`
- Badge renders at same size but visual center is higher

**HTML:**
```html
<img src=".demo/assets/badge-with-padding.svg" alt="screenshots" align="middle">
```

**Rendered:**
- Text before badge <img src=".demo/assets/badge-with-padding.svg" alt="screenshots" align="middle"> text after badge.

**Notes:**
- When `align="middle"` is applied, the modified viewBox causes better alignment
- Requires modifying the SVG file (**not allowed in this project**)
- Would provide the best visual result if image modification were permitted

---

### 5. SVG with Physical Height Increase (Modified Image)

This approach increases the SVG's physical height while adding transparent top padding.

**Modified Image:** `badge-tall-with-top-padding.svg`
- Height changed from `24px` to `36px`
- viewBox kept at `"0 0 119 36"` 
- Content shifted down with `transform="translate(0, 6)"`

**HTML:**
```html
<img src=".demo/assets/badge-tall-with-top-padding.svg" alt="screenshots" align="middle">
```

**Rendered:**
- Text before badge <img src=".demo/assets/badge-tall-with-top-padding.svg" alt="screenshots" align="middle"> text after badge.

**Notes:**
- Increases overall image dimensions
- May affect layout if used at scale
- Requires modifying the SVG file (**not allowed in this project**)

---

### 6. Convert to PNG with Transparent Padding (Theoretical)

**Approach:**
- Convert SVG to PNG
- Add transparent pixels at top/bottom
- Keep badge content centered

**Notes:**
- Loses vector scalability advantages
- File size larger than SVG
- Requires creating a new image file (**not allowed in this project**)
- Not recommended for this use case

---

## Summary & Recommendations

### Current Implementation ✅
**Approach 1** (`align="middle"`) is currently implemented and is the **best available option** given the constraints:
- ✅ No image modification required
- ✅ Works with GitHub's markdown sanitizer
- ✅ Simple and maintainable
- ⚠️ Not perfectly centered but acceptable

### If Image Modification Were Allowed
**Approach 4** (SVG with adjusted viewBox) would provide the best result:
- ✅ Maintains vector quality
- ✅ No file size increase
- ✅ Better visual alignment
- ❌ Requires modifying the original SVG file

---

## Technical Details

### GitHub Markdown Limitations
- Strips inline `style` attributes for security (XSS prevention)
- Allows certain deprecated HTML attributes like `align`
- Limited CSS/HTML support compared to standard HTML

### Alignment Options in HTML
- `align="top"` - Aligns top of image with top of text
- `align="middle"` - Aligns middle of image with baseline of text (**current**)
- `align="bottom"` - Aligns bottom of image with bottom of text (default)
- `vertical-align` CSS - Not available in GitHub markdown (stripped)

---

**Last Updated:** 2025-12-08  
**Repository:** qizh/taxiboatdriver.com  
**Related PR:** #11
