# Tugas Pendahuluan Modul 5 Pemrograman Web - Bootstrap

## 1. Memasang Bootstrap

Ada beberapa cara untuk menggunakan Bootstrap pada project:

1. **CDN (Content Delivery Network)**: menautkan file CSS dan JavaScript Bootstrap langsung dari server online. Cara ini paling mudah karena tidak perlu mengunduh file, tetapi membutuhkan koneksi internet. File CSS ditaruh di bagian head, sedangkan file JavaScript ditaruh sebelum penutup body.
2. **Download manual**: mengunduh file Bootstrap dari situs resminya, menyimpannya di folder project, lalu menautkannya secara lokal. Cara ini membuat halaman tetap berjalan tanpa koneksi internet.
3. **Package manager**: memasang Bootstrap menggunakan npm, yarn, atau composer. Cara ini umum dipakai pada project yang lebih besar atau yang memakai framework dan bundler.
4. **Compile dari source Sass**: menggunakan source Sass Bootstrap, mengubah variabelnya (misalnya warna dan ukuran), lalu meng-compile menjadi CSS. Cara ini cocok jika membutuhkan tema khusus atau ingin ukuran file yang lebih kecil.

## 2. Grid dan Breakpoint

**Class grid.** Grid Bootstrap membagi lebar halaman menjadi 12 kolom dan dibangun di atas flexbox. Susunannya terdiri dari tiga lapis: `container` sebagai pembungkus, `row` sebagai baris yang menampung kolom, dan `col` sebagai kolom. Class kolom diikuti angka (misalnya `col-6`) yang menunjukkan jumlah kolom yang dipakai dari total 12. Class `col` tanpa angka membagi lebar secara otomatis dan rata. Jika jumlah kolom dalam satu baris melebihi 12, kolom berlebih akan turun ke baris berikutnya.

**Kegunaan breakpoint.** Breakpoint adalah batas lebar layar tempat tampilan dapat berubah. Kegunaannya adalah membuat tampilan responsif, yaitu satu halaman yang tetap nyaman dilihat di ponsel, tablet, maupun desktop. Bootstrap memiliki enam breakpoint: extra small (di bawah 576px), small (576px ke atas), medium (768px ke atas), large (992px ke atas), extra large (1200px ke atas), dan extra extra large (1400px ke atas). Bootstrap menggunakan pendekatan mobile-first: class tanpa keterangan breakpoint berlaku untuk semua ukuran layar, sedangkan class dengan keterangan breakpoint (misalnya `col-md-6`) berlaku mulai ukuran tersebut ke atas. Dengan begitu, kolom dapat tersusun menumpuk di layar kecil dan berdampingan di layar besar.

## 3. Class Bootstrap

- `container`: pembungkus konten yang lebarnya menyesuaikan layar dan berada di tengah halaman.
- `btn` dan `btn-primary`: mengubah elemen menjadi tombol dengan gaya dan warna Bootstrap.
- `text-center`: meratakan teks ke tengah.
- `mt-3`, `mb-3`, `p-4`, dan sejenisnya: utility spacing untuk mengatur margin (m) dan padding (p) pada sisi tertentu dengan skala ukuran 0 sampai 5.
- `bg-success`: memberi warna latar hijau pada elemen.
- `shadow`: memberi bayangan pada elemen.
- `d-flex`: mengubah elemen menjadi flexbox untuk mengatur susunan elemen di dalamnya.
- `form-control`: memberi gaya pada input form agar rapi dan selebar elemen induknya.

## 4. Gambar Responsif

Agar gambar menyesuaikan ukuran layar, tambahkan class `img-fluid` pada elemen gambar. Class ini menerapkan `max-width: 100%` dan `height: auto`. Dengan `max-width: 100%`, gambar tidak akan melebihi lebar elemen induknya sehingga ikut mengecil saat layar menyempit. Dengan `height: auto`, tinggi gambar menyesuaikan otomatis sehingga rasio aspek tetap terjaga dan gambar tidak gepeng atau melar. Di luar Bootstrap, hasil yang sama bisa didapat dengan menulis kedua aturan CSS tersebut secara manual. Selain itu, halaman perlu memiliki meta viewport agar browser di perangkat mobile menampilkan halaman sesuai lebar layarnya.

## 5. Membuat Tampilan dengan Bootstrap

Halaman login **Ruang Baca** dibuat pada file `index.html` dengan Bootstrap 5.3.3 yang dimuat melalui CDN.

- **Navbar**: menggunakan komponen `navbar` dengan latar hijau (`bg-success`) dan teks terang. Nama "Ruang Baca" berada di kiri, sedangkan menu Beranda, Tentang, dan Bantuan berada di kanan. Pada layar kecil, menu berubah menjadi tombol hamburger yang dapat dibuka dan ditutup.
- **Tata letak**: menggunakan grid Bootstrap (`container`, `row`, `col`) dengan lebar kolom yang berbeda untuk tiap breakpoint, sehingga form memenuhi lebar layar di ponsel dan lebih ramping serta berada di tengah pada layar besar.
- **Form login**: ditempatkan dalam komponen `card` dengan bayangan. Isinya judul "Masuk ke Ruang Baca", subjudul, input Username, input Password, checkbox "Ingat saya", dan tombol "Masuk" selebar penuh berwarna hijau.
- **Footer card**: berlatar abu-abu muda dan berisi tautan "Lupa password?".
- **Utility Bootstrap**: digunakan untuk mengatur warna, jarak, lebar, dan bayangan sesuai contoh.

Fokus tugas ini adalah tampilan, sehingga tidak ada autentikasi, penyimpanan data login, maupun pemulihan password.
