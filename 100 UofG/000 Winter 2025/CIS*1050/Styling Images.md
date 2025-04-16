**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS Image Styling

## Basic Image Styling Techniques

### Rounded Edges

```css
img {
  border-radius: 8px;
}
```

### Responsive Images

Automatically adjust to fit screen size:

```css
img {
  max-width: 100%;
  height: auto;
}
```

### Image Positioning

#### Center an Image

```css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 70%;
}
```

#### Position from Left Margin

```css
img {
  display: block;
  margin-left: 20px;
}
```

### Transparency

Set image opacity (0.0-1.0):

```css
img {
  opacity: 0.4;
}
```

## Image Filters

CSS offers various filters through the `filter` property. Note that not all browsers support all filters.

### Blur Example

```css
img {
  filter: blur(4px);
}
```

### Common Image Filters

|Filter|Syntax|Description|
|---|---|---|
|Brightness|brightness(%)|0% = black, 100% is the original image, >100% is a brighter image|
|Grayscale|grayscale(%)|0% is the original image, 100% is the completely gray image|
|Contrast|contrast(%)|0% = black, 100% is the original image, >100% adds more contrast|
|Hue Rotation|hue-rotate(deg)|0deg is the original image. The maximum value is 360deg around a colour wheel|
|Invert|invert(%)|0% is the original image. 100% is the image completely inverted|
|Opacity|opacity(%)|0% is the image completely transparent, 100% represents the original image|
|Saturation|saturate(%)|0% = completely unsaturated, 100% is the original image, >100% adds more saturation|
|Sepia|sepia(%)|0% is the original image, 100% represents the image changed to Sepia|
|Drop Shadow|drop-shadow(px px px px color)|Parameters: horizontal shadow, vertical shadow, blur effect (optional), spread value (optional), color (default: black)|
|Blur|blur(px)|A larger value creates more blur (e.g., 4px)|

## Responsive Image Gallery

CSS can create responsive image galleries that rearrange images when the screen is resized.

### Components Typically Used:

- Class for responsive design (`responsive`)
- Class for the gallery structure (`gallery`)
- Class for image descriptions (`desc`)

### Implementation

A gallery implementation typically includes:

- Container elements with appropriate display properties
- Media queries for different screen sizes
- Flexible image dimensions (often percentage-based)
- Consistent spacing and alignment properties