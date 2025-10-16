# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the MarketDominate landing page. Perfect for beginners learning HTML and CSS.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <a href="#" class="text-xl font-bold">MarketDominate</a>
</header>
```
To update the company name:
1. Locate the `<a>` tag with class `text-xl font-bold`
2. Replace "MarketDominate" with your company name
3. Keep the `text-xl font-bold` classes to maintain styling

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Dominate Google.<br/>Expand Your Reach
</h1>
```
To modify the main headline:
1. Find the `<h1>` tag in the first section
2. Update the text while keeping the `<br/>` tag for line breaks
3. The responsive text sizes are:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-sm hover:shadow-lg transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">More Traffic</h3>
    <p class="text-gray-600">Drive qualified traffic...</p>
</div>
```
To update feature cards:
1. Locate the feature section with `id="features"`
2. Find each card within the grid
3. Update the `<h3>` title and `<p>` description
4. Maintain the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="http://pf.kakao.com/_xdYaxhn">Get Started</a>
</div>
```
To update links:
1. Internal links (starting with #) connect to section IDs
2. For external links, replace `http://pf.kakao.com/_xdYaxhn` with your desired URL
3. Ensure all section IDs match their corresponding link references

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-600 hover:text-gray-900">About Us</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900">Blog</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900">Careers</a></li>
</ul>
```
To update footer links:
1. Replace `#` with actual page URLs
2. Example: `<a href="about.html">About Us</a>`
3. Keep the `text-gray-600 hover:text-gray-900` classes for consistent styling

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
```html
<!-- Find this section in the footer -->
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```
To implement:
1. Create privacy.html and terms.html in your root directory
2. Update href attributes to point to these files
3. Maintain consistent styling classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Check that you've maintained all responsive classes:
     - `md:` prefix for tablet
     - `lg:` prefix for desktop
   - Don't remove display classes like `hidden md:flex`

3. **Styling Inconsistencies**
   - Keep all Tailwind utility classes when updating content
   - Maintain spacing classes (mb-4, py-24, etc.)
   - Preserve hover effects (hover:text-gray-900, hover:scale-105)

### Need Help?
- Double-check HTML syntax and closing tags
- Verify all links start with either `#`, `http://`, or a relative path
- Test the page at different screen sizes
- Ensure Tailwind CDN script remains in the head section

Remember to test all changes in multiple browsers and screen sizes before deploying to production.