# KELOMPOK 4B
### 1. Dela Agreni Suarang
### 2. Siti Naurah Fatinah Malihah
### 3. Josua Aido Arta Sitorus
### 4. Hijrah
### 5. Aulia Zezarya


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


Untuk membuktikan bahwa rumus tersebut benar, kita kalikan ruas kiri dengan matriks $(A + BCD)$.

---

### Langkah 1

$$
A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}
$$

---

### Langkah 2

Gunakan sifat distributif perkalian matriks.

$$
= A^{-1}A + A^{-1}BCD - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}DA^{-1}A - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}DA^{-1}BCD
$$

---

### Langkah 3

Sederhanakan beberapa bagian matriks.

Karena:

$$
A^{-1}A = I
$$

maka diperoleh:

$$
= I + A^{-1}BCD - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}D - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}DA^{-1}BCD
$$

---

### Langkah 4

Gunakan identitas:

$$
D = C^{-1}C D
$$

sehingga diperoleh:

$$
= I + A^{-1}BCD - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}C^{-1}CD - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}DA^{-1}BCD
$$

---

### Langkah 5

Gabungkan faktor matriks:

$$
= I + A^{-1}BCD - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}(C^{-1}+DA^{-1}B)CD
$$

---

### Langkah 6

Karena:

$$
(C^{-1}+DA^{-1}B)^{-1}(C^{-1}+DA^{-1}B) = I
$$

maka:

$$
= I + A^{-1}BCD - A^{-1}BCD
$$

---

### Hasil Akhir

$$
= I
$$

---

## Kesimpulan

Karena

$$
(A + BCD)^{-1}(A + BCD) = I
$$

maka terbukti bahwa:

$$
(A + BCD)^{-1} = A^{-1} - A^{-1}B(C^{-1}+DA^{-1}B)^{-1}DA^{-1}
$$

yang disebut sebagai **Matrix Inversion Lemma**.

# Pembuktian Matrix Inversion Lemma

### Rumus Utama
Diberikan identitas **Matrix Inversion Lemma**:
$$(A + BCD)^{-1} = A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}$$

### Bukti Aljabar
Untuk membuktikan identitas ini, kita akan mengalikan ruas kanan dengan $(A + BCD)$. Jika hasilnya adalah matriks identitas ($I$), maka rumus tersebut terbukti benar.

#### **Langkah 1: Post-multiplication**
$$[A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}] (A + BCD)$$

#### **Langkah 2: Sifat Distributif**
Kalikan setiap suku di dalam kurung pertama dengan $(A + BCD)$:
$$= A^{-1}(A + BCD) - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}(A + BCD)$$
$$= A^{-1}A + A^{-1}BCD - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}A - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}BCD$$

#### **Langkah 3: Sederhanakan Identitas $A^{-1}A = I$**
$$= I + A^{-1}BCD - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}D - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}BCD$$

#### **Langkah 4: Gunakan Identitas $D = C^{-1}CD$**
Kita substitusikan $D$ pada suku ketiga untuk mempermudah faktorisasi:
$$= I + A^{-1}BCD - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}C^{-1}CD - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}BCD$$

#### **Langkah 5: Faktorisasi Matriks**
Keluarkan faktor $A^{-1}B(C^{-1} + DA^{-1}B)^{-1}$ dan $CD$ dari dua suku terakhir:
$$= I + A^{-1}BCD - A^{-1}B(C^{-1} + DA^{-1}B)^{-1} [C^{-1} + DA^{-1}B] CD$$

#### **Langkah 6: Eliminasi Invers**
Karena $(C^{-1} + DA^{-1}B)^{-1}(C^{-1} + DA^{-1}B) = I$, maka:
$$= I + A^{-1}BCD - A^{-1}B(I)CD$$
$$= I + A^{-1}BCD - A^{-1}BCD$$

### **Hasil Akhir**
$$= I$$

---

### **Kesimpulan**
Karena hasil perkaliannya adalah Matriks Identitas ($I$), maka terbukti secara sah bahwa:
$$(A + BCD)^{-1} = A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}$$
