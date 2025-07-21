# XstreamFlex Landing Page Maintenance Guide

This guide will help you maintain and customize the XstreamFlex landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**:
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">
    Xstream<span class="text-green-500">Flex</span>
</a>
```
- Change "Xstream" or "Flex" by editing the text directly
- The green color is controlled by `text-green-500`

2. **Navigation Menu Items**:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Edit text between `<a>` tags to change menu labels
- `space-x-8` controls spacing between items
- `text-gray-600` sets the default text color

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Launch Your Online Course in <span class="text-green-500">3 Days</span>
</h1>
```
- Change heading text directly
- Text sizes are responsive:
  - Mobile: `text-4xl`
  - Tablet: `sm:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 border border-gray-100">
    <!-- Icon container -->
    <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Custom Website</h3>
    <p class="text-gray-600 leading-relaxed">
        Get a professionally designed website that perfectly represents your brand and courses.
    </p>
</div>
```
- Update heading text in `<h3>` tags
- Modify description text in `<p>` tags
- Keep the class structure intact for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#how-it-works">How It Works</a>
<a href="#pricing">Pricing</a>
<a href="#blog">Blog</a>
```

To update:
1. Change the `href` value to match your section IDs
2. For external links, use full URLs:
   ```html
   <a href="https://example.com/blog">Blog</a>
   ```
3. For internal pages, use relative paths:
   ```html
   <a href="./blog.html">Blog</a>
   ```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Twitter icon -->
    </a>
</div>
```
Replace `#` with your social media URLs:
```html
<a href="https://twitter.com/yourusername" class="text-gray-400 hover:text-white transition-colors duration-300">
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="/gdpr" class="text-gray-400 hover:text-white transition-colors duration-300">GDPR</a></li>
    </ul>
</div>
```

To link properly:
1. Create your policy pages (privacy.html, terms.html)
2. Update the href attributes:
```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Styles**
   - Verify the Tailwind CDN link is working
   - Check for typos in class names
   - Ensure responsive classes (sm:, md:, lg:) are correctly ordered

2. **Navigation Links Not Working**
   - Confirm section IDs match href values
   - Check for proper URL formatting
   - Verify file paths for internal pages

3. **Responsive Design Issues**
   - Test on different screen sizes
   - Verify breakpoint classes are correct:
     - sm: 640px
     - md: 768px
     - lg: 1024px

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.