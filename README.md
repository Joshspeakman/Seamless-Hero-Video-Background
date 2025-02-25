# Seamless Hero Video Background

A responsive and customizable hero section with a seamless YouTube video background that integrates perfectly into any website without showing typical YouTube controls or interfaces. This component automatically hides YouTube controls and overlays for a clean, professional appearance.



## Features

- **Seamless YouTube Integration**: Embeds YouTube videos as full-width background with no visible player interface
- **Control-Free Display**: Completely hides YouTube controls and branding for a truly seamless appearance
- **Responsive Design**: Adapts perfectly to all screen sizes from mobile to 4K displays
- **Customizable Call-to-Action**: Easily modify the CTA button style, text, and link
- **Adjustable Overlay**: Control the darkness/opacity of the video overlay
- **Smooth Animations**: Elegant fade-in transitions when the page loads
- **Mobile Optimization**: Special handling for smaller screens with customizable behavior

## Installation

1. Copy the HTML, CSS, and JavaScript code into your website
2. Include Font Awesome for the button icons: `<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>`
3. Customize as needed (see customization section below)

## Usage

```html
<!-- Hero Video Background Component -->
<header class="hero-video-header">
  <div id="video-container">
    <!-- YouTube iframe - Change video ID in the src URL -->
    <iframe 
      src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1&mute=1&controls=0&loop=1&playlist=YOUR_VIDEO_ID&playsinline=1&rel=0&modestbranding=1&iv_load_policy=3" 
      frameborder="0" 
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
      allowfullscreen
    ></iframe>
    <!-- Transparent overlay -->
    <div id="transparent-overlay"></div>
  </div>
  <div id="black-overlay"></div>
  <div class="content-container">
    <div id="cta-container">
      <!-- Call to action button - Change href to update button link -->
      <a href="/your-link-here/" id="cta-button" class="cta-button">
        <!-- Button icon - Change class to use a different Font Awesome icon -->
        <i class="fas fa-shopping-cart cta-icon"></i>YOUR TEXT
      </a>
    </div>
  </div>
</header>
```

## Customization

### Change the YouTube Video

Replace `YOUR_VIDEO_ID` in the iframe src URL with your YouTube video ID.

```html
<iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1&mute=1..."></iframe>
```

### Modify Call-to-Action Button

1. **Change the link**: Update the `href` attribute in the anchor tag
2. **Change the text**: Replace "YOUR TEXT" with your desired button text
3. **Change the icon**: Update the class of the `<i>` element to use a different Font Awesome icon

```html
<a href="/your-new-link/" id="cta-button" class="cta-button">
  <i class="fas fa-arrow-right cta-icon"></i>LEARN MORE
</a>
```

### Adjust Overlay Opacity

Modify the background-color rgba value in the CSS to change the overlay darkness:

```css
#transparent-overlay {
  background-color: rgba(0, 0, 0, 0.5); /* 0.5 = 50% opacity black overlay */
}
```

### Color Scheme

Update the color values in the CSS to match your brand:

```css
.cta-button {
  border: 2px solid #YOUR_COLOR;
  color: #YOUR_COLOR;
}

.cta-button:hover {
  background-color: #YOUR_COLOR_WITH_OPACITY;
}
```

## Media Queries

The component includes media queries for different screen sizes:
- Large screens (2560px+)
- Desktop (up to 1440px)
- Small desktop/tablet (up to 1024px)
- Tablet (up to 768px)
- Mobile (up to 900px)

You can adjust these breakpoints and styles to match your design requirements.

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Dependencies

- Font Awesome (for button icons)

## License

MIT License

## Notes

- YouTube's terms of service require some form of attribution. While this component hides the standard YouTube controls for a cleaner design, please ensure you comply with YouTube's terms of service.
- Some mobile browsers have restrictions on autoplay videos. The component includes fallbacks for mobile viewing.
