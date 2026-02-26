# 🌊 MSDAM - Multi Source Data Analysis Monitor (v1.9.7)

**A high-performance scientific suite built in Rust for Atlantic Meridional Overturning Circulation (AMOC) monitoring.**

MSDAM is a specialized tool designed to bridge the gap between complex satellite raw data (`.nc` files) and climate research. It provides an intuitive way to analyze Sea Surface Temperature (SST) and Sea Level Anomaly (MSL) across the North Atlantic corridor.

---

## 🚀 Overview
MSDAM (formerly AMOC-DAM) allows researchers and climate enthusiasts to process NetCDF datasets from **NASA (JPL)**, **Copernicus (Marine)**, and **IFREMER (OSI-SAF)**. The application automates data extraction across critical North Atlantic latitudes (**40°N to 65°N**) at a fixed longitude (**15.0°W**).

## ✨ Key Features
* **Multi-Source Integration:** Native support for NASA (MUR-Infrared), Copernicus (Altimetry/MSL), and IFREMER (VIIRS/SAT).
* **Hybrid Toolset:** Includes both a **Graphical Interface (GUI)** for visualization and a **Console Version** for quick terminal-based audits.
* **Scientific Consistency:** Uses `egui_plot` with auto-bounds for SST (°C) and Sea Level (m), ensuring data integrity.
* **Security & Integrity:** Integrated **SHA1 hashing** for every file processed to ensure data traceability.
* **Linux Optimized:** Specifically tailored for high performance on **openSUSE Tumbleweed** and rolling-release distributions.

---

## 🖥️ Versions & Usage

### 1. GUI Version (`gui_multi`)
The flagship version with real-time plotting and interactive data grids.
* **How to run:**
    1. Give execution permission: `chmod +x gui_multi`
    2. Run it: `./gui_multi`
* **Interaction:** Use the "📂 Abrir NetCDF" button to select any compatible file. The app detects the provider automatically.

### 2. Console Version (`amoc_console`)
A lightweight, lightning-fast terminal tool for quick data extraction.
* **How to run:**
    1. Give execution permission: `chmod +x amoc_console`
    2. Run it: `./amoc_console`
* **Output:** Direct ASCII/Table output of the coordinates and values.

---

## 🛠️ Technical Stack
* **Language:** Rust 🦀
* **GUI:** eframe / egui (Immediate mode GUI)
* **Data Format:** NetCDF-4 (via `netcdf` crate)
* **Integrity:** SHA-1 Checksumming
* **Platform:** Linux (Tested on openSUSE Tumbleweed x64)

## 📋 Requirements (Linux)
To run the pre-compiled binaries, ensure you have the NetCDF C libraries installed:
```bash
# On openSUSE:
sudo zypper install libnetcdf19  # or equivalent netcdf-devel

# On Ubuntu/Debian:
sudo apt-get install libnetcdf-dev

🦖 License & Usage
Freeware for Science, Research & Home Use. This tool is provided as-is for the advancement of climate change monitoring and oceanographic research.

🌐 Developed by
AS - Adelino Saldanha - www.adelinosaldanha.site
