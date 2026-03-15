# Matrix Inversion Lemma
## Definisi Matrix Inversioin Lemma 
    Matrix Inversion Lemma adalah rumus yang digunakan untuk menghitung invers dari matriks yang berbentuk penjumlahan matriks tanpa harus menghitung invers besar secara langsung.
## Syarat Matrix Inversion Lemma
    Agar rumus ini bisa digunakan:
    Matriks A harus memiliki invers
    Matriks C harus memiliki invers
    Dimensi matriks harus cocok untuk perkalian.
## Rumus Matrix Conversion Lemma
$$[A + BCD]^{-1} = A^{-1} - A^{-1}B[C^{-1} + DA^{-1}B]^{-1}DA^{-1}$$
**Keterangan**  
1.  $A$: Matriks utama berukuran $n \times n$. Syarat utamanya adalah $A$ harus memiliki   invers ($A^{-1}$).
2. $C$: Matriks inti dari perubahan berukuran $k \times k$. Matriks ini juga harus memiliki invers ($C^{-1}$).
3. $B$ dan $D$: Matriks pengali atau matriks struktur yang menghubungkan dimensi $n$ dan $k$
4. $B$ berukuran $n \times k$
5. $D$ berukuran $k \times n$
    
## Pembuktian Rumus Matrix Conversion Lemma
   # Prosedur Matrix Inversion Lemma

### 1. Langkah-Langkah Penggunaan Praktis
Untuk menghitung invers dari $[A + BCD]$ menggunakan metode ini, prosedur dilakukan secara sistematis sebagai berikut:

1.  **Identifikasi Parameter:** Tentukan matriks $A$, $B$, $C$, dan $D$. Pastikan $A$ dan $C$ memiliki invers yang sudah diketahui atau mudah dihitung.
2.  **Inversi Matriks Tengah:** Hitung invers dari matriks $C$ (dilambangkan $C^{-1}$).
3.  **Operasi Matriks Internal:** Lakukan perkalian matriks $D \times A^{-1} \times B$.
4.  **Inversi Inti (Kernel):** Jumlahkan hasil langkah 2 dan 3, kemudian hitung inversnya: $[C^{-1} + DA^{-1}B]^{-1}$.
5.  **Konstruksi Koreksi:** Kalikan secara berurutan: $A^{-1}B \times (\text{hasil langkah 4}) \times DA^{-1}$.
6.  **Hasil Akhir:** Kurangi invers awal ($A^{-1}$) dengan hasil langkah 5.

---

### 2. Langkah-Langkah Pembuktian Matematis
Pembuktian dilakukan dengan menunjukkan bahwa perkalian antara rumus invers dan matriks asli menghasilkan Matriks Identitas ($I$).

**Persamaan Pengujian:**
$$[A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}] \times [A + BCD]$$

#### Langkah 1: Distribusi Suku Pertama
Suku $A^{-1}$ dikalikan ke dalam $[A + BCD]$:
$$A^{-1}A + A^{-1}BCD = I + A^{-1}BCD$$

#### Langkah 2: Distribusi Suku Kedua
Suku $-A^{-1}B[C^{-1} + DA^{-1}B]^{-1}DA^{-1}$ dikalikan ke dalam $[A + BCD]$:
$$= -A^{-1}B[C^{-1} + DA^{-1}B]^{-1}(DA^{-1}A + DA^{-1}BCD)$$
$$= -A^{-1}B[C^{-1} + DA^{-1}B]^{-1}(D + DA^{-1}BCD)$$

#### Langkah 3: Faktorisasi Matriks Koreksi
Bagian $(D + DA^{-1}BCD)$ difaktorkan agar memiliki komponen yang sama dengan matriks invers di tengah:
$$(D + DA^{-1}BCD) = (C^{-1} + DA^{-1}B)CD$$
*(Catatan: Penjumlahan di dalam kurung disesuaikan agar kompatibel dengan invers di Langkah 2).*

#### Langkah 4: Eliminasi Melalui Identitas
Substitusi hasil Langkah 3 kembali ke dalam persamaan Langkah 2:
$$-A^{-1}B \underbrace{[C^{-1} + DA^{-1}B]^{-1} [C^{-1} + DA^{-1}B]}_{I} CD$$
Bagian tengah menghasilkan matriks identitas ($I$), sehingga tersisa:
$$-A^{-1}BCD$$

