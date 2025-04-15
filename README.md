# Web Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the Web Agency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    WebAgency
</a>
```
Simply replace "WebAgency" with your company name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Sydney
</h1>
<p class="text-2xl md:text-3xl text-gray-300 mb-12 leading-relaxed">
    Grow your business with clicks
</p>
```

### Tailwind CSS Tips
- `text-4xl`: Controls text size (ranges from text-xs to text-9xl)
- `md:text-5xl`: Applies different text size on medium screens
- `font-bold`: Makes text bold
- `mb-8`: Adds margin bottom (spacing)
- `text-gray-300`: Sets text color

## Managing Links

### Internal Navigation Links
Current internal links use hashtags to scroll to sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Ensure the href matches the section ID
2. Example: `href="#features"` links to `<section id="features">`

### External Links
The landing page contains several external links to "fixrr.online":
```html
<!-- Example of external link -->
<a href="https://fixrr.online" class="inline-flex items-center...">
```

To update:
1. Replace "https://fixrr.online" with your desired URL
2. Always include "https://" for external links
3. Test links after updating

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:
1. Create new files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling:
   - Copy the header and footer from index.html to your new pages
   - Use the same Tailwind CSS classes for consistency

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Look for classes starting with:
     - `sm:` (small screens)
     - `md:` (medium screens)
     - `lg:` (large screens)
   - Don't remove these prefixes as they're essential for responsive design

3. **Styling Problems**
   - Keep the original Tailwind CSS classes
   - Add new classes at the end of the class list
   - Example: `class="text-xl font-bold your-new-class"`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always make a backup of your files before making significant changes.