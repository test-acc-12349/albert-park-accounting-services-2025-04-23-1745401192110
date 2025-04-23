# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**:
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park    <!-- Change this text -->
</a>
```

2. **Navigation Menu Items**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>    <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>    <!-- Change menu text here -->
    <a href="#contact">Contact</a>      <!-- Change menu text here -->
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight">
    Your financial success is our bottom line    <!-- Change headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">
    Professional accounting services...    <!-- Change subtext -->
</p>
```

### Styling Tips for Beginners
- Don't remove `md:` or `lg:` prefixes - they control responsive design
- Keep the existing class structure (e.g., `text-5xl md:text-6xl lg:text-7xl`)
- Common Tailwind classes used:
  - `text-{size}`: Controls font size
  - `mb-{number}`: Adds margin bottom
  - `py-{number}`: Adds padding top and bottom
  - `px-{number}`: Adds padding left and right

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com" class="...">
    Get Started    <!-- Update both href and text -->
</a>
```

### Updating Links Step-by-Step
1. Internal Links (sections on same page):
   ```html
   <!-- Keep the # symbol for same-page navigation -->
   <a href="#sectionname">Section Name</a>
   ```

2. External Links:
   ```html
   <!-- Replace with your actual URL -->
   <a href="https://your-actual-website.com">Link Text</a>
   ```

3. Email Links:
   ```html
   <!-- Update with your actual email -->
   <a href="mailto:support@example.com">Contact Us</a>
   ```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer's Company section:

```html
<div>
    <h4 class="font-semibold mb-4">Company</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
        <!-- Add these new links -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use consistent styling:
```html
<!-- privacy.html or terms.html template -->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy the same head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100">
    <!-- Copy the header from index.html -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy the footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in href values
   - Verify that # symbol is included for internal links

2. **Responsive Design Issues**
   - Don't remove responsive prefixes (sm:, md:, lg:)
   - Keep the existing class order
   - Test on different screen sizes

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Navigation Menu Not Showing on Mobile**
   - The `hidden md:flex` class intentionally hides the menu on mobile
   - Don't remove unless implementing a mobile menu alternative

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Keep the existing class structure intact
- Maintain consistent styling across all pages