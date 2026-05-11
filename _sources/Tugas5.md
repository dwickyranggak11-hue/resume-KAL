# Eigen Value dan Eigen Vector

Link Colab Program Pyhton: https://colab.research.google.com/drive/1q8F1_UzZpoYex3Zvdg-y2MZ7boE4UXiB?usp=sharing

Diketahui matriks:

$$
A=
\begin{bmatrix}
2 & 1\\
1 & 2
\end{bmatrix}
$$

Metode QR Iteration digunakan untuk mencari eigenvalue suatu matriks.

Prinsip dasar metode QR:

1. Faktorkan matriks menjadi:

$$
A_k = Q_kR_k
$$

dengan:

- $Q_k$ = matriks ortogonal
- $R_k$ = matriks segitiga atas

2. Bentuk matriks baru:

$$
A_{k+1}=R_kQ_k
$$

3. Ulangi proses tersebut hingga elemen di luar diagonal mendekati nol.

---

### ITERASI 0

Matriks awal:

$$
A_0=
\begin{bmatrix}
2 & 1\\
1 & 2
\end{bmatrix}
$$

---

## Langkah 1 — Menentukan Vektor Kolom

Kolom pertama:

$$
a_1=
\begin{bmatrix}
2\\
1
\end{bmatrix}
$$

Kolom kedua:

$$
a_2=
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

---

## Langkah 2 — Mencari $q_1$

Rumus:

$$
q_1=\frac{a_1}{||a_1||}
$$

Menghitung panjang $a_1$:

$$
||a_1||=
\sqrt{2^2+1^2}
$$

$$
=
\sqrt{4+1}
$$

$$
=
\sqrt5
$$

Maka:

$$
q_1=
\begin{bmatrix}
\frac2{\sqrt5}\\
\frac1{\sqrt5}
\end{bmatrix}
$$

---

## Langkah 3 — Mencari $v_2$

Rumus Gram-Schmidt:

$$
v_2=a_2-(q_1\cdot a_2)q_1
$$

---

#### Menghitung $q_1 \cdot a_2$

$$
\left(\frac2{\sqrt5}\times1\right)
+
\left(\frac1{\sqrt5}\times2\right)
$$

$$
=
\frac2{\sqrt5}
+
\frac2{\sqrt5}
$$

$$
=
\frac4{\sqrt5}
$$

---

#### Menghitung $(q_1 \cdot a_2)q_1$

$$
\frac4{\sqrt5}
\begin{bmatrix}
\frac2{\sqrt5}\\
\frac1{\sqrt5}
\end{bmatrix}
$$

$$
=
\begin{bmatrix}
\frac85\\
\frac45
\end{bmatrix}
$$

---

#### Menghitung $v_2$

$$
v_2=
\begin{bmatrix}
1\\
2
\end{bmatrix}
-
\begin{bmatrix}
\frac85\\
\frac45
\end{bmatrix}
$$

$$
=
\begin{bmatrix}
-\frac35\\
\frac65
\end{bmatrix}
$$

---

## Langkah 4 — Mencari $q_2$

Rumus:

$$
q_2=\frac{v_2}{||v_2||}
$$

---

#### Menghitung panjang $v_2$

$$
||v_2||=
\sqrt{
\left(-\frac35\right)^2+
\left(\frac65\right)^2
}
$$

$$
=
\sqrt{
\frac9{25}+\frac{36}{25}
}
$$

$$
=
\sqrt{\frac{45}{25}}
$$

$$
=
\frac3{\sqrt5}
$$

---

#### Menghitung $q_2$

$$
q_2=
\begin{bmatrix}
-\frac35\\
\frac65
\end{bmatrix}
\div
\frac3{\sqrt5}
$$

$$
=
\begin{bmatrix}
-\frac1{\sqrt5}\\
\frac2{\sqrt5}
\end{bmatrix}
$$

---

## Langkah 5 — Membentuk Matriks $Q$

$$
Q_0=(q_1,q_2)
$$

$$
Q_0=
\begin{bmatrix}
\frac2{\sqrt5} & -\frac1{\sqrt5}\\
\frac1{\sqrt5} & \frac2{\sqrt5}
\end{bmatrix}
$$

