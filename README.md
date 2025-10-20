# SVG to XAML Converter

Client‑side tool to turn SVG into XAML (WPF/UWP/MAUI and other XAML frameworks).

- Open `index.html`
- Drop or paste an SVG
- XAML is generated instantly — copy or download

Works entirely in the browser (no build/server). License: MIT.

## Pages

- SVG → XAML: `index.html` — Convert SVG to XAML with live preview and download.
- SVG → Bitmap: `svg-to-bmp.html` — Batch-convert SVGs to BMP with size presets or custom size.

## Key functions (XAML page)

- `convertSvgToXaml(svgCode)`: Parses SVG and builds XAML (`Path`, `Ellipse`, `Rectangle`, `Line`, `TextBlock`), including styles and transforms.
- `updateXamlPreview()`: Renders the generated XAML back into an SVG preview for quick visual verification.
- `extractStyles(element)` + `applyStylesToXaml(styles)`: Maps SVG fill/stroke/opacity to XAML attributes.
- `convertTransform(transform)`: Converts `translate/scale/rotate` to XAML transform elements.
- `convertColor(color)` and `convertXamlColorToSvg(xamlColor)`: Handles color formats (hex, rgb/rgba, `#AARRGGBB`).
- `downloadFile(content, filename)`: Utility to download the XAML result.

## Key functions (Bitmap page)

- `convertAllFiles()`: Orchestrates batch conversion with progress UI and results list.
- `convertSVGToBMP(file)` → `processSVGToBMP(svgData, fileName)`: Draws SVG on canvas (with optional aspect ratio) and prepares BMP.
- `canvasToBMP(canvas)`: Creates a 24‑bit BMP blob (proper headers, row padding, BGR order).
- `downloadFile(index)` / `downloadFileByBlob(blob, name)` / `downloadAllFiles()`: Single and bulk downloads (ZIP via JSZip).
- `addFiles(files)` + `updateFilesDisplay()` + `createFileItem(file, index)`: File intake and UI list management.
- Size and layout: `handleSizePresetClick`, `handleCustomSizeChange`, `handleAspectRatioChange`, `getCurrentSize`.