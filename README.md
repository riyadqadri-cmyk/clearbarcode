# clearbarcode

A lightweight, browser-based barcode label generator designed for fast, reliable printing on thermal labels. This project is intentionally simple: it runs as a standalone HTML app with no backend or server required.

This repository contains two versions:

- BarcodeSIMPLE.html — a simplified version built for everyday use, with English and Arabic labels
- BarcodePRO.html — a more advanced designer with draggable and resizable label elements and a built-in self-updating shell that can hot-swap app logic from app.html in the project root

The main focus is reliability, especially for older users or people who are not comfortable with technology.

## Project purpose

The software is designed to make barcode label printing easy and dependable in real-world situations. It helps users:

- enter item names, prices, and barcodes
- adjust label dimensions
- preview the label before printing
- print directly to a thermal label printer
- keep label preferences saved in the browser

## Features

### Simple version

The simplified page is meant to be very easy to use. It includes:

- English and Arabic labels
- item name, barcode, and price inputs
- width and height settings for the label
- automatic barcode generation
- barcode number toggle
- print preview
- browser local storage for saved dimensions and settings

### Pro version

The pro version adds more design power for users who need custom label layouts. It includes:

- draggable text and barcode elements
- resizable objects on the label
- multiple element types such as item name, price, barcode image, barcode number, and custom text
- grid toggle for easier placement
- saved layout in browser local storage
- more flexible printing for custom label arrangements
- a self-updating / hot-swappable app shell that can fetch and apply newer app.html logic while keeping the stable shell in place

## Barcode logic

The barcode generator follows a practical rule:

- If the barcode value is exactly 13 digits and valid as EAN-13, it is drawn as EAN-13
- Otherwise, it uses Code 128 symbology
- The barcode width is adjusted automatically to help maintain reliable scanning
- The app does not change the entered value unnecessarily; it preserves the user's original barcode data when possible

This keeps the system simple, consistent, and familiar for common barcode label uses.

## Local storage

The app stores important settings in the browser's local storage, including:

- label dimensions
- field positions and layout data
- saved design information for repeated use

That means users do not need a database or backend service just to keep their label sizes and layout preferences available.

## Reliability-first design

The major objective of this project is reliability, especially for older or non-technical users. This is reflected in:

- large, easy-to-read controls
- clear label naming
- minimal interface complexity
- bilingual fields in the simplified version
- automatic barcode sizing to reduce scanning problems
- a straightforward print workflow

## How to use

1. Open either BarcodeSIMPLE.html or BarcodePRO.html in a modern browser.
2. Enter the item name, barcode, and price as needed.
3. Adjust the label width and height if necessary.
4. Check the preview before printing.
5. Click Print and use your browser's print dialog to send the label to the printer.

## Example use cases

- retail product labels
- inventory item tagging
- warehouse stock labels
- small shop or business barcode printing
- quick label creation without a software installation

## Notes

- The project is intentionally self-contained and lightweight
- It works entirely in the browser, with no server required
- It is optimized for practical reliability rather than advanced enterprise features
- BarcodePRO includes a hot-swappable update mechanism that can refresh the app from app.html in the root while preserving the shell UI

This was made with the help of ChatGPT.

---

License: This project is licensed under the [MIT License](LICENSE). See the [LICENSE](LICENSE) file for full terms and conditions.
