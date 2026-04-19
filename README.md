# Image Gallery with Lightbox

In this coding exercise, you will build a simple image gallery that allows the user to click on a thumbnail image and view a larger version in a lightbox.

A **lightbox** is a large image overlay that appears on top of the page when an image is clicked. This is a common feature on portfolio sites, travel pages, photography websites, product pages, and many other kinds of websites.

This project is a good example of how HTML, CSS, and simple JavaScript can work together:
- **HTML** creates the page structure
- **CSS** controls the layout and appearance
- **JavaScript** adds the click behavior that opens and closes the lightbox

Even if you're not planning on having a gallery in your final project, this exercise is good practice for combining structure, styling, and interactivity. If your final project *does* include multiple images, this is a feature you may be able to adapt and reuse later.

---

## What You Will Build

In this project, you will create:

- A simple page with a title and short introductory text
- A gallery of images arranged using **CSS Grid**
- A hover effect on the images
- A hidden lightbox overlay
- JavaScript that:
  - opens the lightbox when an image is clicked
  - swaps in the correct larger image
  - closes the lightbox when the X button is clicked
  - closes the lightbox when the dark background is clicked

---

## Files Included

File :

    lightbox-simple/
    │
    ├── index.html
    ├── lightbox.css
    ├── lightbox.js
    ├── reset.css
    │
    └── images/
        ├── smpte.jpg
        ├── indian.jpg
        └── bbc.jpg

---

## What to Pay Attention To

As you work through this coding exercise, focus on these ideas:

### In the HTML
- The gallery images each use the class `.thumbnail`
- The lightbox already exists in the HTML, but starts hidden
- The lightbox contains:
  - a close button
  - an empty image element that JavaScript will update later

### In the CSS
- `.gallery` becomes a **grid container**
- `grid-template-columns: 1fr 1fr 1fr;` creates 3 equal-width columns
- `gap` adds space between images
- the thumbnails are styled to look clean and clickable
- the lightbox uses `position: fixed` to cover the entire screen
- the lightbox uses Flexbox to center its content

### In the JavaScript
- `querySelectorAll('.thumbnail')` selects all gallery images
- `addEventListener('click', ...)` is used to respond to user clicks
- the `src` and `alt` of the lightbox image are updated dynamically
- the lightbox is shown and hidden using `style.display`

---

## How It Works (Big Picture)

1. The page loads and the gallery images are visible
2. The lightbox is hidden (`display: none`)
3. When a thumbnail is clicked:
   - JavaScript copies the image source (`src`)
   - JavaScript copies the alt text
   - the lightbox is displayed
4. When the user clicks the X or the dark background:
   - the lightbox is hidden again

---

## Tips

- **All of the images in your gallery should be the same size**
  - If they're different dimensions the grid will look uneven
- Test your page frequently as you work

- If something is not working, check:
  - spelling of class names and IDs
  - file paths
  - missing semicolons or brackets

---

## Optional Ideas

If you want to experiment, you could try:

- Adding more images to the gallery
- Changing the number of columns
- Adjusting the hover effect
- Styling the lightbox differently
- Adding captions below the images

