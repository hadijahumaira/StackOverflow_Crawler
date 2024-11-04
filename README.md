# Stack Overflow Crawler

Crawler ini digunakan untuk mengambil data link pertanyaan dari halaman stackoverflow. Data hasil crawling akan disimpan dalam format CSV untuk analisis lebih lanjut.

## File dan Penggunaan

- **HasilCrawl_Request.csv**:  
  File ini berisi URL dari pertanyaan-pertanyaan di Stack Overflow yang akan di-scrape. Setiap URL harus berada dalam satu baris di bawah kolom `Link_question`.

- **stackedoverflow_crawl_request copy.ipynb**:  
  Notebook ini menggunakan library `requests` dan `BeautifulSoup` untuk mengambil dan mengurai konten HTML dari halaman pertanyaan Stack Overflow.

  **Penggunaan**:
  - Muat URL dari file `HasilCrawl_Request.csv`.
  - Crawl setiap halaman untuk mengambil detail seperti judul pertanyaan, konten, jumlah vote, tag, dan jawaban.
  - Simpan data yang diekstraksi ke dalam file CSV bernama `HasilScrappingWithCSV_Request.csv`.

- **stackedoverflow_crawl_selenium.ipynb**:  
  Notebook ini menggunakan Selenium untuk menangani konten dinamis pada halaman pertanyaan Stack Overflow yang mungkin tidak dapat diakses melalui `requests` dan `BeautifulSoup`.

  **Penggunaan**:
  - Pastikan WebDriver yang sesuai (misalnya, ChromeDriver) sudah terinstal dan kompatibel dengan versi browser Anda.
  - Selenium mengotomatisasi browser untuk memuat setiap halaman pertanyaan, berinteraksi jika diperlukan, dan mengurai konten halaman.
  - Data yang diekstraksi disimpan dalam file `HasilScrappingWithSelenium_Request.csv`.

---

