# MYSQL
## Praktikum3

* Nama   : Fergiawan Satrio Bagaskoro
* Nim    : 312210169
* Kelas  : TI.22.A2



### 1. Lakukan penambahan data pada tabel mahasiswa dengan mengisi kd_ds yang belum ada pada data dosen. 

![ss1](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/1723a510-8e66-4d9c-ac4c-cb022a3c3838)

![ss2](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/69840f33-c3fe-40fe-b649-599c034598a2)

![ss3](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/803d6d6f-baec-48e0-86b7-7995c4716bc3)

![ss4](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/1ef27cdc-9ee7-4f49-9994-09c781af137f)

### 2. Hapus satu record dat pada tabel dosen yang telah dirujuk pada tabel mahasiswa

![ss5](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/c86d9ffd-bc32-4bdb-88ef-618142575d2f)

![ss6](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/2f554b3e-6bd5-438f-8547-27c0cfd2bfd6)

### 3. Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT. 


![ss7](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/ce5f7cd4-463d-4c1b-b5ac-b1d4139cdcaf)

### 4. Lakukan perubahan data pada tabel dosen (kd_ds).

![ss8](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/c422a6f5-0d81-43ae-a603-3b3b9e84211b)

### 5. Lakukan penghapusan data pada tabel dosen, 

![ss10](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/8ff58b9a-9121-4469-8b23-da0d91db94d2)

### 6. Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL 
Untuk Dapat menghapus data kita bisa masukan perintah seperti berikut

***
ALTER TABLE mahasiswa ADD CONSTRAINT FK_Dosen FOREIGN KEY (kd_ds) REFERENCES dosen(kd_ds) ON UPDATE CASCADE ON DELETE SET NULL;
***

### 7. Lakukan penghapusan data pada tabel dosen.

![ss9](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/d01a5eb0-8127-478b-8dfe-0201f3aac3f7)


## Evaluasi Dan Pertanyaan

1. Apa bedanya pengguna RESTRICT dan CASCADE ?

RESTRICT dan CASCADE adalah dua opsi yang digunakan dalam konstrain referensial di dalam basis data untuk menentukan bagaimana perilaku pembaruan atau penghapusan akan berpengaruh pada entitas terkait. Berikut adalah perbedaan antara RESTRICT dan CASCADE:

*    RESTRICT: RESTRICT digunakan untuk mencegah pembaruan atau penghapusan entitas yang akan melanggar konstrain referensial. Jika terdapat referensi yang terhubung ke entitas yang akan diubah atau dihapus, operasi tersebut akan ditolak dan menghasilkan error. RESTRICT memastikan keberadaan integritas referensial dan mencegah tindakan yang dapat merusak konsistensi data.

*    CASCADE: CASCADE digunakan untuk mengubah atau menghapus entitas utama beserta entitas terkait secara otomatis. Jika terdapat referensi yang terhubung ke entitas utama yang diubah atau dihapus, aksi CASCADE akan mengubah atau menghapus entitas terkait secara otomatis. Dengan menggunakan CASCADE, perubahan atau penghapusan pada entitas utama akan ditransfer ke entitas terkait tanpa harus melakukan tindakan tambahan secara eksplisit.

2. Berikan kesimpulan

menggunakan CASCADE dapat mempercepat dan menyederhanakan proses karena tidak perlu mengubah entitas terkait secara terpisah. Namun, harus hati-hati dalam penggunaan CASCADE untuk menghindari perubahan atau penghapusan yang tidak disengaja pada entitas. Sedangkan RESTRICT lebih disukai jika ingin memastikan keberadaan integritas referensial dan mengontrol secara langsung perubahan atau penghapusan pada entitas terkait.













