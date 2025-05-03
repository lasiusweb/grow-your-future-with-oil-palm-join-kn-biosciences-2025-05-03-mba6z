# KN Biosciences Landing Page - Maintenance Guide

This guide will help you maintain and customize the KN Biosciences oil palm cultivation landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Name:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-green-400 to-emerald-600 bg-clip-text text-transparent">
    KN Biosciences  <!-- Edit this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Edit menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtitle:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Grow Your Future with Oil Palm: Join KN Biosciences  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Transform your land and life...  <!-- Subtitle text -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Large text size (mobile)
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Bottom margin spacing
- `text-gray-300`: Light gray text color

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Ensure section IDs match these href values
2. For external pages, replace with full URLs:
```html
<a href="https://example.com/features">Features</a>
```

### Contact Section Links
Update email address in two locations:
```html
<a href="mailto:oilpalm@knbiosciences.in">Contact Us Now</a>
<p class="mt-8 text-gray-400">Email: oilpalm@knbiosciences.in</p>
```

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links in footer:
```html
<div class="mt-4 space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
```

### Maintaining Consistent Styling
Copy these classes to new links for consistent appearance:
- `hover:text-white`: White text on hover
- `transition-colors`: Smooth color transition
- `duration-300`: Transition timing

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly (case-sensitive)
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Verify mobile classes are present:
   ```html
   <div class="text-4xl md:text-5xl lg:text-6xl">
   ```
   - Always include mobile size first, then larger screens

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
   ```html
   bg-gradient-to-r from-green-400 to-emerald-600 bg-clip-text text-transparent
   ```

### Tips for Testing
1. Test all links after updating
2. View page at different screen sizes
3. Check hover effects on all interactive elements
4. Verify email links open mail client correctly

Remember to:
- Back up files before making changes
- Test changes in multiple browsers
- Keep consistent styling across all pages
- Maintain the same color scheme (green/emerald gradients)

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)