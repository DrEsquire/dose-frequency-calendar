# Dosing Calendar Generator

A simple, client‑side web app that generates printable monthly dosing calendars for intravenous medications (e.g., Vancomycin). The tool runs entirely in the browser—no data is stored, uploaded, or transmitted.

## Features

- Optional patient information (Name, DOB, MRN) displayed on each printed page.
- Drug name and dosing interval shown in the header.
- Start time selector with 30‑minute increments (`step="1800"`).
- Choose stop condition by number of doses, number of days, or a specific date.
- Automatic selection of the stop‑condition radio button when you type in the corresponding input.
- Print button triggers `window.print()`.
- Calendar header shows only month and year (no duplicate year).
- Each month’s header, title, and table stay together on the same page when printing (via `page-break-inside: avoid`).
- Day number and dose times are stacked inside each cell for uniform column width.
- No cookies, local storage, or analytics—patient data is used only for on‑screen display and printing.

## Usage

1. Open the page (or visit the live GitHub Pages link).
2. Fill in:
   - **Drug:** medication name and dose (e.g., "Dobutamine 5 mg/mL").
   - **Dosing Interval (hours):** time between doses (e.g., `6` or `8`).
   - **Start Date** and **Start Time** (default 08:00).
   - Optional **Patient** fields (Name, Date of Birth, MRN).
   - Choose a stop condition and enter the corresponding value.
3. Click **Generate Calendar**.
4. The calendar appears below; click **Print** to print or save as PDF.

## Privacy

All calculations and data handling occur locally in your browser. The tool never:
- Saves data to disk, localStorage, or cookies.
- Sends data to any server or third‑party service.
- Uses analytics or tracking.

Patient‑identifying fields are used solely to render the header and on‑screen reference; they disappear when the page is reloaded.

## Live Demo

https://DrEsquire.github.io/dose-frequency-calendar/

## Development

The app is a single HTML file (`index.html`) with embedded CSS and JavaScript. No build steps required.

## License

This project is open source and available under the MIT License.
