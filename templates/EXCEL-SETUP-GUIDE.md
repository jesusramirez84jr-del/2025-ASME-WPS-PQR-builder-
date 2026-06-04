# WPS/PQR Builder — Excel Setup Guide

## Overview

This guide walks you through setting up and using the Excel-based WPS/PQR Builder templates. These templates mirror the functionality of the web application and include automation, data validation, and print-ready formatting.

## Files Included

1. **WPS-PQR-Builder.xlsx** - Full Excel workbook with macros and automation
2. **WPS-PQR-Builder-template.csv** - CSV template for data import/export

## System Requirements

### For Excel Workbook
- **Microsoft Excel 2016 or later** (Windows or Mac)
- **Macros enabled** - Allow VBA macros when prompted
- **Optional**: Python 3.7+ (if using advanced data processing features)

### For CSV Template
- Any spreadsheet application (Excel, Google Sheets, LibreOffice, etc.)

## Getting Started

### Step 1: Enable Macros

1. Open `WPS-PQR-Builder.xlsx` in Microsoft Excel
2. When prompted: **"Enable Content"** or **"Enable Macros"** - Click **Yes**
3. If no prompt appears, go to:
   - **File → Options → Trust Center → Trust Center Settings → Macro Settings**
   - Select **"Enable all macros"**

### Step 2: Add Your Company Branding

1. Navigate to the **"Company Settings"** sheet
2. **Upload Company Logo**:
   - Click **"Insert → Pictures → This Device"**
   - Select your company logo (PNG, JPG, or BMP)
   - Resize and position in the designated area
3. **Enter Company Information**:
   - Company Name
   - Address
   - Phone Number
   - Email
   - Website (optional)
4. Click **"Save Branding"** button to apply to all sheets

### Step 3: Enter WPS Data

1. Go to **"WPS Data Entry"** sheet
2. Fill in the following sections:

