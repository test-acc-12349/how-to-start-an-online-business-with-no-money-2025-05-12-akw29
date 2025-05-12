# BusinessPlan.AI Landing Page Maintenance Guide

This guide will help you maintain and customize the BusinessPlan.AI landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

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
- Call to Action
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Located at the top of the page -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    How To Start An Online Business With No Money
</h1>
```
To update the main headline:
1. Locate this `<h1>` tag
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Get Ideas</h3>
    <p class="text-gray-600">Discover profitable business ideas...</p>
</div>
```
To update feature cards:
1. Find the feature section (identified by `id="features"`)
2. Locate each card's `<h3>` and `<p>` elements
3. Update the text while keeping the classes intact

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The page uses these breakpoints:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (36px)
- Tablet: text-5xl (48px)
- Desktop: text-6xl (60px)

#### Common Class Modifications

1. **Changing Colors**
```html
<!-- Original button -->
<a href="#" class="bg-blue-600 text-white">

<!-- To change to red -->
<a href="#" class="bg-red-600 text-white">
```

2. **Adjusting Spacing**
```html
<!-- Original padding -->
<div class="p-8">

<!-- To increase padding -->
<div class="p-12">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute
3. For external links, add `https://`
4. For internal links, use `#section-id`

### Call-to-Action Buttons
```html
<!-- Main CTA button -->
<a href="https://ninja200.online" class="inline-block bg-blue-600 text-white">
```
To update:
1. Replace `https://ninja200.online` with your desired URL
2. Test the link after updating

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Current footer links:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
- Check that you haven't removed any essential Tailwind classes
- Verify all opening tags have corresponding closing tags
- Ensure the Tailwind CDN link is present in the head section

2. **Links Not Working**
- Verify file paths are correct
- Ensure internal links match section IDs exactly
- Check for typos in URLs
- Test links in different browsers

3. **Responsive Issues**
- Make sure viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- Check responsive classes (md: and lg: prefixes) are correct
- Test on different devices or using browser dev tools

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Compare against the original code provided above

Remember to always test your changes across different devices and browsers before deploying to production.