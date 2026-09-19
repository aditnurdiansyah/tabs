# Tabs

## Project Overview

This project is a simple **Tabs Interface** built using HTML, CSS, and JavaScript. The main objective is to create an interactive tab component that allows users to switch between multiple content sections without reloading the page.

The project focuses on practicing essential frontend concepts such as DOM manipulation, JavaScript event handling, CSS classes, button states, content visibility, external font integration, favicon configuration, SEO metadata, and Open Graph metadata.

The project also includes a basic asset structure that can be extended for future frontend projects.

## Project Requirements

- **Tab Navigation**
  Create multiple tab buttons that allow users to switch between different content sections.

- **Interactive Tab Content**
  Display only the selected tab's content while hiding the other sections.

- **Active Tab State**
  Apply a visual active state to the currently selected tab.

- **JavaScript Integration**
  Use JavaScript to control tab switching and dynamically update the interface.

- **CSS Styling**
  Use CSS to style the tab navigation, active state, hover state, content area, and images.

- **SEO Meta Tags**
  Include basic metadata such as description, keywords, and author information.

- **Open Graph Tags**
  Include Open Graph metadata for optimized link previews when the page is shared.

- **Favicon**
  Include favicon assets for browser and device recognition.

- **Google Fonts**
  Use the Rosarivo font from Google Fonts for the website typography.

## Features

### 1. Four Interactive Tabs

The interface contains four tabs:

- First Tab
- Second Tab
- Third Tab
- Fourth Tab

Each tab is connected to its own content section.

### 2. Default Tab

The first tab is displayed when the page is initially loaded.

JavaScript also initializes the first `.tab-content` element when the DOM has finished loading.

### 3. Active Tab Indicator

The selected tab receives the `.active` CSS class, which changes its appearance and adds a bottom border to indicate the current tab.

### 4. Hover Effect

Tab buttons include a hover state that changes the background and applies rounded top corners.

### 5. Responsive Image

The image inside the first tab uses:

```css
max-width: 100%;
height: auto;
```

This allows the image to scale within its container.

### 6. SEO and Social Sharing

The project includes:

- Meta description
- Meta keywords
- Author metadata
- Open Graph type
- Open Graph URL
- Open Graph title
- Open Graph description
- Open Graph image

## Technologies Used

- **HTML5** — Structure and content
- **CSS3** — Layout and visual styling
- **JavaScript** — Tab interaction and DOM manipulation
- **Google Fonts** — Rosarivo typography
- **Open Graph** — Social media link preview metadata
- **Favicon** — Browser and device branding

## Project Structure

```text
tabs/
├── assets/
│   ├── favicon/
│   │   ├── android-chrome-192x192.png
│   │   ├── android-chrome-512x512.png
│   │   ├── apple-touch-icon.png
│   │   ├── favicon-16x16.png
│   │   ├── favicon-32x32.png
│   │   ├── favicon.ico
│   │   └── favicon.svg
│   ├── images/
│   │   └── placeholder.png
│   └── open-graph/
│       ├── aditnurdiansyah-full-stack-developer-og.jpg
│       └── aditnurdiansyah-full-stack-developer-og.pdf
├── css/
│   └── style.css
├── js/
│   └── script.js
├── index.html
└── README.md
```

## How It Works

The tab interface uses a simple JavaScript function:

```javascript
function openTab(evt, tabName) {
  var tabContent = document.querySelectorAll('.tab-content');
  tabContent.forEach(content => content.style.display = 'none');

  var tabLinks = document.querySelectorAll('.tab-link');
  tabLinks.forEach(link => link.classList.remove('active'));

  document.getElementById(tabName).style.display = 'block';
  evt.currentTarget.classList.add('active');
}
```

When a tab button is clicked, the function:

1. Finds all elements with the `.tab-content` class.
2. Hides all tab contents.
3. Finds all elements with the `.tab-link` class.
4. Removes the `.active` class from every tab.
5. Displays the selected tab content.
6. Adds the `.active` class to the clicked tab.

This creates a simple single-page tab navigation experience without requiring a page reload.

## HTML Structure

The main interface is organized into a `.tabs` container containing two major parts:

```html
<main class="tabs">
  <div class="tab-links">
    <!-- Tab buttons -->
  </div>

  <div class="tab-content" id="Tab1">
    <!-- Tab 1 content -->
  </div>

  <div class="tab-content" id="Tab2">
    <!-- Tab 2 content -->
  </div>

  <div class="tab-content" id="Tab3">
    <!-- Tab 3 content -->
  </div>

  <div class="tab-content" id="Tab4">
    <!-- Tab 4 content -->
  </div>
</main>
```

Each button uses an `onclick` event to call `openTab()` with the corresponding content ID.

## CSS Styling

The project uses a minimal layout with an 80% content width:

```css
.tabs {
  width: 80%;
  margin: 0 auto;
}
```

The tab buttons are arranged horizontally using Flexbox:

