# Materi 1

## PERSAMAAN LINIER


Secara matematis, persamaan linear adalah sebuah persamaan yang memiliki derajat(pangkat) tertinggi satu. Jika sebuah persamaan memiliki variabel x atau y, maka variabel tersebut tidak boleh memiliki pangkat selain satu(misal:x^2,x^3, dst tidak diperbolehkan. Mengingat bahwa sebuah garis dua dimensi dalam sistem koordinat xy dapat direpresentasikan dengan bentuk persamaan:

$$
ax + by = c(a,b /ne 0)
$$

Dan sebuah bidang tiga dimensi dalam sistem koordinat xyz dapat direpresentasikan dengan bentuk persamaan:

$$
ax + by + cz = d (a,b,c /ne 0)
$$

Bentuk-bentuk di atas adalah contoh-contoh dari persamaan linear, dimana yang pertama dalam variabel x dan y sedangkan yang kedua dalam variabel x, y dan z. Secara umum, sebuah persamaan linear dalam n variabel x_1,x_2,...,x_n dapat direpresentasikan dalam bentuk:

$$
a_1x_1 + a_2 x_2 + ... a_n x_n = b
$$

Dimana a_1, a_2, ..., a_n dan b adalah konstanta dan semua a tidak nol. Dalam kasus khusus dimana n=2 atau n=3, akan sering digunakan variabel tanpa subscript dan persamaan linear dalam bentuk:

$$
a_1 x + a_2 y = b (a_1, a-2 /ne 0)
a_1 x + a_2 y + a_3 z = b (a_1, a_2, a_3 /ne 0)
$$

Dalam kasus khusus dimana b=0, persamaan bentuk (1) menjadi:

$$
a_1 x_1 + a_2 x_2 + ..., a_n, x_n = 0
$$

Disebut persamaan liniar homogen dalam variabel x_1, x_2, ..., x_n.

Contoh 1: Persamaan Linear
Perhatikan bahwa suatu persamaan linier tidak melibatkan variabel berupa hasil kali atau bentuk akar. Semua variabel hanya berpangkat satu dan tidak dituliskan. Berikut ini adalah contoh persamaan linear:

$$
x + 3y = 7
\frac{1}{2}x - y + 3z = -1
x_1 - 2x_2 - 3x_3 + x_4 = 0
x_1 + x_2 +...+ x_n = 1
$$

Berikut ini adalah contoh bukan persamaan linier:

$$
x + 3y_2 = 4
3x + 2y - xy = 5
sin x + y = 0
\sqrt{x_1} + 2x_2 + x_3 = 1
$$

Himpunan terbatas dari persamaan linier disebut sistem persamaan  disebut sistem persamaan linier atau sistem linier. Variabelnya disebut tak diketahui. sebagai contoh, sistem (5) berikut ini memiliki x dan y yang tak diketahui dan sistem (6) memiliki x_1, x_2, dan x_3 yang tak diketahui. 

$$
\begin{cases}
5x + y = 3 \\
2x - y = 4
\end{cases}

\begin{cases}
4x_1 - x_2 + 3x_3 = -1 \\
3x_1 + x_2 + 9x_3 = -4
\end{cases}
$$

Secara umum, sistem linier dari m persamaan dengan variabel n tak diketahui dapat ditulis sebagai:

$$
\left.
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n &= b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n &= b_m
\end{aligned}
\right\}
$$

Solusi dari sistem linier dalam n variabel tak diketahui x_1, x_2,..., x_n adalh barisan dari n bilangan s_1, s_2, ..., x_n dimana substitusinya adalah:

$$
x_1 = s_1, x_2 = s_2, ..., x_n = s_n
$$

Yang membuat masing-masing persamaan menjadi pernyataan yang benar. Sebagai contoh, sistem (5) memiliki solusi:

$$
x = 1, y = -2
$$

Dan sistem (6) memiliki solusi:

$$
x_1 = 1, x_2 = 2, x_3 = -1
$$

Dimana nama-nama variabel diabaikan. Notasi ini, membolehkan kita menginterpretasikan solusi secara geometri sebagai titik-titik dalam ruang 2 dimensi dan 3 dimensi. Secara umum, solusinya adalah:

$$
x_1 = s_1, x_2 = s_2,..., x_n = s_n
$$

Dari sistem linier dengan n variabel tak diketahui dapat ditulis sebgai;

$$
(s_1, s_2,.., s_n)
$$

Yang disebut sebgai pasangan ganda (kembar) n berurutan. Dengan notasi ini dapat dipahami bahwa semua variabel muncul dalam ururtan yang sama dalam setiap persamaan. Jika n = 2 maka pasangan ganda (kembar) n berurutan disebut pasangan berurutan dan jika n = 3 disebut pasangan ganda (kembar) 3 berurutan.

Bentuk standar persamaan linear dengan n variabel adalah:


          a_1 x_1 + a_2 x_2 + ... + a_n x_n = b

Dimana:



*   a_1,a_2,...: adalah koefisien(angka pendamping variabel)
*   x_1,x_2,...: adalah variabel(nilai yang belum diketahui)
*   b: adalah kostanta

Dalam ruang dua dimensi(2D) setiap pasangan nilai(x,y) yang memenuhi persamaan tersebut, jika dihubungkan akan membentuk garis lurus(line) yang tidak terputus dan tidak berbelok. Secara geometris, persamaan linear merepresentasikan perubahan yang konstan. Jika nilai x bertambah, maka nilai y akan bertambah(atau berkurang) dengan rasio yang tetap. itulah yang disebut gradien atau kemiringan garis.

Persamaan linear memiliki sifat-sifat unik yang membedakannya dari persamaan non-linear(seperti kuadrat atau eksponensial):



1.   Sifat penjumlahan: kita bisa menambahkan atau mengurangi kedua ruas dengan angka yang sama tanpa mengubah nilai kebenaran persamaan.
2.   Sifat perkalian: Kita bisa mengali atau membagi kedua ruas dengan angka yang sama(selama bukan nol).
3.   Visualisasi: Didalam koordinat kartesius, ia tidak akan pernah memiliki titik puncak atau lembah(parabola), melainkan membentang lurus hingga tak terhingga.


Contoh dua persamaan linier dengan dua variabel

$$f:3x + 4y = 24$$
$$g:5x - 2y = 14$$

![Persamaan Linear](grafik/persamaan_linear_1.png)

$$f:3x + 2y = 10$$
$$g:2x + 5y = 14$$

![Persamaan Linear](grafik/persamaan_linear_2.png)



