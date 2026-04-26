# Sistem Persamaan Linear (SPL)
## Apa itu Sistem Persamaan Linear?
**Sistem persamaan linear** merupakan salah satu konsep penting dalam matematika yang memiliki peran besar di berbagai bidang kehidupan. Tidak hanya dalam dunia akademik, konsep ini juga banyak diterapkan dalam ekonomi, teknik, ilmu komputer, hingga analisis data. 
**Sistem Persamaan Linear** adalah sekumpulan dua atau lebih persamaan yang memiliki variabel yang sama dan derajat satu. Persamaan linear disebut “linear” karena grafiknya membentuk garis lurus. 

**Contoh Umum Sistem Persamaan Linear:**
1. 2x + 3y = 6
2. x – y = 2<p>Kedua persamaan ini membentuk sistem dua variabel, yaitu x dan y. Tujuan dari sistem ini adalah mencari nilai x dan y yang memenuhi kedua persamaan secara bersamaan.</p>

**Bentuk Umum Sistem Persamaan Linear:**
1. a₁x + b₁y = c₁
2. a₂x + b₂y = c₂<p>Bentuk ini sangat berguna ketika kita ingin menyelesaikan sistem persamaan dengan metode aljabar linear seperti eliminasi Gauss atau matriks invers.</p>

**Jenis-jenis Sistem Persamaan Linear** <p>Sistem Persamaan Linier dibedakan menjadi 3 jenis berdasarkan jumlah variabelnya:</p>
1. Sistem Persamaan Linear Dua Variabel (SPLDV), Contoh: x + y = 10
2. Sistem Persamaan Linear Tiga Variabel (SPLTV), Contoh: x + 2y + z = 6
3. Sistem Persamaan Linear n Variabel (SPLNV), Sistem yang memiliki lebih dari tiga variabel, umumnya digunakan dalam bidang teknik dan data science.

## Apa Solusi Sistem Persamaan Linear?
**Solusi Sistem Persamaan LInear** adalah setiap n-tuple nilai (s1, s2,...,sn) yang memenuhi persamaan linear. Misalnya (−1, -1) merupakan solusi dari persamaan linear x + 3y = -4 dengan bukti -1 + (3 x -1) = -1 + (-3) = -4
<p>Secara umum, untuk setiap sistem persamaan linear terdapat tiga kemungkinan solusi:


1. **Solusi Tunggal (unik):** Dalam solusi ini, hanya ada satu himpunan solusi spesifik. Secara geometris, ini berarti bahwa n bidang yang ditentukan oleh setiap persamaan dari sistem linear semuanya berpotongan pada satu titik unik di ruang yang ditentukan oleh variabel-variabel sistem tersebut (Garis berpotongan).

    **Contoh:**   

    $\begin{cases}
    x + 2y = 4 \\
    3x - y = 5
    \end{cases}$

    **Langkah-langkah Operasi Baris Elementer (OBE):**
    1. Bentuk Matriks:
        
        $\left[
        \begin{array}{cc|c}
        1 & 2 & 4 \\
        3 & -1 & 5
        \end{array}
        \right]$
    2. Hilangkan elemen di bawah pivot pertama

        Gunakan: R2 = R2 - 3R1

        Matriks menjadi:

        $\left[
        \begin{array}{cc|c}
        1 & 2 & 4 \\
        0 & -7 & -7
        \end{array}
        \right]$
    3. Jdikan pivot kedua bernilai 1

        $\left[
        \begin{array}{cc|c}
        1 & 2 & 4 \\
        0 & 1 & 1
        \end{array}
        \right]$

    4. Hilangkan elemen di atas pivot kedua

        Gunakan: R1 = R1 - 2R2

        Matriks akhir (bentuk eselon tereduksi):

        $\left[
        \begin{array}{cc|c}
        1 & 0 & 2 \\
        0 & 1 & 1
        \end{array}
        \right]$
    5. Hasil

        X = 2  Y = 1
    
    6. Kode Python:

        ```python
        import numpy as np

        # Matriks koefisien
        A = np.array([
            [1, 2],
            [3, -1]
        ], dtype=float)

        # Matriks konstanta
        B = np.array([4, 5], dtype=float)

        # Bentuk matriks augmentasi
        aug = np.hstack((A, B.reshape(-1, 1)))

        print("Matriks awal:")
        print(aug)

        # 1️⃣ R2 = R2 - 3R1
        aug[1] = aug[1] - 3 * aug[0]

        print("\nSetelah R2 = R2 - 3R1:")
        print(aug)

        # 2️⃣ R2 = (-1/7) R2
        aug[1] = (-1/7) * aug[1]

        print("\nSetelah R2 = (-1/7) R2:")
        print(aug)

        # 3️⃣ R1 = R1 - 2R2
        aug[0] = aug[0] - 2 * aug[1]

        print("\nSetelah R1 = R1 - 2R2:")
        print(aug)

        # Ambil solusi
        x = aug[0, -1]
        y = aug[1, -1]

        print("\nKesimpulan: Sistem memiliki solusi tunggal.")
        print(f"x = {x}")
        print(f"y = {y}")
    7. Geogebra
        
        <iframe src="https://www.geogebra.org/calculator/kfracqtx?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
       
    

2. **Tidak Ada Solusi:** Persamaan-persamaan tersebut disebut tidak konsisten dan menentukan n bidang di ruang angkasa yang tidak berpotongan atau tumpang tindih. Tidak mungkin untuk menentukan himpunan solusi yang memenuhi semua persamaan sistem tersebut (Garis sejajar).

    **Contoh:**

    $\begin{cases}
    3x - 2y = 2 \\
    3x - 2y = -2
    \end{cases}$

    **Langkah-langkah Operasi Baris Elementer (OBE):**
    1. Bentuk Matriks:

        $\left[
        \begin{array}{cc|c}
        3 & -2 & 2 \\
        3 & -2 & -2
        \end{array}
        \right]$

    2. Hilangkan elemen di bawah pivot pertama

        Gunakan: R2 = R2 - R1

        Matriks menjadi:

        $\left[
        \begin{array}{cc|c}
        3 & -2 & 2 \\
        0 & 0 & -4
        \end{array}
        \right]$

    3. Interpretasi Baris Kedua

        Baris kedua menyatakan:

        $0x + 0y = -4$
        $0 = -4$
        Ini adalah *kontradiksi*, karena tidak mungkin benar.
    
    4. Hasil
        
        Karena muncul baris:

        $0 = -4$

        Maka ini **Tidak Ada Solusi**. Secara geometri, dua garis memiliki gradien sama tetapi berbeda titik potong → garis sejajar dan tidak berpotongan.

    5. Kode Python:
        ```python
        import numpy as np

        # Matriks koefisien
        A = np.array([
            [3, -2],
            [3, -2]
        ], dtype=float)

        # Matriks konstanta
        B = np.array([2, -2], dtype=float)

        # Gabungkan menjadi matriks augmentasi
        aug = np.hstack((A, B.reshape(-1, 1)))

        print("Matriks awal:")
        print(aug)

        # Operasi Baris Elementer
        aug[1] = aug[1] - aug[0]   # R2 = R2 - R1

        print("\nSetelah OBE (R2 = R2 - R1):")
        print(aug)

        # Cek jenis solusi
        if np.allclose(aug[1, :-1], 0) and not np.isclose(aug[1, -1], 0):
            print("\nKesimpulan: Sistem tidak memiliki solusi (inkonsisten).")
        elif np.allclose(aug[1], 0):
            print("\nKesimpulan: Sistem memiliki tak hingga solusi.")
        else:
            print("\nKesimpulan: Sistem memiliki solusi tunggal.")

    6. Geogebra

        <iframe src="https://www.geogebra.org/calculator/kfracqtx?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
        
    

