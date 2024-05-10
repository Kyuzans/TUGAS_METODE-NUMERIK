Kode yang diberikan berisi tiga proyek berbeda yang semuanya bertujuan untuk menyelesaikan sistem persamaan linier Ax = b. Berikut adalah penjelasan masing-masing proyek dalam Bahasa Indonesia:

Proyek 1: Penyelesaian Persamaan Linier dengan Invers Matriks

Proyek ini berfokus pada penyelesaian sistem persamaan linier (Ax = b) menggunakan metode invers matriks. Proyek ini mengimplementasikan fungsi solve_persamaan_linear_invers(matriks_A, vektor_b) yang menerima matriks koefisien matriks_A dan vektor konstan vektor_b sebagai input.
Fungsi ini mencoba menghitung invers dari matriks koefisien matriks_A menggunakan np.linalg.inv(). Jika berhasil, fungsi ini menghitung vektor solusi vektor_solusi dengan mengalikan matriks invers dengan vektor konstan.
Namun, jika matriks_A singular (tidak dapat diinvers), fungsi ini akan mengeluarkan error np.linalg.LinAlgError dan mencetak pesan yang menyatakan bahwa invers tidak dapat dihitung. Dalam kasus ini, fungsi mengembalikan None untuk menunjukkan ketidakmampuan menemukan solusi.
Kode pengujian yang disediakan menunjukkan penggunaan fungsi tersebut dengan membuat contoh matriks koefisien matriks_A dan vektor konstan vektor_b, menyelesaikan sistem persamaan menggunakan fungsi, dan mencetak vektor solusi yang dihasilkan.

Proyek 2: Penyelesaian Persamaan Linier dengan Dekomposisi LU (Metode Gauss)

Proyek ini menangani masalah yang sama yaitu menyelesaikan persamaan linier (Ax = b) tetapi menggunakan dekomposisi LU (metode Gauss) untuk mendapatkan solusi. Proyek ini mengimplementasikan fungsi solusi_persamaan_lu_gauss(matriks_A, vektor_b) yang menerima matriks koefisien matriks_A dan vektor konstan vektor_b sebagai input.
Fungsi ini menggunakan fungsi linalg.lu() dari pustaka scipy.linalg untuk melakukan dekomposisi matriks koefisien matriks_A menjadi matriks segitiga bawah L, matriks segitiga atas U, dan matriks permutasi P.
Selanjutnya, fungsi ini menggunakan fungsi linalg.solve_triangular() untuk menyelesaikan sistem persamaan untuk vektor antara y menggunakan matriks segitiga bawah L dan vektor konstan vektor_b.
Terakhir, fungsi ini memecahkan sistem persamaan lagi untuk vektor solusi vektor_solusi menggunakan matriks segitiga atas U dan vektor antara y.
Fungsi ini menangani potensi masalah dengan matriks singular (matriks_A) dengan mengeluarkan error ValueError dan mencetak pesan yang menyatakan bahwa dekomposisi LU tidak mungkin dilakukan. Dalam kasus tersebut, fungsi mengembalikan None untuk menunjukkan tidak adanya solusi.
Kode pengujian yang disediakan menunjukkan penggunaan fungsi tersebut dengan membuat contoh matriks koefisien matriks_A dan vektor konstan vektor_b, menyelesaikan sistem persamaan menggunakan fungsi, dan mencetak vektor solusi yang dihasilkan.

Proyek 3: Penyelesaian Persamaan Linier dengan Dekomposisi Crout

Proyek ini juga menangani masalah penyelesaian persamaan linier (Ax = b) tetapi menggunakan metode dekomposisi Crout untuk menemukan solusinya. Proyek ini mengimplementasikan fungsi solusi_persamaan_linear_crout(matriks_A, vektor_b) yang menerima matriks koefisien matriks_A dan vektor konstan vektor_b sebagai input.
Fungsi ini menggunakan fungsi linalg.lu() dari pustaka scipy.linalg untuk melakukan dekomposisi matriks koefisien matriks_A menjai matriks segitiga bawah L, matriks segitiga atas U, dan matriks permutasi P, dengan pengaturan khusus parameter permute_l menjadi False untuk menyatakan tidak ada permutasi.
Mirip dengan dekomposisi LU menggunakan metode Gauss, fungsi ini menggunakan fungsi linalg.solve_triangular() untuk menyelesaikan sistem persamaan untuk vektor antara y menggunakan matriks segitiga bawah L dan vektor konstan vektor_b.
Terakhir, fungsi ini memecahkan sistem persamaan lagi untuk vektor solusi vektor_solusi menggunakan matriks segitiga atas U dan vektor antara y.
Fungsi ini menangani potensi masalah dengan matriks singular (matriks_A) dengan mengeluarkan error ValueError dan mencetak pesan yang menyatakan bahwa dekomposisi LU tidak mungkin dilakukan. Dalam kasus tersebut, fungsi mengembalikan None untuk menunjukkan tidak adanya solusi.
Kode pengujian yang disediakan menunjukkan penggunaan fungsi tersebut dengan membuat contoh matriks koefisien matriks_A dan vektor konstan vektor_b, menyelesaikan sistem persamaan
