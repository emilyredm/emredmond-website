# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website with a creative rotary phone interface. The site uses a vintage rotary dial as the primary navigation method, where users can dial numbers to access different sections.

## Architecture

### Core Navigation Flow
1. **Landing Page** (`index.html`): Displays a rotary phone image with scroll/swipe-up navigation to enter the dial interface
2. **Rotary Interface** (`rotary.html`): Interactive rotary dial where users can dial numbers 0-9 to navigate to different pages
3. **Content Pages**: Basic HTML pages for different sections (about.html, projects.html, etc.)

### Key Components

**Rotary Dial System**:
- `scripts/rotary.js`: Core dial mechanics using mouse/touch events and CSS transforms
- `styles/rotary.css`: Visual styling for the rotary dial component
- `styles/demo.css`: Layout and animations for the dial interface
- `scripts/zepto.custom.js`: Lightweight jQuery-like library for DOM manipulation

**Page Navigation Mapping**:
```
1 → about.html
2 → projects.html  
3 → blog.html
4 → resume.html
5 → contact.html
6 → press.html
7 → listen.html
8 → read.html
9 → secret.html
0 → portal.html
```

### Technical Implementation

**Interaction Handling**:
- Touch and mouse events for dial rotation
- Scroll and swipe gestures for navigation
- Smooth CSS transitions with fade effects
- Rotation calculations using trigonometry and CSS transforms

**UI State Management**:
- Opacity transitions for page changes
- Scroll position tracking for gesture navigation
- Prevention of double-redirects during transitions

## File Structure

- `index.html` - Landing page with phone image
- `rotary.html` - Main rotary dial interface
- `scripts/` - JavaScript functionality
- `styles/` - CSS styling and animations
- `SVG/` - Vector graphics assets
- `old code/` - Legacy files

## Development Notes

- No build system or package manager - pure HTML/CSS/JS
- Uses Zepto.js (lightweight jQuery alternative) for DOM manipulation
- CSS transforms and transitions for smooth animations
- Touch and mouse event handling for cross-device compatibility
- Responsive design with viewport-based sizing

## Testing

Since this is a static website with no build process, testing is done by:
1. Opening files directly in a browser
2. Testing touch interactions on mobile devices
3. Verifying smooth transitions and animations
4. Checking cross-browser compatibility