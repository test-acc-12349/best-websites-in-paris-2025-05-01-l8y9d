# Landing Page Maintenance Guide

This guide will help you maintain and customize the Best Websites Paris landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Company Name and Branding
```html
<!-- Header Section -->
<div class="text-2xl font-bold text-gray-800">
    Best Websites Paris  <!-- Update your company name here -->
</div>
```

#### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Custom Websites For Your Business  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Professional web development services in Paris  <!-- Update subheading here -->
</p>
```

#### Features and Benefits
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-magic text-3xl"></i>  <!-- Change icon class here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Easy to Use</h3>  <!-- Update feature title -->
    <p class="text-gray-600">Intuitive interfaces...</p>  <!-- Update feature description -->
</div>
```

### Tailwind CSS Classes Explained

#### Common Layout Classes
- `container`: Centers content and sets max-width
- `mx-auto`: Centers element horizontally
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `grid`: Creates grid layout
- `grid-cols-1 md:grid-cols-3`: Single column on mobile, three columns on medium screens

#### Text Styling
- `text-xl`, `text-2xl`, etc.: Text size
- `font-bold`: Bold text
- `text-gray-600`: Text color
- `text-center`: Center align text

#### Responsive Design
Classes with `md:` or `lg:` prefix apply at specific breakpoints:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">  <!-- Increases text size on larger screens -->
```

## Fixing Broken Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Internal section link -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, use `#section-id`
2. For external links, use full URL: `https://example.com`
3. Verify all IDs match their corresponding sections

### Call-to-Action Links
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600...">
    Get Started Today
</a>
```
Replace `https://sigmaseo.io` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Check for extra spaces in IDs
   - Verify the # symbol is included in href

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Test all breakpoints

3. **Icon Not Showing**
   - Verify Font Awesome CDN link in header
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check Font Awesome [icon reference](https://fontawesome.com/icons)
- Use browser developer tools to inspect elements

Remember to always test changes across different devices and browsers before deploying to production.