(representing images)
[[Computing]]
#12/10/24

## Binary Quick Recap
For any given number of bits (n), there are 2$^{n}$ possible combinations.

---
## Bitmapped Graphics
- Computers process real-world data by converting it into digital form (patterns of 1s and 0s).
- This differs from analog data, which theoretically allows for infinite accuracy.

---
## How Humans See Images
- We see images by detecting light reflected off objects. Different wavelengths create different colours, with theoretically infinite possible colours. Although humans do see around 16 million colours.
- Digital cameras attempt to capture and approximate these colours for digital use.

---
## Image capture in Digital Cameras
- A camera captures images by breaking them down into a grid of pixels. Each pixel's colour is measured, and the result is converted into binary using an analog-to-digital converter.
- The number of pixels in the grid affects the file size, with more pixels creating larger files.

---
## Understanding Bitmapped (Raster) Graphics

- Bitmapped images are formed from a grid of pixels, with each pixel assigned a colour value.
- The resolution of an image is defined by its width and height in pixels (e.g., 1080x768).
    - 72 dpi (dots per inch) is screen resolution.
    - 300 dpi is typical for print-quality resolution.

---

## Common Bitmap File Types:
- BMP, JPG, GIF, PNG, TIF.

---

## Pixels and Resolution
- The resolution is the width multiplied by the height of an image in pixels (e.g., 1000x1000 pixels = 1 megapixel image).
- The physical size of an image is not defined by its resolution, so resizing an image increases or decreases pixel size but maintains the same resolution.

---

## Color Depth
- Each pixel is given a binary value corresponding to a color.
- More bits per pixel allow for more color combinations:
    - 1 bit = 2 colors
    - 2 bits = 4 colors
    - 8 bits = 256 colors

---

## File Size Calculation
- The size of an image file depends on the number of pixels and color depth.
- For example, a 2-megapixel image with 24-bit color depth requires 6 MB of storage (2 million pixels x 24 bits per pixel = 48 million bits ÷ 8 = 6 MB).

---

## Metadata
- Image files also store metadata such as creation date, pixel dimensions, color depth, and even GPS coordinates of the photo location.

---

## Vector Graphics (A-Level)
- Vector images are composed of geometric shapes instead of individual pixels.
- The properties of each shape, such as its position, fill color, and size, are stored and redrawn mathematically.
- Unlike bitmap images, vector graphics do not pixelate when resized.

---

## Comparing Bitmaps and Vectors
- **Bitmap Graphics**: Made up of pixels; smaller file size; pixelates when resized; common file types include PNG, BMP, JPG.
- **Vector Graphics**: Composed of shapes; larger file size; no loss of quality when resized; common file types include SWF, EPS, SVG.

---
## Conclusion
- Resolution refers to pixel density, not image size.
- Bit depth influences how many colors can be displayed.
- A trade-off exists between image quality and file size.
- Metadata provides additional information about the image.