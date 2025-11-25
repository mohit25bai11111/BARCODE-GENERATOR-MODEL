# 📄 Project Statement: Barcode & QR Code Generator

**Project Name:** Python Barcode & QR Code Generator  
**Domain:** Software Development / Utility Tools  
**Author:** MOHIT PILLAI  
**ID:** 25BAI11111  
**Date:** November, 2025

---

## 1. The Problem
In inventory management, retail, and digital information sharing, the need to generate barcodes and QR codes is frequent.
* **Current Limitations:** Most existing solutions are online web converters that are often riddled with ads, require an internet connection, or pose privacy risks when handling sensitive data.
* **The Gap:** There is a need for a lightweight, offline, and programmable tool that can generate compliant barcodes quickly without external dependencies.

## 2. Proposed Solution
This project provides a **Command-Line Interface (CLI) Application** capable of generating industry-standard barcodes and QR codes instantly.

The system allows users to:
1.  Select from multiple standard formats (QR, EAN-13, UPC-A, Code 128, Code 39).
2.  Input data (URLs, text, or product numbers).
3.  Automatically validate the input (e.g., ensuring EAN-13 has the correct number of digits).
4.  Save high-quality PNG images locally for immediate use.

## 3. Objectives & Goals
* **Versatility:** Support the most common barcode standards used in retail and logistics.
* **Automation:** Automatically handle file naming and directory management (`generated/` folder).
* **Reliability:** Implement input validation to prevent the generation of invalid or unreadable barcodes.
* **Usability:** Include an integrated image viewer to inspect the output immediately after generation.

## 4. Methodology
The application is built using **Python 3.x** with an Object-Oriented approach:
* **Core Logic:** Encapsulated in a `BarcodeQRGenerator` class.
* **Libraries:**
    * `qrcode`: For generating 2D Quick Response codes.
    * `python-barcode`: For generating 1D linear barcodes (EAN, UPC, Code 128).
    * `opencv-python`: For rendering and displaying the generated images to the user.
* **Workflow:** User Input -> Validation Check -> Image Generation -> File Saving -> Optional Display.

## 5. Scope and Constraints
* **In Scope:**
    * Generation of static PNG images.
    * Support for QR, EAN-13, UPC-A, Code 128, and Code 39.
    * Local file system integration.
* **Out of Scope:**
    * Batch processing (generating 100+ codes at once) - *Planned for future v2.0*.
    * Database integration.
    * Graphical User Interface (GUI) - *Currently CLI only*.

## 6. Expected Impact
This tool serves as a foundational utility for small businesses or developers who need to integrate barcode generation into their workflow. It provides a secure, offline, and cost-free alternative to web-based generators.