3. **Solusi Tak Terhingga:** kondisi ketika suatu sistem persamaan linier memiliki banyak solusi yang tidak terbatas jumlahnya(Garis berimpit).

    **Contoh:**

    $\begin{cases}
    x + y + z = 2 \\
    2x + 2y + 2z = 4
    \end{cases}$

    **Langkah-langkah Operasi Baris Elementer (OBE):**
    1. Bentuk Matriks:

        $\left[
        \begin{array}{ccc|c}
        1 & 1 & 1 & 2 \\
        2 & 2 & 2 & 4
        \end{array}
        \right]$

    2. Hilangkan elemen di bawah pivot pertama

        Gunakan: R2 = R2 - 2R1

        Matriks menjadi:

        $\left[
        \begin{array}{ccc|c}
        1 & 1 & 1 & 2 \\
        0 & 0 & 0 & 0
        \end{array}
        \right]$
    
    3. Interpretasi Baris Kedua

        Baris kedua menyatakan:
        $0x + 0y + 0z = 0$

        Artinya tidak ada informasi baru → sistem memiliki variabel bebas. 
        
        Dari baris pertama:
        $x + y + z = 2$

        Misalkan:

        $y = s, \quad z = t$

        Maka:

        $x = 2 - s - t$

    4. Hasil (Bentuk Solusi Parametrik):

        $\begin{cases}
        x = 2 - s - t \\
        y = s \\
        z = t
        \end{cases}
        \quad \text{dengan } s,t \in \mathbb{R}$

        Karena s dan t bebas, **maka solusinya tak terhingga banyaknya.**
    
    5. Kode Python:

         ```python
        import numpy as np

        # Matriks koefisien
        A = np.array([
            [1, 1, 1],
            [2, 2, 2]
        ], dtype=float)

        # Matriks konstanta
        B = np.array([2, 4], dtype=float)

        # Bentuk matriks augmentasi
        aug = np.hstack((A, B.reshape(-1, 1)))

        print("Matriks awal:")
        print(aug)

        # 1️⃣ R2 = R2 - 2R1
        aug[1] = aug[1] - 2 * aug[0]

        print("\nSetelah R2 = R2 - 2R1:")
        print(aug)

        # Cek jenis solusi
        if np.allclose(aug[1], 0):
            print("\nKesimpulan: Sistem memiliki tak hingga solusi (variabel bebas).")
            
            print("\nBentuk persamaan tersisa:")
            print("x + y + z = 2")
            
            print("\nMisalkan:")
            print("y = s")
            print("z = t")
            
            print("\nMaka:")
            print("x = 2 - s - t")
            
            print("\nBentuk solusi parametrik:")
            print("x = 2 - s - t")
            print("y = s")
            print("z = t")
            print("dengan s, t ∈ R")
        else:
            print("\nSistem bukan kasus tak hingga solusi.")
    6. Geogebra

        <iframe src="https://www.geogebra.org/calculator/nygupfj2?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
       