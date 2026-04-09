# Skill: Manage Blog for Fishing Frenzy

## 🎯 Context
- Game: Fishing Frenzy  
- Website: https://fishingfrenzy.co  
- Blog type: Pure HTML (no framework, no CMS)  
- Goal: Maintain blog pages + ensure SEO + track all user interactions  

---

## 🚫 Strict Restrictions
- **Resources Folder is Read-Only:** Do NOT modify (create, edit, remove, or rename) any files or directories inside the `resources/` folder under any circumstances. You may read from it to move or copy content to the public blog, but the source files in `resources/` must remain untouched.

## 🧩 Responsibilities

### 1. Blog Content Management
- Create new blog posts as `.html` files
- Follow consistent structure:
  - `<title>`
  - `<meta description>`
  - `<h1>` main title
  - `<article>` content

### 2. URL Strategy & Directory Structure
- Use **directory-based URLs** for all blog posts to maintain clean routing.
- For each new post, create a folder under `public/blog/` named with the URL slug (e.g., `public/blog/article-slug/`).
- The main HTML file inside the folder MUST be named `index.html`. 
- This guarantees clean URLs without `.html` extensions (e.g., `https://fishingfrenzy.co/blog/article-slug/`).

### 3. Homepage & Sitemap Integration
- **Homepage Update**: Whenever adding a new article, update the `<div class="blog-grid">` inside `public/index.html` to include a new `<a class="blog-card">` entry linking to the article.
- **Sitemap Update**: Always update `public/sitemap.xml` by adding a `<url>` entry with the new article's `<loc>`.

### 4. Asset Management
- Store media (images/videos) in `public/assets/` or `public/assets/images/`.
- Always use relative paths when linking to them (e.g., `/assets/fishingfrenzy.mp4`).
- For inline gameplay videos, use `<video autoplay loop muted playsinline>` to ensure they play properly on all devices.

### 5. SEO & Tracking
- Ensure proper `<title>` and `<meta name="description">` are set for each article.
- Include Open Graph tags (`og:title`, `og:description`) for better social sharing.
- Ensure the Google Analytics tracking snippet (`gtag`) is maintained across all pages to track clicks and interactions.