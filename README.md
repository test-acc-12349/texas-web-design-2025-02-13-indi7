# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page consists of these major sections:
- Header (Navigation)
- Hero Section
- Features Section
- Video Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Hero Section
To update the main headline, locate this section:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-8 leading-tight">
    Texas Web Design
</h1>
```
Simply replace "Texas Web Design" with your desired text while keeping the surrounding tags intact.

#### Features Section
Each feature card follows this structure:
```html
<div class="group p-8 bg-white rounded-2xl border border-gray-100 hover:shadow-xl transition-all duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Feature Title</h3>
    <p class="text-gray-600 leading-relaxed">Feature description text here.</p>
</div>
```
To update a feature:
1. Find the feature card you want to change
2. Modify the text between the `<h3>` tags for the title
3. Modify the text between the `<p>` tags for the description

### Understanding Tailwind Classes

Key Tailwind classes used in this page:

#### Text Sizes
- `text-5xl`, `text-6xl`, `text-7xl`: Large headline text
- `text-2xl`, `text-3xl`: Medium-sized text
- `text-lg`: Slightly larger than normal text
- `text-base`: Normal text size

#### Colors
- `text-gray-900`: Very dark gray (almost black)
- `text-gray-600`: Medium gray
- `text-white`: White text

#### Spacing
- `px-6`: Horizontal padding
- `py-4`: Vertical padding
- `mb-8`: Bottom margin
- `gap-12`: Space between grid items

To modify spacing, simply adjust the numbers:
- `px-4` (smaller) → `px-8` (larger)
- `mb-4` (smaller) → `mb-12` (larger)

## Managing Links

### Current Link Structure
The page contains these types of links:

1. Navigation Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
    <a href="https://twd.com">Get Started</a>
</div>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="inline-flex items-center justify-center...">
    Start Your Project
</a>
```

### Updating Links

To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the opening and closing tags

Example:
```html
<!-- Before -->
<a href="https://twd.com">Get Started</a>

<!-- After -->
<a href="https://yournewdomain.com">Start Now</a>
```

### Internal vs External Links
- Internal links (same page sections) start with #: `href="#features"`
- External links need full URLs: `href="https://example.com"`

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. Broken Links
- Check for typos in URLs
- Ensure files exist in the correct directory
- Verify that external URLs include `https://`

2. Styling Problems
- Make sure you haven't removed any essential Tailwind classes
- Check that you've maintained the proper class structure
- Verify that the Tailwind CDN link in the header is working

3. Responsive Issues
- Keep the `md:` and `lg:` prefixed classes for proper responsive behavior
- Test your changes at different screen sizes
- Don't remove the viewport meta tag in the header

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all changes against the original code
3. Test the page in multiple browsers
4. Ensure all files are properly saved and uploaded

Remember to always backup your files before making changes!