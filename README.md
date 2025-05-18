# Shopify Collection Filter – Frontend Filtering

This project customizes a Shopify collection page with advanced client-side filtering using JavaScript. It enables users to filter products by price, size, color, availability, and sort order — all **without reloading the page**.

## 🔗 Live Preview

- **Store URL**: [https://sleepycat-customfilter.myshopify.com/collections/products](https://sleepycat-customfilter.myshopify.com/collections/products)
- **Password**: `aireur`

---

## 🧰 Setup & Installation

1. Based on **Shopify Dawn Theme**
2. A custom template was created:
   - File: `templates/collection.custom-filter.liquid`
3. To preview:
   - Assign the `collection.custom-filter` template to any collection from Shopify admin.
   - Visit the live link above to test filtering.

---

## 💡 Features Implemented

### 🔄 Filtering (Fully Frontend/JavaScript)

- **Price Range**:
  - Under ₹1000
  - ₹1000–₹3000
  - Over ₹3000

- **Size**:  
  - Dynamically extracted from:
    - **Product variant options** named “Size”
    - **Tags** (e.g., `size:XL`, `size:M`)

- **Color**:  
  - Dynamically extracted from:
    - **Variant options** (e.g., `Color: Red`)
    - **Tags** (e.g., `color:red`, `colour:blue`)
    - **Metafields** (e.g., `product.metafields.custom.color`)

- **Availability**:
  - Checkbox to filter only "In Stock" products

- **Sort By**:
  - Featured (manual)
  - Price: Low to High / High to Low
  - Newest First
  - Best Selling

### 🖼️ Product Display

Each product card shows:
- Featured Image (lazy loaded)
- Title, Price, Vendor
- First tag as a **badge**
- Available variant options as **badges**

### 📱 Mobile Support

- Mobile filters open in a sliding drawer panel
- Accordion-style filter sections
- Works from screen widths as low as 360px

### 🧠 Extra Features

- **Lazy load images** using `IntersectionObserver`
- **Loading animation** (simulated delay)
- **URL parameter syncing**:
  - Example:  
    `?price=1000-3000&size=M,color=red&availability=in-stock&sort=price-ascending`

---

## 📁 Folder Structure

shopify-custom-filter/
├── templates/
│ └── collection.custom-filter.liquid
└── README.md


---

## 📝 Assumptions

- Product tags may include `color:red`, `colour:blue`, or `size:M`
- Metafield used: `product.metafields.custom.color`
- Only first tag is used as badge (for simplicity)
- Products may have one or multiple variants, and variant options are used as size/color

---

## 📸 Optional (Add Screenshots or Video Demo Here)
- Added Demo Video
- <video controls src="20250518-1731-52.5143961.mp4" title="Title"></video>
- Mobile filter drawer view
- Filtering animation/loading

---

## 📦 Submission Checklist

- ✅ Shopify Partner Store with password-protected link
- ✅ `collection.custom-filter.liquid` using Dawn theme
- ✅ GitHub repo with this file and the template
- ✅ Filters handled completely on frontend
- ✅ All required and optional features covered
