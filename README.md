# API Testing with Postman (Sprint 4)

**Status:** Evidence-only (Postman exports unavailable).  
This repo documents my Sprint 4 API testing work for **Urban Grocers (Kits)** and **Fast Delivery (XML)**.  
I designed and executed positive/negative test cases, recorded results, and produced reports.

## 🗂 Structure (for when I add exports later)


## 🧪 Coverage summary
- **Kits**: `POST /api/v1/kits/:id/products`
  - Valid kit id vs non-existent kit id → 200 / 404
  - Product ID checks; non-existent → 400
  - `productsList` length ≤ 30 (unique IDs) and body structure validation
- **Fast Delivery (XML)**: `/fast-delivery/v3.1.1/calculate-delivery.xml`
  - `deliveryTime` vs operating hours (boundary tests)
  - `productsWeight`, `productsCount` positive/negative limits

## 📎 Evidence (Bootcamp submission)
- Sprint 4 Test Cases (Google Sheets): https://docs.google.com/spreadsheets/d/1ZZraSr_65qMXobSshkjoaxbP2ZvL70asP6Fcbx59VPs/edit?usp=share_link
- All Projects Drive: https://drive.google.com/drive/folders/10c1yiXWxxvxvGhwz4A6iF-qZ_fyullpm?usp=share_link

## ▶️ How to make this runnable later
1. Export Postman **collection** (v2.1) → place in `collections/`
2. Export Postman **environment** (with `base_url`) → place in `environments/`
3. Install and run with Newman:
   ```bash
   npm i -g newman newman-reporter-htmlextra
   newman run collections/<your-collection>.json \
     -e environments/<your-environment>.json \
     -r cli,htmlextra \
     --reporter-htmlextra-export reports/report.html
