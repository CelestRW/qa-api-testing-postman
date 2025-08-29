# API Testing with Postman (Sprint 4)

**Status:** Evidence-only (Postman exports unavailable).  
This repo documents my Sprint 4 API testing work for **Urban Grocers (Kits)** and **Fast Delivery (XML)**.  
I designed and executed positive/negative test cases, recorded results, and produced reports.

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

