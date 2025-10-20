# SVG to XAML Converter

A simple, client-side web application that converts SVG icons to XAML format compatible with WPF, UWP, and other XAML-based applications.

## Features

- Simple, streamlined interface with minimal tabs
- Drag and drop or click to select SVG files
- Automatic conversion on file upload - no need to click convert
- Clean side-by-side preview of both SVG and XAML
- Convenient download button right under the XAML preview
- Real-time conversion as you type SVG code
- Works entirely in the browser - no server-side processing required

## Supported SVG Elements

The converter handles the following SVG elements:

- Paths (`<path>`)
- Circles (`<circle>`)
- Ellipses (`<ellipse>`)
- Rectangles (`<rect>`)
- Lines (`<line>`)
- Polylines (`<polyline>`)
- Polygons (`<polygon>`)
- Text (`<text>`)
- Groups (`<g>`)

## Supported SVG Attributes

The converter preserves the following attributes:

- Fill color
- Stroke color and width
- Opacity
- Transformations (translate, scale, rotate)
- Font properties (for text elements)

## How to Use

1. Simply open the `index.html` file in your web browser.
2. Use the default "Drop SVG File" tab:
   - Drag and drop an SVG file onto the drop zone, or
   - Click anywhere in the drop zone to select a file
3. Or switch to the "Paste SVG Code" tab to paste SVG code directly
4. The app will automatically convert your SVG to XAML and show both previews side-by-side
5. Click the "Download XAML" button under the XAML preview to save the file

## Compatibility

The generated XAML is designed to work with:

- Windows Presentation Foundation (WPF)
- Universal Windows Platform (UWP)
- Xamarin.Forms
- MAUI
- Other XAML-based frameworks

## Local Development

No build process is required. Just clone the repository and open the `index.html` file in a browser.

```
git clone https://github.com/yourusername/svg-to-xaml.git
cd svg-to-xaml
```

Then open `index.html` in your preferred browser.

## License

MIT 