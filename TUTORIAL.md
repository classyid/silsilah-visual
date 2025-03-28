# Tutorial Penggunaan Silsilah Visual dengan Data dari Keluarga Visualizer

Dalam tutorial ini, Anda akan belajar cara mengimpor data dari aplikasi Keluarga Visualizer ke Silsilah Visual untuk mendapatkan tampilan yang lebih modern dan interaktif untuk pohon silsilah keluarga Anda.

## Daftar Isi
1. [Persiapan](#1-persiapan)
2. [Membuat Data Silsilah dengan Keluarga Visualizer](#2-membuat-data-silsilah-dengan-keluarga-visualizer)
3. [Mengambil Data dari Keluarga Visualizer](#3-mengambil-data-dari-keluarga-visualizer)
4. [Mengimpor Data ke Silsilah Visual](#4-mengimpor-data-ke-silsilah-visual)
5. [Menyesuaikan Konfigurasi Tampilan](#5-menyesuaikan-konfigurasi-tampilan)
6. [Menggunakan Fitur Silsilah Visual](#6-menggunakan-fitur-silsilah-visual)
7. [Tips dan Trik](#7-tips-dan-trik)
8. [Pemecahan Masalah](#8-pemecahan-masalah)

## 1. Persiapan

Sebelum memulai, pastikan Anda memiliki:

- Browser web modern (Chrome, Firefox, Edge, atau Safari terbaru)
- Akses ke aplikasi [Keluarga Visualizer](https://github.com/username/keluarga-visualizer)
- Aplikasi [Silsilah Visual](https://github.com/username/silsilah-visual) yang sudah Anda download
- Editor teks sederhana (Notepad, VS Code, dll.)

## 2. Membuat Data Silsilah dengan Keluarga Visualizer

Tahap pertama adalah membuat data silsilah keluarga menggunakan Keluarga Visualizer.

### Langkah-langkah:

1. Buka aplikasi Keluarga Visualizer (melalui file index.html atau versi online)
2. Tambahkan anggota generasi awal (generasi 0) dengan mengisi form:
   - Nama: [nama anggota keluarga]
   - Generasi: 0
   - Status: centang jika almarhum/ah
   - Pasangan: [nama pasangan] (jika ada)
   - Parent ID: kosongkan (karena ini generasi awal)
3. Tambahkan anak-anak dengan mengklik tombol "+ Tambah Anak" pada data generasi awal
4. Lanjutkan menambahkan anggota keluarga sampai data silsilah lengkap
5. Anda juga dapat menggunakan fitur impor untuk memuat data JSON yang sudah ada

> **Catatan**: Untuk tutorial lengkap tentang Keluarga Visualizer, lihat dokumentasinya di [DOKUMENTASI.md](https://github.com/username/keluarga-visualizer/blob/main/DOKUMENTASI.md)

## 3. Mengambil Data dari Keluarga Visualizer

Setelah data silsilah selesai dibuat, Anda perlu mengekstrak data dalam format JavaScript.

### Langkah-langkah:

1. Di aplikasi Keluarga Visualizer, klik tombol "Generate CompleteData"
2. Panel "Generated CompleteData" akan menampilkan struktur data JavaScript
3. Klik tombol "Copy Code" untuk menyalin kode ke clipboard
4. Data yang disalin akan terlihat seperti ini:

```javascript
const completeData = [
  {
    "name": "Haji Slamet Riyadi",
    "generation": 0,
    "deceased": true,
    "spouse": "Hj. Siti Aminah",
    "spouseDeceased": true,
    "children": [
      {
        "name": "Ahmad Sukarno",
        "generation": 1,
        "deceased": true,
        "spouse": "Maryati",
        "children": [
          // Data anak dan keturunan lainnya
        ]
      },
      // Data anak-anak lain
    ]
  }
];
```

> **Penting**: Pastikan format data sudah benar dan struktur JSON valid sebelum menggunakannya di Silsilah Visual.

## 4. Mengimpor Data ke Silsilah Visual

Sekarang saatnya mengimpor data ke Silsilah Visual.

### Langkah-langkah:

1. Buka file `index.html` dari Silsilah Visual di editor teks
2. Cari bagian kode yang berisi variabel `completeData`, yang terlihat seperti:

```javascript
const completeData = [
  // Data contoh yang sudah ada
];
```

3. Ganti seluruh isi variabel `completeData` (termasuk kurung siku `[]`) dengan data yang Anda salin dari Keluarga Visualizer
4. Pastikan Anda **hanya** mengganti bagian di dalam variabel `completeData` dan tidak mengubah struktur kode lainnya
5. Simpan file `index.html`

> **Tip**: Jika Anda ragu, buat cadangan file `index.html` asli sebelum mengeditnya.

## 5. Menyesuaikan Konfigurasi Tampilan

Anda juga dapat menyesuaikan tampilan Silsilah Visual dengan mengubah konfigurasi.

### Langkah-langkah:

1. Di file `index.html` yang sama, cari bagian kode yang memuat variabel `familyConfig`:

```javascript
const familyConfig = {
    familyName: "Keluarga Sejahtera",
    description: "Silsilah Lengkap Keluarga Besar",
    additionalFields: [
        // Field tambahan
    ],
    generationLabels: [
        "Generasi Awal",
        "Anak",
        "Cucu",
        "Cicit",
        "Canggah",
        "Wareng"
    ]
};
```

2. Ubah nilai-nilai berikut sesuai kebutuhan:
   - `familyName`: Nama keluarga yang akan ditampilkan di header
   - `description`: Deskripsi singkat tentang silsilah keluarga
   - `generationLabels`: Label untuk setiap generasi (jika berbeda dari default)

3. Simpan file setelah melakukan perubahan

## 6. Menggunakan Fitur Silsilah Visual

Setelah data berhasil diimpor, buka file `index.html` Silsilah Visual di browser Anda. Berikut cara menggunakan fitur-fitur utamanya:

### a. Navigasi Dasar
- **Klik pada anggota keluarga**: Untuk melihat detail lengkap
- **Klik pada nama di panel detail**: Untuk berpindah ke anggota keluarga tersebut

### b. Pencarian
- Gunakan kotak pencarian di bagian atas untuk mencari anggota keluarga
- Ketik sebagian nama dan hasil akan muncul secara otomatis
- Klik pada hasil pencarian untuk melihat anggota tersebut dalam pohon

### c. Filter Generasi
- Klik ikon filter di sebelah kotak pencarian
- Centang/hapus centang generasi yang ingin ditampilkan/sembunyikan
- Filter akan diterapkan secara langsung ke pohon silsilah

### d. Fitur Zoom
- Gunakan tombol "+" di pojok kanan bawah untuk memperbesar
- Gunakan tombol "-" untuk memperkecil
- Tombol reset untuk kembali ke skala normal

### e. Mode Gelap
- Klik ikon matahari/bulan di pojok kanan atas untuk beralih antara mode terang dan gelap
- Preferensi mode akan disimpan di browser Anda

## 7. Tips dan Trik

### Menangani Keluarga Besar
- Gunakan filter generasi untuk fokus pada generasi tertentu
- Manfaatkan fitur zoom untuk melihat gambaran keseluruhan atau detail
- Gunakan pencarian untuk menemukan anggota spesifik dengan cepat

### Navigasi Mobile
- Gunakan gestur cubit (pinch) untuk zoom di perangkat mobile
- Geser (swipe) untuk menavigasi pohon
- Ketuk pada anggota keluarga untuk melihat detail di panel yang muncul dari bawah

### Berbagi dengan Keluarga
- Simpan versi yang sudah diperbarui ke GitHub Pages atau hosting lain
- Kirim tautan kepada anggota keluarga lain
- Untuk berbagi secara offline, Anda dapat mengekspor halaman web lengkap (HTML + CSS + JS)

## 8. Pemecahan Masalah

### Pohon Tidak Muncul
- Periksa apakah format data `completeData` sudah benar
- Pastikan tidak ada tanda koma yang hilang atau berlebih di JSON
- Periksa konsol browser (F12) untuk melihat pesan error

### Masalah dengan ID
- Silsilah Visual akan secara otomatis menambahkan ID jika tidak ada
- Jika terjadi masalah dengan ID, pastikan setiap anggota keluarga memiliki ID unik

### Tampilan Tidak Responsif
- Pastikan Anda menggunakan browser terbaru
- Coba muat ulang halaman (Ctrl+F5)
- Jika masih bermasalah, coba buka di browser yang berbeda

### Data Hilang Setelah Refresh
- Silsilah Visual tidak menyimpan data secara otomatis
- Pastikan Anda menyimpan file HTML setelah mengimpor data

### Koneksi Garis Tidak Muncul
- Hubungan antar anggota keluarga ditampilkan dengan garis
- Jika garis tidak muncul, coba resize browser atau zoom in/out
- Jika masih bermasalah, periksa struktur data parent/children sudah benar

---

Dengan mengikuti tutorial ini, Anda dapat dengan mudah mengambil data dari Keluarga Visualizer dan menampilkannya dengan tampilan yang lebih modern dan interaktif menggunakan Silsilah Visual. Jika Anda masih memiliki pertanyaan atau mengalami masalah, jangan ragu untuk membuka Issue di repository GitHub kami.
