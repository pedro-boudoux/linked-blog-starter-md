**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:**
# Notes on Images for Web Design

## Historical Context

- First web photo uploaded by Tim Berners-Lee in 1992 (CERN house band Les Horribles Cernettes)
- Images break up text and enhance visual appeal
- Balance needed between visual content and descriptive text

## Digital Image Basics

### Pixels

- Building blocks of digital images
- Grayscale pixels: Values from 0 (black) to 255 (white)
- Color pixels: Three values (Red, Green, Blue/RGB)
- Example: RGB value 61-80-136 converts to grayscale 92 ((61+80+136)/3)
- Pixels are abstract, size-less elements whose display size depends on device

### Megapixels (MP)

- Describes number of pixels in millions
- Examples:
    - 12MP = ~3000×4000 pixels (4:3 aspect ratio)
    - 24MP = ~5656×4242 pixels (4:3) or 4000×6000 pixels (3:2)
    - 4K TV = 3840×2160 pixels (~8MP)

### Resolution

- Level of visual detail in an image
- Measured as:
    - Pixels per inch (PPI) for digital devices
    - Dots per inch (DPI) for printing
- Low-resolution images appear blocky on high-resolution displays

**Table 5.1: Pixel Density in Common Devices**

|Device|Resolution|PPI|Total pixels|
|---|---|---|---|
|iPhone X, XS|2436 x 1125|458|2,740,500|
|Apple Watch (44mm)|368x448|326|164,864|
|MacBook Air Retina|2560x1600|227|4,096,000|
|Google Pixel 3|1080x2160|443|2,332,800|

### Bits

- 8-bit image: 2^8 (256) colors (grayscale)
- 24-bit image: 8 bits per RGB layer, 2^24 (16,777,216) colors

### Compression

- **Lossy**: Reduces file size by eliminating data; quality loss in details
- **Lossless**: No quality loss but larger file sizes

### Transparency

- Full transparency: Parts of image completely invisible
- Partial transparency: Creates translucent effect
- Supported by GIF, PNG, TIFF formats

## Image Formats

### JPEG/JPG

- Most common web format
- Small file size, fast loading
- 24-bit color depth
- Lossy compression
- May show artifacts (blocky portions) at high compression
- Best for photographs

### PNG

- Lossless format designed to replace GIF
- Supports transparency (including alpha channel)
- No artifacts but larger file sizes
- PNG-8: 256 colors, 1-bit transparency
- PNG-24: 24-bit, 16.8 million colors
- Best for screenshots and graphics

### GIF

- Small file size with 256 colors
- Supports lossless LZW compression
- Supports animation
- Limited colors can cause banding in photographs
- Best for simple animations and graphics

### TIFF

- Very high quality
- Extremely large file size
- Not suitable for web use
- Best for originals/commercial work

**Table 5.2: Strengths and Weaknesses of Common Image Formats**

|Format|Strength|Weakness|Best use?|
|---|---|---|---|
|JPG|small file size, versatile|loss of fine details|full-colour photographs|
|PNG|versatile, transparency|large file sizes, hard to print|graphical elements|
|GIF|small file size, animation|loss of quality in photographs|simple animations, graphics with few colours|
|TIFF|super high quality|huge file size, little browser support|commercial work, original images|

### Newer Formats

#### WebP

- Designed by Google as universal web format
- Lighter than JPEG without visual quality loss
- Supports lossless compression, transparency, animation
- 24-bit, 16.8 million colors
- Not universally supported yet

#### HEIC/HEIF

- Developed by Moving Picture Experts Group (MPEG)
- Debuted on iPhone with iOS 11
- Supports multi-frame images with compression
- Good for HDR, multi-focus, multi-view images

#### SVG

- Scalable Vector Graphics
- XML-based vector format
- Supports interactivity and animation
- Can scale to any dimension without quality loss
- W3C open standard since 1999

## Browser Compatibility

**Table 5.3: Image Format Compatibility by Browser**

|Browser|JPEG|GIF|PNG|APNG|SVG|WebP|
|---|---|---|---|---|---|---|
|Internet Explorer|✓|✓|≥7|-|≥9|-|
|Edge|✓|✓|✓|≥75|✓|✓|
|Chrome|✓|✓|✓|✓|✓|✓|
|Firefox|✓|✓|✓|✓|✓|✓|
|Safari|✓|✓|✓|✓|✓|-|
|Opera|✓|✓|✓|✓|✓|≥11.5|