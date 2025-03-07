# Replaced Elements in HTML

## What Are Replaced Elements?
Replaced elements in HTML are elements whose appearance is controlled by an external source, not by the CSS properties of the element itself. The content of replaced elements is replaced by external resources like images, videos, or embedded content.

### Examples of Replaced Elements:
- `<img>` (Images)
- `<video>` (Videos)
- `<audio>` (Audio)
- `<iframe>` (Embedded content like maps or videos)

```html
<img src="image.jpg" alt="Example Image">
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
```

---

# Optimizing Media Assets

## Common Ways to Optimize Media Assets
1. **Use Compressed Images**: Convert large images to smaller sizes using tools like TinyPNG or ImageOptim.
2. **Choose the Right Format**:
   - JPEG for photos
   - PNG for transparency
   - WebP or AVIF for modern compression
3. **Lazy Loading**: Load images only when they appear in the viewport.
4. **Use Responsive Images**: Provide different sizes using the `srcset` attribute.
5. **Optimize Videos**:
   - Use compressed formats (MP4, WebM)
   - Host videos on external services (YouTube, Vimeo)

```html
<img src="image.jpg" loading="lazy" alt="Lazy Loaded Image">
```

---

# Image Licenses

## Types of Image Licenses
1. **Public Domain (CC0)** - Free to use without attribution.
2. **Creative Commons (CC)** - Different levels of permissions (e.g., CC-BY, CC-BY-SA).
3. **Royalty-Free (RF)** - One-time payment for use.
4. **Rights-Managed (RM)** - Pay per use case.
5. **Editorial Use Only** - Cannot be used for commercial purposes.

```markdown
[![Creative Commons License](https://example.com/cc-license.png)](https://creativecommons.org/licenses/)
```

---

# Scalable Vector Graphics (SVG)

## What Are SVGs?
SVGs are XML-based vector images that scale without losing quality.

## When to Use SVGs?
- Icons, logos, and graphics that require scalability
- When animations or interactivity are needed
- When you want small file sizes for simple graphics

```xml
<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>
```

---

# HTML Audio and Video Elements

## How Do Audio and Video Elements Work?
These elements allow embedding and controlling multimedia in web pages.

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
</audio>

<video controls width="400">
  <source src="video.mp4" type="video/mp4">
</video>
```

### Attributes:
- `controls` - Shows built-in player controls
- `autoplay` - Plays automatically (without user interaction)
- `loop` - Repeats playback
- `muted` - Starts muted

---

# Embedding Videos with `<iframe>`

## How to Embed Videos Using `<iframe>`?
The `<iframe>` tag allows embedding external video content like YouTube.

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>
```

### Attributes:
- `src` - URL of the video
- `width` & `height` - Dimensions of the player
- `allowfullscreen` - Enables fullscreen mode

---

These notes provide a concise reference with explanations and code snippets. You can save and push this markdown file to your GitHub repository!

