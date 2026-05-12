# Tugas Eigen Value dan Eigen Vektor dengan Dekomposisi

## Link Colab:
https://colab.research.google.com/drive/1yqguK8LLd_RI2jY1VJhMVmLloSH42xRV?usp=sharing

## Tahap 1 - Menentukan Matriks Awal

Langkah pertama adalah menentukan Matriks 2 x 2:

$$A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$$

Kemudian matriksnya dipecah menjadi dua vektor kolom yaitu 

$$a_{1} [2, 1] \text{ dan } a_{2} [1, 2]$$

## Tahap 2 - Membentuk Vektor q1

Langkah kedua adalah mencari panjang dari  vektor a_1 = [2, 1] menggunakan rumus Pythagoras:

$$\|a_1\| = \sqrt{x^2 + y^2}$$

$$\|a_1\| = \sqrt{2^2 + 1^2} = \sqrt{5} \approx 2.23606797749979$$

Setelah tahu panjangnya maka kita harus ubah vektor a_1 agar tetap menunjukkan arah yang sama, lalu panjangnya jadi 1. Caranya dengan membagi setiap komponen vektor a_1 dengan nilai normanya:

$$q_1 = \frac{a_1}{\|a_1\|}$$

Maka didapatkan vektor q1: 

$q_1 = [0.89442719, 0.4472136]$

## Tahap 3 - Menghitung Proyeksi a2

Setelah tau panjang bayangannya, ubala angkanya menjadi sebuah vektor.

Rumusnya: 

$$\text{Proyeksi } a_2 \text{ pada } q_1 = (q_1 \cdot a_2) \times q_1$$

Jadinya:

$$q_1 \cdot a_2 = 1.7888543819998317$$

$$\text{proj}_{q_1} a_2 = \begin{bmatrix} 1.6 & 0.8 \end{bmatrix}$$

## Tahap 4 - Membentuk Vektor Ortoganal u2

Vektor asli $a_2$: $[1, 2]$

Vektor Proyeksi  (proj): $[1.6, 0.8]$

Perhitungannya:

$$u_2 = \begin{bmatrix} 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 1.6 \\ 0.8 \end{bmatrix} = \begin{bmatrix} 1 - 1.6 \\ 2 - 0.8 \end{bmatrix} = \begin{bmatrix} -0.6 \\ 1.2 \end{bmatrix}$$

## Tahap 5 - Membentuk Vektor q2

Setelah mendapatkan vektor $u_2 = [-0.6, 1.2]$, maka cari panjangnya(norma).

Rumus:

$$\|u_2\| = \sqrt{(-0.6)^2 + (1.2)^2}$$
 
jadinya:

$$\|u\|_2 = 1.3416407864998738$$

Setelah itu bai setiap komponen vektor u2 dengan panjangnya sehingga panjngnya 1.

Rumus:

$$q_2 = \frac{u_2}{\|u_2\|}$$

jadinya:

$$\mathbf{q_2} = \begin{bmatrix} -0.4472136 & 0.89442719 \end{bmatrix}$$

## Tahap 6 - Membentuk Matriks Q dan R

Matriks A menjadi dua matriks:

$$\mathbf{Q} = \begin{bmatrix} 0.89442719 & -0.4472136 \\ 0.4472136 & 0.89442719 \end{bmatrix}$$

$$\mathbf{R} = \begin{bmatrix} 2.23606798 & 1.78885438 \\ 3.33066907 \times 10^{-16} & 1.34164079 \end{bmatrix}$$

## Tahap 7 - Verifikasi Dekomposisi QR

Hasil dari Q x R adalah:

$$\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$$

## Tahap 8 - Membentuk Matriks Iterasi Baru

Mengalikan R setelah itu Q:

$$\mathbf{A_1} = \mathbf{RQ} = \begin{bmatrix} 2.8 & 0.6 \\ 0.6 & 1.2 \end{bmatrix}$$

## Tahap 9 - Iterasi QR hingga 10 kali

Proses Konvergensi Eigenvalue menggunakan Aloritma QR

Iterasi 2
[[2.9756 0.2195]
 [0.2195 1.0244]]

Iterasi 3
[[2.9973 0.074 ]
 [0.074  1.0027]]

Iterasi 4
[[2.9997 0.0247]
 [0.0247 1.0003]]

Iterasi 5
[[3.     0.0082]
 [0.0082 1.    ]]

Iterasi 6
[[3.0e+00 2.7e-03]
 [2.7e-03 1.0e+00]]

Iterasi 7
[[3.e+00 9.e-04]
 [9.e-04 1.e+00]]

Iterasi 8
[[3.e+00 3.e-04]
 [3.e-04 1.e+00]]

Iterasi 9
[[3.e+00 1.e-04]
 [1.e-04 1.e+00]]

Iterasi 10
[[3. 0.]
 [0. 1.]]

## Tahap 10 - Kesimpulan Nilai Eigen

Setelah dilakukan 10 x iterasi, maka matriks akhirnya :

$$\begin{bmatrix}
3 & 0 \\
0 & 1
\end{bmatrix}$$

Nilai Eigen:

lambda_1 = 3.0

lambda_2 = 1.0

Kesimpulan:

Metode QR berhasil menemukan nilai eigen
dari matriks A melalui proses iterasi.