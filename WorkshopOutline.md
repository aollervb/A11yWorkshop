# Mobile Screen Readers Workshop - Speaker Notes

## Introduction (3 mins)
- Quick overview of mobile accessibility importance
    1. Screen readers are necessary for blind people, important for partially-sighted users and helpful for people with reading disorders.
    2. It is hard to teach about web accessibility without talking about screen readers. Screen readers has become for web accessibility what wheel chairs is for accessibility. Even though it is a myth that accessibility is just for blind or partially-sighted users, screen reader support is a mandatory topic.
- What we'll cover today
- Goal: Understand screen readers and common issues

## Screen Readers Quick Guide (5 mins)
- Quick demo of three main readers:
  * iOS VoiceOver: Triple-click side button
  * Android TalkBack: Quick Settings or volume keys
  * Fire VoiceView: Press power until tone + 2 fingers
- Basic gesture: Swipe to navigate, double tap to select

## Key WCAG/CCR Rules (5 minutes)

### 1. Alt Text (WCAG 1.1.1) - 1.5 mins
Images must have descriptive alt text for screen readers

```html
❌ Inaccessible:
<img src="book.jpg">

✅ Accessible:
<img src="book.jpg" alt="The Way of Kings book cover">
```

Key Points:
- Meaningful images need alt text
- Decorative images use alt=""
- Avoid "image of" or "picture of"

### 2. Document Structure (WCAG 1.3.1) - 1.5 mins
Proper semantic structure helps screen reader navigation

```html
❌ Inaccessible:
<div class="header">
<h3>Main Title</h3>

✅ Accessible:
<header role="banner">
<h1>Main Title</h1>
```

Key Points:
- Use proper heading hierarchy (h1 → h2 → h3)
- Use semantic HTML (header, nav, main)
- Include proper landmarks

### 3. Form Labels (WCAG 3.3.2) - 1 min
Forms must be properly labeled for screen reader users

```html
❌ Inaccessible:
<input type="text" placeholder="Enter name">

✅ Accessible:
<label for="name">Full Name</label>
<input id="name" type="text">
```

Key Points:
- Every input needs a label
- Mark required fields
- Provide clear error messages

### 4. ARIA Usage (WCAG 4.1.2) - 1 min
Use ARIA properly to enhance accessibility

```html
❌ Inaccessible:
<button role="button">Click</button>
<a href="/" role="link">Home</a>

✅ Accessible:
<button aria-expanded="false">Menu</button>
<a href="/">Home</a>
```

Key Points:
- Don't duplicate native roles
- Use ARIA for states and properties
- Keep it simple and meaningful

## Demo Notes
- Show examples in test pages
- Point out issues in inaccessible version
- Highlight fixes in accessible version
- Discuss real-world impact

## Interactive Elements
- Have participants spot issues
- Compare accessible vs inaccessible versions
- Discuss how it feels using screen reader

## Resources
- WCAG Guidelines: https://www.w3.org/WAI/WCAG21/quickref/
- Test Pages: https://aollervb.github.io/A11yWorkshop/
```