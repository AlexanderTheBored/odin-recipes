# Odin Recipes – Project Cleanup & Improvement Guide ✨

This project is off to a solid start — but there are a few key areas that could use polishing for readability, maintainability, and best practices. Here's a friendly guide to help clean things up and future-proof the repo.

---

## 💅 Code Formatting & Readability

- Install **Prettier** (or another code formatter) to automatically clean up indentation, line wrapping, spacing, etc.
- Maintain consistent indentation (2 or 4 spaces — just pick one and stick with it).
- Break long attribute lines (like in `<img>` tags) for readability.
- Consider alphabetizing attributes inside tags for consistency.
- Use semantic HTML where appropriate: `<main>`, `<section>`, `<article>`, etc.
- Avoid using `<br />` for layout spacing — use proper `margin` or `padding` in CSS instead.

---

## 📁 Recommended File Structure

Organizing your project clearly makes collaboration easier and helps avoid broken links:

odin-recipes/
├── index.html
├── css/
│ └── index.css
├── images/
│ └── (local image files go here)
├── videos/
│ └── (any hosted video files)
└── recipes/
├── macaroni.html
├── mangofloat.html
└── spaghetti.html


Try to avoid keeping everything in the root folder — keeping assets in dedicated folders is best practice.

---

## 🧼 CSS Best Practices

- Centralize styling in `index.css`.
- Avoid inline styles or embedded `<style>` blocks.
- Don’t rely on `<br />` for spacing — use `margin-bottom` or padding via CSS.
- If needed later, you can split CSS into `home.css` and `recipe.css` for separate page styles.

---

## ⚠️ Please Avoid Hotlinking Images

Right now, some images are linked directly from external websites like AllRecipes and Wikipedia. While convenient, **hotlinking is discouraged or prohibited** by most Terms of Service.

### Why it’s a problem:
- Can break if the image is removed or renamed.
- Uses someone else’s bandwidth.
- May violate copyright or hosting site rules.
- Looks unprofessional if the source blocks it.

### ✅ Suggested Fix:
- Download the images locally.
- Store them in your `/images/` folder.
- Add proper `alt` text or citation in the caption if needed.

---

## 🔗 Link Consistency

- Stick to **relative paths** throughout the project:
  - ✅ `../images/macaroni.jpg`
  - ❌ `https://some-site.com/image.jpg`
- Don’t mix absolute and relative paths unless necessary for deployment.

---

## ♿ Accessibility & Semantic Tips

- All `<img>` elements should include `alt=""` text — describe what’s in the image, or leave empty if decorative.
- Use `<figure>` and `<figcaption>` for contextual images.
- Use headings properly: `<h1>` for page title, followed by `<h2>`, `<h3>`, etc. — don’t skip levels.
- The `<html lang="en">` declaration is good — leave that in!

---

## 🧪 Running the Project Locally

```bash
1. Clone this repository
2. Open index.html in your browser
3. Confirm all local images load from /images/
4. Navigate between pages via the folder-style homepage links