#### Langkah 5: Penyederhanaan Akhir
Penggabungan hasil Langkah 1 dan Langkah 4 secara keseluruhan:
$$= (I + A^{-1}BCD) - (A^{-1}BCD)$$
$$= I$$

**Kesimpulan:**
Terbukti bahwa hasil operasi adalah $I$, sehingga identitas Matrix Inversion Lemma dinyatakan valid.
## Contoh Soal Matrix Conversion Lemma
1. Diberikan sebuah matriks $M$ yang didefinisikan sebagai hasil penjumlahan matriks $A$ dengan gangguan terstruktur $BCD$:
$$M = A + BCD$$

Dik.
- $A = \begin{bmatrix} 4 & 0 \\ 0 & 4 \end{bmatrix}$ (Matriks utama)
- $B = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ (Vektor kolom penghubung)
- $C = [1]$ (Matriks skalar modifikasi)
- $D = \begin{bmatrix} 1 & 0 \end{bmatrix}$ (Vektor baris penghubung)

Hitunglah invers dari matriks $M$ ($M^{-1}$) menggunakan rumus Matrix Inversion Lemma!

---

**Penyelesaian:**

Rumus Matrix Inversion Lemma yang digunakan adalah:
$$[A + BCD]^{-1} = A^{-1} - A^{-1}B[C^{-1} + DA^{-1}B]^{-1}DA^{-1}$$

#### Langkah 1: Identifikasi Invers Dasar
Tentukan invers dari matriks $A$ dan $C$:
- $A^{-1} = \begin{bmatrix} 0.25 & 0 \\ 0 & 0.25 \end{bmatrix}$
- $C^{-1} = [1]^{-1} = [1]$

#### Langkah 2: Hitung Operasi Internal ($DA^{-1}B$)
Lakukan perkalian matriks $D \times A^{-1} \times B$:
$$DA^{-1}B = \begin{bmatrix} 1 & 0 \end{bmatrix} \begin{bmatrix} 0.25 & 0 \\ 0 & 0.25 \end{bmatrix} \begin{bmatrix} 1 \\ 0 \end{bmatrix}$$
$$DA^{-1}B = \begin{bmatrix} 0.25 & 0 \end{bmatrix} \begin{bmatrix} 1 \\ 0 \end{bmatrix} = [0.25]$$

#### Langkah 3: Hitung Invers Inti (Kernel)
Jumlahkan $C^{-1}$ dengan hasil langkah sebelumnya, kemudian lakukan inversi:
$$[C^{-1} + DA^{-1}B]^{-1} = [1 + 0.25]^{-1} = [1.25]^{-1} = [0.8]$$

#### Langkah 4: Hitung Suku Koreksi Akhir
Lakukan perkalian seluruh komponen pada suku kedua rumus:
$$\text{Koreksi} = A^{-1}B \times [0.8] \times DA^{-1}$$
$$\text{Koreksi} = \left( \begin{bmatrix} 0.25 \\ 0 \end{bmatrix} \right) \times [0.8] \times \left( \begin{bmatrix} 0.25 & 0 \end{bmatrix} \right)$$
$$\text{Koreksi} = \begin{bmatrix} 0.2 \\ 0 \end{bmatrix} \begin{bmatrix} 0.25 & 0 \end{bmatrix} = \begin{bmatrix} 0.05 & 0 \\ 0 & 0 \end{bmatrix}$$

#### Langkah 5: Kalkulasi Hasil Akhir
Kurangi invers awal ($A^{-1}$) dengan matriks koreksi:
$$M^{-1} = \begin{bmatrix} 0.25 & 0 \\ 0 & 0.25 \end{bmatrix} - \begin{bmatrix} 0.05 & 0 \\ 0 & 0 \end{bmatrix}$$
$$M^{-1} = \begin{bmatrix} 0.2 & 0 \\ 0 & 0.25 \end{bmatrix}$$

**Kesimpulan:**
Invers dari matriks $M$ adalah $\begin{bmatrix} 0.2 & 0 \\ 0 & 0.25 \end{bmatrix}$. Hasil ini sesuai dengan metode inversi langsung pada $M = \begin{bmatrix} 5 & 0 \\ 0 & 4 \end{bmatrix}$.