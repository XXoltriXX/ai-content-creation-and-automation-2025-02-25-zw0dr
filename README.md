# Antikythera Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Antikythera AI landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<header class="fixed w-full z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800">
    <nav class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
            <a href="/" class="text-2xl font-bold text-purple-500">Antikythera</a>
            <!-- Navigation items -->
        </div>
    </nav>
</header>
```

To modify:
- Company name: Replace "Antikythera" with your company name
- Header background: Adjust `bg-gray-900/95` for different colors/opacity
- Border color: Modify `border-gray-800` to match your theme

### Hero Section
The main banner section contains:

```html
<section class="relative min-h-screen flex items-center justify-center py-24 px-6">
    <div class="relative container mx-auto text-center max-w-4xl">
        <h1 class="text-4xl md:text-6xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">AI Content Creation and Automation</h1>
        <p class="text-xl md:text-2xl mb-12 text-gray-300">Best AI tools for content Creation</p>
        <!-- CTA Button -->
    </div>
</section>
```

To customize:
- Heading: Replace the h1 text
- Gradient colors: Modify `from-purple-400 to-pink-600`
- Subheading: Update the paragraph text
- Background image: Change the URL in `bg-[url('...')`

### Responsive Design Classes
Important Tailwind classes explained:
- `md:text-6xl`: Larger text on medium screens and up
- `text-4xl`: Default text size on mobile
- `max-w-4xl`: Maximum width constraint
- `px-6`: Horizontal padding
- `py-24`: Vertical padding

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-purple-400 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-purple-400 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Ensure the target section has a matching `id` attribute

### External Links
Current external links:
```html
<a href="https://www.antikythera.co.za" class="inline-block bg-purple-600 hover:bg-purple-700 text-white font-semibold px-8 py-4 rounded-lg">Get Started Now</a>
```

To modify:
1. Replace `https://www.antikythera.co.za` with your desired URL
2. Test the link to ensure it works
3. Consider adding `target="_blank"` for external links

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Test on multiple screen sizes
   - Ensure `md:` prefixed classes are appropriate
   - Check that the viewport meta tag is present

3. **Style Inconsistencies**
   - Maintain consistent color classes (e.g., `purple-500`)
   - Keep padding/margin patterns uniform
   - Use the same hover effects across similar elements

4. **Missing Images**
   - Verify image URLs are correct
   - Ensure images are uploaded to the correct location
   - Consider using relative paths for local images

Remember to:
- Test all changes in multiple browsers
- Validate your HTML using W3C validator
- Keep backups before making significant changes
- Maintain consistent spacing and indentation

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)