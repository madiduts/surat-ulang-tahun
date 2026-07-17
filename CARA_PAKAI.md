# Cara Edit & Publish Website Ucapan Ulang Tahun

## 1. Edit teksnya dulu
Buka `index.html` pakai text editor (Notepad, VS Code, atau apapun). Cari teks yang ada tanda kurung siku `[ ... ]`, itu semua placeholder yang harus kamu ganti:

- `[NAMA PACAR]` → nama pacar kamu (ada di 2 tempat)
- `[Nama kamu]` → nama kamu
- Paragraf-paragraf di section surat (`#letter`) → ganti dengan pesan ucapan milikmu
- File Foto (`assets/Foto_Grid_Alisya.jpeg`) → ganti dengan foto terbaik pacarmu atau foto kalian berdua
- Tahun dan nama pada kredit di bagian penutup halaman jika ingin disesuaikan

Tips: jangan kepanjangan per paragraf, 3-5 kalimat udah pas biar tetap elegan dibaca.

## 2. Masukin video & musik kamu

### A. Musik Latar (Lagu Pendukung)
Kita menggunakan pemutar musik latar otomatis yang akan berputar segera setelah pacarmu berinteraksi dengan membuka amplop:

1. **Siapkan File Musik**:
   - Cari file lagu dalam format **MP3** yang ingin kamu gunakan (misalnya lagu kesukaan kalian atau lagu romantis).
2. **Simpan ke Folder assets**:
   - Simpan berkas tersebut ke dalam folder `assets/` dan beri nama file **`music.mp3`** (pastikan menggunakan huruf kecil semua).
   - *Tips*: Jika kamu ingin menggunakan nama file lain, silakan buka `index.html`, cari bagian `<audio id="bgMusic">` lalu ubah `src="assets/music.mp3"` sesuai nama berkas lagumu.

### B. Video YouTube (Embed Player)
Karena video berukuran besar tidak bisa di-upload ke hosting GitHub secara langsung, kita menggunakan metode embed YouTube:

1. **Upload videomu ke YouTube**:
   - Buka YouTube Studio dan upload videomu.
   - Pada pilihan visibilitas, atur menjadi **Unlisted (Tidak Publik)**. Dengan begitu, videomu aman dari konsumsi umum, tidak akan muncul di pencarian publik, dan hanya bisa ditonton oleh orang yang memiliki link-nya (pacarmu).
2. **Dapatkan ID Video YouTube**:
   - Buka video tersebut dan salin ID videonya.
   - ID video adalah kombinasi karakter unik setelah parameter `v=` pada tautan YouTube.
     - Contoh tautan: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
     - Maka ID videonya adalah: `dQw4w9WgXcQ`
3. **Masukkan ke index.html**:
   - Buka file `index.html` dan cari bagian `<!-- ================= VIDEO ================= -->`.
   - Cari tag `<iframe>` dan ubah parameter `src="https://www.youtube.com/embed/dQw4w9WgXcQ"` dengan mengganti bagian `dQw4w9WgXcQ` menggunakan ID video YouTube milikmu sendiri.

## 3. Publish ke internet (gratis, pakai GitHub Pages)
Karena kamu udah punya akun GitHub, ini paling gampang:

1. Buka https://github.com/new → buat repository baru, misal namanya `surat-ulang-tahun`. Set ke **Public**. Jangan centang "Add README".
2. Di halaman repo yang baru dibuat, klik **"uploading an existing file"**.
3. Drag & drop isi folder ini (file `index.html` dan folder `assets` jika ada file poster/gambar pendukung) ke situ, lalu klik **Commit changes**.
4. Masuk ke tab **Settings** → **Pages** (di sidebar kiri).
5. Di bagian **Branch**, pilih `main` dan folder `/ (root)`, klik **Save**.
6. Tunggu 1-2 menit, refresh halaman itu. Nanti muncul link kayak:
   `https://username-kamu.github.io/surat-ulang-tahun/`
7. Itu link publiknya! Tinggal kirim ke pacar kamu, bisa dibuka dari HP atau laptop manapun, nggak perlu localhost.

## 4. Testing sebelum kirim
Buka link-nya sendiri dulu di HP kamu, cek:
- Amplop bisa diklik dan animasinya jalan
- Video muter dengan lancar
- Tampilan nggak berantakan di layar HP (udah didesain responsive, tapi cek aja)

Selesai! Selamat ngasih surprise 🕯️
