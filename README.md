# Well Plate Sample Parser

A web-based utility to visually assign and preview sample positions on 96- or 384-well plates. This tool allows you to import CSV/TXT files containing sample lists or existing well mappings, visualize assignments, and export the final layout.

## 🧪 Features

- 🧬 **Supports 96- and 384-well plates**
- 📄 **Flexible file input**: Accepts `.csv` or `.txt` files with:
  - Sample lists
  - Well-to-sample mappings
  - Mixed formats
- 📈 **Auto-detection** of file type (samples vs mappings)
- 🎯 **Intelligent assignment**:
  - Respects pre-mapped positions
  - Assigns remaining samples based on user-specified direction and starting well
- 🎨 **Color-coded layout**:
  - 🟪 Pre-mapped - from uploaded files
  - 🟦 Previewed - previewed positions before confirmation
  - 🟩 Confirmed - final confirmed positions
  - 🔴 Conflicts - errors, such as invalid well locations or too many samples for plate capacity
- 💾 **Export layout** to `.csv`
- 🔍 **Hover-based tooltips** and sample highlighting

## 📋 File Formats

| Format          | Description |
|-----------------|-------------|
| **Sample List** | A single-column file with sample IDs |
| **Sample Data** | Multi-column (e.g., `SampleID,Rack,Position`) |
| **Well Mappings** | Two-column file: `Well,SampleID` |
| **Separators**  | Comma, tab, space, or pipe supported |
| **Well Format** | Accepts both `A1`, `A01`... up to `H12`/`P24` |

## 🚀 Getting Started

1. Open `PlateParser.html` in any modern web browser (Chrome, Firefox, Edge).
2. Select the plate type (96 or 384).
3. Upload your CSV/TXT file.
4. Configure starting well and direction (horizontal/vertical).
5. Click **Preview Assignment** to visualize.
6. Click **Assign Samples** to finalize.
7. Export the plate layout using **Export Layout**.

## 📤 Export Format

The exported CSV contains:

Well,Sample_ID
A1,SAMPLE001
A2,SAMPLE002