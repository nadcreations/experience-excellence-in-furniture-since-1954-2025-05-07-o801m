# Al Mutlaq Furniture Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Al Mutlaq Furniture landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
Located near the top of the page, the hero section contains the main headline and subheading:

```html
<!-- Original -->
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Experience Excellence in Furniture Since 1954
</h1>
```

To update the headline:
1. Locate the `<h1>` tag within the hero section
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card contains three elements:
- Icon (SVG)
- Heading
- Description

To update a feature card:
```html
<!-- Original Feature Card Structure -->
<div class="bg-gray-50 p-8 rounded-2xl hover:shadow-xl transition-all duration-300 hover:scale-105">
    <div class="w-16 h-16 bg-gray-900 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Project Management</h3>
    <p class="text-gray-600">Expert coordination and execution...</p>
</div>
```

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Colors: `bg-gray-50` (background), `text-gray-600` (text color)
- Typography: `text-xl` (size), `font-semibold` (weight)
- Responsive: `md:text-4xl` (applies at medium screens)

#### Responsive Design Classes
The page uses these breakpoints:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4">
```
This creates a 1-column layout on mobile, 2 columns on medium screens, and 4 columns on large screens.

## Fixing Broken Links

### Navigation Menu Links
The main navigation is in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use the full URL: `https://example.com`

### Social Media Links
Located in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-600 hover:text-gray-900">Facebook</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900">Instagram</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900">LinkedIn</a></li>
</ul>
```

Replace the `#` with actual social media URLs:
```html
<li><a href="https://facebook.com/almutlaqfurniture" class="text-gray-600 hover:text-gray-900">Facebook</a></li>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h4 class="font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#features" class="text-gray-600 hover:text-gray-900">Features</a></li>
        <!-- Add these new links -->
        <li><a href="/privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Section IDs should not contain spaces
   - Check for proper lowercase formatting

2. **Responsive Design Issues**
   - Verify Tailwind breakpoint classes are properly ordered
   - Test on multiple screen sizes
   - Common pattern: `class="base-style md:medium-style lg:large-style"`

3. **Font Issues**
   - Confirm the Google Fonts link in the header is correct
   - Check font family names in classes match exactly
   - Example: `font-['Playfair_Display']`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all external resources (CDN links) are accessible
4. Test the page in multiple browsers

Remember to always make a backup before implementing changes to the live site.