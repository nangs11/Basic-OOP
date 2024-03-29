# Basic OOP Homework

## Deskripsi
Repository ini dibuat sebagai bagian dari tugas Basic OOP oleh kami **Kelompok 17**. Tujuan dari tugas ini adalah untuk membuat class `MarketingDataETL` yang memiliki metode `extract()`, `transform()`, dan `store()`. Selain itu, kita juga diminta untuk membuat class turunan `TargetedMarketingETL` yang menambahkan metode `segment_customers()` dan melakukan overriding terhadap metode `transform()`.

## Files
- `project_3.ipynb`: File Jupyter Notebook yang berisi implementasi tugas Basic OOP.
- `marketing_data.csv`: Contoh file CSV yang digunakan untuk ekstraksi data.
- `transformed_marketing_data.csv`: File CSV hasil transformasi yang disimpan.

## Class dan Metode
### `MarketingDataETL`
- `extract()`: Membaca data dari file CSV.
- `transform()`: Melakukan pembersihan dan transformasi sederhana pada data.
- `store()`: Menyimpan data yang telah ditransformasi ke dalam struktur data DataFrame.

### `TargetedMarketingETL`
- `segment_customers(criteria)`: Mengelompokkan pelanggan berdasarkan kriteria tertentu.
- `transform()`: Melakukan transformasi data serta menambahkan logika segmentasi pelanggan.

## Cara Penggunaan
```python
if __name__ == "__main__":
    # Contoh penggunaan untuk MarketingDataETL
    etl = MarketingDataETL("marketing_data.csv")
    etl.extract()
    etl.transform()
    etl.store("transformed_marketing_data.csv")
    
    # Contoh penggunaan untuk TargetedMarketingETL
    targeted_etl = TargetedMarketingETL("marketing_data.csv")
    targeted_etl.extract()
    targeted_etl.transform()
    targeted_etl.segment_customers('product_category')
