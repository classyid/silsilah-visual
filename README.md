# Silsilah Visual

![Banner Silsilah Visual](https://via.placeholder.com/800x200?text=Silsilah+Visual)

## 📋 Deskripsi

**Silsilah Visual** adalah aplikasi web modern untuk menampilkan dan menjelajahi pohon silsilah keluarga. Aplikasi ini menawarkan pengalaman pengguna yang lebih baik dengan tampilan visual yang menarik, mode gelap, pencarian anggota keluarga, filter berdasarkan generasi, dan fitur zoom untuk navigasi yang mudah.

Silsilah Visual dirancang sebagai pasangan sempurna untuk aplikasi [Keluarga Visualizer](https://github.com/classyid/keluarga-visualizer), yang memungkinkan Anda membuat dan mengelola data silsilah keluarga. Data yang dihasilkan dari Keluarga Visualizer dapat dengan mudah diimpor ke Silsilah Visual untuk mendapatkan tampilan yang lebih modern dan interaktif.

## ✨ Fitur Utama

- ✅ Tampilan pohon silsilah visual yang modern dan intuitif
- ✅ Mode gelap (dark mode) untuk kenyamanan penggunaan di malam hari
- ✅ Pencarian anggota keluarga secara instan
- ✅ Filter berdasarkan generasi untuk fokus pada bagian tertentu
- ✅ Panel detail untuk melihat informasi lengkap anggota keluarga
- ✅ Fitur zoom dan navigasi sentuh untuk perangkat mobile
- ✅ Kompatibilitas penuh dengan data dari Keluarga Visualizer
- ✅ Tampilan responsif untuk desktop dan mobile
- ✅ Animasi dan transisi yang halus

## 🚀 Cara Menggunakan

### Menggunakan Versi Online

Kunjungi [Website ini](https://silsilah-visual.vercel.app) untuk menggunakan aplikasi tanpa perlu menginstal apapun.

### Menjalankan Secara Lokal

1. Clone repository ini
   ```bash
   git clone https://github.com/classyid/silsilah-visual.git
   ```

2. Buka folder project
   ```bash
   cd silsilah-visual
   ```

3. Buka file `index.html` di browser Anda

## 🔄 Mengimpor Data dari Keluarga Visualizer

1. Buat pohon keluarga menggunakan aplikasi [Keluarga Visualizer](https://github.com/classyid/keluarga-visualizer)
2. Tekan tombol "Generate CompleteData" lalu "Copy Code"
3. Buka file `index.html` dari Silsilah Visual di editor kode Anda
4. Cari bagian `const completeData = [...]` dan ganti dengan data dari Keluarga Visualizer
5. Simpan file dan muat ulang halaman untuk melihat pohon keluarga Anda

Lihat [TUTORIAL.md](./TUTORIAL.md) untuk petunjuk langkah-demi-langkah yang lebih detail.

## 📱 Tampilan Aplikasi

![Tampilan Desktop](https://via.placeholder.com/800x450?text=Tampilan+Desktop)
![Tampilan Mobile](https://via.placeholder.com/400x700?text=Tampilan+Mobile)

## 🛠️ Teknologi yang Digunakan

- HTML5
- CSS3 dengan TailwindCSS
- JavaScript
- AlpineJS untuk reaktivitas
- LocalStorage untuk menyimpan preferensi

## 📊 Contoh Data

Aplikasi ini sudah dilengkapi dengan contoh data keluarga. Untuk menggunakan data Anda sendiri, lihat bagian [Mengimpor Data dari Keluarga Visualizer](#-mengimpor-data-dari-keluarga-visualizer).

## 🌟 Perbedaan dengan Keluarga Visualizer

| Fitur | Silsilah Visual | Keluarga Visualizer |
|-------|----------------|---------------------|
| Fokus Utama | Menampilkan silsilah | Membuat dan mengelola data |
| Tampilan | Modern dengan mode gelap | Fungsional |
| Pencarian | Real-time dengan hasil detail | Highlight simpel |
| Filter | Filter multi-generasi | Filter satu generasi |
| Detail | Panel informasi terpisah | Informasi langsung di tree |
| Responsif | Optimized untuk mobile | Basic responsive |
| Zoom | Fitur zoom in/out | Tidak ada |

## 🤝 Kontribusi

Kontribusi selalu disambut baik! Silakan buat Pull Request atau buka Issue jika Anda memiliki saran atau menemukan bug.

## 📄 Lisensi

Project ini dilisensikan di bawah [MIT License](./LICENSE).

---

Dibuat dengan ❤️ oleh [Andri Wiratmono](https://github.com/classyid)
