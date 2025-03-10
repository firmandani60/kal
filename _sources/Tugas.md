---
title: Untitled

---

### Operasi Baris Elementer 
Operasi Baris Elementer (OBE) adalah serangkaian operasi yang digunakan untuk memanipulasi baris dalam matriks tanpa mengubah solusi dari sistem persamaan linear yang direpresentasikan oleh matriks tersebut. OBE sering digunakan dalam metode eliminasi Gauss dan Gauss-Jordan untuk menyelesaikan sistem persamaan linear, mencari invers matriks, dan menentukan determinan.
1. Pertukaran Baris (Row Swapping)
2. Perkalian Baris dengan Skalar (Row Scaling)
3. Penjumlahan Baris (Row Addition/Subtraction)

Operasi-operasi ini digunakan untuk mengubah matriks ke dalam bentuk eselon baris atau eselon baris tereduksi, yang mempermudah penyelesaian sistem persamaan linear.

### Eliminasi Gauss 
Eliminasi Gauss adalah metode yang digunakan untuk menyelesaikan sistem persamaan linear dengan mengubah matriks yang merepresentasikan sistem tersebut menjadi bentuk eselon baris melalui Operasi Baris Elementer (OBE). Metode ini juga digunakan dalam perhitungan invers matriks dan determinan.
Tahapan Eliminasi Gauss

Eliminasi Gauss dilakukan dalam dua tahap utama:

1.Eliminasi Maju (Forward Elimination)
- Mengubah matriks menjadi bentuk eselon baris (row echelon form).
- Elemen-elemen di bawah diagonal utama dijadikan nol.
2. Substitusi Mundur (Back Substitution)
- Menyelesaikan sistem persamaan dari baris terakhir ke baris pertama untuk mendapatkan nilai variabel.

### Contoh Soal 1
Selesaikan dengan menggunakan eleminasi gauss

$$
\begin{array}{cc}
x_1+2x_2+3x_3&=6\\
2x_1+4x_2+6x_3&=12\\
x_3+x_2&=2
\end{array}
$$

Penyelesaian
Langkah 1: Tulis dalam Bentuk Matriks Augmented
Bentuk matriks augmented dari sistem ini adalah:

\begin{bmatrix}
1 & 2 & 3 & | 6 \\
2 & 4 & 6 & | 12 \\
0 & 1 & 1 & | 2
\end{bmatrix}


Langkah 2: Eliminasi Baris
Kita akan menghilangkan elemen di bawah elemen utama di kolom pertama. Gunakan operasi:

\begin{array}{cc}
R_2 \rightarrow R_2 - 2R_1
\end{array}


Sehingga:

\
\begin{bmatrix}
1 & 2 & 3 & | 6 \\
0 & 0 & 0 & | 0 \\
0 & 1 & 1 & | 2
\end{bmatrix}

Langkah 3: Interpretasi
Baris kedua dirubah menjadi *0 = 0*

\begin{aligned}
x_1 + 2x_2 + 3x_3 &= 6 \\
x_2 + x_3 &= 2
\end{aligned}

Langkah 4: Substitusi
Dari persamaan kedua:

\begin{array}{cc}
x_2 = 2 - x_3
\end{array}

Substitusikan ke persamaan pertama:

\begin{array}{cc}
x_1 + 2(2 - x_3) + 3x_3& = 6\\
x_1 + 4 - 2x_3 + 3x_3& = 6\\
x_1 + 4 + x_3& = 6\\
x_1 =& 2 - x_3
\end{array}

Kesimpulan
Solusi umum dari sistem ini adalah:

\begin{aligned}
x_1 &= 2 - x_3 \\
x_2 &= 2 - x_3 \\
x_3 &= x_3
\end{aligned}


### Contoh Soal 2 
Selesaikan dengan menggunakan eliminasi gauss
$$
\begin{array}{cc}
x_1+x_2+x_3&=3\\
2x_1+x_3&=5\\
x_1+2x_2&=3
\end{array}
$$

Penyelesaian 
Langkah 1: Tulis dalam Bentuk Matriks Augmented

\begin{bmatrix}
1 & 1 & 1 & | 3 \\
2 & 0 & 1 & | 5 \\
1 & 2 & 0 & | 3
\end{bmatrix}

Langkah 2: Eliminasi Baris
Kita akan menghilangkan elemen di bawah elemen utama di kolom pertama.

\begin{array}{cc}
R_2 \rightarrow R_2 - 2R_1
\end{array}

\begin{array}{cc}
R_3 \rightarrow R_3 - R_1
\end{array}

Sehingga matriks berubah menjadi:

\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & -2 & -1 & | -1 \\
0 & 1 & -1 & | 0
\end{bmatrix}

Selanjutnya, buat elemen utama di baris kedua menjadi 1 dengan membagi baris kedua dengan -2:

\begin{array}{cc}
R_2 \rightarrow \frac{R_2}{-2}
\end{array}

Hasilnya:

\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & 1 & \frac{1}{2} & | \frac{1}{2} \\
0 & 1 & -1 & | 0
\end{bmatrix}

Kemudian eliminasi elemen di bawah elemen utama dengan:

\begin{array}{cc}
R_3 \rightarrow R_3 - R_2
\end{array}

Sehingga diperoleh:
\begin{bmatrix}
1 & 1 & 1 & | 3 \\
0 & 1 & \frac{1}{2} & | \frac{1}{2} \\
0 & 0 & -\frac{3}{2} & | -\frac{1}{2}
\end{bmatrix}
Langkah 3: Substitusi Balik*
Dari baris ketiga:

\begin{array}{cc}
-\frac{3}{2} x_3 = -\frac{1}{2}
\end{array}

\begin{array}{cc}
x_3 = \frac{1}{3}
\end{array}

Dari baris kedua:

\begin{array}{cc}
x_2 + \frac{1}{2} x_3 = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 + \frac{1}{2} \times \frac{1}{3} = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 + \frac{1}{6} = \frac{1}{2}
\end{array}

\begin{array}{cc}
x_2 = \frac{1}{2} - \frac{1}{6} = \frac{3}{6} - \frac{1}{6} = \frac{2}{6} = \frac{1}{3}
\end{array}

Dari baris pertama:
\begin{array}{cc}
x_1 + x_2 + x_3 = 3
\end{array}

\begin{array}{cc}
x_1 + \frac{1}{3} + \frac{1}{3} = 3
\end{array}

\begin{array}{cc}
x_1 = 3 - \frac{2}{3} = \frac{9}{3} - \frac{2}{3} = \frac{7}{3}
\end{array}

Kesimpulan
Jadi, solusi dari sistem persamaan adalah:
\begin{aligned}
x_1 &= \frac{7}{3} \\
x_2 &= \frac{1}{3} \\
x_3 &= \frac{1}{3}
\end{aligned}

### Contoh Soal 3 
Selesaikan dengan menggunakan eliminasi gauss
$$
\begin{array}{cc}
2x_1+2x_2&=4\\
x_1+x_2&=2
\end{array}
$$

Penyelesaian 
Langkah 1 : Menyelesaikan ke bentuk matriks augmented 

\begin{bmatrix} 
2 & 2 & | 4 \\ 
1 & 1 & | 2 
\end{bmatrix}

Langkah 2 : membuat elemen di bawah pivot menjadi nol. 

\begin{array}{cc}
R_1 \leftarrow R_1 - 2R_2
\end{array}

Setelah melakukan perhitungan kita mendapatkan :

$$
\begin{array}{cc}
R_1: 2 - 2 \cdot 1 = 0\\
2 - 2 \cdot 1 = 0\\
4 - 2 \cdot 2 = 0
\end{array}
$$

Sehingga matriks augmented menjadi : 

\begin{bmatrix} 
1 & 1 & | 2 \\
0 & 0 & | 0 
\end{bmatrix}

Dari baris kedua, kita dapat mengekspresikan (x_1) dalam bentuk (x_2): 

\begin{array}{cc}
x_1 + x_2 = 2 \Rightarrow x_1 = 2 - x_2
\end{array}


Karena kita memiliki satu persamaan dengan dua variabel, kita dapat menyatakan solusi dalam bentuk parameter. Misalkan (x_2 = t), maka:

\begin{array}{cc}
x_1 = 2 - t
\end{array}

Jadi, solusi umum dari sistem persamaan ini adalah:

\begin{cases} 
x_1 = 2 - t\\
x_2 = t
\end{cases}

di mana (t) adalah parameter bebas.

### Contoh Soal 4 
Selesaikan dengan menggunakan eliminasi gauss
$$
\begin{array}{cc}
x_1+x_2&=5\\
x_1+2x_3&=6\\
\end{array}
$$

Penyelesaian : 

1. Tulis sistem persamaan dalam bentuk matriks augmented:

\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
1 & 0 & 2 & | & 4
\end{bmatrix}


2. Lakukan operasi baris untuk mendapatkan bentuk eselon baris:


\begin{array}{cc}
R_2 \rightarrow R_2 
\end{array}

Hasilnya : 

\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & -1 & 2 & | & -1
\end{bmatrix}

\begin{array}{cc}
R_2 \rightarrow \frac{R_2}{-1}
\end{array}

Hasilnya : 

\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & 1 & -2 & | & 1
\end{bmatrix}

3. Lakukan substitusi mundur untuk menemukan solusi:

- Dari baris 2:

\begin{array}{cc}
x_1 + x_2 = 2 \Rightarrow x_1 = 2 - x_2
\end{array}

- Dari baris 1:

\begin{array}{cc}
x_1 + x_2 = 5 \implies x_1 + (1 + 2x_3) = 5 \implies x_1 = 4 - 2x_3
\end{array}

4. Solusi Akhir:

\begin{aligned}
x_1 &= 4 - 2x_3 \\
x_2 &= 1 + 2x_3 \\
x_3 &= x_3
\end{aligned}

Jadi, solusi dari sistem persamaan adalah:

\begin{array}{cc}
\left(x_1, x_2, x_3\right) = \left(4 - 2t, 1 + 2t, t\right), \quad t \in \mathbb{R}
\end{array}

Sistem ini memiliki banyak solusi karena terdapat parameter bebas $( t )$.