---

## Langkah 6 — Membentuk Matriks $R$

Rumus:

$$
R=
\begin{bmatrix}
a_1\cdot q_1 & a_2\cdot q_1\\
0 & a_2\cdot q_2
\end{bmatrix}
$$

---

#### Menghitung $a_1 \cdot q_1$

$$
(2\times\frac2{\sqrt5})
+
(1\times\frac1{\sqrt5})
$$

$$
=
\frac4{\sqrt5}+\frac1{\sqrt5}
$$

$$
=
\frac5{\sqrt5}
$$

$$
=
\sqrt5
$$

---

#### Menghitung $a_2 \cdot q_1$

$$
(1\times\frac2{\sqrt5})
+
(2\times\frac1{\sqrt5})
$$

$$
=
\frac2{\sqrt5}+\frac2{\sqrt5}
$$

$$
=
\frac4{\sqrt5}
$$

---

#### Menghitung $a_2 \cdot q_2$

$$
(1\times-\frac1{\sqrt5})
+
(2\times\frac2{\sqrt5})
$$

$$
=
-\frac1{\sqrt5}+\frac4{\sqrt5}
$$

$$
=
\frac3{\sqrt5}
$$

---

### Matriks $R$

$$
R_0=
\begin{bmatrix}
\sqrt5 & \frac4{\sqrt5}\\
0 & \frac3{\sqrt5}
\end{bmatrix}
$$

---

## Langkah 7 — Menghitung $A_1$

Rumus:

$$
A_1=R_0Q_0
$$

---

#### Elemen (1,1)

$$
\left(\sqrt5\times\frac2{\sqrt5}\right)
+
\left(\frac4{\sqrt5}\times\frac1{\sqrt5}\right)
$$

$$
=
2+\frac45
$$

$$
=
\frac{14}5
$$

$$
=
2.8
$$

---

#### Elemen (1,2)

$$
\left(\sqrt5\times-\frac1{\sqrt5}\right)
+
\left(\frac4{\sqrt5}\times\frac2{\sqrt5}\right)
$$

$$
=
-1+\frac85
$$

$$
=
\frac35
$$

$$
=
0.6
$$

---

#### Elemen (2,1)

$$
\left(0\times\frac2{\sqrt5}\right)
+
\left(\frac3{\sqrt5}\times\frac1{\sqrt5}\right)
$$

$$
=
0+\frac35
$$

$$
=
0.6
$$

---

#### Elemen (2,2)

$$
\left(0\times-\frac1{\sqrt5}\right)
+
\left(\frac3{\sqrt5}\times\frac2{\sqrt5}\right)
$$

$$
=
0+\frac65
$$

$$
=
1.2
$$

---

## Hasil Iterasi Pertama

$$
A_1=
\begin{bmatrix}
2.8 & 0.6\\
0.6 & 1.2
\end{bmatrix}
$$

---

### ITERASI 1

Diketahui:

$$
A_1=
\begin{bmatrix}
2.8 & 0.6\\
0.6 & 1.2
\end{bmatrix}
$$

Lakukan dekomposisi QR:

$$
A_1=Q_1R_1
$$

Kemudian hitung:

$$
A_2=R_1Q_1
$$

Hasil:

$$
A_2\approx
\begin{bmatrix}
2.9756 & 0.2195\\
0.2195 & 1.0244
\end{bmatrix}
$$

Terlihat bahwa elemen luar diagonal mulai mengecil:

$$
0.6 \rightarrow 0.2195
$$

---

### ITERASI 2

Gunakan hasil sebelumnya:

$$
A_2\approx
\begin{bmatrix}
2.9756 & 0.2195\\
0.2195 & 1.0244
\end{bmatrix}
$$

Lakukan lagi:

$$
A_2=Q_2R_2
$$

Kemudian:

$$
A_3=R_2Q_2
$$

Hasil:

$$
A_3\approx
\begin{bmatrix}
2.9973 & 0.0739\\
0.0739 & 1.0027
\end{bmatrix}
$$

Elemen luar diagonal semakin kecil:

