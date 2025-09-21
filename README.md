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
1. Duplicate handling (Dropped 5.200 duplicate data)
2. Missing value handling (Dropped 55 data)
3. Convert `date` to datetime format  
4. Convert `CustomerNo` from float to obj format 
5. Add and drop columns 

---

## Results
- **Total Sales:** $630M  
- **Total Transactions:** 23K 
- **Total Customers:** 4.738  

**Customer Distribution:**
- Champion: 82.3%
- Loyal: 12.9%
- Potential: 2.8%
- At Risk: 2%
