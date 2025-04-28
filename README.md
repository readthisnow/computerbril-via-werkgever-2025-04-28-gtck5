# Landing Page Maintenance Guide

This guide will help you maintain and customize the Computerbril landing page. The instructions are specifically tailored for beginners working with HTML and Tailwind CSS.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-indigo-600">Computerbril</a>
```
Simply replace "Computerbril" with your desired text.

2. **Navigation Items:**
```html
<a href="#features" class="text-gray-600 hover:text-indigo-600">Voordelen</a>
<a href="#benefits" class="text-gray-600 hover:text-indigo-600">Benefits</a>
<a href="#faq" class="text-gray-600 hover:text-indigo-600">FAQ</a>
```
Replace "Voordelen", "Benefits", and "FAQ" with your desired menu items.

### Hero Section
Located right after the header:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight mb-8">
    Computerbril Via Werkgever
    <span class="block text-indigo-600 mt-2">Tijdelijk 20% Korting</span>
</h1>
```
- Replace the main heading and subheading text
- Keep the class structure intact for responsive design
- The `sm:` and `lg:` prefixes control text size on different screen sizes

### Tailwind CSS Class Guide
Common classes used in this page:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold, etc.)
- `bg-{color}`: Sets background color
- `text-{color}`: Sets text color
- `p-{size}`: Sets padding
- `m-{size}`: Sets margin

## Managing Links

### Navigation Links
Current link structure:
```html
<!-- Internal section links -->
<a href="#features">Voordelen</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>

<!-- External shop link -->
<a href="https://computerbril.org/winkel">Bestel Nu</a>
```

To update:
1. Internal links (starting with #) point to sections within the page
2. Change the `href="#features"` to match your section IDs
3. External links (starting with http) should be updated to your actual URLs

### Footer Links
Located at the bottom of the page:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```
Replace the `#` with actual URLs to your policy pages.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
```html
<!-- Replace these placeholder links -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check that all `href` attributes have correct paths
   - Internal links should start with `#`
   - External links should start with `http://` or `https://`

2. **Responsive Design Issues**
   - Don't remove `sm:`, `md:`, or `lg:` prefixes from classes
   - Test on different screen sizes using browser dev tools
   - Keep the mobile menu toggle functionality intact

3. **Styling Problems**
   - Ensure Tailwind CSS CDN link remains in the header
   - Don't remove Alpine.js script for mobile menu functionality
   - Maintain the existing class structure for consistent design

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Keep backups before making significant changes
- Validate all external links
- Maintain consistent branding and messaging

Need help? Contact support@example.com (update this email in the footer section).