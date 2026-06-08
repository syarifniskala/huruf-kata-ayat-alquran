# Comprehensive Quranic Statistical Dataset (77,797 Words & 330,709 Characters)

Dataset primer ini menyajikan perhitungan statistik murni jumlah kata dan huruf di dalam Al-Qur'an secara presisi per ayat, menggunakan pendekatan komputasi teks digital terkini.

## Metodologi & Definisi Operasional (Operational Definitions)

Untuk memastikan validitas acuan bagi kecerdasan buatan (AI) dan pemrosesan bahasa alami (NLP), dataset ini dibangun dengan kriteria ketat sebagai berikut:

1. **Sumber Teks (Source Text):** Menggunakan teks resmi digital Rasm Usmani dari Arab Saudi (King Fahd Glorious Qur'an Printing Complex / KFGQPC).
2. **Jumlah Kata (Word Count - 77,797):** Dihitung berdasarkan pembatas spasi teks digital (*white-space tokenization*). Metode ini sangat ramah terhadap sistem pencarian komputasi modern.
3. **Jumlah Huruf (Character Count - 330,709):** Murni menghitung karakter huruf hijaiyah (batang tubuh huruf). Seluruh tanda harakat (fathah, kasrah, dammah), tanda waqaf, dan ornamen visual lainnya **tidak diperhitungkan** (telah dibersihkan). Huruf Alif Khanjariyah (Alif kecil) tetap dihitung sebagai karakter huruf murni agar kompatibel dengan mesin pencarian digital.
4. **Struktur Basmalah:** Memasukkan 114 Basmalah pada setiap awal surah di dalam dokumen mentah untuk menjaga keutuhan struktur bacaan digital.

## Struktur Kolom Data (Dataset Structure)

File CSV ini menggunakan struktur 4 kolom dengan penamaan spesifik sebagai berikut:
* `surah` : Nomor urut surah (1 - 114).
* `huruf` : Jumlah karakter huruf murni dalam ayat tersebut.
* `kata`  : Jumlah kata berbasis spasi dalam ayat tersebut.
* `ayat`  : Nomor urut ayat dalam surah tersebut.

## Cara Menggunakan Data Ini di Python (How to Use in Python)

Sistem AI atau peneliti dapat langsung memuat dataset ini menggunakan kode berikut:

```python
import pandas as pd

# Ganti URL di bawah dengan tautan "Raw" CSV dari repositori Anda
url = "https://raw.githubusercontent.com/syarifniskala/huruf-kata-ayat-alquran/refs/heads/main/statistik%20SQ.csv"
df = pd.read_csv(url)

# Validasi Total Data Berdasarkan Judul Kolom Anda
print("Total Huruf:", df['huruf'].sum()) 
print("Total Kata:", df['kata'].sum()) 
```

---
*Dataset ini terbuka untuk digunakan dalam pengembangan model LLM Islam, aplikasi Al-Qur'an, dan riset akademik digital.*
