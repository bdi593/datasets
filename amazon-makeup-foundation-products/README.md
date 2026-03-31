# 📦 Amazon Product JSON Dataset

This repository contains a collection of JSON files representing Amazon search results and detailed product data gathered through [HasData](https://www.hasdata.com).

The dataset is organized to support exploration, data processing, and integration into analytics or data engineering workflows.

---

## 📁 Folder Structure

```
.
├── search-results/
│   ├── foundation-page-01.json
│   ├── foundation-page-02.json
│   └── ...
│
├── product-results/
│   ├── B01H1V7WQU.json
│   ├── B008C13146.json
│   └── ...
│
├── products.csv
└── README.md
```

---

## 🔍 `search-results/`

- Contains paginated search result data
- File naming pattern: `foundation-page-{n}.json`
- Each file includes:
  - Request metadata
  - A list of products under `productResults`

### Key Fields

- `requestMetadata`: Information about the request
- `productResults`: Array of product objects

Each product may include:

- `asin` (string): Unique product identifier
- `title` (string): Product name
- `price` (object): Pricing information
- `reviews` (object): Ratings and review counts
- `badges` (object): Flags such as Prime or Best Seller
- `deliveryInfo` (object): Shipping estimates

---

## 🛍️ `product-results/`

- Contains detailed product-level data
- One file per product
- File naming pattern: `{asin}.json`

These files typically include richer and more complete information compared to search results.

---

## 📄 `products.csv`

A flattened dataset derived from search results, containing:

- `asin`
- `title`

This file can be used for quick lookup, indexing, or joining with detailed product data.

---

## 🧾 Example JSON Structure

### Search Results Example

```json
{
  "requestMetadata": { ... },
  "productResults": [
    {
      "asin": "B01H1V7WQU",
      "title": "Product title",
      "price": {
        "currentPrice": 19
      },
      "reviews": {
        "rating": 4.2
      }
    }
  ]
}
```

---

## ⚠️ Data Notes

- Not all fields are present for every product
- Nested objects (e.g., `price`, `reviews`) may be partially populated
- Field availability may vary across pages and products
- Data types are generally consistent but should not be strictly assumed

---

## 📜 License

This dataset is provided for educational and research purposes.
