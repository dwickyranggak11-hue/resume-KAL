# Tugas Eliminasi Gaussian

## Membuat 5 Persamaan dan 5 Variabel

## Matriks Awal

$$
\begin{aligned}
x_1 + 2x_2 &= 5 \\
x_2 + 3x_3 &= 11 \\
x_3 + 4x_4 &= 19 \\
x_4 + 5x_5 &= 29 \\
x_1 + x_3 &= 4
\end{aligned}
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
1&0&1&0&0&4
\end{bmatrix}
$$

### Langkah 1 
Hilangkan elemen pada kolom 1 baris 5

$$
R_5 \leftarrow R_5 - R_1
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&-2&1&0&0&-1
\end{bmatrix}
$$

---

### Langkah 2
Hilangkan elemen pada kolom 2 baris 5

$$
R_5 \leftarrow R_5 + 2R_2
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&7&0&0&21
\end{bmatrix}
$$

---

### Langkah 3
Hilangkan elemen pada kolom 3 baris 5

$$
R_5 \leftarrow R_5 - 7R_3
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&-28&0&-112
\end{bmatrix}
$$

---

### Langkah 4
Membuat pivot 1 pada baris 5 kolom 4

$$
R_5 \leftarrow \frac{1}{-28}R_5
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&1&0&4
\end{bmatrix}
$$

---

### Langkah 5
Menukar baris agar pivot terurut
$$
R_4 \leftrightarrow R_5
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&0&4\\
0&0&0&1&5&29
\end{bmatrix}
$$

---

### Langkah 6
Hilangkan elemen 4 pada kolom 4 baris 3

$$
R_3 \leftarrow R_3 - 4R_4
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&1&5&29
\end{bmatrix}
$$

---

### Langkah 7
Hilangkan elemen pada kolom 4 baris 5

$$
R_5 \leftarrow R_5 - R_4
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&5&25
\end{bmatrix}
$$

---

### Langkah 8
Membuat pivot 1 pada kolom 5 baris 5

$$
R_5 \leftarrow \frac{1}{5}R_5
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&1&5
\end{bmatrix}
$$

---

### Langkah 9
Hilangkan elemen pada kolom 3 baris 2

$$
R_2 \leftarrow R_2 - 3R_3
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&1&5
\end{bmatrix}
$$

---

### Langkah 10
Hilangkan elemen pada kolom 2 baris 1

$$
R_1 \leftarrow R_1 - 2R_2
$$

$$
\begin{bmatrix}
1&0&0&0&0&1\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&1&5
\end{bmatrix}
$$

$$
\begin{aligned}
x_1 &= 1 \\
x_2 &= 2 \\
x_3 &= 3 \\
x_4 &= 4 \\
x_5 &= 5
\end{aligned}
$$