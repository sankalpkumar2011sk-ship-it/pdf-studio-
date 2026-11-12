# PDF Studio – Professional PDF Viewer & PDF Maker (Android)

**PDF Studio** is a complete, offline-first, production-ready Android application built with **Kotlin**, **Jetpack Compose (Material Design 3)**, **MVVM + Clean Architecture**, **Room Database**, **DataStore Preferences**, and **Apache PDFBox-Android / Native Android PDF Engines**.

---

## Key Features Included

### 1. Professional Home Dashboard
- **Instant Bilingual Support**: Full English and **हिंदी (Hindi Unicode)** UI and PDF generation.
- **Quick Actions**: Create PDF, Open PDF (Storage Access Framework), and Scan Document.
- **Sections**: Search Bar, Quick PDF Tools Strip, Folders Filter, Recent Files, Starred Files, All PDFs with Live Page Thumbnails, and Device Storage Overview.

### 2. Professional PDF Viewer
- **Reading Modes**: Continuous Vertical Scroll, Horizontal Page Pager, and Single Page View.
- **Zoom & Navigation**: Pinch-to-Zoom, Double-Tap Zoom (`1x -> 2x -> 3x`), Fit to Page, Page Rotation (`90°/180°/270°`), Direct Page Jump, and Page Thumbnails Drawer.
- **Visual Comfort**: Standard Mode, Warm Sepia Reading Mode, Inverted Night Mode, In-App Brightness Control, Full-Screen Immersive Mode, and Portrait/Landscape Orientation Toggle.
- **In-PDF Search & Text Extraction**: Case-sensitive and case-insensitive text search across all pages with match count, snippet highlights, and a selectable Page Text Reader to copy or share text.
- **Bookmarks & Auto-Resume**: Automatically saves and restores the last read page and zoom level; add, view, and jump to bookmarks.
- **Live Annotation & Markup Studio**: Freehand Pen, Highlighter, Underline, Strikethrough, Rectangle, Circle, Arrow, Sticky Notes, Text Notes, Eraser, Undo/Redo, Signature Stamp, and Save/Export Annotated PDF.

### 3. Professional PDF Maker (5 Modes)
- **Images to PDF**: Multi-photo import (zero-permission Photo Picker) and Camera capture, reorder, rotate, crop inset, image scale modes, quality control, and conversion to PDF.
- **Rich Text to PDF (with Hindi Unicode)**: Headings, subheadings, bold, italic, underline, alignment, font families (including bundled `Noto Sans Devanagari`), colors, bullet/numbered lists, and automatic pagination.
- **Create Blank PDF**: A4, A3, A5, US Letter, US Legal, and Custom dimensions with Portrait/Landscape, custom margins, paper colors, and Ruled / Square Grid / Dot Matrix / Plain templates.
- **Scanner to PDF**: Camera capture & scan processing with crop adjustment, rotation, and real pixel filters (Original, Magic Vivid, Grayscale, High-Contrast Black & White).
- **HTML / Document to PDF**: Converts HTML markup and structured text into paginated PDFs.

### 4. Advanced PDF Editor & 20 Built-In PDF Tools
1. **PDF Merger**: Combine multiple PDFs in custom order.
2. **PDF Splitter**: Split by custom page ranges (e.g., `1-2, 3-5`).
3. **PDF Compressor**: Low, Medium, High, and Custom DPI/Quality compression with exact size reduction stats.
4. **PDF Lock (Encrypt)**: 128-bit standard PDF encryption with User/Owner passwords and Print/Copy/Edit restrictions.
5. **PDF Unlock**: Remove password encryption using the authorized password.
6. **PDF Watermark**: Custom text or image watermarks with position, opacity, rotation, size, and page range.
7. **PDF Signature**: Interactive signature drawing pad, Room DB signature storage, and PDF stamping.
8. **Page Organizer**: Reorder, duplicate, delete, insert blank pages, or add image pages.
9. **PDF Rotate**: Rotate individual or all pages.
10. **PDF Crop**: Trim page margins cleanly.
11. **PDF to Images**: Export all PDF pages into high-resolution **PNG** or **JPEG** images.
12. **Images to PDF**
13. **Text to PDF**
14. **Page Numbers**: Add `Page X of Y` numbering.
15. **Header & Footer**: Running headers and footers across pages.
16. **Extract PDF Pages**
17. **Remove PDF Pages**
18. **Add Images to PDF**
19. **PDF Information**: Full metadata, dimensions, encryption status, and byte size.
20. **Print PDF**: Native Android `PrintManager` integration.

### 5. File Manager, Recycle Bin & App Lock Security
- **File Manager**: All Files, Recent, Starred, Folders, and Recycle Bin with 6 sorting modes, Grid/List view, and Multi-Select bulk actions.
- **Recycle Bin**: Restore deleted files, permanently delete, empty bin, and automatic cleanup settings (7, 15, 30 days).
- **App Lock Vault**: SHA-256 salted PIN lock (never stored in plain text), Security Question PIN recovery, Biometric / Device Credential unlock, Auto-Lock on background, and Hide Sensitive File Previews.

---

## Build & Installation Instructions

### Build Debug APK
```bash
gradle assembleDebug
```
- **Output Path**: `app/build/outputs/apk/debug/app-debug.apk`

### Build Release APK & App Bundle
```bash
gradle assembleRelease
gradle bundleRelease
```
- **Release APK Output**: `app/build/outputs/apk/release/app-release.apk`
- **Release AAB Output**: `app/build/outputs/bundle/release/app-release.aab`
- *Signing Note*: The Debug APK is signed with the standard Android debug keystore and is immediately installable on any Android device (Android 7.0+ / API 24–36). For production Play Store distribution, supply your private upload keystore via `KEYSTORE_PATH`, `STORE_PASSWORD`, and `KEY_PASSWORD` environment variables.

### Run Automated Unit & Robolectric Tests
```bash
gradle :app:testDebugUnitTest
```
