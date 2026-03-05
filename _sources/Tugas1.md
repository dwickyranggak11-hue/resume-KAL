# Tugas Eliminasi Gaussian

## Membuat 5 Persamaan dan 5 Variabel

# Eliminasi Gauss {#eliminasi-gauss .unnumbered}

Matriks awal:

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
1&0&1&0&0&4
\end{bmatrix}$$

Langkah 1: Hilangkan angka 1 di bawah pivot pertama (kolom 1)

$$R_5 \leftarrow R_5 - R_1$$

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&-2&1&0&0&-1
\end{bmatrix}$$

Langkah 2: Hilangkan -2 di kolom 2 baris 5

$$R_5 \leftarrow R_5 + 2R_2$$

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&7&0&0&21
\end{bmatrix}$$

Langkah 3: Hilangkan 7 di kolom 3 baris 5

$$R_5 \leftarrow R_5 - 7R_3$$

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&-28&0&-112
\end{bmatrix}$$

Langkah 4: Hilangkan -28 di kolom 4 baris 5

$$R_5 \leftarrow R_5 + 28R_4$$

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&0&140&700
\end{bmatrix}$$

Langkah 5: Buat pivot jadi 1

$$R_5 \leftarrow \frac{1}{140}R_5$$

$$\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&0&1&5
\end{bmatrix}$$

Lanjutkan eliminasi ke atas hingga diperoleh:

$$\begin{bmatrix}
1&0&0&0&0&1\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&1&5
\end{bmatrix}$$

Sehingga solusi sistem adalah:

$$(x_1,x_2,x_3,x_4,x_5) = (1,2,3,4,5)$$
