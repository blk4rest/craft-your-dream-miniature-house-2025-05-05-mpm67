# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Kitzey miniature house crafting landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name:**
```html
<a href="/" class="text-xl font-bold text-indigo-600">Kitzey</a>
```
- Replace "Kitzey" with your company name
- The `text-xl` class controls size
- `text-indigo-600` controls the color

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Keep the `hover:text-gray-900` class for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Craft Your Dream Miniature House
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Transform Your Hobby Into Art
</p>
```
- `text-4xl`, `md:text-5xl`, `lg:text-6xl` control responsive text sizing
- `mb-6` and `mb-10` control bottom margins
- Modify text while keeping the classes intact

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-xl`, `mb-6`) control size
- `md:` and `lg:` prefixes apply styles at different screen sizes
- Color classes follow pattern: `text-[color]-[shade]` (e.g., `text-indigo-600`)
- Don't remove `transition`, `duration`, or `hover` classes as they control animations

## Managing Links

### Current Link Locations

1. **Navigation Menu Links:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#guides">Guides</a>
    <a href="#faq">FAQ</a>
    <a href="https://kitzey.curatedspot.com/">Get Started</a>
</div>
```

2. **Call-to-Action Links:**
```html
<a href="https://kitzey.curatedspot.com/" class="inline-flex items-center...">
    Start Creating Today
</a>
```

### Updating Links

1. For internal section links:
- Keep the `#` prefix
- Ensure the ID matches in the corresponding section
- Example: `href="#features"` links to `<section id="features">`

2. For external links:
- Replace `https://kitzey.curatedspot.com/` with your desired URL
- Always include `https://` or `http://`
- Test links after updating

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<footer class="bg-gray-900 text-white py-12">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

2. Add new links (insert before the copyright notice):
```html
<div class="text-center md:text-left">
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <div class="space-y-2">
        <a href="/privacy.html" class="text-gray-400 hover:text-white block">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white block">Terms of Service</a>
    </div>
</div>
```

### Style Consistency
- Use `text-gray-400` for normal state
- Add `hover:text-white` for hover effect
- Maintain the `block` class for proper spacing

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
- Verify that section IDs match exactly with href values
- Check for typos in ID names
- IDs are case-sensitive

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixed classes
- Keep the `container` class on parent elements
- Maintain the viewport meta tag in the header

3. **Style Inconsistencies**
- Copy existing classes for similar elements
- Use the same color scales (e.g., indigo-600) throughout
- Keep transition classes for interactive elements

Need additional help? Contact: kitzey@protonmail.com

---

Remember to test all changes on multiple screen sizes and browsers before deploying to production.