```css
.tab-links {
  display: flex;
}
```

The active tab is visually differentiated using:

```css
.tab-link.active {
  border-bottom: 2px solid #000;
  border-radius: 5px 5px 0 0;
  background: #f4f4f4;
}
```

The content areas use a light background and padding:

```css
.tab-content {
  display: none;
  padding: 20px;
  background: #f4f4f4;
}
```

## How to Use

No build tools or package installation are required.

### 1. Clone the Repository

```bash
git clone https://github.com/aditnurdiansyah/tabs.git
```

### 2. Navigate to the Project

```bash
cd tabs
```

### 3. Open the Website

Open `index.html` directly in a modern web browser.

Alternatively, use the **Live Server** extension in Visual Studio Code for local development.

## Customization

### Change Tab Names

Modify the button labels inside `index.html`:

```html
<button class="tab-link active" onclick="openTab(event, 'Tab1')">
  First Tab
</button>
```

The text can be replaced with any section name, such as:

```html
<button class="tab-link active" onclick="openTab(event, 'Tab1')">
  About
</button>
```

### Change Tab Content

Replace the content inside each `.tab-content` element:

```html
<div class="tab-content" id="Tab1">
  <h2>Content for Tab 1</h2>
  <p>Your content goes here.</p>
</div>
```

### Add More Tabs

To add another tab:

```html
<button class="tab-link" onclick="openTab(event, 'Tab5')">
  Fifth Tab
</button>

<div class="tab-content" id="Tab5">
  <h2>Content for Tab 5</h2>
  <p>This is the content of Tab 5.</p>
</div>
```

The button's second argument must match the `id` of its corresponding content section.

### Change the Visual Style

The main styles can be modified in:

```text
css/style.css
```

You can customize:

- Width
- Padding
- Background colors
- Border colors
- Border radius
- Typography
- Hover effects
- Image sizing

## Current Implementation Notes

The current project is intentionally simple and focuses on the core functionality of a tab component.

The current implementation includes:

- Four static tabs
- JavaScript-based tab switching
- Active tab styling
- Hover styling
- Basic responsive image behavior
- SEO metadata
- Open Graph metadata
- Favicon assets
- Google Fonts

The current project does not include:

- A JavaScript framework
- Backend integration
- Database integration
- Dynamic data loading
- URL/hash-based tab navigation
- Persistent tab state
- Advanced keyboard navigation
- ARIA tab roles and keyboard behavior
- Automated tests
- A build system or package manager

## Accessibility Considerations

The project currently uses native `<button>` elements for tab controls, which provides a good foundation for keyboard interaction.

For a more complete accessible tabs implementation, future improvements could include:

- `role="tablist"`
- `role="tab"`
- `role="tabpanel"`
- `aria-selected`
- `aria-controls`
- `aria-labelledby`
- Arrow-key navigation between tabs
- Proper focus management
- Handling `Home` and `End` keyboard navigation

These improvements would make the component more closely follow the WAI-ARIA Tabs pattern.

## SEO and Open Graph

The project already contains basic SEO and social sharing metadata.

Example:

```html
<meta
  name="description"
  content="Personal portfolio of Adit Nurdiansyah, a Full Stack Developer."
>

<meta property="og:type" content="website">
<meta property="og:url" content="https://aditnurdiansyah.my.id">
<meta property="og:title" content="Adit Nurdiansyah - Full Stack Developer">
<meta
  property="og:description"
  content="Single Page CV of Adit Nurdiansyah, a Full Stack Developer."
>
```

The project also includes an Open Graph image under:

```text
assets/open-graph/
```

This provides a foundation for better previews when the page URL is shared on supported platforms.

## Browser Compatibility

The project uses standard HTML, CSS, and JavaScript features that are supported by modern browsers.

Recommended browsers include:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

## Future Improvements

Potential improvements include:

- Implement a fully accessible ARIA Tabs pattern.
- Add keyboard arrow navigation.
- Add smooth tab transition animations.
- Add responsive mobile tab scrolling.
- Use JavaScript event listeners instead of inline `onclick` handlers.
- Add URL hash support so individual tabs can be linked directly.
- Persist the selected tab using `localStorage`.
- Add icons to tab buttons.
- Add dynamic tab generation from JavaScript data.
- Add automated testing.
- Improve semantic relationships between tabs and tab panels.
- Add a reusable tab component structure for larger projects.

## Conclusion

This project provides a simple and practical implementation of an interactive tab interface using fundamental web technologies.

By completing this project, the developer gains practical experience with **HTML structure, CSS Flexbox, CSS states, JavaScript DOM manipulation, event handling, content visibility, SEO metadata, Open Graph integration, favicon configuration, and external font integration**.

The project can serve as a foundation for building more advanced reusable UI components and can later be extended with accessibility improvements, animations, URL-based navigation, persistent state, and dynamic content.

## Repository

This project is available on GitHub:

https://github.com/aditnurdiansyah/tabs
