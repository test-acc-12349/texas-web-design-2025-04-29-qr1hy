# Texas Web Design Landing Page - Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located in the nav section -->
<a href="#" class="text-2xl font-bold text-white">
    TWD  <!-- Change company name/logo text here -->
</a>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Texas Web Design  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300">
    Premium web design solutions...  <!-- Subheadline -->
</p>
```

### Understanding Tailwind Classes

#### Common Class Patterns
1. Spacing Classes:
   - `px-6`: Padding left/right 1.5rem
   - `py-4`: Padding top/bottom 1rem
   - `mb-8`: Margin bottom 2rem

2. Responsive Classes:
   - `md:text-5xl`: Applies on medium screens (768px+)
   - `lg:text-6xl`: Applies on large screens (1024px+)

#### Example: Modifying Button Styles
```html
<!-- Original Button -->
<button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">

<!-- To make button larger -->
<button class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-full">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Keep the `#` prefix for same-page sections
2. For external pages, use full URLs:
```html
<a href="https://example.com/features">Features</a>
```

### Footer Links
Current footer links structure:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Home</a></li>
    <!-- Other links -->
</ul>
```

To update footer links:
1. Replace `#` with proper URLs
2. Maintain the class structure for consistent styling

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Located in the footer section:
```html
<!-- Original Code -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>

<!-- Updated Code -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
```html
<!-- Wrong -->
<a href="features">Features</a>

<!-- Correct -->
<a href="#features">Features</a>
```

2. Missing Responsive Classes
```html
<!-- Wrong -->
<h1 class="text-4xl">Title</h1>

<!-- Correct -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">Title</h1>
```

3. Incorrect Color Classes
```html
<!-- Wrong -->
<div class="bg-blue">

<!-- Correct -->
<div class="bg-blue-600">
```

### Need Help?
- Double-check all href attributes start with "#" for internal links
- Verify all external links include "https://"
- Ensure all Tailwind classes are spelled correctly
- Test responsive design using browser dev tools

Remember to always test your changes across different screen sizes and browsers after making modifications.