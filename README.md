# Bild Quelle Banner

A simple, responsive banner component for embedding in the BILD app as an iframe.

## Overview

This project displays a clickable banner image that links to Google's source preferences page for BILD.de. The banner is designed to be embedded as an iframe within the BILD mobile app.

## Deployment

The page is deployed at:
https://www.bild.de/ig/e1bf1a45-507f-4c02-aeb3-7aa0cf9ea680/index/index.html

## Features

- **Responsive design**: Maximum width of 992px, scales down proportionally on smaller screens
- **Clickable banner**: Opens the Google preferences link in a new tab
- **Dynamic height reporting**: Uses `postMessage` API to communicate iframe height to parent page
- **DAVIZ integration**: Implements the DAVIZ embed-size protocol for proper iframe sizing

## Technical Details

### Height Reporting

The page continuously reports its height to the parent window using:
- `requestAnimationFrame` for accurate post-layout measurements
- `ResizeObserver` to detect size changes
- `postMessage` API with DAVIZ provider format

### Responsive Behavior

- Desktop/tablet: Banner displays at full size (up to 992px wide)
- Mobile: Banner scales down maintaining aspect ratio
- Always positioned at top-left of container

## Files

- `index.html` - Main HTML file with embedded CSS and JavaScript
- `bildquellebanner.png` - Banner image asset
- `README.md` - This file
