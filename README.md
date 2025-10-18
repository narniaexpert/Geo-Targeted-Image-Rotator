# Geo-Targeted-Image-Rotator
A simple, dependency-free image rotator that displays different images based on the user's geographic location. This project is contained within a single HTML file, uses vanilla JavaScript for its logic, and is styled with Tailwind CSS via a CDN.

It is designed to be lightweight, easy to configure, and free of dependencies on services (like Google Fonts) that may be restricted in certain regions, ensuring wider accessibility.

# Features
Geographic Image Targeting: Automatically detects the user's country via their IP address and displays the appropriate ad set.

Multiple Image Formats: Includes examples for responsive 3:1 ratio images as well as fixed-size 336x280 and 300x600 ad units.

Resilient Fallback System: Uses a primary and a secondary geolocation API. If both fail, it gracefully defaults to a specified image set (e.g., USA image).

Easy to Customize: image URLs and targeting logic are stored in a simple configuration object within the JavaScript, making it easy to adapt for your own needs.

Self-Contained: All necessary HTML, CSS, and JavaScript are in a single file for maximum portability.

# How It Works
1. On page load, a JavaScript function calls a primary geolocation API (freegeoip.app) to get the user's location data.

2. If the primary API fails, it automatically calls a fallback API (ipinfo.io) to ensure a high success rate.

3. If both geolocation APIs are unreachable, the rotator defaults to showing the USA-specific images.

4. Based on the returned country code, the script selects the appropriate image set from the image configuration object.

5. The src attributes of the <img> elements on the page are dynamically updated with the selected image URLs, and the images fade in.

# Technologies Used
HTML5

Tailwind CSS (via CDN)

Vanilla JavaScript (ES6+)

# Configuration
Configuration
To customize the image rotator, you only need to edit the <script> section of the image-rotator.html file.

1. Update Image URLs: Modify the images object to point to your image creatives. You can add, remove, or change properties to fit your campaign.
2. Adjust Targeting Logic: The image selection is handled by a simple if/else block within the initializeImageRotator function. You can add more else if conditions to target different countries or regions.

# Usage

No installation is required. Simply download the ad-rotator.html file and open it in any modern web browser.
