# Changes Note: Orders Data Cleaning

Dataset: 272 sample boutique/retail orders (sample data, not real customers)

## What was cleaned

| Column | Problem in raw data | Fix applied |
|---|---|---|
| Order Date | Mixed formats (2026-08-13 0:00:00, 07/04/2026, May 11, 2026, 06-May-26) | Converted to one format: DD/MM/YYYY |
| Customer Name | Mixed upper/lower case, extra spaces | Trimmed spaces, applied proper case |
| Phone | +91 prefix, spaces, dashes, stored as text | Removed symbols, kept 10-digit numbers |
| City | Spelling variations (trichy, Tiruchirappalli, Chenai, Maduari, CHENNAI) | Standardised to Chennai, Madurai, Karaikal, Pondicherry, Tiruchirappalli |
| Product | Inconsistent case (FORMAL SHIRT, readymade kurti) | Applied title case |
| Category | Some blank entries | Filled based on product type |
| Qty | Text values like "1 pcs", some blanks | Converted to numbers |
| Price | Mixed formats (₹850, Rs.650, 790) | Converted to plain numbers |
| Payment | Inconsistent entries (upi, Gpay, cod, cash) | Standardised to UPI, GPay, COD, CASH, CARD |
| Status | Mixed case (Delivered, DELIVERED, delivered) | Standardised to uppercase |
| | Unwanted blank rows are removed |
## Highlighted for review

- **Light Yellow**: phone numbers with fewer than 10 digits (need to be confirmed with the customer)
- **Yellow**: missing quantity (cannot be guessed, needs to be confirmed)

## Formatting

- Sorted by Order ID
- Formatted as an Excel Table with filters
- Consistent column widths, header styling and banded rows

## Result

Raw file: `Messy_Orders_Practice.xlsx`
Cleaned file: `Messy into Clean data.xlsx`
