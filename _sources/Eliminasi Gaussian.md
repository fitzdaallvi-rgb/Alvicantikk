# Eliminasi Gaussian

## Definisi Eliminasi Gaussian

Eliminasi Gaussian adalah suatu prosedur atau algoritma sistematis yang digunakan untuk menyelesaikan sistem persamaan linear (SPL). Proses ini bekerja dengan cara menerima masukan berupa matriks augmentasi, lalu mereduksinya menjadi matriks baru yang ekuivalen baris dalam Bentuk Eselon Baris. Tujuan utama dari penyederhanaan ini adalah agar hubungan antarvariabel menjadi jauh lebih jelas, sehingga solusi dari sistem persamaan tersebut dapat ditemukan dengan mudah melalui metode substitusi balik.

## Operasi Baris Elementer (OBE)

Untuk mereduksi suatu matriks hingga mencapai bentuk eselon baris, kita menggunakan proses yang disebut reduksi baris. Dalam proses ini, ada 3 jenis operasi dasar yang legal dan aman digunakan tanpa mengubah nilai solusi asli dari sistem linear tersebut:

    1. Perkalian Skalar: Mengalikan sebuah baris dengan bilangan tak-nol 
    $c \neq 0$ 
    (artinya, mengganti baris $r_i$ dengan 
    $c \cdot r_i$ 
    dengan cara mengalikan semua entri di baris tersebut dengan 
    $c$).V

    2. Pertukaran Baris: Menukar posisi dua baris sembarang di dalam matriks.
    
    3. Penjumlahan Baris: Menambahkan kelipatan satu baris ke baris yang lain (artinya, mengganti baris $r_i$ dengan $r_i + c \cdot r_j$ untuk suatu konstanta $c$).