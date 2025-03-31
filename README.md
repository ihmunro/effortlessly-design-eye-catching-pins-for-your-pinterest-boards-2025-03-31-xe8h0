# PinDesigner Landing Page Maintenance Guide

This guide will help you maintain and customize the PinDesigner landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this section in the header -->
<span class="font-bold text-xl">PinDesigner</span>
```
Simply replace "PinDesigner" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
</div>
```
To modify menu items:
- Change the text between `<a>` tags
- Keep the `class` attributes unchanged to maintain styling
- Update `href` attributes to match your new section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Effortlessly Design Eye-Catching Pins for Your Pinterest Boards
</h1>
```
Important Tailwind classes explained:
- `text-4xl`: Base text size
- `md:text-5xl`: Tablet size
- `lg:text-6xl`: Desktop size
- `mb-8`: Bottom margin (2rem)

### Understanding Responsive Classes
Tailwind uses prefixes for different screen sizes:
- No prefix: Mobile (default)
- `md:`: Tablet (768px+)
- `lg:`: Desktop (1024px+)

Example:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
```
This creates:
- 1 column on mobile
- 3 columns on tablet and larger screens
- 12 units of gap between items

## Fixing Broken Links

### Current Link Inventory
1. Navigation Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://pinterestpingenerator.com">Get Started</a>
```

To update external links:
1. Locate the `href` attribute
2. Replace `https://pinterestpingenerator.com` with your new URL
3. Test the link after updating

### Internal Section Links
Ensure section IDs match navigation links:
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Corresponding section -->
<section id="features" class="py-24 bg-white">
```

## Linking Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<div>
    <h4 class="text-white font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout:**
- Check for missing closing tags
- Verify Tailwind classes are spelled correctly
- Ensure responsive prefixes (`md:`, `lg:`) are properly used

2. **Non-Working Links:**
- Verify file names match exactly (case-sensitive)
- Ensure internal section IDs exist and match
- Test external URLs in a browser

3. **Inconsistent Styling:**
- Compare classes with working elements
- Check for missing utility classes
- Verify color classes match the design system

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different screen sizes and browsers before deploying to production.