$$
0.2195 \rightarrow 0.0739
$$

---

### ITERASI 3

Diketahui:

$$
A_3\approx
\begin{bmatrix}
2.9973 & 0.0739\\
0.0739 & 1.0027
\end{bmatrix}
$$

Lakukan:

$$
A_3=Q_3R_3
$$

Kemudian:

$$
A_4=R_3Q_3
$$

Hasil:

$$
A_4\approx
\begin{bmatrix}
2.9997 & 0.0247\\
0.0247 & 1.0003
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.0739 \rightarrow 0.0247
$$

---

### ITERASI 4

Diketahui:

$$
A_4\approx
\begin{bmatrix}
2.9997 & 0.0247\\
0.0247 & 1.0003
\end{bmatrix}
$$

Lakukan:

$$
A_4=Q_4R_4
$$

Kemudian:

$$
A_5=R_4Q_4
$$

Hasil:

$$
A_5\approx
\begin{bmatrix}
2.99997 & 0.00823\\
0.00823 & 1.00003
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.0247 \rightarrow 0.00823
$$

---

### ITERASI 5

Diketahui:

$$
A_5\approx
\begin{bmatrix}
2.99997 & 0.00823\\
0.00823 & 1.00003
\end{bmatrix}
$$

Lakukan:

$$
A_5=Q_5R_5
$$

Kemudian:

$$
A_6=R_5Q_5
$$

Hasil:

$$
A_6\approx
\begin{bmatrix}
2.999996 & 0.00274\\
0.00274 & 1.000004
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.00823 \rightarrow 0.00274
$$

---

### ITERASI 6

Diketahui:

$$
A_6\approx
\begin{bmatrix}
2.999996 & 0.00274\\
0.00274 & 1.000004
\end{bmatrix}
$$

Lakukan:

$$
A_6=Q_6R_6
$$

Kemudian:

$$
A_7=R_6Q_6
$$

Hasil:

$$
A_7\approx
\begin{bmatrix}
2.9999995 & 0.000914\\
0.000914 & 1.0000005
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.00274 \rightarrow 0.000914
$$

---

### ITERASI 7

Diketahui:

$$
A_7\approx
\begin{bmatrix}
2.9999995 & 0.000914\\
0.000914 & 1.0000005
\end{bmatrix}
$$

Lakukan:

$$
A_7=Q_7R_7
$$

Kemudian:

$$
A_8=R_7Q_7
$$

Hasil:

$$
A_8\approx
\begin{bmatrix}
2.99999994 & 0.000305\\
0.000305 & 1.00000006
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.000914 \rightarrow 0.000305
$$

---

### ITERASI 8

Diketahui:

$$
A_8\approx
\begin{bmatrix}
2.99999994 & 0.000305\\
0.000305 & 1.00000006
\end{bmatrix}
$$

Lakukan:

$$
A_8=Q_8R_8
$$

Kemudian:

$$
A_9=R_8Q_8
$$

Hasil:

$$
A_9\approx
\begin{bmatrix}
2.99999999 & 0.000102\\
0.000102 & 1.00000001
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.000305 \rightarrow 0.000102
$$

---

### ITERASI 9

Diketahui:

$$
A_9\approx
\begin{bmatrix}
2.99999999 & 0.000102\\
0.000102 & 1.00000001
\end{bmatrix}
$$

Lakukan:

$$
A_9=Q_9R_9
$$

Kemudian:

$$
A_{10}=R_9Q_9
$$

Hasil:

$$
A_{10}\approx
\begin{bmatrix}
3 & 0.000034\\
0.000034 & 1
\end{bmatrix}
$$

Elemen luar diagonal:

$$
0.000102 \rightarrow 0.000034
$$

---

### Kesimpulan

Semakin banyak iterasi QR dilakukan:

- elemen luar diagonal semakin mendekati nol
- elemen diagonal semakin mendekati eigenvalue

Hasil akhir:

$$
A_{10}\approx
\begin{bmatrix}
3 & 0\\
0 & 1
\end{bmatrix}
$$

Maka eigenvalue matriks:

$$
\lambda_1=3
$$

dan

$$
\lambda_2=1
$$