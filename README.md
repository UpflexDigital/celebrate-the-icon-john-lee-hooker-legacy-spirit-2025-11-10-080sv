# John Lee Hooker Legacy Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your landing page. This guide is designed for developers of all skill levels.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Customizing Colors and Styling](#customizing-colors-and-styling)
8. [Common Issues and Troubleshooting](#common-issues-and-troubleshooting)
9. [Best Practices](#best-practices)

---

## Getting Started

### What You'll Need

- A text editor (VS Code, Sublime Text, Notepad++, or even Notepad)
- Basic understanding of HTML structure
- A web browser to preview changes
- The index.html file provided

### How to Edit the File

1. **Open the HTML file** in your text editor
2. **Make your changes** using the guides below
3. **Save the file** (Ctrl+S on Windows, Cmd+S on Mac)
4. **Preview in browser** by opening the file (double-click or drag into browser)
5. **Refresh the page** (F5 or Cmd+R) after each save to see changes

---

## Understanding the Page Structure

Your landing page is organized into distinct sections. Here's a visual breakdown:

```
┌─────────────────────────────────────────┐
│ HEADER & NAVIGATION                     │  (Sticky, always visible)
├─────────────────────────────────────────┤
│ HERO SECTION                            │  (Main banner with CTA)
├─────────────────────────────────────────┤
│ FEATURES SECTION                        │  (3 feature cards)
├─────────────────────────────────────────┤
│ BENEFITS SECTION                        │  (3 benefit cards)
├─────────────────────────────────────────┤
│ CTA SECTION                             │  (Call-to-action banner)
├─────────────────────────────────────────┤
│ TESTIMONIALS SECTION                    │  (4 customer reviews)
├─────────────────────────────────────────┤
│ FAQ SECTION                             │  (5 expandable questions)
├─────────────────────────────────────────┤
│ ABOUT US SECTION                        │  (Story and mission)
├─────────────────────────────────────────┤
│ NEWSLETTER SECTION                      │  (Email signup)
├─────────────────────────────────────────┤
│ CONTACT FORM SECTION                    │  (Contact form)
├─────────────────────────────────────────┤
│ FOOTER                                  │  (Links and info)
└─────────────────────────────────────────┘
```

---

## Updating Text Content

### 1. Changing the Page Title

**Location:** Lines 7-8 in the `<head>` section

**Current Code:**
```html
<meta name="description" content="Celebrate the Icon: John Lee Hooker Legacy Spirit - Honor the undeniable talent and lasting influence of the King of the Boogie.">
<meta name="keywords" content="John Lee Hooker, Legacy, Blues, Collectibles, Bourbon, Memorabilia">
<meta name="author" content="John Lee Hooker Legacy">
<title>Celebrate the Icon: John Lee Hooker Legacy Spirit</title>
```

**How to Update:**

1. Find the line that starts with `<title>`
2. Replace the text between `<title>` and `</title>` with your new title
3. Also update the `content` attribute in the `<meta name="description"...` line

**Example - Changing to a Different Product:**
```html
<title>Your New Product Name - Premium Collection</title>
<meta name="description" content="Your new description here">
```

### 2. Updating the Logo Text

**Location:** Lines 65-68 in the header navigation

**Current Code:**
```html
<div class="flex items-center space-x-2">
    <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center">
        <i class="fas fa-music text-white text-lg"></i>
    </div>
    <span class="text-xl font-bold text-gray-900">Hooker Legacy</span>
</div>
```

**How to Update the Logo Text:**

1. Find the `<span>` tag that contains `Hooker Legacy`
2. Replace `Hooker Legacy` with your desired text
3. Keep the `class="text-xl font-bold text-gray-900"` unchanged

**Example:**
```html
<span class="text-xl font-bold text-gray-900">My New Brand Name</span>
```

### 3. Updating the Hero Section Title

**Location:** Lines 110-114

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Celebrate the Icon: <span class="gradient-text">John Lee Hooker Legacy Spirit</span>
</h1>
```

**How to Update:**

1. Find the `<h1>` tag in the hero section
2. You can replace either:
   - The regular text before the `<span>` (before the gradient effect)
   - The text inside the `<span class="gradient-text">` (the purple-to-pink gradient text)
3. Keep the HTML structure intact

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Discover the Best: <span class="gradient-text">Premium Product Collection</span>
</h1>
```

### 4. Updating the Hero Subtitle

**Location:** Lines 116-120

**Current Code:**
```html
<p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed font-light">
    Honor the undeniable talent and lasting influence of the King of the Boogie. Experience an exclusive collection celebrating a blues legend whose revolutionary sound shaped generations of musicians and captivated millions of listeners worldwide.
</p>
```

**How to Update:**

1. Find the paragraph (`<p>`) tag with this long description
2. Replace the text while keeping the `class` attribute exactly the same
3. The class controls the styling (size, color, spacing)

**Example:**
```html
<p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed font-light">
    Your new description goes here. Make it compelling and relevant to your product or service.
</p>
```

### 5. Updating Section Headings

**Location:** Multiple sections (Features, Benefits, Testimonials, FAQ, About)

**Example - Features Section Heading (Line 142):**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 tracking-tight">
    Exclusive Features
</h2>
```

**How to Update All Section Headings:**

1. Search for each `<h2>` tag in the document
2. Replace the text between `<h2>` and `</h2>`
3. Keep the `class` attribute unchanged

**All Section Headings to Update:**
- Line 142: "Exclusive Features"
- Line 152: "Why Choose Our Legacy Collection"
- Line 362: "Ready to Honor a Legend?"
- Line 397: "What Our Community Says"
- Line 434: "Frequently Asked Questions"
- Line 461: "About the John Lee Hooker Legacy"

### 6. Updating Feature Card Content

**Location:** Lines 161-210 (Feature 1), Lines 213-262 (Feature 2), Lines 265-314 (Feature 3)

**Current Feature 1 Structure:**
```html
<div class="card-hover smooth-transition bg-white rounded-2xl p-8 border border-gray-200 hover:border-purple-300">
    <div class="bg-gradient-to-br from-purple-100 to-pink-100 w-16 h-16 rounded-xl flex items-center justify-center mb-6">
        <svg class="w-8 h-8 text-purple-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Limited Edition Collectibles</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Own a piece of music history...
    </p>
    <ul class="space-y-3">
        <li class="flex items-start space-x-3">
            <!-- Checkmark items -->
        </li>
    </ul>
</div>
```

**How to Update a Feature Card:**

1. **Update the title:** Find the `<h3>` tag and change "Limited Edition Collectibles"
2. **Update the description:** Find the first `<p>` tag and change the description text
3. **Update the bullet points:** Find each `<li>` tag inside the `<ul>` and change the text

**Example - Updating Feature 1 Title and Description:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-4">Your New Feature Title</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Your new feature description goes here. Explain the benefit clearly and concisely.
</p>
```

**Updating Bullet Points:**
```html
<li class="flex items-start space-x-3">
    <svg class="w-5 h-5 text-purple-600 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
    </svg>
    <span class="text-sm text-gray-700">Your new bullet point text here</span>
</li>
```

### 7. Updating Testimonials

**Location:** Lines 433-530

**Current Testimonial Structure:**
```html
<div class="bg-white rounded-2xl p-8 border border-gray-200 hover:shadow-xl smooth-transition">
    <div class="flex items-center mb-4">
        <!-- Star ratings -->
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed">
        "This is the testimonial text..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-gray-900">Person Name</p>
        <p class="text-sm text-gray-600">Job Title or Description</p>
    </div>
</div>
```

**How to Update a Testimonial:**

1. Find the testimonial you want to update
2. Change the quoted text (the review)
3. Change the person's name
4. Change their title/description

**Example:**
```html
<p class="text-gray-700 mb-6 leading-relaxed">
    "This is an amazing product! I absolutely love it and recommend it to everyone."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-gray-900">Sarah Johnson</p>
    <p class="text-sm text-gray-600">Marketing Director</p>
</div>
```

### 8. Updating FAQ Questions and Answers

**Location:** Lines 470-570

**Current FAQ Structure:**
```html
<div class="faq-item bg-white rounded-2xl border border-gray-200 overflow-hidden">
    <button class="faq-question w-full px-8 py-6 flex items-center justify-between hover:bg-gray-50 smooth-transition cursor-pointer">
        <h3 class="text-lg font-semibold text-gray-900 text-left">
            Are all items in the collection authentically verified?
        </h3>
        <svg class="faq-icon w-6 h-6 text-purple-600 flex-shrink-0 smooth-transition" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
        </svg>
    </button>
    <div class="faq-answer hidden px-8 pb-6 text-gray-600 leading-relaxed border-t border-gray-200">
        <p class="mb-4">
            First paragraph of the answer...
        </p>
        <p>
            Second paragraph of the answer...
        </p>
    </div>
</div>
```

**How to Update FAQ Content:**

1. Find the `<h3>` tag inside the `<button class="faq-question">` - this is your question
2. Replace the question text
3. Find the `<div class="faq-answer hidden">` section
4. Replace the paragraph text inside

**Example:**
```html
<h3 class="text-lg font-semibold text-gray-900 text-left">
    What is your return policy?
</h3>
```

```html
<div class="faq-answer hidden px-8 pb-6 text-gray-600 leading-relaxed border-t border-gray-200">
    <p class="mb-4">
        We offer a 30-day money-back guarantee on all purchases.
    </p>
    <p>
        If you're not satisfied with your purchase, simply contact us within 30 days for a full refund.
    </p>
</div>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses utility classes to style elements. Instead of writing custom CSS, you apply pre-made classes directly to HTML elements. Here are the most common classes used in your landing page:

### Common Classes Explained

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Makes text larger (xl = extra large) | `<h1 class="text-xl">` |
| `text-gray-900` | Makes text dark gray | `<p class="text-gray-900">` |
| `bg-white` | White background | `<div class="bg-white">` |
| `p-8` | Padding (space inside) of 8 units | `<div class="p-8">` |
| `mb-4` | Margin bottom (space below) of 4 units | `<div class="mb-4">` |
| `rounded-lg` | Rounded corners | `<div class="rounded-lg">` |
| `hover:bg-purple-50` | Changes background on hover | `<button class="hover:bg-purple-50">` |
| `md:text-5xl` | Applies on medium screens and up | `<h1 class="md:text-5xl">` |
| `flex` | Makes items display in a row | `<div class="flex">` |
| `grid` | Creates a grid layout | `<div class="grid">` |

### Responsive Design Breakpoints

Your page uses responsive classes that change based on screen size:

- **No prefix** (e.g., `text-lg`) = Mobile (small screens)
- **`sm:`** = Small screens (640px and up)
- **`md:`** = Medium screens (768px and up)
- **`lg:`** = Large screens (1024px and up)

### Example: Changing Text Size

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900">
    Celebrate the Icon
</h1>
```

**What This Does:**
- On mobile: `text-4xl` (extra large)
- On medium screens: `md:text-5xl` (larger)
- On large screens: `lg:text-6xl` (largest)

**How to Make It Smaller:**
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900">
    Celebrate the Icon
</h1>
```

### Example: Changing Colors

**Current Code:**
```html
<p class="text-gray-600">Your text here</p>
```

**Available Text Colors:**
- `text-gray-900` (very dark)
- `text-gray-700` (dark)
- `text-gray-600` (medium)
- `text-purple-600` (purple)
- `text-pink-600` (pink)
- `text-white` (white)

**To Change to Purple:**
```html
<p class="text-purple-600">Your text here</p>
```

### Example: Changing Spacing (Padding/Margin)

**Padding (space inside):**
```html
<div class="p-8">  <!-- 8 units of padding all around -->
<div class="px-8"> <!-- 8 units left and right only -->
<div class="py-4"> <!-- 4 units top and bottom only -->
```

**Margin (space outside):**
```html
<div class="m-8">  <!-- 8 units of margin all around -->
<div class="mb-4"> <!-- 4 units margin below -->
<div class="mt-8"> <!-- 8 units margin above -->
```

### Example: Changing Border Radius (Rounded Corners)

**Current Code:**
```html
<div class="rounded-2xl">Content</div>
```

**Size Options:**
- `rounded-lg` (slightly rounded)
- `rounded-xl` (more rounded)
- `rounded-2xl` (very rounded)
- `rounded-full` (circle)

### Example: Modifying Button Styles

**Current Button:**
```html
<a href="#" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full font-semibold smooth-transition button-pulse hover:shadow-xl cursor-pointer">
    Click Me
</a>
```

**To Make Button Larger:**
```html
<a href="#" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-12 py-6 rounded-full font-semibold smooth-transition button-pulse hover:shadow-xl cursor-pointer">
    Click Me
</a>
```
(Changed `px-8 py-4` to `px-12 py-6`)

**To Change Button Colors:**
```html
<!-- Change from purple-pink gradient to blue gradient -->
<a href="#" class="bg-gradient-to-r from-blue-600 to-blue-700 text-white px-8 py-4 rounded-full font-semibold smooth-transition button-pulse hover:shadow-xl cursor-pointer">
    Click Me
</a>
```

### Example: Changing Grid Layout

**Current 3-Column Layout:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- 3 feature cards here -->
</div>
```

**To Change to 2 Columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
    <!-- cards here -->
</div>
```

**To Change to 4 Columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
    <!-- cards here -->
</div>
```

---

## Fixing and Managing Links

### Understanding Link Types

Your page uses two types of links:

1. **Internal Links** - Link to sections within the same page
2. **External Links** - Link to other websites

### 1. Navigation Menu Links

**Location:** Lines 73-83 (Desktop Menu) and Lines 93-99 (Mobile Menu)

**Current Code:**
```html
<!-- Desktop Menu -->
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Benefits</a>
    <a href="#testimonials" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Testimonials</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">FAQ</a>
    <a href="#about" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">About</a>
</div>
```

**How These Links Work:**
- `href="#features"` links to an element with `id="features"`
- When clicked, the page smoothly scrolls to that section

**All Navigation Links Reference:**
| Link Text | Target ID | Section |
|-----------|-----------|---------|
| Features | `#features` | Line 133 |
| Benefits | `#benefits` | Line 305 |
| Testimonials | `#testimonials` | Line 397 |
| FAQ | `#faq` | Line 461 |
| About | `#about` | Line 576 |

**To Add a New Navigation Link:**

1. Add the link to the desktop menu (around line 78):
```html
<a href="#contact" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">Contact</a>
```

2. Add the same link to the mobile menu (around line 96):
```html
<a href="#contact" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium py-2">Contact</a>
```

3. Make sure there's a section with matching ID in your page:
```html
<section id="contact">
    <!-- Your contact section content -->
</section>
```

### 2. Hero Section CTA Buttons

**Location:** Lines 125-135

**Current Code:**
```html
<a href="https://seelbachs.com/products/john-lee-hooker-legacy-spirits-boogie-chillen-bourbon-kentucky-straight-bourbon-collection" target="_blank" rel="noopener noreferrer" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full font-semibold smooth-transition button-pulse hover:shadow-xl cursor-pointer inline-flex items-center space-x-2">
    <span>Explore Collection</span>
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
    </svg>
</a>
```

**Attributes Explained:**
- `href="..."` - The URL to link to
- `target="_blank"` - Opens link in new tab
- `rel="noopener noreferrer"` - Security measure for external links

**How to Update the Link:**

1. Find the `href="https://seelbachs.com/..."` attribute
2. Replace the entire URL with your new URL
3. Keep `target="_blank" rel="noopener noreferrer"` unchanged

**Example - Changing to Your Store:**
```html
<a href="https://yourstore.com/products/your-product" target="_blank" rel="noopener noreferrer" class="...">
    <span>Explore Collection</span>
    ...
</a>
```

### 3. CTA Section Button

**Location:** Lines 365-369

**Current Code:**
```html
<a href="https://seelbachs.com/products/john-lee-hooker-legacy-spirits-boogie-chillen-bourbon-kentucky-straight-bourbon-collection" target="_blank" rel="noopener noreferrer" class="inline-block bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full font-semibold smooth-transition button-pulse hover:shadow-2xl cursor-pointer">
    Shop the Collection Now
</a>
```

**How to Update:**
Same process as the hero button. Replace the URL in the `href` attribute.

### 4. Footer Links

**Location:** Lines 660-678 (Quick Links), Lines 681-688 (Legal), Lines 691-698 (Contact)

**Current Code - Quick Links:**
```html
<ul class="space-y-3">
    <li><a href="#features" class="text-gray-400 hover:text-purple-400 smooth-transition">Features</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-purple-400 smooth-transition">Benefits</a></li>
    <li><a href="#testimonials" class="text-gray-400 hover:text-purple-400 smooth-transition">Testimonials</a></li>
    <li><a href="#faq" class="text-gray-400 hover:text-purple-400 smooth-transition">FAQ</a></li>
    <li><a href="#about" class="text-gray-400 hover:text-purple-400 smooth-transition">About Us</a></li>
</ul>
```

**These are internal links** - they work the same as navigation menu links.

**Current Code - Legal Links:**
```html
<ul class="space-y-3">
    <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 smooth-transition">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 smooth-transition">Terms of Service</a></li>
    <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 smooth-transition">Blog</a></li>
    <li><a href="mailto:technoeg2723@gmail.com" class="text-gray-400 hover:text-purple-400 smooth-transition">Contact</a></li>
</ul>
```

**These link to separate pages** - see the [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages) section below.

### 5. Email Links

**Location:** Multiple locations (footer, contact info)

**Current Code:**
```html
<a href="mailto:technoeg2723@gmail.com" class="...">technoeg2723@gmail.com</a>
```

**How to Update:**
Replace `technoeg2723@gmail.com` with your email address. Keep `mailto:` at the beginning.

**Example:**
```html
<a href="mailto:hello@yourcompany.com" class="...">hello@yourcompany.com</a>
```

### 6. Social Media Links

**Location:** Lines 701-718

**Current Code:**
```html
<div class="flex space-x-4">
    <a href="#" aria-label="Facebook" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-purple-600 flex items-center justify-center smooth-transition">
        <i class="fab fa-facebook-f text-white"></i>
    </a>
    <a href="#" aria-label="Twitter" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-purple-600 flex items-center justify-center smooth-transition">
        <i class="fab fa-twitter text-white"></i>
    </a>
    <!-- More social links... -->
</div>
```

**How to Update Social Media Links:**

1. Find each `href="#"` in the social media section
2. Replace `#` with your actual social media URL

**Example - Adding Your Facebook:**
```html
<a href="https://facebook.com/yourpage" aria-label="Facebook" class="...">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Social Media URL Formats:**
- Facebook: `https://facebook.com/yourpage`
- Twitter: `https://twitter.com/yourhandle`
- Instagram: `https://instagram.com/yourhandle`
- YouTube: `https://youtube.com/yourchannel`

### 7. Checking for Broken Links

**Common Issues:**

1. **Typos in URLs** - Double-check spelling
2. **Missing # for internal links** - Should be `#features` not `features`
3. **Wrong file paths** - If linking to files, ensure correct location
4. **External links without protocol** - Should be `https://` not just `www.`

**How to Test Links:**

1. Open the HTML file in a browser
2. Click each link to verify it works
3. For internal links (#features), ensure the page scrolls to that section
4. For external links, ensure they open in a new tab
5. Check the browser console (F12) for any errors

---

## Linking Privacy and Terms Pages

### Understanding the Current Setup

Your index.html currently links to `privacy.html`, `terms.html`, and `blog.html`, but these files don't exist yet. You need to create them.

### Step 1: Create the Privacy Policy Page

**Create a new file called `privacy.html`:**

1. Open your text editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`
4. Add the following template code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - John Lee Hooker Legacy">
    <title>Privacy Policy - John Lee Hooker Legacy</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
        }
        .smooth-transition {
            transition: all 300ms cubic-bezier(0.4, 0, 0.2, 1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 border-b border-gray-200 backdrop-filter backdrop-blur-lg bg-white bg-opacity-95">
        <nav class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-music text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Hooker Legacy</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-white">
        <div class="container mx-auto max-w-4xl px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="text-gray-700 leading-relaxed">
                        John Lee Hooker Legacy ("we," "us," or "our") operates the John Lee Hooker Legacy website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information Collection and Use</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We collect several different types of information for various purposes to provide and improve our Service to you.
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 mt-4">
                        <li>Personal Data: Email address, name, phone number</li>
                        <li>Usage Data: Browser type, pages visited, time spent</li>
                        <li>Cookies and tracking technologies</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Data</h2>
                    <p class="text-gray-700 leading-relaxed">
                        John Lee Hooker Legacy uses the collected data for various purposes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 mt-4">
                        <li>To provide and maintain our Service</li>
                        <li>To notify you about changes to our Service</li>
                        <li>To allow you to participate in interactive features</li>
                        <li>To provide customer support</li>
                        <li>To gather analysis or valuable information</li>
                        <li>To monitor the usage of our Service</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Security of Data</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:technoeg2723@gmail.com" class="text-purple-600 hover:text-purple-700">technoeg2723@gmail.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 John Lee Hooker Legacy. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Create a new file called `terms.html`:**

1. Open your text editor
2. Create a new file
3. Save it as `terms.html` in the same folder as `index.html`
4. Add the following template code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - John Lee Hooker Legacy">
    <title>Terms of Service - John Lee Hooker Legacy</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
        }
        .smooth-transition {
            transition: all 300ms cubic-bezier(0.4, 0, 0.2, 1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 border-b border-gray-200 backdrop-filter backdrop-blur-lg bg-white bg-opacity-95">
        <nav class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-music text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Hooker Legacy</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-white">
        <div class="container mx-auto max-w-4xl px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Permission is granted to temporarily download one copy of the materials (information or software) on John Lee Hooker Legacy's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 mt-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials on John Lee Hooker Legacy's website are provided on an 'as is' basis. John Lee Hooker Legacy makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall John Lee Hooker Legacy or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on John Lee Hooker Legacy's website, even if John Lee Hooker Legacy or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials appearing on John Lee Hooker Legacy's website could include technical, typographical, or photographic errors. John Lee Hooker Legacy does not warrant that any of the materials on its website are accurate, complete, or current. John Lee Hooker Legacy may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        John Lee Hooker Legacy has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by John Lee Hooker Legacy of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="text-gray-700 leading-relaxed">
                        John Lee Hooker Legacy may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:technoeg2723@gmail.com" class="text-purple-600 hover:text-purple-700">technoeg2723@gmail.com</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 John Lee Hooker Legacy. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Create the Blog Page

**Create a new file called `blog.html`:**

1. Open your text editor
2. Create a new file
3. Save it as `blog.html` in the same folder as `index.html`
4. Add the following template code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - John Lee Hooker Legacy">
    <title>Blog - John Lee Hooker Legacy</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
        }
        .smooth-transition {
            transition: all 300ms cubic-bezier(0.4, 0, 0.2, 1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 border-b border-gray-200 backdrop-filter backdrop-blur-lg bg-white bg-opacity-95">
        <nav class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-music text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Hooker Legacy</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 smooth-transition font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-white">
        <div class="container mx-auto max-w-4xl px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Blog</h1>
            <p class="text-xl text-gray-600 mb-12">
                Stories, insights, and updates from the John Lee Hooker Legacy community.
            </p>

            <div class="space-y-12">
                <!-- Blog Post 1 -->
                <article class="border-b border-gray-200 pb-12">
                    <div class="mb-4">
                        <span class="text-sm font-semibold text-purple-600">March 15, 2025</span>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">
                        <a href="#" class="hover:text-purple-600 smooth-transition">The Legacy of John Lee Hooker: A Blues Icon</a>
                    </h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        John Lee Hooker revolutionized the blues genre with his distinctive "boogie" style and electrifying guitar work. In this post, we explore his most influential recordings and lasting impact on modern music.
                    </p>
                    <a href="#" class="text-purple-600 hover:text-purple-700 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 2 -->
                <article class="border-b border-gray-200 pb-12">
                    <div class="mb-4">
                        <span class="text-sm font-semibold text-purple-600">March 8, 2025</span>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">
                        <a href="#" class="hover:text-purple-600 smooth-transition">Collecting Blues Memorabilia: A Beginner's Guide</a>
                    </h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Interested in starting your own blues collectibles collection? Learn about authentication, storage, and investment potential in our comprehensive guide for collectors.
                    </p>
                    <a href="#" class="text-purple-600 hover:text-purple-700 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 3 -->
                <article>
                    <div class="mb-4">
                        <span class="text-sm font-semibold text-purple-600">March 1, 2025</span>
                    </div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">
                        <a href="#" class="hover:text-purple-600 smooth-transition">Supporting Blues Education: Impact Stories</a>
                    </h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Discover how your donations are making a real difference in young musicians' lives. Read inspiring stories from students in our supported music education programs.
                    </p>
                    <a href="#" class="text-purple-600 hover:text-purple-700 font-semibold">Read More →</a>
                </article>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2025 John Lee Hooker Legacy. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

### Step 4: Verify Links Are Working

**Folder Structure Should Look Like:**
```
your-project-folder/
├── index.html
├── privacy.html
├── terms.html
└── blog.html
```

**Test the Links:**

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should open `privacy.html`
4. Click "← Back to Home" - should return to `index.html`
5. Repeat for "Terms of Service" and "Blog"

### Step 5: Update Email Address Across All Pages

**Locations to Update:**

In `index.html`:
- Line 701 (footer contact)
- Line 710 (footer email link)

In `privacy.html`, `terms.html`, and `blog.html`:
- In the Contact Us section, replace `technoeg2723@gmail.com` with your email

**Search and Replace Method (Easiest):**

1. Open your text editor
2. Use Find & Replace (Ctrl+H on Windows, Cmd+H on Mac)
3. Find: `technoeg2723@gmail.com`
4. Replace with: `your-email@yourcompany.com`
5. Replace all instances across all files

---

## Customizing Colors and Styling

### Understanding the Color System

Your page uses a purple-to-pink gradient theme. Colors are applied through Tailwind CSS classes.

### Primary Colors Used

| Color | Class | Used For |
|-------|-------|----------|
| Purple 600 | `from-purple-600` | Gradients, text, hovers |
| Pink 600 | `to-pink-600` | Gradients, accents |
| Gray 900 | `text-gray-900` | Main text |
| Gray 700 | `text-gray-700` | Secondary text |
| Gray 600 | `text-gray-600` | Tertiary text |
| White | `text-white` | Light text on dark |

### Changing the Gradient Color Scheme

**Current Gradient (Purple to Pink):**
```html
<div class="bg-gradient-to-r from-purple-600 to-pink-600">
```

**To Change to Blue Gradient:**
```html
<div class="bg-gradient-to-r from-blue-600 to-blue-700">
```

**To Change to Green Gradient:**
```html
<div class="bg-gradient-to-r from-green-600 to-emerald-600">
```

**To Change to Red Gradient:**
```html
<div class="bg-gradient-to-r from-red-600 to-pink-600">
```

**Locations to Update Gradients:**
1. Line 43 - Gradient text in hero
2. Line 66 - Logo background
3. Line 125 - Primary CTA button
4. Line 365 - CTA section button
5. Line 640 - Newsletter section
6. Line 701+ - Footer social icons

### Changing Accent Colors

**Example: Change hover color from purple to blue**

Find all instances of:
```html
hover:text-purple-600
```

Replace with:
```html
hover:text-blue-600
```

**Common Color Replacements:**
- `purple-600` → `blue-600`
- `purple-600` → `green-600`
- `purple-600` → `indigo-600`
- `pink-600` → `rose-600`

### Changing Button Colors

**Current Primary Button:**
```html
<a class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full font-semibold">
    Button Text
</a>
```

**To Make It Solid Color Instead of Gradient:**
```html
<a class="bg-purple-600 hover:bg-purple-700 text-white px-8 py-4 rounded-full font-semibold">
    Button Text
</a>
```

**To Make It Larger:**
```html
<a class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-12 py-6 rounded-full font-semibold">
    Button Text
</a>
```
(Changed `px-8 py-4` to `px-12 py-6`)

### Changing Background Colors

**Current Hero Background:**
```html
<section class="bg-gradient-to-br from-gray-50 via-white to-gray-50">
```

**To Make It Solid White:**
```html
<section class="bg-white">
```

**To Add a Light Purple Tint:**
```html
<section class="bg-purple-50">
```

### Changing Text Colors

**Example: Making all section headings blue instead of gray**

Find all `<h2>` tags with:
```html
<h2 class="... text-gray-900 ...">
```

Change to:
```html
<h2 class="... text-blue-900 ...">
```

### Changing Border Colors

**Current Feature Card:**
```html
<div class="border border-gray-200 hover:border-purple-300">
```

**To Change to Blue:**
```html
<div class="border border-blue-200 hover:border-blue-300">
```

### Tailwind Color Palette

**Grays:**
- `gray-50` (lightest)
- `gray-100`, `gray-200`, `gray-300`, `gray-400`, `gray-500`, `gray-600`, `gray-700`, `gray-800`
- `gray-900` (darkest)

**Primary Colors:**
- `purple-50` through `purple-900`
- `pink-50` through `pink-900`
- `blue-50` through `blue-900`
- `green-50` through `green-900`
- `red-50` through `red-900`

**Lighter numbers (50, 100) = lighter shade**
**Higher numbers (700, 800, 900) = darker shade**

---

## Common Issues and Troubleshooting

### Issue 1: Links Not Working

**Symptom:** Clicking a link does nothing

**Possible Causes:**
1. Wrong URL format
2. Missing `#` for internal links
3. Typo in the href attribute

**Solution:**
```html
<!-- Wrong -->
<a href="features">Click me</a>

<!-- Correct -->
<a href="#features">Click me</a>
```

### Issue 2: Styling Looks Broken

**Symptom:** Colors wrong, spacing off, or layout broken

**Possible Causes:**
1. Accidentally deleted a class
2. Wrong class name
3. Tailwind CDN not loading

**Solution:**
1. Check the browser console (F12) for errors
2. Verify all classes are spelled correctly
3. Ensure Tailwind CDN link is present (Line 11):
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Issue 3: Mobile Menu Not Working

**Symptom:** Mobile menu button doesn't toggle the menu

**Possible Causes:**
1. JavaScript error
2. Mobile menu HTML changed
3. Classes removed from elements

**Solution:**
1. Check browser console (F12) for JavaScript errors
2. Verify the mobile menu structure hasn't changed
3. Ensure the JavaScript at the bottom of the file is intact

### Issue 4: Images Not Showing

**Symptom:** Image placeholders appear instead of actual images

**Possible Causes:**
1. Image URL is broken
2. Image file doesn't exist
3. Wrong file path

**Solution:**
```html
<!-- Using external image (works) -->
<img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?w=600&h=400&fit=crop" alt="Description">

<!-- Using local image (make sure file exists) -->
<img src="images/my-image.jpg" alt="Description">
```

### Issue 5: Form Not Submitting

**Symptom:** Contact form doesn't send messages

**Possible Causes:**
1. Web3Forms access key not set
2. Form HTML changed
3. JavaScript error

**Solution:**
1. Sign up at [web3forms.com](https://web3forms.com)
2. Get your access key
3. Replace `YOUR_WEB3FORMS_ACCESS_KEY` on line 629:
```html
<input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
```

### Issue 6: Styling Different on Different Browsers

**Symptom:** Page looks different in Chrome vs Firefox

**Possible Causes:**
1. Browser compatibility issue
2. CSS not fully loaded
3. Browser cache

**Solution:**
1. Clear browser cache (Ctrl+Shift+Delete)
2. Try in incognito/private mode
3. Test in different browsers

### Issue 7: Page Loads Slowly

**Symptom:** Page takes a long time to load

**Possible Causes:**
1. Large image files
2. Too many external resources
3. Slow internet connection

**Solution:**
1. Optimize image sizes
2. Use image compression tools
3. Check browser network tab (F12) to see what's slow

---

## Best Practices

### 1. Always Back Up Before Making Changes

**Before editing:**
```
1. Create a copy of the file (index.html → index_backup.html)
2. Make your changes to the original
3. Keep the backup in case you need to revert
```

### 2. Test Changes Immediately

**After each change:**
```
1. Save the file (Ctrl+S)
2. Refresh the browser (F5)
3. Verify the change looks correct
```

### 3. Use Consistent Naming

**When creating new files or sections:**
```html
<!-- Good: Clear, descriptive names -->
<section id="premium-features">
<div class="feature-card">
<a href="privacy.html">

<!-- Avoid: Vague or inconsistent names -->
<section id="section1">
<div class="card">
<a href="page1.html">
```

### 4. Keep Classes Together

**Good:**
```html
<div class="flex items-center space-x-2 p-4 bg-white rounded-lg">
```

**Avoid:**
```html
<div class="flex
           items-center
           space-x-2
           p-4
           bg-white
           rounded-lg">
```

### 5. Comment Important Sections

**Add comments to mark sections:**
```html
<!-- ===== FEATURES SECTION ===== -->
<section id="features">
    <!-- Your content -->
</section>

<!-- ===== TESTIMONIALS SECTION ===== -->
<section id="testimonials">
    <!-- Your content -->
</section>
```

### 6. Test All Links Regularly

**Weekly checklist:**
- [ ] All navigation links work
- [ ] External links open in new tabs
- [ ] Email links work
- [ ] Internal section links scroll correctly

### 7. Keep Content Updated

**Maintain:**
- [ ] Current contact information
- [ ] Active social media links
- [ ] Updated testimonials
- [ ] Fresh blog content

### 8. Mobile Responsive Testing

**Test on:**
- [ ] Desktop (1920px wide)
- [ ] Tablet (768px wide)
- [ ] Mobile (375px wide)

**Use browser DevTools:**
1. Press F12
2. Click device toggle button
3. Select different device sizes

### 9. Use Meaningful Alt Text for Images

```html
<!-- Good -->
<img src="image.jpg" alt="John Lee Hooker playing guitar in 1960s">

<!-- Avoid -->
<img src="image.jpg" alt="image">
```

### 10. Keep File Sizes Reasonable

**Optimize images:**
- Use tools like [TinyPNG](https://tinypng.com)
- Compress before uploading
- Use appropriate formats (JPG for photos, PNG for graphics)

---

## Quick Reference Guide

### File Locations - Key Sections

| Section | Line Numbers | Element |
|---------|--------------|---------|
| Header/Nav | 64-101 | Navigation menu |
| Hero | 107-135 | Main banner |
| Features | 133-314 | 3 feature cards |
| Benefits | 305-387 | 3 benefit cards |
| CTA Banner | 362-372 | Call-to-action |
| Testimonials | 397-530 | 4 reviews |
| FAQ | 461-570 | 5 questions |
| About | 576-620 | Story & mission |
| Newsletter | 640-650 | Email signup |
| Contact Form | 654-720 | Contact form |
| Footer | 721-750+ | Footer content |

### Common Tailwind Classes

```html
<!-- Text Sizes -->
text-sm, text-base, text-lg, text-xl, text-2xl, text-3xl, text-4xl, text-5xl, text-6xl

<!-- Spacing (Padding) -->
p-2, p-4, p-6, p-8, p-12, p-16

<!-- Spacing (Margin) -->
m-2, m-4, m-6, m-8, m-12, m-16
mb-4 (margin bottom), mt-8 (margin top), ml-4 (margin left), mr-4 (margin right)

<!-- Colors -->
text-white, text-gray-900, text-purple-600, text-pink-600
bg-white, bg-gray-50, bg-purple-600

<!-- Flexbox -->
flex, items-center, justify-center, justify-between, space-x-4, space-y-2

<!-- Grid -->
grid, grid-cols-1, grid-cols-2, grid-cols-3, gap-8

<!-- Borders -->
border, border-gray-200, rounded-lg, rounded-2xl, rounded-full

<!-- Responsive -->
md:text-5xl, lg:text-6xl, md:grid-cols-2, lg:grid-cols-3
```

### Common Edits Checklist

- [ ] Page title (Line 8)
- [ ] Meta description (Line 7)
- [ ] Logo text (Line 68)
- [ ] Hero title (Line 111)
- [ ] Hero subtitle (Line 117)
- [ ] Feature titles & descriptions (Lines 161-314)
- [ ] CTA button links (Lines 128, 365)
- [ ] Testimonials (Lines 433-530)
- [ ] FAQ content (Lines 470-570)
- [ ] About section text (Lines 576-620)
- [ ] Footer links (Lines 660-698)
- [ ] Contact email (Lines 701, 710)
- [ ] Social media links (Lines 701-718)

---

## Support Resources

### Learning Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **HTML Guide:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS Guide:** https://developer.mozilla.org/en-US/docs/Web/CSS
- **Font Awesome Icons:** https://fontawesome.com/icons

### Tools

- **Browser DevTools:** F12 (inspect elements, debug)
- **Color Picker:** https://www.color-hex.com
- **Image Optimizer:** https://tinypng.com
- **Icon Library:** https://fontawesome.com

### Getting Help

If you encounter issues:

1. **Check the browser console** (F12 → Console tab) for error messages
2. **Search for the error message** online
3. **Review the relevant section** of this guide
4. **Compare with the original code** to spot differences
5. **Contact support** if issues persist

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your John Lee Hooker Legacy landing page. Remember to:

- Always back up before making major changes
- Test frequently
- Keep your content updated
- Follow the Tailwind CSS conventions
- Use meaningful links and alt text

Happy customizing! 🎵