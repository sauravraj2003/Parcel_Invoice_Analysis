# Parcel Invoice Analysis — Normalized Shipment Cost Model

Analysis of carrier invoice data for a shoe company shipping 4 lb parcels domestically across India. The goal is to build a normalized cost per shipment so that carriers like Delhivery, DTDC, Blue Dart, Ekart, and others can be compared fairly.

## What's in the notebook

- Data cleaning — fixes mixed formatting (currency symbols, weight units, zone labels) across two source formats merged into one file
- Charge classification — 196 unique charge type labels categorized into base charges, surcharges, penalties, and exclusions, with reasoning for each decision
- Normalized cost model — aggregates multiple invoice lines per shipment into a single comparable cost figure
- Carrier comparison — mean cost by carrier before and after normalization, with a zone breakdown to separate pricing differences from route mix differences
- Worst-10% analysis — identifies the most expensive shipments, checks whether they cluster by carrier or zone, and estimates their share of total spend

## Files

- `Parcel_Invoice_Analysis.ipynb` — main notebook with all code, outputs, and commentary
- `Parcel_Invoice_Dataset.csv` — raw invoice data (input)

## Requirements

```
pandas
numpy
matplotlib
seaborn
```

Install with `pip install pandas numpy matplotlib seaborn`.

## AI Usage

Gemini was used to draft an initial classification of the 196 charge type labels in the dataset. The categories were then reviewed and adjusted manually. All code and analysis decisions are my own.
