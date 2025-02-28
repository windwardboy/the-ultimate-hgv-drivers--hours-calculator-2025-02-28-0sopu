# HGV Drivers' Hours Calculator Landing Page - Maintenance Guide

This guide will help you maintain and customize the HGV Drivers' Hours Calculator landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "DriverCompliance":
```html
<a href="/" class="text-2xl font-bold text-white hover:text-purple-400 transition-colors duration-300">
    DriverCompliance
</a>
```

2. **Navigation Items**: Update menu items in this section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
The main banner section contains:

1. **Main Heading**: Update this text:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">
    The Ultimate HGV Drivers' Hours Calculator
</h1>
```

2. **Subheading**: Modify this paragraph:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Identify & Avoid HGV Driving & Rest Time Regulations
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-4xl`: Large text (increases with number)
- `md:text-6xl`: Larger text on medium screens
- `bg-gray-900`: Dark background
- `text-gray-300`: Light gray text
- `hover:text-white`: Text becomes white on hover
- `transition-colors`: Smooth color transitions

## Managing Links

### Navigation Menu Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Replace `#section-name` with your new section ID
2. Ensure the corresponding section has matching ID:
```html
<section id="your-section-name">
```

### External Links
The main call-to-action buttons link to:
```html
<a href="https://drivercompliance.co.uk">
```

To update:
1. Replace the URL with your desired destination
2. Test the link before deploying
3. Consider adding `target="_blank"` for external links:
```html
<a href="https://your-url.com" target="_blank">
```

## Adding Privacy and Terms Pages

### Current Footer Links
Located in:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS imports
3. Maintain the same color scheme and styling classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Check media query classes (md:, lg:)
- Test on multiple screen sizes
- Common responsive classes used:
  ```html
  grid-cols-1 md:grid-cols-2 lg:grid-cols-3
  text-4xl md:text-6xl
  hidden md:flex
  ```

3. **Styling Problems**
- Ensure Tailwind CSS is properly loaded
- Check for typos in class names
- Verify class order (responsive classes should come after base classes)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test thoroughly before deploying to production.