# WhatsBot AI Landing Page - Maintenance Guide

This guide will help you maintain and customize the WhatsBot AI landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Navigation Links](#managing-navigation-links)
3. [Setting Up Policy Pages](#setting-up-policy-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The main logo and navigation menu are located in the `<header>` section:

```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    WhatsBot AI  <!-- Change logo text here -->
</a>
```

To modify the logo:
1. Locate this code block at the top of the page
2. Replace "WhatsBot AI" with your desired text
3. Maintain the existing classes to preserve the gradient effect

### Hero Section
The main headline and subtitle are in the first `<section>` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-blue-500 mb-6">
    Chatbots para WhatsApp  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Crear chatbots con inteligencia o agentes para WhatsApp  <!-- Subtitle -->
</p>
```

To update:
1. Replace the text inside the `<h1>` tags for the main headline
2. Modify the text in the `<p>` tags for the subtitle
3. Keep the existing classes to maintain responsive design

### Understanding Tailwind Classes
Common classes used throughout the page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `md:text-[size]`: Applies styles at medium screen sizes
- `bg-[color]`: Sets background colors
- `py-[number]`: Adds padding top and bottom
- `mb-[number]`: Adds margin bottom

## Managing Navigation Links

### Main Navigation Menu
Located in the header section:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Características</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Beneficios</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors">Contacto</a>
</div>
```

To update navigation links:
1. Locate the `<a>` tags within this section
2. Modify the `href` attribute to point to your desired location
3. Update the link text between the opening and closing tags

### Call-to-Action Buttons
There are two main CTA buttons:

```html
<!-- Hero section button -->
<a href="https://inteligenciaartificialai.com/" class="inline-block bg-gradient-to-r from-purple-600 to-blue-500 text-white font-semibold px-8 py-4 rounded-full shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
    Comenzar Ahora
</a>
```

To update:
1. Change the `href` attribute to your desired URL
2. Modify the button text between the tags
3. Keep the classes to maintain styling and hover effects

## Setting Up Policy Pages

### Footer Links
Located at the bottom of the page:

```html
<div>
    <h4 class="text-white font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-sm">
        <li><a href="#" class="hover:text-white transition-colors">Términos y Condiciones</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Política de Privacidad</a></li>
        <li><a href="https://newscontetcreation.com/" target="_blank" class="hover:text-white transition-colors">News Content Creation</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create new files named `terms.html` and `privacy.html`
2. Update the href attributes:
```html
<li><a href="terms.html" class="hover:text-white transition-colors">Términos y Condiciones</a></li>
<li><a href="privacy.html" class="hover:text-white transition-colors">Política de Privacidad</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes start with either `#` for internal links or `https://` for external links
   - Verify that file names match exactly (including case) for policy pages

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the existing responsive class structure
   - Test on different screen sizes using browser dev tools

3. **Gradient Text Not Showing**
   - Ensure these classes remain together:
     ```html
     text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-blue-500
     ```

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all HTML tags are properly closed
3. Ensure Tailwind CSS and Alpine.js CDN links are working
4. Contact technical support at the email provided in the footer

Remember to always test changes in a development environment before pushing to production.
