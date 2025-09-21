# Customer Segmentation on Ecommerce

## 📌 Business Understanding

Sebuah perusahaan ingin memahami pola pembelian dan karakteristik pelanggan mereka berdasarkan data transaksi yang terjadi. Dengan menganalisis produk terlaris, periode penjualan tertinggi, serta pelanggan dengan kontribusi terbesar, perusahaan dapat menyusun strategi pemasaran dan pengelolaan stok yang lebih efektif untuk meningkatkan penjualan.

**Key Questions:**
- Produk apa yang paling sering dibeli?
- Siapa pelanggan dengan total pembelian tertinggi?
- Pada bulan apa penjualan paling tinggi terjadi?
- Berapa total penjualan (revenue) yang dihasilkan selama periode data?
- Apakah ada produk yang sering dibeli dalam kuantitas besar (bulk order)?
- Siapa segmen pelanggan yang paling menguntungkan?

---

## Data Understanding
- Source: https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business

| Nama Kolom               | Deskripsi                                |
|--------------------------|------------------------------------------|
| TransactionNo              | Kode Unik setiap transaksi. Huruf C dalam kode artinya cancellation.   |
| Date                   | Tanggal setiap transaksi terjadi          |
| ProductNo                     | Kode Unik suatu produk                |
| Product            | Nama produk|
| Price                   | Harga produk per unit                  |
| Quantity             | Jumlah produk terjual                          |
| CustomerNo               | Kode unik pelanggan                    |
| Country                 | Negara tempat customer tinggal               | 

---

## Data Preprocessing
1. Convert `date` to datetime format  
2. Handle duplicates (dropped 18 duplicated values)  
3. Drop irrelevant columns (e.g., personal info, payment method)  
4. Filter USA transactions only  
5. Handle missing values using logical formulas:  
   - `Total Purchases = Total Amount / Amount`  
   - `Amount = Total Amount / Total Purchases`  
   - `Total Amount = Total Purchases × Amount`  
6. Apply **RFM analysis** (added 9 new columns for RFM scores & segmentation)

---

## ✅ Results
- **Total Sales:** $130M  
- **Total Transactions:** ~95K  
- **Total Customers:** ~58K  

**Customer Distribution:**
- Potential Loyalists → **60% of customers** (~75M sales, 102K transactions)  
- Needs Attention → **27%** (~15M sales, 25K transactions)  
- Loyal Customers → **13%** (~38M sales, 78K transactions)  
- Champions → **<0.1%** (~500K sales, 2K transactions)  

**Trends (July 2023 – Feb 2024):**
- Potential Loyalists declined after July 2023  
- Needs Attention increased sharply since July 2023  
- Loyal Customers decreased gradually  
- Champions remained very low  
