# Tugas SVD

## Link Colab:
https://colab.research.google.com/drive/1x8DhLNZYLB2rclqrHnUm7qK2yefZUOBQ?usp=sharing

## Langkah 1 : Upload dan Menyiapkan Citra Gambar (Preprocessing)

Pada tahap pertama yaitu menyiapkan data. Algoritma matematika SVD hanya dapat memproses matriks dengan dimensi dua (m x n), maka gambar asli yang diunggah (Berwarna/RGB) harus dikonversi menjadi skala abu-abu (Grayscale) terlebih dahulu. Setelah dikonversi setiap kotak di dalam matriks hanya akan berisi satu angka tunggal yang merepresentasikan tingkat kecerahan piksel yaitu mulai dari 0 (Hitam pekat) sampai 255 (Putih terang).

Berdasarkan output tugas saya, gambar anak kecil yang saya unggah berhasil dibaca dengan teks "Gambar berhasil dimuat dengan dimensi : 678 x 736 piksel". Angka ini menunjukkan bahwa gambar saya memiliki resolusi yang cukup tinggi yaitu terdiri dari 678 baris dan 736 kolom data piksel yang siap ke langkah berikutnya.

## Langkah 2 : Dekomposisi Matriks SVD

Pada tahap kedua ini matriks gambar asli (A) dibongkar secara matematis menggunakan fungsi aljabar linear np.Linalg.svd menjadi tiga komponen matriks terpisah sesuai persamaan rumus dasar

$$A = U \Sigma V^T$$

SVD secara otomatis akan mengurutkan seluruh fitur informasi gambar dari yang paling dominan hingga yang paling tidak penting dalam matriks diagonalnya.

Pada output saya hasil pembongkaran matriks gambar asli berukuran 678 x 736 menjadi tiga komponen baru dengan dimensi yaitu:

1. Matris U berukuran persegi (678, 678) yang mewakili fitur spesial vertikal pada gambar.

2. Vektor S sepanjang (678) elemen yang menyimpan nilai singular sebagai bobot penting fitur.

3. Matriks $V^T$ berukuran (678, 736) yang mewakili fitur spasial horizontal gambar. Jika ketiga matriks komponen dikalikan kembali secara utuh menggunakan operasi matematika maka  saya mendapatkan gambar asli 100% tanpa ada perubahan.

## Langkah 3 : Rekonstruksi / Kompresi Gambar (Variasi Nilai K)

Pada langkah ketiga menerapkan konsep Low-Rank Approximation (Pendekatan Matriks Berpangkat Rendah). Yaitu dengan melakukan uji coba kompresi gambar dengan memotong ukuran ketiga komponen matriks (U, S dan $V^T$) yang hanya sampai indeks ke-k tertentu, lalu mengalikan sisanya kembali $(U_k \times \Sigma_k \times V_k^T)$. Tujuannya yaitu membuktikan seberapa banyak data yang bisa dibuang tanpa merusak kualitas visual gambar utama.

Pada output saya visualisasi keajaiban proses rekonstruksi wajah berdasarkan variasi jumlah komponen k adalah:

1. Pada k = 2 data memori yang digunakan hanya 0.6%. Hasil gambarnya masih berupa garis-garis abstrak hitam putih karena saya baru mengambil informasi pencahayaan global luar saja.

2. Pada k = 10 dengan memori kecil sebesar 2.8% bentuk poni rambut, mata dan siluet wajah anak kecil sudah mulai bisa dikenali.

3. Pada k = 30 dengan memori hemat 8.9% bentuk wajah, mata hingga detail jari tangan sudah terlihat jelas.

4. Pada k = 60 kualitas gambar sudah sangat tajam dan hampir tidak bisa dibedakan dengan mata dari gambar aslinya. Padahal memori data yang digunakan hanya 17.0%.

Jadi saya berhasil membuang sekitar 83% data redundan pada gambar namun tetap mempertahankan kualitas visual wajahnya secara optimal.

## Langkah 4 : Grafik Diagnostik Proses SVD (Distribusi Energi)

Grafik  ini dinamakan Scree Plot yang berfungsi sebagai alat bukti ilmiah untuk memvisualisasikan tingkat penurunan (Decay Rate) nilai singular (S). Grafik ini melandasi alasan logis mengapa pemotongan matriks (Kompresi) pada langkah 3 sah dilakukan secara sistematis.

Berdasarkan output saya sumbu X menunjukkan indeks nilai singular dari 0 sampai 678 dan sumbu Y adalah nilai energinya:
1. Pada titik awal (Indeks 0) grafik melonjak menembus angka di atas 90.000. Yang menjadi bukti bahwa informasi struktur utama pembentuk gambar semuanya berpusat di beberapa komponen awal saja.

2. Setelah itu grafiknya langsung turun ke angka 5.000, lalu mendatar secara konstan mendekati angka 0 mulai dari indeks 60 hingga akhir grafik di angka 678.

Garis mendatar panjang membuktikan bahwa ratusan data dari indeks 60 sampai ke belakang nilainya tidak signifikan dan hanya berupa detail mikro atau noise kamera yang tidak terlalu penting. Jadi keputusan saya memilih nilai kompresi murni di rentang siku grafik seperti (k = 60) terbukti sukses memotong data kosong demi menghemat ruang penyimpanan.  