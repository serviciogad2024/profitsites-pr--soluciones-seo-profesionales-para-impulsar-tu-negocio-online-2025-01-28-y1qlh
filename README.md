# ProfitSites PR Landing Page - Maintenance Guide

This guide will help you maintain and customize the ProfitSites PR landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu:

```html
<div class="text-2xl font-bold text-blue-600">ProfitSites PR</div>
```

To change the company name:
1. Locate this div in the header section
2. Replace "ProfitSites PR" with your desired text
3. Adjust text size using these Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and description are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
    ProfitSites PR: Soluciones SEO Profesionales para Impulsar tu Negocio Online
</h1>
```

To update:
1. Change the text between the `<h1>` tags
2. Maintain the responsive text sizes:
   - `text-4xl`: mobile devices
   - `md:text-5xl`: medium screens
   - `lg:text-6xl`: large screens

### Services Cards
Each service card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-chart-line text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Estrategias SEO Personalizadas</h3>
    <p class="text-gray-600">Desarrollamos estrategias únicas...</p>
</div>
```

To modify:
1. Change the icon by updating the `fa-chart-line` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#servicios" class="hover:text-blue-600 transition-colors duration-300">Servicios</a>
    <a href="#beneficios" class="hover:text-blue-600 transition-colors duration-300">Beneficios</a>
    <a href="#faq" class="hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contacto" class="hover:text-blue-600 transition-colors duration-300">Contacto</a>
</div>
```

To update:
1. The `href="#servicios"` links to the section with `id="servicios"`
2. To link to external pages, replace with full URLs: `href="https://example.com"`
3. For internal pages, use relative paths: `href="about.html"`

### Call-to-Action Button
The main CTA button currently links to:

```html
<a href="https://marketingdigitalfinanzas.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Impulsa tu Negocio Ahora
</a>
```

To update:
1. Replace the URL in `href`
2. Modify button text between the `<a>` tags
3. Adjust colors using Tailwind classes:
   - Background: `bg-blue-600`
   - Text: `text-white`

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Términos y Condiciones</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Términos y Condiciones</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on different screen sizes using browser dev tools

3. **Icon Not Showing**
   - Verify Font Awesome CSS is properly linked
   - Check icon class names on [Font Awesome](https://fontawesome.com/icons)
   - Ensure internet connection for CDN access

4. **Styling Problems**
   - Don't remove `transition-colors duration-300` from hover effects
   - Maintain the hierarchy of Tailwind classes
   - Keep responsive classes (`md:`, `lg:`) after base classes

Remember to always test changes in multiple browsers and screen sizes before publishing updates.