# Landing Page Maintenance Guide
## 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

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
- Services Section
- Benefits Section
- FAQ Section
- Call-to-Action Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located in the header section -->
<span class="text-xl font-bold text-gray-900">101Headshots</span>
```
To change the company name, simply modify the text between the `<span>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight">
    Gladstone, Missouri Corporate Headshot Photography Services
</h1>
<p class="mt-6 text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto">
    Creating visual impressions for Gladstone professionals.
</p>
```
To update:
1. Replace the h1 text to change the main headline
2. Modify the paragraph text to update the subheading

### Understanding Tailwind Classes

#### Responsive Design Classes
The landing page uses these breakpoint prefixes:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Spacing: `px-4`, `py-24`, `mt-6`, `mb-4`
- Colors: `text-gray-900`, `bg-white`, `text-blue-600`
- Typography: `font-bold`, `text-xl`, `tracking-tight`
- Layout: `flex`, `grid`, `max-w-7xl`

## Fixing Broken Links

### Current Link Structure
```html
<!-- Navigation Links -->
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.101headshots.com">Book Now</a>
```

### Updating Navigation Links
1. Internal Links (Same Page):
   ```html
   <!-- Format for section links -->
   <a href="#sectionname">Link Text</a>
   ```
   
2. External Links:
   ```html
   <!-- Format for external links -->
   <a href="https://full-website-url.com">Link Text</a>
   ```

### Checking Links
1. Internal links should match section IDs exactly:
   ```html
   <!-- Navigation link -->
   <a href="#services">Services</a>
   
   <!-- Corresponding section -->
   <section id="services" class="py-24 bg-white">
   ```

2. External links should include the full URL with `https://`

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
   ```html
   <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Verify Tailwind breakpoint prefixes are correct
   - Check viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Style Inconsistencies**
   - Ensure Tailwind CSS CDN is properly loaded
   - Check for typos in class names
   - Maintain consistent color classes throughout

### Need Help?
If you encounter issues:
1. Verify all changes against the original code
2. Check the browser console for errors
3. Ensure all files are in the correct directory
4. Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different devices and browsers before deploying to production.