AMOC - DAM (Daily Analysis Monitor) v1.7
A high-performance, cross-platform desktop application built in Rust for analyzing and visualizing Sea Surface Temperature (SST) data from NetCDF files, specifically tailored for monitoring the Atlantic Meridional Overturning Circulation (AMOC).

🚀 Overview
AMOC - DAM provides researchers and climate enthusiasts with a streamlined interface to process OSISAF NetCDF datasets. The app automates the extraction of temperature data across specific North Atlantic latitudes (40°N to 65°N) at a fixed longitude, providing immediate visual feedback through interactive plotting and data grids.

✨ Key Features
Automated NetCDF Discovery: On startup, the app automatically scans the local directory for relevant .nc files containing "OSISAF" in the filename.

Multithreaded Processing: Data extraction and analysis run on a background thread to keep the UI responsive, featuring a real-time progress bar.

Scientific Plotting: Utilizes egui_plot to render SST (°C) against Latitude (N) with a fixed scale to ensure scientific consistency.

Detailed Data Grid: A scrollable, striped data table for precise reading of temperature values at specific coordinates.

Native File Dialogs: Easily browse and select specific NetCDF files using a native system explorer.

🛠️ Technical Stack
Language: Rust

GUI Framework: eframe / egui (Immediate mode GUI)

Data Format: NetCDF (Network Common Data Form)

Concurrency: std::sync (Arc, Mutex) and std::thread

File Handling: rfd (Rust File Dialog)

📋 Requirements
To compile this project, you will need:

Rust Toolchain (Cargo, rustc)

NetCDF C Libraries (The netcdf crate requires the underlying C library installed on your system: libnetcdf-dev on Ubuntu/Debian or netcdf via Homebrew on macOS).

🖥️ Usage
Place your .nc (NetCDF) files in the application folder or use the "Abrir Ficheiro" button.

The app targets the North Atlantic corridor (Longitude ~15.0° W).

The graph will automatically populate with the Sea Surface Temperature gradient from 40°N to 65°N.

Developed by
Adelino Saldanha - www.adelinosaldanha.site
