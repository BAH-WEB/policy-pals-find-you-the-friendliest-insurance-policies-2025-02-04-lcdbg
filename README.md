# PolicyPals Landing Page Maintenance Guide

This guide will help you maintain and customize the PolicyPals insurance landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-md z-50 border-b border-gray-800">
```
To modify the header:
- Company name: Look for `PolicyPals` within the `<a>` tag
- Navigation items: Located in `<div class="hidden md:flex space-x-8">`
- Button text: Find `Get Started` in the header's last `<a>` tag

Key Tailwind classes explained:
- `fixed`: Keeps header at top of page
- `w-full`: Full width
- `bg-gray-900/95`: Dark background with 95% opacity
- `backdrop-blur-md`: Adds blur effect
- `z-50`: Ensures header stays above other content

### Hero Section
To update the main headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
- Replace text between opening and closing tags
- Maintain existing classes for responsive design:
  - `text-4xl`: Base size on mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:shadow-xl hover:shadow-purple-500/10 transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-user-check text-2xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-400 leading-relaxed">
        [Feature description here]
    </p>
</div>
```
To modify:
1. Change icon: Update `fa-user-check` to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Replace text in `<h3>` tag
3. Update description: Modify text in `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Replace `#section-name` with your desired anchor
2. Ensure corresponding sections have matching IDs
3. For external links, use full URLs: `href="https://example.com"`

### Call-to-Action Buttons
```html
<a href="https://PolicyPals.Co.Uk" class="px-8 py-4 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">
    Get Started Now
</a>
```
Replace `https://PolicyPals.Co.Uk` with your actual URL

### Social Media Links
Located in footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-purple-400">
        <i class="fab fa-twitter text-xl"></i>
    </a>
</div>
```
Replace `#` with actual social media profile URLs

## Linking Privacy and Terms Pages

Add these links to the footer section:
```html
<!-- Add this to the Quick Links column in footer -->
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4 text-gray-400">
        <li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

For consistency:
1. Place new links in footer's grid system
2. Maintain existing styling classes
3. Create corresponding privacy.html and terms.html files
4. Ensure files are in the same directory as index.html

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design**
   - Check media query classes (md:, lg:) are intact
   - Verify Tailwind CSS link is working
   - Keep original responsive classes when updating

2. **Missing Icons**
   - Confirm Font Awesome CSS is properly linked
   - Check icon class names against Font Awesome documentation
   - Ensure proper prefix (fas, fab, far) is used

3. **Navigation Links Not Working**
   - Verify section IDs match href attributes
   - Check for typos in href values
   - Ensure smooth scroll class remains on html tag

Remember:
- Always test changes across different screen sizes
- Maintain the existing color scheme using Tailwind's color classes
- Back up files before making significant changes
- Use browser developer tools to inspect elements when troubleshooting

Need more help? Contact support@policypals.co.uk