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