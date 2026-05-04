# Transformasi Geometri Sumbu Y

link colab : https://colab.research.google.com/drive/12A7BTAVEJgqoGO9w1LhpLuS_Jbe_9N60?usp=sharing

## Titik Awal
terdapat bangun berbentuk persegi dengan titik-titik:

$A(-9, 2)$

$B(-7, 2)$

$C(-7, 4)$

$D(-9, 4)$

Bangun ini berada di sebelah kiri sumbu Y.

## Matriks Refleksi terhadap Sumbu Y

Refleksi terhadap sumbu Y dapat dinyatakan dalam bentuk matriks:

$$
\begin{bmatrix}
x' \\
y'
\end{bmatrix}
=
\begin{bmatrix}
-1 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

Hasilnya:
- x' = -x  
- y' = y  

Sehingga:
(x, y) → (-x, y)

---

Jika diterapkan pada titik-titik bangun:

$A(-9, 2) → A'(9, 2)$  

$B(-7, 2) → B'(7, 2)$ 

$C(-7, 4) → C'(7, 4)$  

$D(-9, 4) → D'(9, 4)$  

Matriks ini menunjukkan bahwa refleksi terhadap sumbu Y hanya mengubah tanda koordinat x, sedangkan koordinat y tetap.

## Translasi
Translasi menggeser setiap titik sejauh t satuan ke arah sumbu x:
(x, y) → (x + t, y)

Maka:

$A(-9, 2) → A₁(-9 + t, 2)$

$B(-7, 2) → B₁(-7 + t, 2)$

$C(-7, 4) → C₁(-7 + t, 4)$

$D(-9, 4) → D₁(-9 + t, 4)$

Semua titik bergeser sejauh yang sama tanpa mengubah bentuk bangun.

## Refleksi Setelah Translasi
Hasil translasi direfleksikan kembali terhadap sumbu Y:
(x + t, y) → (-(x + t), y)

Maka:

$A₁(-9 + t, 2) → A₁'(9 - t, 2)$

$B₁(-7 + t, 2) → B₁'(7 - t, 2)$

$C₁(-7 + t, 4) → C₁'(7 - t, 4)$

$D₁(-9 + t, 4) → D₁'(9 - t, 4)$

## Hubungan Transformasi
Transformasi yang terjadi:
$(x, y) → (x + t, y) → (-(x + t), y)$

Setiap titik hasil refleksi selalu memiliki jarak yang sama terhadap sumbu Y dengan titik hasil translasi, tetapi berada di sisi yang berlawanan.

### Kesimpulan
Refleksi terhadap sumbu Y mengubah tanda koordinat x, sedangkan translasi menggeser posisi titik tanpa mengubah bentuk. Kombinasi keduanya menghasilkan bangun yang tetap simetris terhadap sumbu Y dan bergerak secara berlawanan arah antara bangun asli dan bayangannya.