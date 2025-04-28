# Landing Page Maintenance Guide

This guide will help you maintain and customize the Nachtbril landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Nachtbril</a>
```
- Replace "Nachtbril" with your desired text
- Adjust size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)

2. **Navigation Links:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- More links -->
</div>
```
- Update link text between `<a>` tags
- Maintain the `space-x-8` class for consistent spacing

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Nachtbril Polariserend
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Tijdelijk 20% KORTING - Verbeter je nachtzicht nu!
</p>
```

To modify:
- Change heading text between `<h1>` tags
- Update promotional text in the `<p>` tag
- Maintain responsive classes (`md:`, `lg:` prefixes)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Gepolariseerde Lenzen</h3>
    <p class="text-gray-600">Verminder verblinding...</p>
</div>
```

To update:
- Replace feature title in `<h3>` tags
- Update description in `<p>` tags
- Keep the existing classes for consistent styling

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="https://nachtbril.com/shop">Shop Nu</a>
```

To update external links:
1. Locate the `href` attribute
2. Replace `https://nachtbril.com/shop` with your shop URL
3. Test the link after updating

### Internal Links (Page Sections)
Format: `href="#section-id"`
```html
<!-- Example section target -->
<section id="features" class="py-24 bg-white">
```

To fix:
1. Ensure section IDs match navigation links
2. Check for proper scroll behavior
3. Maintain the `scroll-smooth` class on the HTML tag

## Linking Privacy and Terms Pages

### Adding Footer Links
Locate the footer section and add new links:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Nachtbril. Alle rechten voorbehouden.</p>
    <!-- Add these lines -->
    <div class="mt-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white mr-4">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white">Terms of Service</a>
    </div>
</div>
```

### Styling Consistency
- Use `text-gray-400` for default state
- Add `hover:text-white` for hover effect
- Maintain spacing with `mr-4` between links

## Troubleshooting

### Common Issues

1. **Broken Responsive Design:**
- Check for missing `md:` or `lg:` prefixes
- Verify container classes: `container mx-auto px-4`
- Test on multiple screen sizes

2. **Navigation Issues:**
- Verify section IDs match href attributes
- Check for proper scroll-smooth behavior
- Ensure Alpine.js is loading (`<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>`)

3. **Styling Problems:**
- Confirm Tailwind CSS is properly loaded
- Check for typos in class names
- Verify class combinations are valid

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser console for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different devices and browsers before deploying to production.