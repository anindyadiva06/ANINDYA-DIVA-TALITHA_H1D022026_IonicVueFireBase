**ANINDYA DIVA TALITHA || H1D022026**

**Login Page**

![file_2024-11-21_15 01 12 1](https://github.com/user-attachments/assets/aafe2208-c9ce-4476-9465-081daba96304)
![WhatsApp Image 2024-11-21 at 22 01 54_f0fa4cd4](https://github.com/user-attachments/assets/517a02a8-afa1-422f-9c65-1baf5c5727a8)

Pada LoginPage.vue, pengguna akan diarahkan ke halaman login di mana terdapat tombol untuk melakukan autentikasi dengan Google. Ketika pengguna mengklik tombol tersebut maka fungsi login() dipanggil yang kemudian menggunakan metode loginWithGoogle dari store auth.ts seperti pada sintaks dibawah ini

![image](https://github.com/user-attachments/assets/d7ebd9d5-3bc0-43ea-97c2-6840263f2ddd)

Ketika proses login menggunakan Google Auth dimulai maka kredensial pengguna disalin ke Firebase Authentication.

**Home Page**

![WhatsApp Image 2024-11-21 at 21 58 36_67712d92](https://github.com/user-attachments/assets/7b71987e-f3eb-4374-b2b2-f34ac93d424b)

Setelah login berhasil, aplikasi secara otomatis akan mengarahkan pengguna ke halaman utama (HomePage.vue) melalui router.push("/home") yang terjadi karena pengaturan di index.ts yang memastikan pengguna yang sudah terautentikasi tidak perlu login lagi ketika mengakses halaman yang memerlukan autentikasi seperti pada sintaks dibawah ini

![image](https://github.com/user-attachments/assets/c34290ae-c216-4f09-aac2-0acae2bf7bf7)

Pada HomePage.vue, aplikasi menampilkan halaman utama yang berisi menu tab yang mengarah ke halaman beranda dan halaman profil 

**Profile Page**

![WhatsApp Image 2024-11-21 at 21 58 07_fa3d8413](https://github.com/user-attachments/assets/579e9870-d66e-43ae-9f01-54aa59bae19f)

Pada halaman profil (ProfilePage.vue)terdapat informasi lebih detail tentang pengguna seperti nama dan email. Data ini diambil dari objek user yang terhubung ke store auth.ts. Di halaman profil, terdapat gambar avatar pengguna yang diambil dari user.photoURL seperti pada sintaks berikut

![image](https://github.com/user-attachments/assets/0b270921-bd24-4089-b360-5b85713db4a8)
![image](https://github.com/user-attachments/assets/41eba878-2b3a-4890-9665-f090ad5a7fc1)

Pada halaman profil, pengguna juga dapat keluar dari akun dengan menekan tombol logout untuk melakukan sesi keluar dari aplikasi.

**Logout**

![file_2024-11-21_14 59 14 1](https://github.com/user-attachments/assets/bacd23c6-0132-4205-ad67-e6c943c5a976)
![file_2024-11-21_15 01 12 1](https://github.com/user-attachments/assets/1fd84248-1d29-4928-949b-bc47a30323a9)

Proses logout memanfaatkan fungsi logout() dalam store auth.ts yang akan menghapus sesi pengguna kemudian mengarahkan pengguna kembali ke halaman login.
