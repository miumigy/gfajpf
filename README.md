# Simple Green Field Analysis by Japan Prefecture

This is a browser-based, single-file application for **green field analysis** (GFA) in Japan using 46 prefectural capital cities (excluding Okinawa). It enables users to:

- Select demand sites (randomly or manually)
- Set the number of warehouse facilities (k)
- Solve the facility location problem using the **HiGHS optimizer (WASM)**
- Visualize optimized warehouse placement and assignments
- Fetch and display realistic road routes via **OSRM API**
- Ensure that facility candidates are placed only on land (with sea/mask exclusion)

---

## 🔧 Features

- 📍 **Demand Sites**: Choose from 46 prefectures
- ⚙️ **HiGHS Optimization**: Mixed Integer Programming (MIP) solving in-browser
- 🗺 **Map Visualization**: Powered by [Leaflet](https://leafletjs.com)
- 🚗 **Route Overlay**: Fetch real road paths using OSRM
- 🌏 **Land-Only Filtering**: Includes custom landmask logic using Turf.js

---

## 🚀 How to Use

1. Open the HTML file in a modern browser (no server needed).
2. Select demand sites (manually or click "Random Select").
3. Set number of warehouse sites (e.g., 4).
4. Click "Optimize" to run HiGHS and show optimal placement.
5. Click "Search Routes" to overlay real road routes (via OSRM).

---

## 📦 Dependencies

- [Leaflet.js](https://leafletjs.com/)
- [HiGHS WASM](https://github.com/ERGO-Code/HiGHS)
- [Turf.js](https://turfjs.org/)
- [OSRM API](http://project-osrm.org/)

These libraries are loaded via CDN — no installation required.

---

## 📁 File Structure

This project is a **single HTML file** and contains:

- Embedded `<style>` and `<script>`
- JSON-encoded land polygons and bay masks
- LP model generation and MIP solving
- DOM interaction for configuration

---

## 📜 License

This project is released under the MIT License.

---

## 🙏 Acknowledgements

- OSRM for free routing API
- HiGHS team for a powerful open-source solver
- Leaflet for great map rendering
- Turf.js for spatial computation utilities

---

## 🗾 Author Note

This tool was designed as an educational and planning aid for logistics and supply chain visualization in Japan. Inspired by simplicity and direct interaction, it allows users to experiment with optimization and mapping — all within a self-contained browser environment.
