# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Raleigh Custom Home Builders landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
Located near the top of the page, find this section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Build Your Dream Home in Raleigh, NC
</h1>
```
To update:
1. Locate the text between the opening and closing tags
2. Replace with your desired heading
3. Maintain the existing HTML tags

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-comments text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Consultation</h3>
    <p class="text-gray-600 leading-relaxed">
        Begin your journey with a complimentary consultation...
    </p>
</div>
```
To modify:
1. Change the icon by updating the `fa-comments` class to another FontAwesome icon
2. Update the heading text within the `<h3>` tags
3. Modify the description text within the `<p>` tags

### Tailwind CSS Classes

#### Understanding Key Classes
- `container`: Centers content and sets max-width
- `mx-auto`: Centers elements horizontally
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `grid`: Creates grid layouts
- `md:grid-cols-3`: Creates 3 columns on medium screens and larger

#### Responsive Design Classes
```html
<div class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- `text-4xl`: Default text size
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. For section links, use `#section-id`
3. For external links, use the full URL: `https://example.com`

### Footer Links
Update social media links in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-facebook"></i>
    </a>
</div>
```
Replace `#` with your social media URLs.

### Quick Links Section
Update the footer quick links:
```html
<ul class="space-y-3">
    <li><a href="#">About Us</a></li>
    <li><a href="#">Our Process</a></li>
    <li><a href="#">Portfolio</a></li>
    <li><a href="#">Testimonials</a></li>
</ul>
```
Replace `#` with appropriate URLs or page names.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<ul class="space-y-3">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in IDs
   - Verify that sections have unique IDs

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query breakpoints are correct
   - Common breakpoints:
     - `md:` = 768px
     - `lg:` = 1024px

3. **Icon Display Problems**
   - Verify FontAwesome CDN is loaded
   - Check icon class names against FontAwesome documentation
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CDN links are accessible
3. Test on multiple browsers
4. Ensure all HTML tags are properly closed

Remember to always test changes in multiple browsers and screen sizes before deploying to production.