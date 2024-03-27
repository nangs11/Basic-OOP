# Marketing Data ETL Project

Proyek ini berisi kelas-kelas untuk Proses Ekstrak, Transformasi, dan Muat (ETL) untuk data pemasaran.

## MarketingDataETL Class

Kelas MarketingDataETL menyediakan metode untuk mengekstrak, mentransformasi, dan menyimpan data pemasaran dari file CSV.

### Methods

1. `extract()`: Mengekstrak data dari file CSV yang ditentukan oleh `file_path`.
2. `transform()`: Membersihkan dan mentransformasi data yang diekstrak.
3. `store(output_file)`: Menyimpan data yang telah ditransformasi ke dalam file CSV yang ditentukan oleh  `output_file`.

## TargetedMarketingETL Class

Kelas `TargetedMarketingETL` mewarisi dari `MarketingDataETL` dan memperluas fungsionalitasnya dengan segmentasi pelanggan tambahan.

### Additional Method

1. `segment_customers(criteria)`: Memsegmentasikan pelanggan berdasarkan kriteria yang ditentukan seperti total pengeluaran atau kategori produk.
   
### Overridden Method

Metode `transform()` dioverride untuk menyertakan logika segmentasi pelanggan selain proses transformasi data standar.

## Example Usage

```python
if __name__ == "__main__":
    # Example usage of MarketingDataETL
    etl = MarketingDataETL("marketing_data.csv")
    etl.extract()
    etl.transform()
    etl.store("transformed_marketing_data.csv")

    # Example usage of TargetedMarketingETL
    targeted_etl = TargetedMarketingETL("marketing_data.csv")
    targeted_etl.extract()
    targeted_etl.transform()
    targeted_etl.segment_customers('product_category')
