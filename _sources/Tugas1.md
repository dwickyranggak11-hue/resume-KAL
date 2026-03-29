# Tugas Eliminasi Gaussian

## Membuat 5 Persamaan dan 5 Variabel

## Matriks Awal

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
1&0&1&0&0&4
\end{bmatrix}
$$

---

### Langkah 1  
Hilangkan 1 di kolom 1 baris 5

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

## Langkah 2  
Hilangkan -2 di kolom 2 baris 5

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

## Langkah 3  
Ubah 7 di kolom 3 baris 5 menjadi 1 (pivot)

$$
R_5 \leftarrow \frac{1}{7}R_5
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&1&0&0&3
\end{bmatrix}
$$

---

## Langkah 4  
Hilangkan 1 di kolom 3 baris 5

$$
R_5 \leftarrow R_5 - R_3
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&1&5&29\\
0&0&0&-4&0&-16
\end{bmatrix}
$$

---

## Langkah 5  
Ubah -4 di kolom 4 baris 5 menjadi 1 (pivot)

$$
R_5 \leftarrow -\frac{1}{4}R_5
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

## Langkah 6
Hilangkan 1 di kolom 4 baris 4

$$
R_4 \leftarrow R_4 - R_5
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&0&5&25\\
0&0&0&1&0&4
\end{bmatrix}
$$

---

## Langkah 7
Ubah 5 di kolom 5 baris 4 menjadi 1 (pivot)

$$
R_4 \leftarrow \frac{1}{5}R_4
$$

$$
\begin{bmatrix}
1&2&0&0&0&5\\
0&1&3&0&0&11\\
0&0&1&4&0&19\\
0&0&0&0&1&5\\
0&0&0&1&0&4
\end{bmatrix}
$$

## Hasil Akhir

$$
\begin{bmatrix}
1&0&0&0&0&1\\
0&1&0&0&0&2\\
0&0&1&0&0&3\\
0&0&0&1&0&4\\
0&0&0&0&1&5
\end{bmatrix}
$$