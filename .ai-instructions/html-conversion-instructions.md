# HTML Conversion Instructions
## Complete Guide for Converting Markdown to HTML

**Version**: 1.0.0  
**Last Updated**: February 2026

---

## Table of Contents

1. [Design System](#design-system)
2. [Component Specifications](#component-specifications)
3. [Markdown to HTML Conversion Rules](#markdown-to-html-conversion-rules)
4. [Content Enrichment Guidelines](#content-enrichment-guidelines)
5. [Responsive Design](#responsive-design)
6. [Accessibility Requirements](#accessibility-requirements)
7. [SEO Optimization](#seo-optimization)
8. [Performance Optimization](#performance-optimization)
9. [Quality Assurance Checklist](#quality-assurance-checklist)

---

## Design System

### Color Palette

#### Primary Colors
```css
--primary-dark: #1a1a2e;      /* Deep navy - main backgrounds */
--primary-medium: #16213e;    /* Medium navy - section backgrounds */
--primary-light: #0f3460;     /* Light navy - hover states */
--accent-gold: #e94560;       /* Coral red - accents, links, highlights */
--accent-amber: #f39c12;      /* Amber - secondary accents, warnings */
```

#### Neutral Colors
```css
--text-primary: #e8e8e8;      /* Off-white - main text */
--text-secondary: #b8b8b8;    /* Light gray - secondary text */
--text-muted: #888888;        /* Gray - muted text, captions */
--background-white: #ffffff;  /* Pure white - code backgrounds, cards */
--background-light: #f5f5f5;  /* Light gray - alternate backgrounds */
--background-dark: #0a0a0a;   /* Near black - dark mode deep backgrounds */
```

#### Semantic Colors
```css
--success: #27ae60;           /* Green - success states */
--warning: #f39c12;           /* Orange - warnings */
--error: #e74c3c;             /* Red - errors, critical */
--info: #3498db;              /* Blue - information */
```

#### Syntax Highlighting (for code blocks)
```css
--code-keyword: #c678dd;      /* Purple - keywords */
--code-string: #98c379;       /* Green - strings */
--code-number: #d19a66;       /* Orange - numbers */
--code-comment: #5c6370;      /* Gray - comments */
--code-function: #61afef;     /* Blue - functions */
```

### Typography

#### Font Families
```css
--font-heading: 'Playfair Display', 'Georgia', serif;
--font-body: 'Inter', 'Helvetica Neue', 'Arial', sans-serif;
--font-mono: 'Fira Code', 'Consolas', 'Monaco', monospace;
```

#### Font Sizes (Responsive Scale)
```css
/* Base size: 16px */
--text-xs: 0.75rem;     /* 12px - Fine print, captions */
--text-sm: 0.875rem;    /* 14px - Small text, labels */
--text-base: 1rem;      /* 16px - Body text */
--text-lg: 1.125rem;    /* 18px - Large body text */
--text-xl: 1.25rem;     /* 20px - Small headings */
--text-2xl: 1.5rem;     /* 24px - H4 */
--text-3xl: 1.875rem;   /* 30px - H3 */
--text-4xl: 2.25rem;    /* 36px - H2 */
--text-5xl: 3rem;       /* 48px - H1 */
--text-6xl: 3.75rem;    /* 60px - Display headings */
```

#### Line Heights
```css
--leading-tight: 1.25;   /* Headings */
--leading-normal: 1.6;   /* Body text */
--leading-relaxed: 1.75; /* Long-form reading */
```

#### Font Weights
```css
--weight-normal: 400;    /* Body text */
--weight-medium: 500;    /* Emphasis */
--weight-semibold: 600;  /* Sub-headings */
--weight-bold: 700;      /* Headings */
--weight-black: 900;     /* Display headings */
```

### Spacing System (8px base)

```css
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
```

### Shadows and Effects

```css
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
--shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.15);
--shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.2);
--shadow-glow: 0 0 20px rgba(233, 69, 96, 0.3);
```

### Border Radius

```css
--radius-sm: 0.25rem;   /* 4px - buttons, inputs */
--radius-md: 0.5rem;    /* 8px - cards, images */
--radius-lg: 1rem;      /* 16px - large cards */
--radius-full: 9999px;  /* Circles, pills */
```

---

## Component Specifications

### Header Component

```html
<header class="site-header">
  <div class="header-container">
    <div class="header-branding">
      <h1 class="site-title">
        <a href="/">Ancient Anomalies</a>
      </h1>
      <p class="site-tagline">Evidence-Based Research on Ancient Engineering Mysteries</p>
    </div>
    <nav class="header-nav">
      <button class="nav-toggle" aria-label="Toggle navigation" aria-expanded="false">
        <span class="hamburger"></span>
      </button>
      <ul class="nav-menu">
        <li><a href="/index.html">Home</a></li>
        <li><a href="/topics.html">Topics</a></li>
        <li><a href="/sites.html">Sites</a></li>
        <li><a href="/about.html">About</a></li>
      </ul>
    </nav>
  </div>
</header>
```

**Styles**:
```css
.site-header {
  background: var(--primary-dark);
  border-bottom: 2px solid var(--accent-gold);
  padding: var(--space-6) var(--space-4);
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: var(--shadow-md);
}

.header-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.site-title {
  font-family: var(--font-heading);
  font-size: var(--text-4xl);
  font-weight: var(--weight-bold);
  margin: 0;
}

.site-title a {
  color: var(--text-primary);
  text-decoration: none;
  transition: color 0.3s ease;
}

.site-title a:hover {
  color: var(--accent-gold);
}

.site-tagline {
  color: var(--text-secondary);
  font-size: var(--text-sm);
  margin: var(--space-2) 0 0;
}

.nav-menu {
  display: flex;
  gap: var(--space-6);
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-menu a {
  color: var(--text-primary);
  text-decoration: none;
  font-weight: var(--weight-medium);
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-sm);
  transition: all 0.3s ease;
}

.nav-menu a:hover,
.nav-menu a.active {
  color: var(--accent-gold);
  background: var(--primary-light);
}
```

### Navigation Sidebar Component

```html
<aside class="sidebar">
  <nav class="sidebar-nav" aria-label="Table of contents">
    <h2 class="sidebar-title">On This Page</h2>
    <ul class="toc-list">
      <li class="toc-item"><a href="#section-1">Introduction</a></li>
      <li class="toc-item"><a href="#section-2">Key Findings</a>
        <ul class="toc-sublist">
          <li class="toc-item"><a href="#section-2-1">Precision Measurements</a></li>
          <li class="toc-item"><a href="#section-2-2">Transport Logistics</a></li>
        </ul>
      </li>
      <li class="toc-item"><a href="#section-3">Conclusion</a></li>
    </ul>
  </nav>
  
  <div class="sidebar-section">
    <h3 class="sidebar-section-title">Related Topics</h3>
    <ul class="related-links">
      <li><a href="/megalithic-engineering.html">Megalithic Engineering</a></li>
      <li><a href="/precision-stonework.html">Precision Stonework</a></li>
    </ul>
  </div>
</aside>
```

**Styles**:
```css
.sidebar {
  background: var(--background-light);
  padding: var(--space-6);
  border-radius: var(--radius-lg);
  position: sticky;
  top: calc(var(--header-height) + var(--space-4));
  max-height: calc(100vh - var(--header-height) - var(--space-8));
  overflow-y: auto;
}

.sidebar-title {
  font-size: var(--text-xl);
  font-weight: var(--weight-semibold);
  margin: 0 0 var(--space-4);
  color: var(--primary-dark);
}

.toc-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.toc-item {
  margin: var(--space-2) 0;
}

.toc-item a {
  color: var(--primary-dark);
  text-decoration: none;
  padding: var(--space-2) var(--space-3);
  display: block;
  border-left: 2px solid transparent;
  transition: all 0.2s ease;
}

.toc-item a:hover,
.toc-item a.active {
  color: var(--accent-gold);
  border-left-color: var(--accent-gold);
  background: rgba(233, 69, 96, 0.05);
}

.toc-sublist {
  margin-left: var(--space-4);
  padding-left: 0;
  list-style: none;
}
```

### Footer Component

```html
<footer class="site-footer">
  <div class="footer-container">
    <div class="footer-section">
      <h3>About Ancient Anomalies</h3>
      <p>Evidence-based documentation of ancient engineering mysteries, precision stonework, and unexplained achievements.</p>
    </div>
    
    <div class="footer-section">
      <h3>Quick Links</h3>
      <ul>
        <li><a href="/index.html">Home</a></li>
        <li><a href="/topics.html">All Topics</a></li>
        <li><a href="/about.html">About</a></li>
        <li><a href="/contribute.html">Contribute</a></li>
      </ul>
    </div>
    
    <div class="footer-section">
      <h3>Documentation</h3>
      <ul>
        <li><a href="/methodology.html">Research Methodology</a></li>
        <li><a href="/sources.html">Sources & Citations</a></li>
        <li><a href="/glossary.html">Glossary</a></li>
      </ul>
    </div>
  </div>
  
  <div class="footer-bottom">
    <p>&copy; 2026 Ancient Anomalies. Licensed under <a href="/license.html">CC BY-SA 4.0</a>.</p>
    <p>Evidence-based research • Critical analysis • Intellectual honesty</p>
  </div>
</footer>
```

**Styles**:
```css
.site-footer {
  background: var(--primary-dark);
  color: var(--text-secondary);
  padding: var(--space-16) var(--space-4) var(--space-8);
  margin-top: var(--space-20);
  border-top: 2px solid var(--accent-gold);
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--space-10);
}

.footer-section h3 {
  color: var(--accent-gold);
  font-size: var(--text-lg);
  margin: 0 0 var(--space-4);
}

.footer-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-section li {
  margin: var(--space-2) 0;
}

.footer-section a {
  color: var(--text-secondary);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-section a:hover {
  color: var(--accent-gold);
}

.footer-bottom {
  max-width: 1200px;
  margin: var(--space-12) auto 0;
  padding-top: var(--space-8);
  border-top: 1px solid var(--primary-light);
  text-align: center;
  font-size: var(--text-sm);
}
```

### Content Card Component

```html
<article class="content-card">
  <header class="card-header">
    <h2 class="card-title">
      <a href="/article-url.html">Article Title</a>
    </h2>
    <div class="card-meta">
      <span class="meta-item">
        <svg class="icon" aria-hidden="true">...</svg>
        Category: Precision Stonework
      </span>
      <span class="meta-item">
        <svg class="icon" aria-hidden="true">...</svg>
        5 min read
      </span>
    </div>
  </header>
  
  <div class="card-content">
    <p>Brief excerpt or description of the article content...</p>
  </div>
  
  <footer class="card-footer">
    <div class="card-tags">
      <span class="tag">Egypt</span>
      <span class="tag">Precision</span>
      <span class="tag">Granite</span>
    </div>
    <a href="/article-url.html" class="card-link">Read more →</a>
  </footer>
</article>
```

**Styles**:
```css
.content-card {
  background: var(--background-white);
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  box-shadow: var(--shadow-md);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.content-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-xl);
}

.card-title {
  font-size: var(--text-2xl);
  margin: 0 0 var(--space-3);
}

.card-title a {
  color: var(--primary-dark);
  text-decoration: none;
}

.card-title a:hover {
  color: var(--accent-gold);
}

.card-meta {
  display: flex;
  gap: var(--space-4);
  color: var(--text-muted);
  font-size: var(--text-sm);
  margin-bottom: var(--space-4);
}

.meta-item {
  display: flex;
  align-items: center;
  gap: var(--space-2);
}

.card-tags {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-2);
}

.tag {
  background: var(--primary-light);
  color: var(--text-primary);
  padding: var(--space-1) var(--space-3);
  border-radius: var(--radius-sm);
  font-size: var(--text-xs);
  font-weight: var(--weight-medium);
}
```

---

## Markdown to HTML Conversion Rules

### Headers

**Markdown**:
```markdown
# H1 Heading
## H2 Heading
### H3 Heading
#### H4 Heading
```

**HTML**:
```html
<h1 id="h1-heading">H1 Heading</h1>
<h2 id="h2-heading">H2 Heading</h2>
<h3 id="h3-heading">H3 Heading</h3>
<h4 id="h4-heading">H4 Heading</h4>
```

**Rules**:
- Always add `id` attributes based on slugified heading text
- Use semantic heading hierarchy (don't skip levels)
- H1 should be page title only (one per page)
- Add anchor links for headers H2-H4

### Paragraphs

**Markdown**:
```markdown
This is a paragraph with some text.

This is another paragraph.
```

**HTML**:
```html
<p>This is a paragraph with some text.</p>
<p>This is another paragraph.</p>
```

### Emphasis

**Markdown**:
```markdown
*italic* or _italic_
**bold** or __bold__
***bold italic***
~~strikethrough~~
```

**HTML**:
```html
<em>italic</em>
<strong>bold</strong>
<strong><em>bold italic</em></strong>
<del>strikethrough</del>
```

### Lists

**Unordered List Markdown**:
```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3
```

**HTML**:
```html
<ul>
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Nested item 2.1</li>
      <li>Nested item 2.2</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>
```

**Ordered List Markdown**:
```markdown
1. First item
2. Second item
3. Third item
```

**HTML**:
```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

### Links

**Markdown**:
```markdown
[Link text](https://example.com)
[Link with title](https://example.com "Title text")
```

**HTML**:
```html
<a href="https://example.com">Link text</a>
<a href="https://example.com" title="Title text">Link with title</a>
```

**External Links Enhancement**:
```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  External link
  <svg class="icon-external" aria-hidden="true">...</svg>
</a>
```

### Images

**Markdown**:
```markdown
![Alt text](image-url.jpg)
![Alt text](image-url.jpg "Image title")
```

**HTML**:
```html
<figure>
  <img src="image-url.jpg" alt="Alt text" loading="lazy">
  <figcaption>Image title</figcaption>
</figure>
```

**Responsive Images**:
```html
<figure>
  <picture>
    <source srcset="image-800.webp" media="(max-width: 800px)" type="image/webp">
    <source srcset="image-1200.webp" media="(min-width: 801px)" type="image/webp">
    <img src="image-1200.jpg" alt="Alt text" loading="lazy" width="1200" height="800">
  </picture>
  <figcaption>Detailed caption with <a href="/source.html">source</a></figcaption>
</figure>
```

### Blockquotes

**Markdown**:
```markdown
> This is a quote.
> It can span multiple lines.
>
> — Author Name
```

**HTML**:
```html
<blockquote>
  <p>This is a quote. It can span multiple lines.</p>
  <cite>— Author Name</cite>
</blockquote>
```

### Code

**Inline Code Markdown**:
```markdown
Use the `code` function.
```

**HTML**:
```html
<p>Use the <code>code</code> function.</p>
```

**Code Block Markdown**:
````markdown
```python
def example():
    return "Hello, World!"
```
````

**HTML**:
```html
<pre><code class="language-python">def example():
    return "Hello, World!"
</code></pre>
```

**Enhanced with Syntax Highlighting**:
```html
<div class="code-block">
  <div class="code-header">
    <span class="language-label">Python</span>
    <button class="copy-button" aria-label="Copy code">
      <svg class="icon-copy">...</svg>
    </button>
  </div>
  <pre><code class="language-python hljs"><!-- highlighted code --></code></pre>
</div>
```

### Tables

**Markdown**:
```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
```

**HTML**:
```html
<div class="table-wrapper">
  <table>
    <thead>
      <tr>
        <th>Header 1</th>
        <th>Header 2</th>
        <th>Header 3</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
        <td>Cell 3</td>
      </tr>
      <tr>
        <td>Cell 4</td>
        <td>Cell 5</td>
        <td>Cell 6</td>
      </tr>
    </tbody>
  </table>
</div>
```

**Table Styles**:
```css
.table-wrapper {
  overflow-x: auto;
  margin: var(--space-6) 0;
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-sm);
}

table {
  width: 100%;
  border-collapse: collapse;
  background: var(--background-white);
}

thead {
  background: var(--primary-dark);
  color: var(--text-primary);
}

th {
  padding: var(--space-4);
  text-align: left;
  font-weight: var(--weight-semibold);
  border-bottom: 2px solid var(--accent-gold);
}

td {
  padding: var(--space-3) var(--space-4);
  border-bottom: 1px solid var(--background-light);
}

tbody tr:hover {
  background: rgba(233, 69, 96, 0.05);
}
```

### Horizontal Rules

**Markdown**:
```markdown
---
```

**HTML**:
```html
<hr class="divider">
```

```css
.divider {
  border: none;
  border-top: 2px solid var(--accent-gold);
  margin: var(--space-12) 0;
  opacity: 0.3;
}
```

---

## Content Enrichment Guidelines

### Add Tooltips for Technical Terms

**Markdown**:
```markdown
The blocks show micron-level precision.
```

**Enhanced HTML**:
```html
<p>The blocks show <span class="tooltip" data-tooltip="Precision at the micrometer scale (0.001mm)">micron-level precision</span>.</p>
```

### Add Citations

**Markdown**:
```markdown
The Great Pyramid base is level to 21mm over 230m (Petrie, 1883).
```

**Enhanced HTML**:
```html
<p>The Great Pyramid base is level to 21mm over 230m 
  <sup class="citation">
    <a href="#ref-petrie-1883" id="cite-petrie-1883" aria-label="Citation: Petrie, 1883">
      [1]
    </a>
  </sup>.
</p>

<!-- In references section -->
<section class="references">
  <h2 id="references">References</h2>
  <ol class="reference-list">
    <li id="ref-petrie-1883">
      Petrie, W.M.F. (1883). <em>The Pyramids and Temples of Gizeh</em>. London: Field & Tuer.
      <a href="#cite-petrie-1883" aria-label="Back to citation">↩</a>
    </li>
  </ol>
</section>
```

### Add Cross-References

**Markdown**:
```markdown
See also: [Precision Stonework](precision-stonework.md)
```

**Enhanced HTML**:
```html
<aside class="cross-reference">
  <h4>Related Topics</h4>
  <ul>
    <li>
      <svg class="icon-link" aria-hidden="true">...</svg>
      <a href="/precision-stonework.html">Precision Stonework</a>
      <p class="cross-ref-description">Detailed analysis of micron-level accuracy in ancient artifacts</p>
    </li>
  </ul>
</aside>
```

### Add Info Boxes

**Markdown** (using special syntax):
```markdown
> **Note**: This measurement is disputed by some researchers.
```

**Enhanced HTML**:
```html
<aside class="info-box info-note">
  <div class="info-icon">
    <svg aria-hidden="true">...</svg>
  </div>
  <div class="info-content">
    <strong>Note:</strong> This measurement is disputed by some researchers.
  </div>
</aside>
```

**Info Box Types**:
- `.info-note` - General information (blue)
- `.info-warning` - Warnings or cautions (orange)
- `.info-important` - Critical information (red)
- `.info-tip` - Helpful tips (green)

---

## Responsive Design

### Breakpoints

```css
/* Mobile-first approach */
:root {
  --breakpoint-sm: 640px;   /* Small tablets */
  --breakpoint-md: 768px;   /* Tablets */
  --breakpoint-lg: 1024px;  /* Laptops */
  --breakpoint-xl: 1280px;  /* Desktops */
  --breakpoint-2xl: 1536px; /* Large desktops */
}

/* Usage */
@media (min-width: 768px) {
  /* Tablet styles */
}

@media (min-width: 1024px) {
  /* Laptop styles */
}
```

### Responsive Layout

```css
.main-layout {
  display: grid;
  gap: var(--space-8);
  max-width: 1400px;
  margin: 0 auto;
  padding: var(--space-4);
}

/* Mobile: single column */
@media (max-width: 767px) {
  .main-layout {
    grid-template-columns: 1fr;
  }
  
  .sidebar {
    position: static;
    max-height: none;
  }
}

/* Tablet: two columns */
@media (min-width: 768px) and (max-width: 1023px) {
  .main-layout {
    grid-template-columns: 250px 1fr;
  }
}

/* Laptop+: three columns with sidebar */
@media (min-width: 1024px) {
  .main-layout {
    grid-template-columns: 250px 1fr 300px;
  }
}
```

### Responsive Typography

```css
/* Fluid typography using clamp() */
h1 {
  font-size: clamp(2rem, 5vw, 3rem);
}

h2 {
  font-size: clamp(1.5rem, 4vw, 2.25rem);
}

p {
  font-size: clamp(1rem, 2vw, 1.125rem);
}
```

### Responsive Images

```html
<img 
  src="image-1200.jpg" 
  srcset="image-400.jpg 400w, 
          image-800.jpg 800w, 
          image-1200.jpg 1200w"
  sizes="(max-width: 640px) 100vw,
         (max-width: 1024px) 80vw,
         1200px"
  alt="Description"
  loading="lazy"
>
```

---

## Accessibility Requirements

### WCAG 2.1 AA Compliance Checklist

#### ✓ Perceivable

**1.1.1 Non-text Content (Level A)**:
- All images must have meaningful `alt` attributes
- Decorative images use `alt=""` or `role="presentation"`
- Complex images have longer descriptions (via `aria-describedby` or `<figcaption>`)

**1.3.1 Info and Relationships (Level A)**:
- Use semantic HTML (`<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, `<footer>`)
- Proper heading hierarchy (don't skip levels)
- Use lists for lists, tables for tabular data

**1.4.3 Contrast (Level AA)**:
- Text vs. background: minimum 4.5:1 ratio
- Large text (18pt+): minimum 3:1 ratio
- Use contrast checker tools

**1.4.5 Images of Text (Level AA)**:
- Avoid images of text when possible
- Use actual HTML text with CSS styling instead

#### ✓ Operable

**2.1.1 Keyboard (Level A)**:
- All functionality available via keyboard
- Visible focus indicators
- Logical tab order

**2.4.1 Bypass Blocks (Level A)**:
```html
<a href="#main-content" class="skip-link">Skip to main content</a>

<main id="main-content">
  <!-- Main content -->
</main>
```

**2.4.2 Page Titled (Level A)**:
```html
<title>Article Title | Ancient Anomalies</title>
```

**2.4.4 Link Purpose (Level A)**:
- Link text should be meaningful
- Avoid "click here" or "read more" without context
- Use `aria-label` for context when needed:
```html
<a href="/article.html" aria-label="Read more about the Great Pyramid">Read more</a>
```

#### ✓ Understandable

**3.1.1 Language of Page (Level A)**:
```html
<html lang="en">
```

**3.2.3 Consistent Navigation (Level AA)**:
- Navigation order consistent across pages
- Same components in same relative order

#### ✓ Robust

**4.1.2 Name, Role, Value (Level A)**:
- Use semantic HTML elements
- Add ARIA attributes when custom components needed:
```html
<button aria-label="Open menu" aria-expanded="false">
  <span class="icon-menu" aria-hidden="true"></span>
</button>
```

### Focus Management

```css
/* Remove default outline */
*:focus {
  outline: none;
}

/* Add custom focus indicator */
*:focus-visible {
  outline: 3px solid var(--accent-gold);
  outline-offset: 2px;
}

/* Skip link */
.skip-link {
  position: absolute;
  left: -9999px;
  top: 0;
  z-index: 999;
  padding: var(--space-4);
  background: var(--accent-gold);
  color: var(--background-white);
  text-decoration: none;
}

.skip-link:focus {
  left: 0;
}
```

### ARIA Landmarks

```html
<header role="banner">...</header>
<nav role="navigation" aria-label="Main navigation">...</nav>
<main role="main">...</main>
<aside role="complementary">...</aside>
<footer role="contentinfo">...</footer>
```

---

## SEO Optimization

### Meta Tags

```html
<head>
  <!-- Essential meta tags -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title - Ancient Anomalies</title>
  <meta name="description" content="150-160 character description of page content">
  
  <!-- Open Graph (Facebook, LinkedIn) -->
  <meta property="og:title" content="Page Title">
  <meta property="og:description" content="Description for social sharing">
  <meta property="og:image" content="https://example.com/share-image.jpg">
  <meta property="og:url" content="https://example.com/page-url.html">
  <meta property="og:type" content="article">
  
  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Page Title">
  <meta name="twitter:description" content="Description for Twitter">
  <meta name="twitter:image" content="https://example.com/share-image.jpg">
  
  <!-- Canonical URL -->
  <link rel="canonical" href="https://example.com/page-url.html">
</head>
```

### Structured Data (Schema.org)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "The Great Pyramid: Precision Engineering",
  "description": "Analysis of precision measurements in the Great Pyramid",
  "image": "https://example.com/great-pyramid.jpg",
  "author": {
    "@type": "Organization",
    "name": "Ancient Anomalies"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Ancient Anomalies",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo.png"
    }
  },
  "datePublished": "2026-02-01",
  "dateModified": "2026-02-10"
}
</script>
```

### Semantic HTML

```html
<article>
  <header>
    <h1>Article Title</h1>
    <time datetime="2026-02-10">February 10, 2026</time>
  </header>
  
  <section>
    <h2>Section Title</h2>
    <p>Content...</p>
  </section>
  
  <footer>
    <p>Author: Ancient Anomalies Team</p>
  </footer>
</article>
```

---

## Performance Optimization

### Critical CSS

Inline critical CSS in `<head>` for above-the-fold content:

```html
<head>
  <style>
    /* Critical CSS - minimal styles for initial render */
    body { font-family: sans-serif; margin: 0; }
    .site-header { background: #1a1a2e; padding: 1.5rem 1rem; }
    /* ... */
  </style>
  
  <!-- Load full CSS asynchronously -->
  <link rel="preload" href="/styles/main.css" as="style" onload="this.onload=null;this.rel='stylesheet'">
  <noscript><link rel="stylesheet" href="/styles/main.css"></noscript>
</head>
```

### Image Optimization

- Use WebP format with JPEG/PNG fallback
- Add `loading="lazy"` for offscreen images
- Specify width and height to prevent layout shift
- Use responsive images with `srcset`

### Font Loading

```html
<head>
  <!-- Preload critical fonts -->
  <link rel="preload" href="/fonts/inter-var.woff2" as="font" type="font/woff2" crossorigin>
  
  <!-- Font display strategy -->
  <style>
    @font-face {
      font-family: 'Inter';
      src: url('/fonts/inter-var.woff2') format('woff2');
      font-display: swap; /* Show fallback immediately, swap when loaded */
    }
  </style>
</head>
```

### Code Splitting

- Separate critical CSS from non-critical
- Load JavaScript asynchronously when possible
- Use `defer` or `async` attributes:

```html
<!-- Defer: Execute after HTML parsing -->
<script src="/js/main.js" defer></script>

<!-- Async: Execute as soon as loaded -->
<script src="/js/analytics.js" async></script>
```

---

## Quality Assurance Checklist

### Before Publishing

#### ✓ HTML Validation
- [ ] No HTML errors (validate with W3C validator)
- [ ] Proper nesting of elements
- [ ] All tags closed
- [ ] Valid attribute values

#### ✓ Semantic HTML
- [ ] Proper heading hierarchy (H1 → H2 → H3)
- [ ] Semantic elements used (`<article>`, `<section>`, etc.)
- [ ] Lists used for lists
- [ ] Tables used for tabular data

#### ✓ Accessibility
- [ ] All images have alt text
- [ ] Color contrast meets WCAG AA (4.5:1)
- [ ] Keyboard navigation works
- [ ] Focus indicators visible
- [ ] ARIA labels where needed
- [ ] Skip links present
- [ ] Landmarks defined

#### ✓ Links
- [ ] All internal links work
- [ ] External links open in new tab with `rel="noopener noreferrer"`
- [ ] Link text is meaningful
- [ ] Anchor links work

#### ✓ Responsive Design
- [ ] Mobile view tested (320px width minimum)
- [ ] Tablet view tested
- [ ] Desktop view tested
- [ ] Images responsive
- [ ] Text readable at all sizes
- [ ] Navigation works on mobile

#### ✓ Performance
- [ ] Images optimized (WebP with fallback)
- [ ] Images have width/height attributes
- [ ] Critical CSS inlined
- [ ] JavaScript deferred or async
- [ ] Fonts optimized (woff2 format)
- [ ] Loading states for dynamic content

#### ✓ SEO
- [ ] Title tag present and descriptive
- [ ] Meta description present (150-160 chars)
- [ ] Canonical URL set
- [ ] Open Graph tags present
- [ ] Structured data (Schema.org) added
- [ ] Sitemap updated

#### ✓ Content
- [ ] Spelling and grammar checked
- [ ] Technical terms have tooltips
- [ ] Citations properly formatted
- [ ] Cross-references accurate
- [ ] Code examples tested
- [ ] Tables formatted correctly

#### ✓ Browser Testing
- [ ] Chrome/Edge (Chromium)
- [ ] Firefox
- [ ] Safari
- [ ] Mobile browsers (iOS Safari, Chrome Android)

---

## Summary

This HTML conversion guide ensures:
1. **Consistent design** across all pages using design system
2. **Semantic HTML** for better accessibility and SEO
3. **Responsive layout** working on all devices
4. **WCAG 2.1 AA accessibility** compliance
5. **Optimized performance** with lazy loading, critical CSS, and code splitting
6. **SEO best practices** with meta tags and structured data
7. **Enhanced content** with tooltips, citations, and cross-references

Always prioritize:
- Semantic HTML over divs
- Accessibility over aesthetics
- Performance over unnecessary features
- Content readability over complexity

---

**Document Version**: 1.0.0  
**Maintained By**: Repository contributors  
**Last Review**: February 2026  
**Next Review**: As needed
