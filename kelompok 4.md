# Matrix Inversion Lemma
## Definisi Matrix Inversion Lemma
    Matrix Inversion Lemma adalah rumus yang digunakan untuk menghitung invers dari matriks yang berbentuk penjumlahan matriks tanpa harus menghitung invers besar secara langsung. 
## Syarat Matrix Inversion Lemma 
    Agar rumus ini bisa digunakan: 
    Matriks A harus memiliki invers
    Matriks C harus memiliki invers 
    Dimensi matriks harus cocok untuk perkalian.
## Rumus

$$[A + BCD]^{-1} = A^{-1} - A^{-1}B[C^{-1} + DA^{-1}B]^{-1}DA^{-1}$$

## Keterangan
1. $A$ (Matriks Utama)   
   Dimensi: $n \times n$.
   Syarat: Harus memiliki invers ($A^{-1}$) atau bersifat non-singular.
   Peran: Mewakili sistem awal atau basis data yang besar.
2. $C$ (Matriks Modifikasi)  
    Dimensi: $k \times k$.
    Syarat: Harus memiliki invers ($C^{-1}$).
    Peran: Mewakili inti dari perubahan yang ditambahkan ke sistem. Biasanya $k$ jauh lebih kecil dari $n$ ($k \ll n$).
3. $B$ (Matriks Penghubung Depan)  
    Dimensi: $n \times k$.
    Peran: Menyesuaikan dimensi dari ruang modifikasi ke ruang sistem utama.
4.  $D$ (Matriks Penghubung Belakang) 
    Dimensi: $k \times n$.
    Peran: Menyesuaikan dimensi kembali dari ruang sistem utama ke ruang modif

### Contoh Soal
Diketahui:
* $A = \begin{bmatrix} 4 & 0 \\ 0 & 4 \end{bmatrix}$
* $B = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$
* $C = [1]$
* $D = \begin{bmatrix} 1 & 0 \end{bmatrix}$
  
**Penyelesaian:**

1. **Hitung Invers A:**
   $$A^{-1} = \begin{bmatrix} 0.25 & 0 \\ 0 & 0.25 \end{bmatrix}$$

2. **Hitung Operasi Internal ($DA^{-1}B$):**
   $$DA^{-1}B = [0.25]$$

3. **Hitung Invers Inti:**
   $$[1 + 0.25]^{-1} = [0.8]$$

4. **Hasil Akhir ($M^{-1}$):**
   $$M^{-1} = \begin{bmatrix} 0.2 & 0 \\ 0 & 0.25 \end{bmatrix}$$