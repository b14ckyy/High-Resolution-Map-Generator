## High-Resolution Map Tile Generator

This is a web-based tool for generating and exporting 100x100 PNG map tiles from high-resolution map providers, designed for RC pilots and hobbyists using Ethos or Yaapu mapping widgets on their radios. It enables quick selection of a flying area and direct download of compatible map tiles to your radio’s SD card or as a ZIP file for later transfer.

---

### Supported Map Providers and Types

- **Providers:**
  - OSM (OpenStreetMap, standard map, non high-res)
  - ESRI (High-Res Satellite and Street)
  - Google (High-Res Satellite, Street, Hybrid)

- **Map Types:**
  - Street
  - Satellite
  - Hybrid (Satellite + Labels, where available)

---

### Key Features

- **Web-based, No Installation:** Download and open the HTML file in your browser.
- **Area Selection:** Draw a rectangle on the map to select your area of interest.
- **Editing Tools:** Edit or clear the selected area easily.
- **Measurement Tool:** Measure distances directly on the map.
- **Full Screen Mode:** Expand the map for easier area selection.
- **Mobile Device Compatibility:** Responsive design for phones and tablets.
- **Settings Memory:** Option to remember your settings for future sessions.
- **Restore Defaults:** Quickly reset all settings to defaults.
- **Zoom Adjustment:** Set minimum and maximum zoom levels for tile export.
- **Search Box:** Find your flying field or any location by name.
- **Geolocation:** Center the map on your current location (browser permission required, session limited to 10 seconds for security).
- **Output Targets:**
	- **[b14ckyy ETHOS Mapping Widget](https://github.com/b14ckyy/ETHOSMappingWidget-Revisited):**
	 - Output path: `/bitmaps/ethosmaps/maps/{Provider}/{MapType}/{Zoom}/{X or Y}/{Y or X}.png`
	- **[Yaapu Widget](https://github.com/yaapu/EthosMappingWidget/tree/main):**
	 - Output path: `/bitmaps/yaapu/maps/{GoogleMapType}/{Zoom}/{Y}/s_{X}.png`
	 - **Note:** For Yaapu, regardless of the selected provider (including ESRI or OSM), the output folder will always use the "Google" naming convention (`GoogleMap`, `GoogleSatelliteMap`, or `GoogleHybridMap`). This is required for compatibility with the Yaapu widget. For example, if you select ESRI as the provider and Satellite as the map type, the output will still be placed in `/bitmaps/yaapu/maps/GoogleSatelliteMap/...` even though the tiles are from ESRI.
- **Direct SD Card Sync:** If your browser supports the File System Access API, write tiles directly to your SD card.
- **ZIP Download Fallback:** If SD card access is not available, the tool will offer a ZIP download for manual transfer.

---

### Syncing Behavior

- **With SD Card Connected:** Clicking “Sync to SD Card” writes the tiles directly to the SD card, creating the correct folder structure for your widget.
- **Without SD Card Connected:** The tool prompts you to download a ZIP file containing the tiles, which you can later extract to your SD card.

---

### Intended Use

This tool is designed for quick, straightforward operation:
- Select your flying area, set your preferences, and export tiles in just a few clicks.
- Ideal for RC pilots who want to prepare maps for their radios with minimal hassle.

---

## How to Use

1. **Download the Tool**
	- Go to the [GitHub repository](https://github.com/MartinovEm/High-Resolution-Map-Generator).
	- Click the green “Code” button and select “Download ZIP”.
	- Extract the ZIP and open `HighResMapDownloader.html` in your browser.

2. **Sync Your Radio/SD Card**
	- (Optional) Click “Link SD Card” to connect your SD card for direct export.

3. **Select Output Target**
	- Choose the widget type based on the Lua script installed on your radio (b14ckyy or Yaapu).

4. **Set Project Name**
	- Enter a name for your project folder.

5. **Set Provider and Map Type**
	- Choose your desired map provider and map type.

6. **Set Zoom Levels**
	- Adjust the minimum and maximum zoom levels for the tiles.

7. **Find Your Flying Field**
	- Use the search box to locate your field, or pan/zoom manually.

8. **Select Area of Interest**
	- Draw a rectangle on the map to define the area for tile download.

9. **Edit Area (Optional)**
	- Adjust or clear the selected area as needed.

10. **Sync or Download**
	 - Click “Sync to SD Card” to export tiles.
	 - If SD card is not connected, a ZIP download will be offered.

11. **Transfer to Device**
	 - If you downloaded a ZIP, extract it and copy the files to your radio’s SD card.

12. **Other Features**
	 - Use the measurement tool, full screen mode, and settings memory as needed.

---

## Notes

- **Geolocation:** The app can center the map on your current location, but for security reasons, browser geolocation permission is only requested for 10 seconds per session.
- **Yaapu Output Folders:** Even when using ESRI or OSM as the provider, the Yaapu output folders will always be named as if they are Google map types. This is required for Yaapu compatibility.

---

For questions or issues, please open an issue on the [GitHub repository](https://github.com/MartinovEm/High-Resolution-Map-Generator/issues).