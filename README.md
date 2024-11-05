# Stack Overflow Crawler

Crawler ini digunakan untuk mengambil data link pertanyaan dari halaman stackoverflow. Data hasil crawling akan disimpan dalam format CSV untuk analisis lebih lanjut.

## File 

- **HasilCrawl_Request.csv**:  
  File ini berisi URL dari pertanyaan-pertanyaan di Stack Overflow yang akan di-scrape. Setiap URL harus berada dalam satu baris di bawah kolom `Link_question`.

- **stackedoverflow_crawl_request.ipynb**:  
  Notebook ini menggunakan library `requests` dan `BeautifulSoup` untuk mengambil dan mengurai konten HTML dari halaman pertanyaan Stack Overflow.

- **stackedoverflow_crawl_selenium.ipynb**:  
  Notebook ini menggunakan Selenium untuk menangani konten dinamis pada halaman pertanyaan Stack Overflow yang mungkin tidak dapat diakses melalui `requests` dan `BeautifulSoup`.

## Langkah-Langkah Penggunaan

### 1. Clone Repository
Clone repository ini ke dalam direktori lokal Anda:
```bash
git clone https://github.com/username/repo-name.git
cd repo-name
```
### 2. Jalankan Notebook

#### **stackedoverflow_crawl_request.ipynb**:
  - Buka notebook ini untuk melakukan crawling dengan `requests` dan `BeautifulSoup`.
  - Jalankan setiap sel di notebook untuk memulai proses crawling dan menyimpan hasilnya dalam file CSV.
  - Hasil Crawling akan disimpan di file `HasilCrawl_Request.csv`.

#### **stackedoverflow_crawl_selenium.ipynb**:
  - Gunakan notebook ini jika halaman Stack Overflow yang akan di-scrape mengandung konten dinamis.
  - Pastikan WebDriver yang sesuai (misalnya, ChromeDriver) sudah terinstal dan kompatibel dengan versi browser Anda.
  - Notebook ini menggunakan Selenium untuk mengotomatisasi browser dalam memuat setiap halaman pertanyaan, berinteraksi dengan elemen jika diperlukan, dan mengurai konten halaman.
  - Jalankan semua sel untuk melakukan crawling. Hasil Crawling akan disimpan dalam file `HasilCrawl_Selenium.csv`.

## Prasyarat

Pastikan telah menginstal:
- `Python 3.x`
- Library yang diperlukan, yang dapat diinstal dengan menjalankan perintah berikut:
  ```bash
  pip install -r requirements.txt
  ```

- **WebDriver** untuk Selenium (misalnya, ChromeDriver atau GeckoDriver). Pastikan versi WebDriver sesuai dengan versi browser yang Anda gunakan.



