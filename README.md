# Gasing: Adu Putaran

Game gasing tradisional Nusantara berbasis web. Tarik tali, lempar gasing ke gelanggang pasir, dan bertahanlah paling lama. Dibuat dengan satu file HTML, tanpa framework dan tanpa instalasi.

**Demo:** `https://github.com/danisutrino/gametradisional

## Fitur

- **Tiga mode:** VS AI untuk main sendiri melawan Naga, 2 pemain di satu layar, atau **Online** dengan kode ruang untuk bermain di perangkat berbeda.
- **Fisika gasing:** gelanggang agak cekung, pinggirnya memantulkan gasing yang pelan, tabrakan memantul, dan gasing yang putarannya lebih lemah terpental lebih jauh serta kehilangan lebih banyak putaran. Satu ronde biasanya berlangsung sekitar 15 sampai 25 detik.
- **Tiga tingkat AI:** Santai, Gesit, dan Jago.
- **Serangan dorongan:** ketuk gelanggang (atau tekan Spasi) untuk mendorong gasingmu ke arah lawan, dengan jeda isi ulang.
- **Tampilan khas:** gelanggang pasir dengan bingkai kayu jati dan lingkar batik, jejak gasing di pasir, percikan api, layar bergetar saat benturan, dan putaran yang goyah saat melambat.
- **Layar loading** dengan gasing berputar dan bar progres.
- **Efek suara** (bisa dimatikan), tampilan responsif untuk HP, dan mendukung tema terang atau gelap sesuai perangkat.

## Cara bermain

1. Tarik ke bawah dari gasing merah (Garuda), seperti menarik tali. Makin jauh tarikan, makin kencang lemparan dan putarannya.
2. Lepas untuk melempar. Kedua gasing akan cenderung bertemu di tengah gelanggang. Setelah itu ketuk gelanggang (atau tekan Spasi) untuk **menyerang** dengan dorongan; isi ulangnya sekitar 2,6 detik dan memakan sedikit putaran.
3. Pinggir gelanggang memantulkan gasing yang pelan. Gasing kalah jika putarannya habis dan tumbang, atau terlempar keluar oleh hantaman sangat keras.
4. Menangkan **dua dari tiga ronde**.

**Mode VS AI:** main sendiri melawan Naga. Pilih tingkat Santai, Gesit, atau Jago.

**Mode Online (kode ruang):** pilih mode Online. Satu pemain menekan **Buat ruang** dan membagikan kode 5 huruf (atau menekan **Salin tautan ajakan**). Pemain lain memasukkan kode lalu menekan **Gabung**, atau cukup membuka tautan ajakan. Pembuat ruang menjadi Garuda (merah), yang bergabung menjadi Naga (hijau) dengan layar dibalik agar gasingnya selalu di bawah. Hanya pembuat ruang yang bisa menekan Mulai ulang.

**Mode 2 pemain:** Pemain 1 menarik dari gasing merah (bawah), Pemain 2 dari gasing hijau (atas). Boleh bersamaan dengan dua jari atau bergantian. Pemain yang belum melempar setelah 5 detik akan dilempar otomatis ke tengah. Untuk menyerang, ketuk separuh layarmu (Spasi untuk P1, Enter untuk P2).

## Menjalankan

Tidak perlu instalasi. Cukup unduh repository ini lalu buka `index.html` di browser.

```bash
git clone https://github.com/danisutrino/gametradisional
cd NAMA-REPO
# buka index.html di browser
```

## Publikasi dengan GitHub Pages

1. Pastikan `index.html` berada di folder paling luar repository.
2. Buka **Settings**, lalu **Pages**.
3. Pada **Branch**, pilih `main` dan folder `/ (root)`, lalu simpan.
4. Tunggu satu sampai dua menit, lalu buka alamat yang ditampilkan.

## Teknologi

- HTML, CSS, dan JavaScript murni
- [PeerJS](https://peerjs.com/) (WebRTC peer-to-peer) untuk mode Online, dimuat dari CDN jsDelivr
- Canvas 2D untuk gelanggang dan gasing
- Web Audio API untuk efek suara
- Font [Almendra Display](https://fonts.google.com/specimen/Almendra+Display) dan [Lora](https://fonts.google.com/specimen/Lora) dari Google Fonts (butuh koneksi internet agar tampilan sama persis)

## Catatan mode Online

- Perlu koneksi internet. Koneksi antar perangkat dibuat lewat server perantara publik milik PeerJS, setelah itu data dikirim langsung antar perangkat.
- Pembuat ruang menjalankan fisika permainan dan mengirim posisi gasing ke pemain lain sekitar 30 kali per detik. Pemain yang bergabung bisa merasakan sedikit jeda sesuai kualitas jaringannya.
- Tanpa server TURN, sebagian jaringan yang ketat (misalnya beberapa operator seluler atau jaringan kantor) bisa gagal tersambung. Jika itu terjadi, coba ganti jaringan (misalnya Wi-Fi yang sama atau hotspot).
- Kode ruang berlaku selama pembuat ruang tetap membuka halaman.

## Struktur

```
.
├── index.html   # seluruh game (HTML, CSS, JS)
└── README.md
```

## Pembuat

Dibuat oleh **Dani Sutrisno** dan **Dava Rianto** RPL.
