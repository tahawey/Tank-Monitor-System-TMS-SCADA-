# Web-Based SCADA for Tank Monitoring System (TMS)

A modern, web-based Supervisory Control and Data Acquisition (SCADA) application designed for Tank Monitoring Systems (TMS). This application seamlessly integrates data from major tank gauging providers like **Veeder-Root**, **ProGauge**, and **Honeywell Enraf** to provide real-time monitoring, advanced reporting, and alarm management for fuel and liquid inventory.

## 🚀 Key Features

*   **Multi-Vendor Tank Gauging Support**: Unified interface for Veeder-Root, ProGauge, and Honeywell Enraf devices.
*   **Real-Time Data Acquisition**: Utilizes a custom Node.js service to poll ProGauge devices and extract data from CSV files every minute for near real-time visibility.
*   **Automated Delivery Reports**: Intelligently detects and generates detailed reports for fuel deliveries, including start/end times, volumes, and water levels.
*   **Comprehensive Alarm Management**: Monitors tank conditions and triggers alerts for critical events like low inventory, high water, and leaks.
*   **POS Backoffice Integration**: Automatically pushes delivery and alarm data to major Point-of-Sale (POS) backoffice systems, including **Verifone**, **Passport**, and **NCR**.
*   **Centralized Dashboard**: A clean, intuitive web interface for at-a-glance monitoring of all tank statuses, inventory levels, and active alarms.

## 🛠️ Technology Stack

*   **Backend:** Node.js 
*   **Data Ingestion:** Custom CSV parser & scheduler (for ProGauge)
*   **Frontend:** (e.g., React, Vue.js, or Angular - *Specify yours here*)
*   **Database:** (e.g., PostgreSQL, MongoDB - *Specify yours here*)
*   **Communication:** REST API, (e.g., SOAP/other for POS integration)

## 📋 Prerequisites

*   Node.js (v16 or higher)
*   npm or yarn
*   (e.g., A running instance of PostgreSQL)

## ⚙️ Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/tahawey/Tank-Monitor-System-TMS-SCADA-.git
    cd Tank-Monitor-System-TMS-SCADA-
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Environment Configuration:**
    Create a `.env` file in the root directory and configure your environment variables:
    ```env


    # ProGauge Data Source
    PROGAUGE_CSV_PATH=/path/to/your/csv/files

 
4.  **Start the application:**
    ```bash
    # For development
    npm run dev

    # For production
    npm start
    ```

    The application will be available at `http://localhost:3000` (or your configured port).

## 🔧 Usage

1.  **Configure Tanks:** Add your tank assets to the system, specifying the associated gauge type (ProGauge, Veeder-Root, etc.).
2.  **Data Flow:** The Node.js service will automatically begin polling the configured data sources (e.g., reading ProGauge CSV files every minute).
3.  **View Dashboard:** Log in to the web dashboard to see real-time tank levels, status, and temperature.
4.  **Manage Alarms:** Set up and acknowledge alarms directly from the interface.
5.  **Generate Reports:** Access the "Reports" section to view and export delivery and inventory history.
