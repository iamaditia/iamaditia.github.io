---
title: "Blog Bermasalah (Lagi)"
excerpt: "Pentingnya swap file bagi server spek minimalis."
category:
  - Build in Public
tags:
  - blog
---

Beberapa hari belakangan setiap saya monitor di Google Search Console, beberapa halaman gagal masuk dalam index google. Gawat ini, pikir saya. Percuma saya tulis artikelnya tapi tidak bisa ditemukan di mesin pencari. Selama ini saya pikir mungkin kesalahan ada pada Google. Saya cukup klik tombol Validate Fix dan biasanya beberapa hari kemudian halaman yang awalnya gagal terindex menjadi oke lagi, alias masuk ke dalam index Google.

Semalam saya coba cek Google Search Console. Kali ini banyak sekali halaman yang tidak terindex. Saya coba akses beberapa kali web blog saya, terkadang bisa, terkadang muncul pesan error 504 Gateway Error (atau sejenisnya, saya lupa). Hmmm, jangan-jangan kegagalan index Google ini gara-gara blog saya down.

Mungkin solusinya dengan meng-update Ghost, software yang saya gunakan untuk blog. Tapi apa daya, mengakses droplet blog saja susahnya minta ampun. Beberapa kali tembus ke dalam console dropletnya, tapi ketika mengetikkan perintah untuk meng-update, tiba-tiba consolenya tidak respon.

Mungkin masalahnya ada di spesifikasi virtual server yang saya gunakan. Mulailah saya pertimbangkan untuk menambah kapasitas memory virtual server. Kenapa saya pikir masalahnya ada di memory? Karena selama ini setiap meng-update Ghost, pasti saya menggunakan perintah tambahan “--no-mem-check”. Kalau tidak menambahkan perintah sakti itu, dijamin proses update tidak akan lanjut karena gagal di pengecekan memory yang tersedia.

Setelah melihat-lihat price list Digital Ocean untuk penambahan memory, saya pun mengurungkan niat. Soalnya nilai sewa bulanan virtual server saya bakal bertambah jadi dua kali lipat tarif sebelumnya. Sebelumnya 6 USD per bulan (sekitar 92 ribu rupiah kurs November 2023), menjadi 12 USD per bulan (185 ribu rupiah kurs November 2023). Anggaran bulanan saya rasanya belum cukup untuk biaya sebanyak itu. Apalagi blog ini belum menghasilkan Rupiah sama sekali.

Sempat juga berpikir untuk mengalihkan isi blog ke alamat blog pribadi yang satu lagi. Tapi setelah mempertimbangkan ranking Google yang sudah susah payah diraih alamat blog sebelumnya, saya coba cari cara lain lagi.

Sebenarnya masih ada cara satu lagi yang berbayar: memindahkan isi droplet saya ke layanan berbayar yang disediakan Ghost. Biayanya tidak semahal meng-upgrade spesifikasi virtual server tadi, cukup 9 USD per bulan (sekitar 138 ribu Rupiah kurs November 2023). Tapi sepertinya proses pindah-pindahnya butuh waktu untuk migrasi, belum lagi berkomunikasi dengan CS Ghost. Jangan dulu ah.

Masalah tadi pun saya endapkan.

Pagi ini ketika baru tiba di kantor, saya coba buka lagi blog saya. Harusnya saya mulai mengetik jurnal harian, tapi entah kenapa tangan saya rasanya gatal ingin membereskan masalah blog yang down. Dan benar juga, blog saya masih belum bisa diakses.

Saya pun coba mencari-cari solusinya via Google, dimulai dengan mengetikkan pesan error yang muncul dan menambahkan kata kunci “Ghost Droplet Digital Ocean”. Ternyata di forum pengguna Ghost, masalah ini juga pernah dibahas. Saya coba postingan di forum tersebut sampai bawah. Ada yang mengalami masalah yang sama dan ternyata bisa.

Saya coba ikuti langkah-langkah di artikel yang disarankan. Alhamdulillah, berhasil. Blog saya kembali live. Bonusnya: ketika saya update Ghost, prosesnya jadi jauh lebih cepat dan lulus pengecekan memory meski tanpa perintah sakti.

Untuk langkah-langkahnya mungkin tidak akan saya jabarkan di sini. Intinya: buat swap file untuk membantu meringankan tugas RAM. Bonus lagi, saya ketemu aplikasi yang bisa memonitor uptime blog dan memberi notifikasi misal blognya down.

Akhirnya satu masalah blog terpecahkan pagi ini.

---

Beberapa artikel yang saya gunakan:
https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-20-04?ref=blog.electroica.com 

https://blog.electroica.com/ghost-blog-crashing-on-digital-ocean-droplet-fixed/ 