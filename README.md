# WPS/PQR Builder — Automated Welding Compliance Tool

An automated industrial compliance tool designed to streamline the generation, tracking, and management of Welding Procedure Specifications (WPS) and Procedure Qualification Records (PQR). This platform helps cross-reference material variables, P-Numbers, and standards to ensure technical accuracy and minimize manual paperwork bottlenecks.

## Overview

The **WPS/PQR Builder** is a web-based application that facilitates compliance with **ASME Section IX** welding standards. It automates the creation and documentation of welding procedures while ensuring all essential variables and qualification ranges are properly tracked and managed.

## Features

### 📋 WPS Data Entry
- Comprehensive welding procedure specification form
- Support for multiple welding processes (SMAW, GTAW, GMAW, FCAW, SAW)
- P-Number and material classification cross-referencing
- F-Number and A-Number filler metal tracking
- Joint design and geometry specification
- Welding parameter management (amperage, voltage, travel speed, heat input)
- Position and preheat requirement definition
- Technique and procedural notes

### 🧪 PQR Test Results
- Procedure Qualification Record data entry
- Test coupon information and actual recorded values
- Mechanical test results tracking (tensile, bend, hardness, impact)
- Test laboratory and certification details
- Pass/fail documentation for all test specimens
- Bend test results (root, face, side)
- Notch toughness (Charpy CVN) tracking
- Visual examination compliance

### ✅ Essential Variables Checklist
- ASME Section IX QW-250 compliance verification
- Essential variables monitoring (P-Number, F-Number, A-Number, process, backing, PWHT, current/polarity, position, preheat, heat input, shielding gas)
- Supplementary essential variables for impact testing
- Change tracking and requalification alerts

### 📄 Formal Document Generation
- Auto-populated WPS document in professional format
- Auto-populated PQR document with test results
- Company logo and branding upload
- Custom company name and contact information
- Print-ready PDF output
- Signature blocks for prepared, reviewed, and approved personnel

### 🏢 Company Customization
- **Upload Company Logo**: Add your company's logo/image to all generated documents
- **Custom Company Name**: Replace branding with your organization name
- **Company Contact Info**: Add address, phone, email, or website details
- **Personalization**: Each document reflects your company's identity

## Technical Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Styling**: Custom design system with responsive grid layout
- **Fonts**: Barlow, Barlow Condensed, Share Tech Mono (Google Fonts)
- **Storage**: Client-side (browser local state)

## ASME Section IX Compliance

This tool ensures compliance with the following standards:

- **QW-482**: Welding Procedure Specification (WPS)
- **QW-483**: Procedure Qualification Record (PQR)
- **QW-250**: Essential Variables
- **QW-402**: Joint Design
- **QW-403**: Base Metal Requirements
- **QW-404**: Filler Metal Requirements
- **QW-405/QW-406**: Position and Preheat
- **QW-407**: Post-Weld Heat Treatment (PWHT)
- **QW-408**: Shielding Gas
- **QW-409**: Welding Parameters
- **QW-410**: Technique Requirements
- **QW-451**: Mechanical Testing
- **QW-461**: Positions of Welds
- **QW-462**: Bend Test Requirements

## Material Classification Support

### P-Numbers (Base Metals)
- P-1: Carbon Steel
- P-4: Alloy Steel 1-1/4 Cr
- P-5A: Alloy Steel 2-1/4 Cr
- P-5B: Alloy Steel 5 Cr
- P-15E: Alloy Steel 9 Cr
- P-8: 300 Series Stainless Steel
- P-10H: Duplex Stainless (2205)

### F-Numbers (Filler Classification)
- F-1, F-2, F-3, F-4, F-6, F-43 electrodes and wire classifications

### A-Numbers (Deposit Chemistry)
- A-1: Carbon Steel
- A-2: Carbon-Molybdenum
- A-3: Chrome (1/2–2%) Molybdenum
- A-4: Chrome (2–6%) Molybdenum
- A-8: Stainless Steel (Cr-Ni)

## Getting Started

1. **Open the application**: Load `index.html` in a modern web browser
2. **Upload Company Branding** (Optional):
   - Upload your company logo
   - Enter your company name
   - Add contact information
3. **Enter WPS Data**: Fill in the WPS identification, base metal, filler metal, and joint design information
4. **Define Welding Parameters**: Add pass/layer information with amperage, voltage, and other parameters
5. **Record Test Results**: Switch to the PQR tab and enter mechanical test results
6. **Verify Essential Variables**: Use the checklist to confirm all essential variables are accounted for
7. **Generate Documents**: View and print professional WPS/PQR documents with your company branding
8. **Export**: Print or save as PDF for records

## Workflow

```
Company Setup → WPS Data Entry → PQR Test Results → Essential Variables → Document Review → Print/PDF
```

## Browser Support

- Chrome/Chromium (recommended)
- Firefox
- Safari
- Edge
- Any modern browser supporting ES5+ JavaScript

## Features by Tab

| Tab | Purpose |
|-----|---------|
| **Company Settings** | Upload logo and customize company information |
| **01 — WPS Data Entry** | Input all welding procedure parameters |
| **02 — PQR Test Results** | Record mechanical test specimen data |
| **03 — Essential Variables** | Verify ASME Section IX essential variables |
| **04 — WPS Document** | View formatted WPS with your company branding |
| **05 — PQR Document** | View formatted PQR with test results |

## Keyboard Shortcuts

- **New**: Clear all data and start fresh
- **PQR**: Jump to PQR document view
- **WPS Document**: Jump to WPS document view
- **Print / PDF**: Open print dialog for active document

## Customization

This tool is designed for any welding, inspection, or QA/QC organization. Simply upload your company's logo and enter your company details to personalize all generated documents.

---

**Last Updated**: June 2026  
**Version**: 1.0  
**Status**: Active Development
