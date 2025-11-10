# Pogiso's Tours Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your luxury chauffeur service landing page.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Troubleshooting Guide](#troubleshooting-guide)
8. [Best Practices](#best-practices)

---

## Quick Start Overview

This landing page is built using:
- **HTML5** - The structure and content
- **Tailwind CSS** - For styling and responsive design
- **Font Awesome Icons** - For visual elements
- **Material Symbols** - For modern icon designs
- **Vanilla JavaScript** - For interactive features (mobile menu, FAQ accordion)

**Key Color Scheme:**
- Primary Purple: `#5B4BFF`
- Accent Green: `#00E5A8`
- Dark Background: `#111827` (gray-900)

---

## Understanding the Page Structure

### Main Sections of Your Landing Page

```
1. Header Navigation (Sticky)
   ├── Logo
   ├── Desktop Menu Links
   ├── CTA Button
   └── Mobile Menu (Hidden on desktop)

2. Hero Section
   ├── Main Headline
   ├── Subheading
   ├── Feature Highlights (3 boxes)
   ├── CTA Buttons
   └── Trust Indicators (Stats)

3. Features Section
   ├── Section Title
   └── 3 Feature Cards (Lightning-Fast Checkout, Bank-Level Security, Instant Digital Vouchers)

4. Benefits Section
   ├── Section Title
   ├── 3 Benefit Cards (Save Money, Travel Smarter, Gift Luxury)
   └── 2 Additional Benefit Boxes (Premium Service, Safety & Reliability)

5. Testimonials Section
   ├── Section Title
   └── 4 Testimonial Cards with Star Ratings

6. About Us Section
   ├── Company History
   ├── Mission Statement
   └── Company Statistics

7. FAQ Section
   ├── Section Title
   └── 5 Expandable FAQ Items

8. Contact Form Section
   ├── Contact Form with Web3Forms Integration
   └── Email Contact Info

9. Footer
   ├── Brand Information
   ├── Quick Links
   ├── Legal Links
   ├── Contact Information
   └── Social Media Links
```

---

## Updating Text Content

### 1. Changing the Header/Navigation

**Location:** Lines 87-129 (Header Navigation Section)

**Current Code:**
```html
<!-- Logo -->
<div class="flex items-center space-x-2">
    <div class="w-10 h-10 rounded-lg bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] flex items-center justify-center">
        <span class="material-symbols-rounded text-white text-2xl">local_taxi</span>
    </div>
    <span class="text-2xl font-bold text-white hidden sm:inline">Pogiso's</span>
</div>
```

**How to Change:**
1. Open your `index.html` file in a text editor (VS Code, Notepad++, or even Notepad)
2. Find the text `Pogiso's` around line 102
3. Replace it with your company name
4. **Example:** Change `Pogiso's` to `Luxury Rides` or `Elite Travel Co.`

```html
<!-- BEFORE -->
<span class="text-2xl font-bold text-white hidden sm:inline">Pogiso's</span>

<!-- AFTER -->
<span class="text-2xl font-bold text-white hidden sm:inline">Elite Travel Co.</span>
```

**What `hidden sm:inline` means:**
- `hidden` = Hide this text on small screens (phones)
- `sm:inline` = Show this text on small screens and larger

---

### 2. Updating Navigation Menu Links

**Location:** Lines 105-108 (Desktop Menu)

**Current Code:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Benefits</a>
    <a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Testimonials</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">FAQ</a>
</div>
```

**How to Change Menu Items:**

**To rename a menu item:**
1. Find the text you want to change (e.g., "Features")
2. Replace it with your new text
3. **Example:** Change "Features" to "Our Services"

```html
<!-- BEFORE -->
<a href="#features" class="...">Features</a>

<!-- AFTER -->
<a href="#services" class="...">Our Services</a>
```

**To add a new menu item:**
1. Add a new line after an existing menu item
2. Copy the structure of an existing link
3. Change the `href` and text

```html
<!-- Add this new line -->
<a href="#pricing" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Pricing</a>
```

**To remove a menu item:**
1. Delete the entire `<a>` tag for that item

---

### 3. Updating the Hero Section Main Headline

**Location:** Lines 146-151 (Hero Heading)

**Current Code:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold mb-6 tracking-tight leading-tight">
    <span class="block text-white mb-4">Ride. Relax. Repeat.</span>
    <span class="gradient-text">Premium Travel Starts Here</span>
</h1>
```

**How to Change:**
1. Replace `Ride. Relax. Repeat.` with your main headline
2. Replace `Premium Travel Starts Here` with your secondary headline

```html
<!-- BEFORE -->
<span class="block text-white mb-4">Ride. Relax. Repeat.</span>
<span class="gradient-text">Premium Travel Starts Here</span>

<!-- AFTER -->
<span class="block text-white mb-4">Your Journey, Your Way.</span>
<span class="gradient-text">Luxury Travel Made Simple</span>
```

**Understanding the styling:**
- `text-5xl sm:text-6xl lg:text-7xl` = Responsive text sizes (smaller on mobile, larger on desktop)
- `text-white` = White text color
- `gradient-text` = Special gradient effect (purple to green)

---

### 4. Updating the Hero Subheading

**Location:** Lines 154-157 (Hero Subheading)

**Current Code:**
```html
<p class="text-lg sm:text-xl text-gray-300 mb-8 max-w-2xl mx-auto font-light leading-relaxed">
    Experience the pinnacle of luxury travel with our exclusive chauffeur packages and premium travel essentials. Designed for those who demand excellence in every journey.
</p>
```

**How to Change:**
1. Replace the paragraph text with your own description
2. Keep the HTML tags the same

```html
<!-- BEFORE -->
<p class="text-lg sm:text-xl text-gray-300 mb-8 max-w-2xl mx-auto font-light leading-relaxed">
    Experience the pinnacle of luxury travel with our exclusive chauffeur packages and premium travel essentials. Designed for those who demand excellence in every journey.
</p>

<!-- AFTER -->
<p class="text-lg sm:text-xl text-gray-300 mb-8 max-w-2xl mx-auto font-light leading-relaxed">
    Premium transportation services tailored to your needs. Book in minutes, travel in style, arrive in comfort.
</p>
```

---

### 5. Updating Feature Highlights (3 Boxes in Hero)

**Location:** Lines 160-177 (Feature Highlight Boxes)

**Current Code:**
```html
<div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-12 max-w-2xl mx-auto">
    <div class="flex items-center justify-center space-x-2 bg-gray-800 bg-opacity-50 rounded-lg px-4 py-3 border border-gray-700">
        <span class="material-symbols-rounded text-[#00E5A8]">check_circle</span>
        <span class="text-sm font-light">Fast Checkout</span>
    </div>
    <!-- More boxes follow -->
</div>
```

**How to Change:**
1. Replace the text (e.g., "Fast Checkout") with your own feature
2. To change the icon, replace `check_circle` with another [Material Symbol](https://fonts.google.com/icons?icon.set=Material+Symbols)

```html
<!-- BEFORE -->
<span class="text-sm font-light">Fast Checkout</span>

<!-- AFTER -->
<span class="text-sm font-light">Quick Booking</span>
```

**Common Icon Names:**
- `check_circle` - Checkmark in circle
- `shield` - Shield icon
- `flash_on` - Lightning bolt
- `star` - Star
- `verified_user` - Verified user
- `card_giftcard` - Gift card

---

### 6. Updating Feature Cards (Full Features Section)

**Location:** Lines 220-300 (Three Feature Cards)

**Current Code (First Feature Card):**
```html
<div class="card-hover bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-[#5B4BFF]">
    <div class="w-16 h-16 rounded-lg bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] flex items-center justify-center mb-6">
        <span class="material-symbols-rounded text-white text-3xl">lightning_bolt</span>
    </div>
    <h3 class="text-2xl font-bold mb-4">Lightning-Fast Checkout</h3>
    <p class="text-gray-400 font-light leading-relaxed mb-4">
        Complete your luxury travel booking in under 60 seconds...
    </p>
    <ul class="space-y-2 text-sm font-light text-gray-300">
        <li class="flex items-center space-x-2">
            <span class="material-symbols-rounded text-[#00E5A8] text-xl">check</span>
            <span>One-click booking</span>
        </li>
        <!-- More list items -->
    </ul>
</div>
```

**How to Change:**

**Step 1: Change the Title**
```html
<!-- BEFORE -->
<h3 class="text-2xl font-bold mb-4">Lightning-Fast Checkout</h3>

<!-- AFTER -->
<h3 class="text-2xl font-bold mb-4">Instant Booking System</h3>
```

**Step 2: Change the Description**
```html
<!-- BEFORE -->
<p class="text-gray-400 font-light leading-relaxed mb-4">
    Complete your luxury travel booking in under 60 seconds...
</p>

<!-- AFTER -->
<p class="text-gray-400 font-light leading-relaxed mb-4">
    Reserve your premium vehicle in seconds with our streamlined booking process.
</p>
```

**Step 3: Change the Bullet Points**
```html
<!-- BEFORE -->
<li class="flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-xl">check</span>
    <span>One-click booking</span>
</li>

<!-- AFTER -->
<li class="flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-xl">check</span>
    <span>Mobile-friendly interface</span>
</li>
```

---

### 7. Updating Testimonials

**Location:** Lines 500-600 (Testimonials Section)

**Current Code (First Testimonial):**
```html
<div class="card-hover bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-[#5B4BFF]">
    <div class="flex items-center mb-4">
        <div class="flex space-x-1">
            <span class="material-symbols-rounded text-[#FFD700] text-xl">star</span>
            <!-- 5 stars total -->
        </div>
    </div>
    <p class="text-gray-300 font-light leading-relaxed mb-6">
        "Pogiso's Tours transformed my business travel experience..."
    </p>
    <div class="flex items-center space-x-4">
        <div class="w-12 h-12 rounded-full bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] flex items-center justify-center">
            <span class="text-white font-bold">JM</span>
        </div>
        <div>
            <p class="font-bold text-white">James Mitchell</p>
            <p class="text-sm text-gray-400 font-light">CEO, TechVision Inc.</p>
        </div>
    </div>
</div>
```

**How to Change a Testimonial:**

**Step 1: Change the Quote Text**
```html
<!-- BEFORE -->
<p class="text-gray-300 font-light leading-relaxed mb-6">
    "Pogiso's Tours transformed my business travel experience..."
</p>

<!-- AFTER -->
<p class="text-gray-300 font-light leading-relaxed mb-6">
    "Best luxury service I've ever experienced. Highly recommended!"
</p>
```

**Step 2: Change the Customer Initials**
```html
<!-- BEFORE -->
<span class="text-white font-bold">JM</span>

<!-- AFTER -->
<span class="text-white font-bold">AB</span>
```

**Step 3: Change the Customer Name**
```html
<!-- BEFORE -->
<p class="font-bold text-white">James Mitchell</p>
<p class="text-sm text-gray-400 font-light">CEO, TechVision Inc.</p>

<!-- AFTER -->
<p class="font-bold text-white">Amanda Brown</p>
<p class="text-sm text-gray-400 font-light">Marketing Director, Creative Agency</p>
```

---

### 8. Updating Company Information (About Section)

**Location:** Lines 620-680 (About Us Section)

**Current Code:**
```html
<p class="text-gray-300 font-light leading-relaxed text-lg mb-6">
    Founded in 2015, Pogiso's Tours emerged from a simple yet powerful vision...
</p>
```

**How to Change:**
1. Replace the entire paragraph with your company's story

```html
<!-- BEFORE -->
<p class="text-gray-300 font-light leading-relaxed text-lg mb-6">
    Founded in 2015, Pogiso's Tours emerged from a simple yet powerful vision...
</p>

<!-- AFTER -->
<p class="text-gray-300 font-light leading-relaxed text-lg mb-6">
    Founded in 2020, Elite Travel Co. has been providing premium transportation services to discerning clients across the region...
</p>
```

---

### 9. Updating Statistics (About Section)

**Location:** Lines 705-730 (Stats Boxes)

**Current Code:**
```html
<div class="grid grid-cols-2 md:grid-cols-4 gap-6">
    <div class="text-center bg-gray-800 rounded-lg p-6 border border-gray-700">
        <p class="text-3xl font-bold text-[#5B4BFF] mb-2">10K+</p>
        <p class="text-gray-400 font-light text-sm">Satisfied Clients</p>
    </div>
    <!-- More stat boxes -->
</div>
```

**How to Change:**
```html
<!-- BEFORE -->
<p class="text-3xl font-bold text-[#5B4BFF] mb-2">10K+</p>
<p class="text-gray-400 font-light text-sm">Satisfied Clients</p>

<!-- AFTER -->
<p class="text-3xl font-bold text-[#5B4BFF] mb-2">5K+</p>
<p class="text-gray-400 font-light text-sm">Happy Customers</p>
```

---

### 10. Updating FAQ Questions and Answers

**Location:** Lines 760-850 (FAQ Section)

**Current Code (First FAQ Item):**
```html
<div class="faq-item bg-gray-900 rounded-xl border border-gray-700 overflow-hidden">
    <button class="faq-question w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-800 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-bold text-white pr-4">How far in advance should I book a chauffeur service?</span>
        <span class="faq-icon material-symbols-rounded flex-shrink-0 text-[#5B4BFF] transition-transform duration-300">expand_more</span>
    </button>
    <div class="faq-answer hidden px-8 py-6 bg-gray-800 bg-opacity-50 border-t border-gray-700">
        <p class="text-gray-300 font-light leading-relaxed">
            We recommend booking at least 24-48 hours in advance...
        </p>
    </div>
</div>
```

**How to Change:**

**Step 1: Change the Question**
```html
<!-- BEFORE -->
<span class="text-lg font-bold text-white pr-4">How far in advance should I book a chauffeur service?</span>

<!-- AFTER -->
<span class="text-lg font-bold text-white pr-4">What types of vehicles do you offer?</span>
```

**Step 2: Change the Answer**
```html
<!-- BEFORE -->
<p class="text-gray-300 font-light leading-relaxed">
    We recommend booking at least 24-48 hours in advance...
</p>

<!-- AFTER -->
<p class="text-gray-300 font-light leading-relaxed">
    We offer a range of luxury vehicles including sedans, SUVs, and limousines to suit your needs...
</p>
```

---

### 11. Updating Footer Information

**Location:** Lines 900-1000 (Footer Section)

**Current Code:**
```html
<div>
    <div class="flex items-center space-x-2 mb-4">
        <div class="w-10 h-10 rounded-lg bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] flex items-center justify-center">
            <span class="material-symbols-rounded text-white text-2xl">local_taxi</span>
        </div>
        <span class="text-xl font-bold text-white">Pogiso's Tours</span>
    </div>
    <p class="text-gray-400 font-light leading-relaxed text-sm">
        Premium luxury chauffeur services and travel essentials for the discerning traveler.
    </p>
</div>
```

**How to Change:**
```html
<!-- BEFORE -->
<span class="text-xl font-bold text-white">Pogiso's Tours</span>

<!-- AFTER -->
<span class="text-xl font-bold text-white">Elite Travel Co.</span>
```

**Updating Footer Contact Information:**

**Location:** Lines 970-980 (Contact Info in Footer)

```html
<!-- BEFORE -->
<p class="text-gray-400 font-light flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#5B4BFF]">mail</span>
    <a href="mailto:info@pogisostours.co.za" class="hover:text-[#5B4BFF] transition-colors duration-300">info@pogisostours.co.za</a>
</p>
<p class="text-gray-400 font-light flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#5B4BFF]">phone</span>
    <span>+27 (0) 11 XXX XXXX</span>
</p>

<!-- AFTER -->
<p class="text-gray-400 font-light flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#5B4BFF]">mail</span>
    <a href="mailto:hello@elitetravel.com" class="hover:text-[#5B4BFF] transition-colors duration-300">hello@elitetravel.com</a>
</p>
<p class="text-gray-400 font-light flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#5B4BFF]">phone</span>
    <span>+1 (555) 123-4567</span>
</p>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS Basics

Tailwind CSS uses short, descriptive class names instead of writing custom CSS. Here are the most common ones used in this landing page:

### 1. Text Sizing and Colors

**Text Size Classes:**
```html
text-sm      = Small text (12px)
text-base    = Base text (16px)
text-lg      = Large text (18px)
text-xl      = Extra large (20px)
text-2xl     = 2x large (24px)
text-3xl     = 3x large (30px)
text-4xl     = 4x large (36px)
text-5xl     = 5x large (48px)
text-6xl     = 6x large (60px)
text-7xl     = 7x large (84px)
```

**How to use:**
```html
<!-- BEFORE: Small text -->
<p class="text-sm">Small paragraph</p>

<!-- AFTER: Larger text -->
<p class="text-lg">Larger paragraph</p>
```

**Text Color Classes:**
```html
text-white       = White text
text-gray-300    = Light gray text
text-gray-400    = Medium gray text
text-gray-900    = Dark gray text
text-[#5B4BFF]   = Custom purple color
text-[#00E5A8]   = Custom green color
```

**How to use:**
```html
<!-- BEFORE: Gray text -->
<p class="text-gray-400">Gray paragraph</p>

<!-- AFTER: White text -->
<p class="text-white">White paragraph</p>
```

---

### 2. Background Colors

**Background Color Classes:**
```html
bg-gray-900      = Dark background
bg-gray-800      = Medium-dark background
bg-white         = White background
bg-[#5B4BFF]     = Custom purple background
bg-[#00E5A8]     = Custom green background
```

**How to use:**
```html
<!-- BEFORE: Gray background -->
<div class="bg-gray-800">Content</div>

<!-- AFTER: Purple background -->
<div class="bg-[#5B4BFF]">Content</div>
```

---

### 3. Padding and Margins

**Padding Classes (Internal Spacing):**
```html
p-2      = 8px padding on all sides
p-4      = 16px padding on all sides
p-6      = 24px padding on all sides
p-8      = 32px padding on all sides
px-4     = 16px padding on left and right only
py-3     = 12px padding on top and bottom only
```

**Margin Classes (External Spacing):**
```html
m-2      = 8px margin on all sides
m-4      = 16px margin on all sides
m-6      = 24px margin on all sides
m-8      = 32px margin on all sides
mx-auto  = Center element horizontally
mb-4     = 16px margin on bottom
mt-4     = 16px margin on top
```

**How to use:**
```html
<!-- BEFORE: Small padding -->
<div class="p-4">Content</div>

<!-- AFTER: Larger padding -->
<div class="p-8">Content</div>
```

---

### 4. Responsive Design Classes

The page uses responsive design to work on all screen sizes. These prefixes control when styles apply:

```html
sm:     = Small screens and up (640px)
md:     = Medium screens and up (768px)
lg:     = Large screens and up (1024px)
```

**How to use:**
```html
<!-- This text is hidden on small screens, shown on medium screens and up -->
<span class="hidden sm:inline">Pogiso's</span>

<!-- This is 3 columns on large screens, 2 columns on medium, 1 column on small -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

**Example: Making a button responsive:**
```html
<!-- BEFORE: Same size on all screens -->
<button class="px-6 py-2 text-lg">Book Now</button>

<!-- AFTER: Smaller on mobile, larger on desktop -->
<button class="px-4 py-2 text-sm sm:px-6 sm:py-3 sm:text-lg">Book Now</button>
```

---

### 5. Flexbox and Grid Layouts

**Flexbox (Linear Layout):**
```html
flex              = Display as flex container
items-center      = Vertically center items
justify-center    = Horizontally center items
space-x-2         = 8px gap between items horizontally
space-y-4         = 16px gap between items vertically
```

**Grid (Multi-column Layout):**
```html
grid                           = Display as grid
grid-cols-1                    = 1 column
grid-cols-2                    = 2 columns
grid-cols-3                    = 3 columns
md:grid-cols-2 lg:grid-cols-3  = 2 columns on medium, 3 on large
gap-8                          = 32px gap between grid items
```

**How to use:**
```html
<!-- BEFORE: Single column -->
<div class="grid grid-cols-1 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>

<!-- AFTER: Responsive columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

---

### 6. Border and Rounded Corners

**Border Classes:**
```html
border           = 1px border
border-gray-700  = Border with gray color
border-t         = Border on top only
border-b         = Border on bottom only
rounded-lg       = Slightly rounded corners
rounded-xl       = More rounded corners
```

**How to use:**
```html
<!-- BEFORE: No border -->
<div class="bg-gray-900 p-8">Content</div>

<!-- AFTER: With border -->
<div class="bg-gray-900 p-8 border border-gray-700 rounded-xl">Content</div>
```

---

### 7. Opacity and Effects

**Opacity Classes:**
```html
opacity-10       = 10% opacity (very transparent)
opacity-20       = 20% opacity
opacity-50       = 50% opacity (half transparent)
opacity-100      = 100% opacity (fully visible)
```

**How to use:**
```html
<!-- BEFORE: Fully visible -->
<div class="bg-gray-800">Content</div>

<!-- AFTER: Semi-transparent -->
<div class="bg-gray-800 opacity-50">Content</div>
```

---

### 8. Hover and Transition Effects

**Hover Classes:**
```html
hover:text-white           = Change text to white on hover
hover:bg-gray-800          = Change background to gray-800 on hover
hover:border-[#5B4BFF]     = Change border to purple on hover
transition-colors          = Smooth color transition
duration-300               = 300ms transition duration
```

**How to use:**
```html
<!-- BEFORE: No hover effect -->
<a href="#" class="text-gray-400">Link</a>

<!-- AFTER: With hover effect -->
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Link</a>
```

---

### 9. Practical Example: Styling a Card

**Original Card:**
```html
<div class="card-hover bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-[#5B4BFF]">
    <h3 class="text-2xl font-bold mb-4">Feature Title</h3>
    <p class="text-gray-400 font-light leading-relaxed">Feature description</p>
</div>
```

**Breaking down the classes:**
- `card-hover` = Custom hover animation
- `bg-gray-900` = Dark background
- `rounded-xl` = Rounded corners
- `p-8` = 32px padding
- `border border-gray-700` = Gray border
- `hover:border-[#5B4BFF]` = Purple border on hover

**To make the card more prominent:**
```html
<!-- BEFORE -->
<div class="card-hover bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-[#5B4BFF]">

<!-- AFTER: Larger, more spacing -->
<div class="card-hover bg-gray-900 rounded-xl p-12 border-2 border-gray-600 hover:border-[#5B4BFF]">
```

---

### 10. Color Scheme Customization

To change the entire color scheme, find and replace these color values:

**Primary Purple `#5B4BFF`:**
- Used for main buttons, headings, and accents
- Find all instances and replace with your brand color

```html
<!-- BEFORE: Purple -->
<button class="bg-[#5B4BFF] text-white">Book Now</button>

<!-- AFTER: Blue -->
<button class="bg-[#0066FF] text-white">Book Now</button>
```

**Accent Green `#00E5A8`:**
- Used for highlights and secondary accents
- Find and replace for consistency

```html
<!-- BEFORE: Green -->
<span class="text-[#00E5A8]">Check</span>

<!-- AFTER: Orange -->
<span class="text-[#FF8C00]">Check</span>
```

**Quick Find & Replace Guide:**
1. Open your HTML file
2. Use Ctrl+H (Cmd+H on Mac) to open Find & Replace
3. Find: `#5B4BFF` Replace with: `#YourColorCode`
4. Find: `#00E5A8` Replace with: `#YourColorCode`

---

## Fixing and Managing Links

### Understanding Link Types

There are three types of links in this landing page:

1. **Internal Links** - Link to sections within the same page (using `#`)
2. **External Links** - Link to other websites
3. **Page Links** - Link to other HTML files on your site

---

### 1. Navigation Links (Internal - Same Page)

**Location:** Lines 105-108 (Desktop Menu)

**Current Code:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">FAQ</a>
```

**How these work:**
- `href="#features"` means "jump to the section with `id="features"`"
- The `#` symbol means "look on this page"

**To verify links are working:**

1. Find the corresponding section ID on the page
2. Search for `id="features"` in the HTML
3. You should find it around line 220

```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Matching section -->
<section id="features" class="py-24 bg-gray-800 bg-opacity-50 border-t border-b border-gray-700">
```

**If a link is broken:**
1. Check that the `id` on the section matches the `href` in the link
2. Make sure the `id` name is exactly the same (case-sensitive)

```html
<!-- WRONG: These don't match -->
<a href="#Features">Features</a>  <!-- Link says "Features" with capital F -->
<section id="features">           <!-- Section says "features" with lowercase f -->

<!-- CORRECT: These match -->
<a href="#features">Features</a>
<section id="features">
```

---

### 2. Booking Button Links (External)

**Location:** Lines 112-114, 182-186, 880-885 (Multiple CTA Buttons)

**Current Code:**
```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-6 py-2 rounded-lg font-bold text-sm transition-all duration-300 hover:shadow-lg inline-block">
    Book Now
</a>
```

**How to Change the Booking Link:**

1. Find `https://pogisostours.co.za/booking`
2. Replace it with your booking page URL

```html
<!-- BEFORE -->
<a href="https://pogisostours.co.za/booking">Book Now</a>

<!-- AFTER -->
<a href="https://yourbookingsite.com/booking">Book Now</a>
```

**Important:** Always include `https://` or `http://` when linking to external websites.

---

### 3. Mobile Menu Links

**Location:** Lines 127-136 (Mobile Menu)

**Current Code:**
```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-gray-800 border-b border-gray-700 md:hidden">
    <div class="max-w-7xl mx-auto px-4 py-4 flex flex-col space-y-4">
        <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-light py-2">Features</a>
        <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-light py-2">Benefits</a>
        <a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300 font-light py-2">Testimonials</a>
        <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-light py-2">FAQ</a>
        <a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-6 py-3 rounded-lg font-bold text-center transition-all duration-300 hover:shadow-lg block">
            Book Now
        </a>
    </div>
</div>
```

**Important:** Keep mobile menu links synchronized with desktop menu. If you change a desktop menu link, make the same change in the mobile menu.

---

### 4. Footer Links

**Location:** Lines 920-960 (Footer Quick Links Section)

**Current Code:**
```html
<div>
    <h3 class="font-bold text-white mb-4 text-lg">Quick Links</h3>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Benefits</a></li>
        <li><a href="#testimonials" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Testimonials</a></li>
        <li><a href="#faq" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">FAQ</a></li>
    </ul>
</div>
```

**How to update:**
- These should match your navigation menu links
- If you add a new section, add it here too

---

### 5. Email Links

**Location:** Lines 975-978 (Footer Contact Email)

**Current Code:**
```html
<p class="text-gray-400 font-light flex items-center space-x-2">
    <span class="material-symbols-rounded text-[#5B4BFF]">mail</span>
    <a href="mailto:info@pogisostours.co.za" class="hover:text-[#5B4BFF] transition-colors duration-300">info@pogisostours.co.za</a>
</p>
```

**How to Change:**
1. Replace `info@pogisostours.co.za` with your email address
2. Keep the `mailto:` part

```html
<!-- BEFORE -->
<a href="mailto:info@pogisostours.co.za">info@pogisostours.co.za</a>

<!-- AFTER -->
<a href="mailto:hello@yourbusiness.com">hello@yourbusiness.com</a>
```

---

### 6. Social Media Links

**Location:** Lines 982-1000 (Footer Social Media)

**Current Code:**
```html
<div class="flex space-x-4 pt-2">
    <a href="#" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300" aria-label="Facebook">
        <i class="fab fa-facebook text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300" aria-label="Instagram">
        <i class="fab fa-instagram text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300" aria-label="LinkedIn">
        <i class="fab fa-linkedin text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300" aria-label="Twitter">
        <i class="fab fa-twitter text-xl"></i>
    </a>
</div>
```

**How to Update Social Media Links:**

1. Replace `#` with your actual social media URL
2. Keep the `aria-label` for accessibility

```html
<!-- BEFORE: No link -->
<a href="#" aria-label="Facebook">

<!-- AFTER: With link -->
<a href="https://facebook.com/yourpage" aria-label="Facebook">
```

**Common Social Media URL Formats:**
```
Facebook:    https://facebook.com/yourpage
Instagram:   https://instagram.com/yourprofile
LinkedIn:    https://linkedin.com/company/yourcompany
Twitter:     https://twitter.com/yourhandle
TikTok:      https://tiktok.com/@yourhandle
```

---

### 7. Checklist: All Links to Update

Print this checklist and verify all links:

```
NAVIGATION & HERO SECTION:
☐ Desktop Menu - Features link (#features)
☐ Desktop Menu - Benefits link (#benefits)
☐ Desktop Menu - Testimonials link (#testimonials)
☐ Desktop Menu - FAQ link (#faq)
☐ Desktop Menu - Book Now button (booking URL)
☐ Mobile Menu - All links (should match desktop)
☐ Hero Section - Start Your Journey button (booking URL)
☐ Hero Section - Learn More button (if linking somewhere)

INTERNAL SECTIONS:
☐ Features section has id="features"
☐ Benefits section has id="benefits"
☐ Testimonials section has id="testimonials"
☐ FAQ section has id="faq"

FOOTER:
☐ Footer Quick Links - All 4 links match navigation
☐ Footer Legal - Privacy Policy link (privacy.html)
☐ Footer Legal - Terms of Service link (terms.html)
☐ Footer Legal - Blog link (blog.html)
☐ Footer Contact - Email address (mailto:)
☐ Footer Social - Facebook URL
☐ Footer Social - Instagram URL
☐ Footer Social - LinkedIn URL
☐ Footer Social - Twitter URL

CONTACT FORM:
☐ Form action is correct (Web3Forms API key)
☐ Redirect URL is set correctly
```

---

## Adding Privacy and Terms Pages

### Step 1: Create the Privacy Policy Page

**Step 1A: Create a new file called `privacy.html`**

1. Open your text editor (VS Code, Notepad++, etc.)
2. Create a new file
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 1B: Add basic HTML structure**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Pogiso's Tours">
    <title>Privacy Policy - Pogiso's Tours</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation (Copy from index.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <span class="text-2xl font-bold text-white">Pogiso's Tours</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Home</a>
            </div>
            <div class="hidden md:block">
                <a href="https://pogisostours.co.za/booking" class="bg-gradient-to-r from-[#5B4BFF] to-[#00E5A8] text-white px-6 py-2 rounded-lg font-bold text-sm transition-all duration-300 hover:shadow-lg inline-block">
                    Book Now
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-5xl font-bold mb-8">Privacy Policy</h1>
        
        <div class="prose prose-invert max-w-none">
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Last updated: January 2025
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">1. Introduction</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Pogiso's Tours ("we," "us," "our," or "Company") operates the landing page. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">2. Information Collection and Use</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                We collect several different types of information for various purposes to provide and improve our Service to you.
            </p>
            
            <h3 class="text-2xl font-bold mt-8 mb-4">Types of Data Collected:</h3>
            <ul class="list-disc list-inside text-gray-300 font-light leading-relaxed mb-6 space-y-2">
                <li>Personal Data: Name, email address, phone number, cookies and usage data</li>
                <li>Usage Data: Information about how you interact with our Service</li>
                <li>Cookies: Small data files stored on your device</li>
            </ul>

            <h2 class="text-3xl font-bold mt-12 mb-4">3. Use of Data</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Pogiso's Tours uses the collected data for various purposes:
            </p>
            <ul class="list-disc list-inside text-gray-300 font-light leading-relaxed mb-6 space-y-2">
                <li>To provide and maintain our Service</li>
                <li>To notify you about changes to our Service</li>
                <li>To provide customer support</li>
                <li>To gather analysis or valuable information</li>
                <li>To monitor the usage of our Service</li>
                <li>To detect, prevent and address technical issues</li>
            </ul>

            <h2 class="text-3xl font-bold mt-12 mb-4">4. Security of Data</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                The security of your data is important to us but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">5. Changes to This Privacy Policy</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last updated" date at the top of this Privacy Policy.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">6. Contact Us</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                If you have any questions about this Privacy Policy, please contact us at:
            </p>
            <p class="text-gray-300 font-light">
                Email: <a href="mailto:info@pogisostours.co.za" class="text-[#5B4BFF] hover:text-[#00E5A8]">info@pogisostours.co.za</a>
            </p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-light text-sm">
                &copy; 2025 Pogiso's Tours. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

**Step 2A: Create a new file called `terms.html`**

1. Open your text editor
2. Create a new file
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2B: Add HTML content**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Pogiso's Tours">
    <title>Terms of Service - Pogiso's Tours</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <span class="text-2xl font-bold text-white">Pogiso's Tours</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Home</a>
            </div>
            <div class="hidden md:block">
                <a href="https://pogisostours.co.za/booking" class="bg-gradient-to-r from-[#5B4BFF] to-[#00E5A8] text-white px-6 py-2 rounded-lg font-bold text-sm transition-all duration-300 hover:shadow-lg inline-block">
                    Book Now
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-5xl font-bold mb-8">Terms of Service</h1>
        
        <div class="prose prose-invert max-w-none">
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Last updated: January 2025
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">1. Agreement to Terms</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">2. Use License</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Permission is granted to temporarily download one copy of the materials (information or software) on Pogiso's Tours website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
            </p>
            <ul class="list-disc list-inside text-gray-300 font-light leading-relaxed mb-6 space-y-2">
                <li>Modify or copy the materials</li>
                <li>Use the materials for any commercial purpose or for any public display</li>
                <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                <li>Remove any copyright or other proprietary notations from the materials</li>
                <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
            </ul>

            <h2 class="text-3xl font-bold mt-12 mb-4">3. Disclaimer</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                The materials on Pogiso's Tours website are provided on an 'as is' basis. Pogiso's Tours makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">4. Limitations</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                In no event shall Pogiso's Tours or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Pogiso's Tours website.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">5. Accuracy of Materials</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                The materials appearing on Pogiso's Tours website could include technical, typographical, or photographic errors. Pogiso's Tours does not warrant that any of the materials on its website are accurate, complete, or current. Pogiso's Tours may make changes to the materials contained on its website at any time without notice.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">6. Links</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Pogiso's Tours has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Pogiso's Tours of the site. Use of any such linked website is at the user's own risk.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">7. Modifications</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                Pogiso's Tours may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">8. Governing Law</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
            </p>

            <h2 class="text-3xl font-bold mt-12 mb-4">9. Contact Us</h2>
            <p class="text-gray-300 font-light leading-relaxed mb-6">
                If you have any questions about these Terms of Service, please contact us at:
            </p>
            <p class="text-gray-300 font-light">
                Email: <a href="mailto:info@pogisostours.co.za" class="text-[#5B4BFF] hover:text-[#00E5A8]">info@pogisostours.co.za</a>
            </p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-light text-sm">
                &copy; 2025 Pogiso's Tours. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Update Footer Links in index.html

Now that you have created `privacy.html` and `terms.html`, you need to link to them from your main page.

**Location:** Lines 945-952 (Footer Legal Links Section)

**Current Code:**
```html
<div>
    <h3 class="font-bold text-white mb-4 text-lg">Legal</h3>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Terms of Service</a></li>
        <li><a href="blog.html" class="text-gray-400 hover:text-[#5B4BFF] transition-colors duration-300 font-light">Blog</a></li>
    </ul>
</div>
```

**The links are already correct!** The code already has:
- `href="privacy.html"` - Links to your Privacy Policy
- `href="terms.html"` - Links to your Terms of Service

**Verify the links work:**
1. Save all three files in the same folder:
   - `index.html`
   - `privacy.html`
   - `terms.html`
2. Open `index.html` in your browser
3. Scroll to the footer
4. Click on "Privacy Policy" - it should take you to `privacy.html`
5. Click on "Terms of Service" - it should take you to `terms.html`

---

### Step 4: Add Navigation Links Back to Home

To make it easy for users to return to the main page from the policy pages, we already added a "Home" link in the header.

**In `privacy.html` and `terms.html`:**
```html
<a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-light">Home</a>
```

This link is already included in the header of both pages.

---

### Step 5: Customize the Policy Content

You should customize the privacy policy and terms of service with your actual company information.

**Things to customize in `privacy.html`:**
1. Change the email address: `info@pogisostours.co.za` to your email
2. Update the company name: `Pogiso's Tours` to your company name
3. Add your actual privacy practices
4. Update the "Last updated" date

**Things to customize in `terms.html`:**
1. Change the email address: `info@pogisostours.co.za` to your email
2. Update the company name: `Pogiso's Tours` to your company name
3. Change jurisdiction: `South Africa` to your country
4. Update the "Last updated" date

---

### Step 6: Test All Links

**Complete Testing Checklist:**

```
✓ From index.html footer, click "Privacy Policy" - opens privacy.html
✓ From index.html footer, click "Terms of Service" - opens terms.html
✓ From privacy.html header, click "Home" - returns to index.html
✓ From terms.html header, click "Home" - returns to index.html
✓ From privacy.html, click "Book Now" - opens booking URL
✓ From terms.html, click "Book Now" - opens booking URL
✓ All email links work (mailto:)
✓ All social media links work (if added)
```

---

## Troubleshooting Guide

### Common Issues and Solutions

---

### Issue 1: Links Not Working (404 Errors)

**Problem:** When you click a link, you get a "404 Not Found" error or the page doesn't exist.

**Solution:**

1. **Check file names are spelled correctly:**
   ```
   Correct: privacy.html (lowercase)
   Wrong:   Privacy.html (uppercase)
   Wrong:   privacypolicy.html (different name)
   ```

2. **Check files are in the same folder:**
   ```
   Folder structure should be:
   /website-folder/
   ├── index.html
   ├── privacy.html
   ├── terms.html
   └── blog.html
   ```

3. **Verify href matches filename exactly:**
   ```html
   <!-- WRONG: File is named "privacy.html" but link says "privacypolicy.html" -->
   <a href="privacypolicy.html">Privacy</a>
   
   <!-- CORRECT: -->
   <a href="privacy.html">Privacy</a>
   ```

4. **For external links, include full URL:**
   ```html
   <!-- WRONG: Missing https:// -->
   <a href="pogisostours.co.za/booking">Book</a>
   
   <!-- CORRECT: -->
   <a href="https://pogisostours.co.za/booking">Book</a>
   ```

---

### Issue 2: Internal Links Not Jumping to Section

**Problem:** Clicking a navigation link doesn't jump to the section; page stays at the top.

**Solution:**

1. **Verify section has matching ID:**
   ```html
   <!-- Navigation link -->
   <a href="#features">Features</a>
   
   <!-- Matching section (should exist somewhere on page) -->
   <section id="features">
       ...
   </section>
   ```

2. **Check ID spelling matches exactly (case-sensitive):**
   ```html
   <!-- WRONG: Capitalization doesn't match -->
   <a href="#Features">Features</a>
   <section id="features">
   
   <!-- CORRECT: Both lowercase -->
   <a href="#features">Features</a>
   <section id="features">
   ```

3. **Verify ID is unique (no duplicates):**
   ```html
   <!-- WRONG: Two sections with same ID -->
   <section id="features">First</section>
   <section id="features">Second</section>
   
   <!-- CORRECT: Different IDs -->
   <section id="features">First</section>
   <section id="services">Second</section>
   ```

---

### Issue 3: Text Appears Too Small or Too Large

**Problem:** Text doesn't look right on mobile or desktop.

**Solution:**

**Understanding responsive text sizing:**
```html
<!-- This text is different sizes on different screens -->
<h1 class="text-5xl sm:text-6xl lg:text-7xl">
    Heading
</h1>
```

Breakdown:
- `text-5xl` = Size on all small screens (phones)
- `sm:text-6xl` = Size on small screens and up (tablets)
- `lg:text-7xl` = Size on large screens and up (desktops)

**To make text larger on all screens:**
```html
<!-- BEFORE -->
<p class="text-lg">Paragraph</p>

<!-- AFTER: Larger -->
<p class="text-xl">Paragraph</p>

<!-- Even larger -->
<p class="text-2xl">Paragraph</p>
```

**To make text smaller on mobile:**
```html
<!-- BEFORE: Same size everywhere -->
<h2 class="text-4xl">Heading</h2>

<!-- AFTER: Smaller on mobile, larger on desktop -->
<h2 class="text-3xl sm:text-4xl lg:text-5xl">Heading</h2>
```

---

### Issue 4: Colors Look Wrong

**Problem:** Custom colors don't display correctly.

**Solution:**

1. **Verify color code format:**
   ```html
   <!-- WRONG: Missing brackets -->
   <div class="bg-#5B4BFF">Content</div>
   
   <!-- CORRECT: -->
   <div class="bg-[#5B4BFF]">Content</div>
   ```

2. **Check color code is valid hex:**
   ```html
   <!-- WRONG: Invalid hex code -->
   <div class="text-[#ZZZZZZ]">Content</div>
   
   <!-- CORRECT: Valid hex code -->
   <div class="text-[#FF5733]">Content</div>
   ```

3. **Verify color isn't obscured by background:**
   ```html
   <!-- WRONG: White text on white background (invisible) -->
   <div class="bg-white">
       <p class="text-white">Text</p>
   </div>
   
   <!-- CORRECT: White text on dark background -->
   <div class="bg-gray-900">
       <p class="text-white">Text</p>
   </div>
   ```

---

### Issue 5: Hover Effects Not Working

**Problem:** Buttons/links don't change color or style when you hover over them.

**Solution:**

1. **Verify hover class is included:**
   ```html
   <!-- WRONG: No hover effect -->
   <a href="#" class="text-gray-400">Link</a>
   
   <!-- CORRECT: With hover effect -->
   <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Link</a>
   ```

2. **Check transition class is present:**
   ```html
   <!-- WRONG: Hover effect but no smooth transition -->
   <button class="bg-gray-800 hover:bg-[#5B4BFF]">Button</button>
   
   <!-- CORRECT: With smooth transition -->
   <button class="bg-gray-800 hover:bg-[#5B4BFF] transition-all duration-300">Button</button>
   ```

---

### Issue 6: Mobile Menu Not Opening

**Problem:** Hamburger menu button doesn't open the mobile menu on phones.

**Solution:**

1. **Verify JavaScript is included:**
   - Check that the `<script>` section at the bottom of the page is present
   - Look for this code around line 1050:
   ```html
   <script>
       document.addEventListener('DOMContentLoaded', function() {
           // Mobile Menu Toggle
           const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
           // ... more code
       });
   </script>
   ```

2. **Check mobile menu button exists:**
   ```html
   <!-- Should exist in header -->
   <button class="mobile-menu-button md:hidden text-white text-2xl focus:outline-none focus:ring-2 focus:ring-[#5B4BFF] rounded-lg p-2" aria-label="Toggle mobile menu">
       <i class="fas fa-bars"></i>
   </button>
   ```

3. **Verify mobile menu div exists:**
   ```html
   <!-- Should exist in header -->
   <div class="mobile-menu hidden absolute top-full left-0 right-0 bg-gray-800 border-b border-gray-700 md:hidden">
       <!-- Menu items -->
   </div>
   ```

4. **Test on actual mobile device or use browser's mobile view:**
   - In Chrome: Press F12, then click the phone icon in the top left
   - In Firefox: Press Ctrl+Shift+M

---

### Issue 7: FAQ Accordion Not Expanding

**Problem:** Clicking FAQ questions doesn't expand to show answers.

**Solution:**

1. **Verify JavaScript for FAQ is present:**
   ```html
   <script>
       // FAQ Accordion Toggle
       const faqItems = document.querySelectorAll('.faq-item');
       faqItems.forEach(item => {
           const question = item.querySelector('.faq-question');
           // ... more code
       });
   </script>
   ```

2. **Check FAQ structure is correct:**
   ```html
   <!-- Should have this structure -->
   <div class="faq-item">
       <button class="faq-question">Question Text</button>
       <div class="faq-answer hidden">Answer Text</div>
   </div>
   ```

3. **Verify CSS for faq-answer exists:**
   ```html
   <style>
       .faq-answer {
           transition: all 300ms ease-out;
           max-height: 1000px;
       }
       
       .faq-answer.hidden {
           max-height: 0;
           overflow: hidden;
       }
   </style>
   ```

---

### Issue 8: Form Not Sending Messages

**Problem:** Contact form doesn't send messages or shows errors.

**Solution:**

1. **Verify Web3Forms API key is correct:**
   ```html
   <!-- Around line 820 -->
   <input type="hidden" name="access_key" value="3bb39263-2490-491b-89f8-213fa513edae">
   ```
   
   This API key is required. If you're getting errors:
   - Go to https://web3forms.com
   - Sign up for a free account
   - Get your API key
   - Replace the value above with your key

2. **Check form fields have correct names:**
   ```html
   <!-- Required fields -->
   <input type="text" name="name" required>
   <input type="email" name="email" required>
   <textarea name="message" required></textarea>
   ```

3. **Verify form action is correct:**
   ```html
   <form action="https://api.web3forms.com/submit" method="POST">
   ```

4. **Test form submission:**
   - Fill out all required fields
   - Click "Send Message"
   - Check browser console for errors (F12 > Console tab)

---

### Issue 9: Page Looks Different on Mobile

**Problem:** Layout breaks or looks wrong on phones.

**Solution:**

1. **Test responsive design:**
   - In Chrome: Press F12, then click the phone icon
   - Resize browser window to test different sizes

2. **Check responsive classes are used:**
   ```html
   <!-- WRONG: Same size everywhere -->
   <div class="px-4 py-8">Content</div>
   
   <!-- CORRECT: Different sizes on mobile vs desktop -->
   <div class="px-2 py-4 sm:px-4 sm:py-8">Content</div>
   ```

3. **Verify viewport meta tag exists in head:**
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

---

### Issue 10: Styles Not Applying

**Problem:** CSS changes don't show up on the page.

**Solution:**

1. **Hard refresh the page:**
   - Windows: Ctrl+Shift+R
   - Mac: Cmd+Shift+R
   - This clears the browser cache

2. **Check Tailwind CSS is loaded:**
   ```html
   <!-- Should be in <head> section -->
   <script src="https://cdn.tailwindcss.com"></script>
   ```

3. **Verify class names are spelled correctly:**
   ```html
   <!-- WRONG: Typo in class name -->
   <div class="bg-gra-900">Content</div>
   
   <!-- CORRECT: -->
   <div class="bg-gray-900">Content</div>
   ```

4. **Check for conflicting styles:**
   - Use browser DevTools (F12) to inspect element
   - Look for crossed-out styles that might be overridden

---

## Best Practices

### 1. Before Making Changes

**Always backup your files:**
1. Copy your `index.html` file and rename it to `index.html.backup`
2. Keep this backup in case you need to revert changes
3. Never work directly on your only copy

---

### 2. Making Content Updates

**Follow this workflow:**

1. **Identify what you want to change**
   - Find the exact text or element
   - Note the line number

2. **Make one change at a time**
   - Don't change multiple things at once
   - This makes it easier to find problems

3. **Save and test**
   - Save the file (Ctrl+S)
   - Refresh the browser (F5)
   - Verify the change looks correct

4. **Document your changes**
   - Keep a list of what you changed
   - This helps when troubleshooting

---

### 3. Organizing Your Files

**Recommended folder structure:**
```
/my-website/
├── index.html              (Main landing page)
├── privacy.html            (Privacy policy)
├── terms.html              (Terms of service)
├── blog.html               (Blog page - optional)
├── images/                 (Folder for images)
│   ├── logo.png
│   ├── hero-image.jpg
│   └── team-photo.jpg
├── css/                    (Folder for custom CSS - optional)
│   └── custom.css
└── js/                     (Folder for custom JavaScript - optional)
    └── custom.js
```

---

### 4. Using Consistent Naming

**File naming conventions:**
- Use lowercase letters only: `privacy.html` not `Privacy.html`
- Use hyphens for spaces: `my-page.html` not `my page.html`
- Be descriptive: `contact-form.html` not `form1.html`

**Class naming conventions:**
- Use the existing naming pattern
- Don't create new custom classes unless necessary
- Stick with Tailwind's built-in classes

---

### 5. Maintaining Consistency

**Keep these consistent across all pages:**
- Header navigation (same links on every page)
- Footer information (same contact info, links)
- Color scheme (same primary and accent colors)
- Typography (same fonts and sizes)

---

### 6. Testing on Multiple Devices

**Always test on:**
- Desktop (1920x1080)
- Tablet (768x1024)
- Mobile (375x667)

**Use browser tools:**
- Chrome DevTools: F12 → Click phone icon
- Firefox DevTools: F12 → Click phone icon

---

### 7. Regular Maintenance Checklist

**Weekly:**
- Check all links work
- Verify contact form sends messages
- Test mobile responsiveness

**Monthly:**
- Update testimonials or statistics
- Review and update pricing/offers
- Check for broken external links

**Quarterly:**
- Update privacy policy if needed
- Review analytics to see popular pages
- Update company information if changed

---

### 8. SEO Best Practices

**For better search engine visibility:**

1. **Keep title tags descriptive:**
   ```html
   <!-- GOOD: Descriptive -->
   <title>Luxury Chauffeur Packages & Travel Essentials — Shop the Elite Way</title>
   
   <!-- BAD: Generic -->
   <title>Home</title>
   ```

2. **Update meta descriptions:**
   ```html
   <meta name="description" content="Your unique value proposition here">
   ```

3. **Use heading hierarchy correctly:**
   ```html
   <h1>Main heading (only one per page)</h1>
   <h2>Section heading</h2>
   <h3>Subsection heading</h3>
   ```

4. **Add alt text to images (when adding images):**
   ```html
   <img src="car.jpg" alt="Luxury black sedan with professional driver">
   ```

---

### 9. Security Best Practices

**Protect your website:**

1. **Keep external links secure (https):**
   ```html
   <!-- WRONG: Not secure -->
   <a href="http://example.com">Link</a>
   
   <!-- CORRECT: Secure -->
   <a href="https://example.com">Link</a>
   ```

2. **Validate form inputs:**
   - The contact form already has validation
   - Always use `required` attribute on important fields

3. **Keep software updated:**
   - Update your text editor
   - Update your browser
   - Keep backup copies

4. **Use strong passwords:**
   - If you have a hosting account, use strong passwords
   - Never share your credentials

---

### 10. Performance Optimization

**Keep your page fast:**

1. **Minimize external requests:**
   - Reduce number of external stylesheets
   - Combine multiple scripts

2. **Optimize images:**
   - Compress images before uploading
   - Use appropriate formats (JPG for photos, PNG for graphics)
   - Resize images to actual display size

3. **Cache static files:**
   - Browser caching is already enabled by Tailwind CDN
   - Consider using a CDN for images

4. **Monitor page speed:**
   - Use Google PageSpeed Insights
   - Use GTmetrix for detailed reports

---

## Quick Reference: Most Common Tasks

### Changing Company Name
1. Find: `Pogiso's Tours`
2. Replace with: Your company name
3. Update in: Header, Footer, Page titles, Meta descriptions

### Updating Email Address
1. Find: `info@pogisostours.co.za`
2. Replace with: Your email
3. Update in: Footer contact, Contact form, Policy pages

### Changing Booking URL
1. Find: `https://pogisostours.co.za/booking`
2. Replace with: Your booking URL
3. Update in: All "Book Now" buttons (appears multiple times)

### Adding New Menu Item
1. Copy existing menu item HTML
2. Paste it next to other menu items
3. Change href and text
4. Add matching section with id attribute

### Changing Colors
1. Find: `#5B4BFF` (purple) or `#00E5A8` (green)
2. Replace with: Your brand colors
3. Use Find & Replace (Ctrl+H) to change all instances

---

## Final Checklist Before Launch

```
CONTENT:
☐ All text is updated with your information
☐ Company name is consistent everywhere
☐ Contact email is correct
☐ Phone number is correct
☐ Testimonials are relevant (or removed)
☐ Statistics are accurate

LINKS:
☐ All navigation links work
☐ Booking button links to correct URL
☐ Email links work (mailto:)
☐ Social media links are correct
☐ Footer links work
☐ Internal section links jump correctly

PAGES:
☐ privacy.html exists and is linked
☐ terms.html exists and is linked
☐ All pages have consistent header/footer
☐ All pages have "Home" link

FUNCTIONALITY:
☐ Mobile menu opens and closes
☐ FAQ accordion works
☐ Contact form sends messages
☐ Hover effects work on buttons/links
☐ Page is responsive on mobile

DESIGN:
☐ Colors match your brand
☐ Text sizes are readable
☐ Layout looks good on desktop
☐ Layout looks good on mobile
☐ Images load correctly (if any)

PERFORMANCE:
☐ Page loads quickly
☐ No console errors (F12 > Console)
☐ No broken images
☐ No 404 errors

SEO:
☐ Page title is descriptive
☐ Meta description is filled in
☐ H1 heading exists and is unique
☐ Links have descriptive text (not "click here")

SECURITY:
☐ All external links use https://
☐ Form has required fields
☐ No sensitive information exposed
☐ Backup copy exists
```

---

## Getting Additional Help

### Resources

1. **Tailwind CSS Documentation:**
   - https://tailwindcss.com/docs
   - Search for class names you want to use

2. **HTML Reference:**
   - https://developer.mozilla.org/en-US/docs/Web/HTML
   - Learn HTML basics and best practices

3. **Web3Forms Documentation:**
   - https://web3forms.com/documentation
   - For contact form troubleshooting

4. **Material Symbols Icons:**
   - https://fonts.google.com/icons
   - Find icons to replace current ones

5. **Color Picker Tools:**
   - https://htmlcolorcodes.com
   - Find hex color codes for your brand

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your Pogiso's Tours landing page. Remember to:

1. **Start small** - Make one change at a time
2. **Test thoroughly** - Always verify changes work
3. **Keep backups** - Save copies before major changes
4. **Stay consistent** - Maintain uniform styling and messaging
5. **Keep learning** - The resources above can help you grow your skills

Good luck with your website! For more complex customizations, consider consulting with a professional web developer.