#### WPS Identification
- WPS Number (e.g., WPS-01-SMAW-CS)
- Revision (default: 0)
- Date (auto-populates today's date)
- Supported by PQR No.

#### Base Metal (QW-403)
- **P-Number**: Dropdown selection
- Group Number
- Base Metal Specification
- Thickness Range (Groove)
- Thickness Range (Fillet)
- Pipe Diameter Range
- PWHT Required: Dropdown
- PWHT Temperature Range

#### Filler Metal (QW-404)
- **F-Number**: Dropdown selection
- **A-Number**: Dropdown selection
- SFA Specification
- AWS Classification
- Filler Trade Name
- Electrode Diameter
- Flux/Shielding Gas
- Gas Flow Rate (CFH)

#### Joint Design (QW-402)
- Joint Type: Dropdown
- Root Opening
- Root Face
- Groove Angle
- Backing: Dropdown
- Backing Material

#### Welding Parameters (QW-409)
- Table format for each pass/layer:
  - Pass/Layer number
  - Process (Dropdown)
  - Filler Size
  - Current Type/Polarity (Dropdown)
  - Amperage Range
  - Voltage Range
  - Travel Speed
  - **Heat Input** (Auto-calculated from voltage × amperage ÷ travel speed)

#### Position & Preheat (QW-405/406)
- Position(s) Qualified: Dropdown
- Weld Progression: Dropdown
- Min. Preheat Temp
- Max. Interpass Temp
- Preheat Maintenance
- Peening: Dropdown

#### Technique (QW-410)
- String/Weave Bead: Dropdown
- Oscillation Max Width
- Multi/Single Pass: Dropdown
- Multi/Single Electrode: Dropdown
- Inter-run Cleaning: Dropdown
- Special Instructions/Notes

### Step 4: Enter PQR Test Results

1. Go to **"PQR Test Results"** sheet
2. Fill in the following sections:

#### PQR Identification
- PQR Number
- Date
- Supports WPS No.
- Certified By (CWI/CWENG)

#### Test Coupon Data
- Base Metal Used
- Coupon Thickness
- Filler Metal Used
- Actual Preheat Temp
- Actual Interpass Temp
- PWHT Actual Temp
- PWHT Time at Temp
- Position Welded

#### Mechanical Test Results
- Testing Laboratory
- Lab Report No.
- Test Date
- **Test Specimens Table** with auto-calculations:
  - Test Type: Dropdown
  - Specimen No.
  - Width (in)
  - Thickness (in)
  - **Area** (Auto = Width × Thickness)
  - Max Load (lbf)
  - **UTS** (Auto = Max Load ÷ Area)
  - Result: Dropdown (PASS/FAIL)

#### Bend & Other Tests
- Bend Test Root: Dropdown
- Bend Test Face: Dropdown
- Bend Test Side: Dropdown
- Notch Toughness (CVN): Dropdown
- Hardness (HBW/HRC)
- Visual Exam: Dropdown

### Step 5: Essential Variables Checklist

1. Go to **"Essential Variables"** sheet
2. Check all applicable essential variables:
   - P-Number changes
   - Base metal thickness changes
   - F-Number changes
   - A-Number changes
   - Welding process changes
   - Backing changes
   - PWHT changes
   - Current/Polarity changes
   - Position changes
   - Preheat temperature changes
   - Heat input changes
   - Shielding gas changes
3. Supplementary essential variables section for impact testing

### Step 6: Generate Documents

#### WPS Document
1. Go to **"WPS Document"** sheet
2. Click **"Generate WPS"** button
3. Document auto-populates from WPS Data Entry sheet
4. Review and verify all information
5. Add signature blocks:
   - Prepared By (with date and signature line)
   - Reviewed By (with date and signature line)
   - Approved By (with date and signature line)

#### PQR Document
1. Go to **"PQR Document"** sheet
2. Click **"Generate PQR"** button
3. Document auto-populates from PQR Test Results sheet
4. Review test results and certification
5. Add signature blocks for certification

### Step 7: Print & Export

#### Print Documents
1. Navigate to **"WPS Document"** or **"PQR Document"** sheet
2. Click **"Print Preview"** button
3. Configure print settings:
   - Orientation: Portrait
   - Margins: 0.5"
   - Include company branding
4. Click **"Print"** or **"Save as PDF"**

#### Export to CSV
1. Go to **"Data Export"** sheet
2. Select data range (or use **"Export All"** button)
3. Click **"Export to CSV"**
4. Choose location and filename
5. File saved as `.csv` for backup or sharing

## Data Validation & Dropdowns

### P-Numbers (Base Metals)
- P-1 — Carbon Steel
- P-4 — Alloy Steel 1-1/4 Cr
- P-5A — Alloy Steel 2-1/4 Cr
- P-5B — Alloy Steel 5 Cr
- P-15E — Alloy Steel 9 Cr
- P-8 — 300 Series Stainless Steel
- P-10H — Duplex Stainless (2205)

### F-Numbers (Filler Classification)
- F-1, F-2, F-3, F-4, F-6, F-43

### A-Numbers (Deposit Chemistry)
- A-1 — Carbon Steel
- A-2 — Carbon-Molybdenum
- A-3 — Chrome (1/2–2%) Molybdenum
- A-4 — Chrome (2–6%) Molybdenum
- A-8 — Stainless Steel (Cr-Ni)

### Welding Processes
- SMAW — Shielded Metal Arc
- GTAW — Gas Tungsten Arc (TIG)
- GMAW — Gas Metal Arc (MIG)
- FCAW — Flux Cored Arc
- SAW — Submerged Arc

## Automatic Calculations

The Excel workbook includes the following auto-calculations:

| Calculation | Formula | Where Used |
|---|---|---|
| **Area (in²)** | Width × Thickness | PQR Test Results |
| **UTS (psi)** | Max Load ÷ Area | PQR Test Results |
| **Heat Input (kJ/in)** | (Voltage × Amperage) ÷ (Travel Speed × 60) | WPS Parameters |
| **Specimen Count** | Count of non-empty rows | PQR Test Results |

**Important**: Do not manually edit calculated fields. Formulas will update automatically.

## Troubleshooting

### Macros Not Running
- **Issue**: Buttons don't work or say "disabled"
- **Solution**: Enable macros in Excel Trust Center (see Step 1)

### Data Not Calculating
- **Issue**: Area or UTS fields show #REF! or 0
- **Solution**: Ensure all input fields (Width, Thickness, Load) contain numbers

### Company Logo Not Appearing
- **Issue**: Logo appears on Company Settings but not on documents
- **Solution**: 
  - Ensure logo is properly sized (max 2" × 2")
  - Check that "Save Branding" button was clicked
  - Regenerate documents after logo upload

### Print Preview Looks Wrong
- **Issue**: Documents don't format correctly for printing
- **Solution**:
  - Set print orientation to **Portrait**
  - Set margins to **0.5 inches** on all sides
  - Use **"Fit to 1 page wide"** in print settings

### CSV Import Not Working
- **Issue**: Data doesn't import correctly
- **Solution**:
  - Ensure CSV file is properly formatted (comma-separated)
  - Check that data types match (numbers, dates, text)
  - Use "Data → Text to Columns" to reformat if needed

## Tips & Best Practices

### Data Entry
- ✅ Use dropdown selections whenever available
- ✅ Enter dates in **MM/DD/YYYY** format
- ✅ Use consistent temperature units (°F or °C)
- ✅ Double-check P-Numbers and F-Numbers against ASME standards

### Document Generation
- ✅ Always verify calculated fields (Heat Input, UTS)
- ✅ Review essential variables before finalizing
- ✅ Save a backup copy before printing
- ✅ Include signature blocks and dates

### Compliance
- ✅ Ensure all essential variables are marked
- ✅ Verify test results meet ASME Section IX requirements
- ✅ Maintain documentation for audit purposes
- ✅ Update PQR when procedure changes exceed qualified ranges

## Security & Backups

### Protecting Your Data
1. **Save regularly**: Use **Ctrl+S** (or **Cmd+S** on Mac)
2. **Create backups**: Copy the workbook to multiple locations
3. **Version control**: Use date suffixes (e.g., `WPS-PQR-Builder_2026-06-04.xlsx`)
4. **Password protect**: 
   - Go to **File → Info → Protect Workbook → Encrypt with Password**
   - Set a strong password to prevent unauthorized changes

### Data Recovery
- If corrupted, Excel has a built-in recovery feature:
  - **File → Info → Manage Workbooks → Recover Unsaved Workbooks**

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| **Ctrl+Home** | Jump to top of sheet |
| **Ctrl+End** | Jump to end of data |
| **Ctrl+P** | Open Print dialog |
| **Ctrl+S** | Save workbook |
| **Alt+F4** | Close workbook |
| **F2** | Edit cell |
| **F9** | Recalculate all formulas |

## Support & Updates

For issues, questions, or feature requests:
1. Check the **"FAQ"** sheet in the workbook
2. Review this guide's Troubleshooting section
3. Ensure you're using the latest version from the repository

---

**Last Updated**: June 2026  
**Excel Version**: 1.0  
**Compatible with**: Excel 2016, 2019, 2021, Microsoft 365
