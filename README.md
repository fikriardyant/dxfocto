# dxfocto
a dxf utility made by curiosity and freetime

## Changelog

- All notable changes to the DXF Utility will be documented in this file.

# Latest Version

## Added
- Area Calculation: Added automatic area calculation (in m² and Hectares) to the Element Details menu when selecting a polygon or closed polyline.
- Unclosed Line Tolerance: Smart detection with a 10-meter tolerance for boundary lines that are almost closed/disconnected, complete with a red (Unclosed) warning.
- Contribute Link: Added a "Contribute" menu in the bottom footer bar that links directly to the GitHub repository fikriardyant/dxfocto.
## Changed
- Mobile Layout Fix: The theme toggle button (Dark/Light) is now combined and aligned with the Config (Gear) button in the top right corner to prevent overlapping on mobile screens.
## Fixed
- Drag-and-Drop Syntax Error: Fixed a syntax error (Unexpected token '[') that caused the browser to freeze due to an invalid array format in the previous update.
- ACI Color Palette: Re-added the missing double quotes (") in the hexadecimal color configuration, ensuring all color layers are extracted correctly.

# Previous Version
## Added

- Offline GeoTIFF Support: Parse and render .tif and .tiff basemaps completely offline. Includes automatic downsampling for images up to 50MB to prevent mobile browser memory crashes.
- Offline KML/KMZ Parsing: Drag and drop Google Earth .kml and .kmz files to view them offline. Automatically preserves layer colors and instantly maps geometries to the global coordinate system (UTM 50N).
- Global Drag-and-Drop: Introduced a full-screen drag-and-drop overlay. Users can drop .dxf, .kml, .kmz, .tif files to view them, or .js files to securely load coordinate configurations.
- Mobile Touch Gestures: Full touchscreen support for the viewer canvas, including 1-finger panning, 2-finger pinch-to-zoom, and tap-to-select for entity details.
- Canvas Rotation & Compass: Added a 2-finger twist gesture to rotate the map. Includes a magnetic compass button in the top right to toggle rotation lock and snap the view back to True North.\
- Desktop Enhancements: Upgraded the desktop UX with a precision crosshair cursor and a real-time mouse coordinate tracker (Easting/Northing) anchored to the bottom-left corner.
- Collapsible Layers Menu: Added a sleek, toggleable "Layers" menu on the top left to manage multiple files without cluttering the screen.
- Dynamic Configuration Loader: Secret coordinate translation logic is now securely loaded via an external, obfuscated config.js file, protecting proprietary math.

## Changed

- Default Viewport: The "Design Viewer" is now the primary, default active tab upon opening the app.
- GPS Tracking Logic: Tapping the GPS button while actively tracking no longer disables the GPS; instead, it instantly centers the camera on the user's current location.
- UI Modernization (Material 3): Completely overhauled the Tailwind CSS color scheme to comply with Android Material 3 (M3) design guidelines, utilizing responsive surface, container, and error tones.
- Configuration Warnings: Replaced intrusive popups with sleek, inline "jiggle" animations and red text warnings if a user attempts to process local coordinates without a loaded configuration.
- White-labeling: Removed specific company/site acronyms from the UI to create a generalized utility.

## Fixed
- Android GPS Timeouts: Fixed a critical bug causing Android browsers to silently fail during cold-starts by replacing standard GPS fetches with a robust watchPosition loop and a 30-second hardware timeout.
- SVG Rendering: Repaired corrupted path data on the "Zoom Extents" icons.
- Canvas Freezing: Resolved an issue where invalid JavaScript interactions prevented canvas elements from responding to touch inputs.
