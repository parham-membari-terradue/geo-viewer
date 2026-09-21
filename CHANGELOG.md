# Changelog

All notable changes to this project will be documented in this file.

## [0.2.0] - 2026-02-22

### Added
- Multi-band support: all bands sent to the webview; band selector dropdown in the bottom bar (hidden for single-band files)
- RGB composite mode with R/G/B band pickers and per-channel percentile stretch; mode selector shown for files with ≥2 bands
- Band count shown in the status bar tooltip
- Histogram panel inside the Statistics section, rendered from already-sorted valid pixel values
- Manual stretch override: Min/Max number inputs below the colorbar with a Reset button; overrides the auto percentile stretch when both values are set
- Loading spinner (pure-CSS animated ring) shown in the canvas area while the file is being parsed
- Export PNG button saves the current canvas view as a lossless PNG
- Ground resolution in the status bar tooltip (m/px for projected CRS, °/px for geographic)
- Full metadata inspector: collapsible panel showing TIFF file directory tags and GeoKeys
- NoData coverage percentage in the Statistics panel
- COG overview loading: large files read from the appropriate overview IFD instead of decompressing the full-resolution image
- Pixel value and geographic coordinates shown in a floating tooltip that follows the cursor instead of a static bar item

### Fixed
- Scroll-wheel zoom now works without holding Ctrl/Cmd
- Scroll-wheel zoom sensitivity normalised across mouse wheel and trackpad so both feel equally responsive

## [0.1.0] - 2026-02-22

### Added
- Initial release
- Custom editor for `.tif`, `.tiff`, `.geotiff` files
- Raster rendering via [geotiff.js](https://github.com/geotiffjs/geotiff.js) — supports LZW, DEFLATE, ZSTD, PackBits, JPEG compressions
- Eight colormaps: Viridis, Plasma, Inferno, Magma, Grayscale, Jet, Terrain, Cool-Warm
- Automatic 2% percentile histogram stretch with configurable clip via `geotiffViewer.stretchPercent`
- Zoom (scroll) and pan (drag) with fit-to-screen on load
- Pixel value and geographic coordinate display on hover
- Statistics panel: min, max, mean, median, standard deviation, valid pixel count
- Colorbar with min/max labels in the bottom bar
- Status bar item showing dimensions, data type, CRS, and compression for the active file
- NoData handling — NoData pixels rendered as transparent
- `geotiffViewer.defaultColormap` setting
