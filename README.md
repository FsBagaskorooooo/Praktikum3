# MYSQL
## Praktikum3

* Nama   : Fergiawan Satrio Bagaskoro
* Nim    : 312210169
* Kelas  : TI.22.A2



### 1. Lakukan penambahan data pada tabel mahasiswa dengan mengisi kd_ds yang belum ada pada data dosen. 

![ss1](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/21662a20-ae21-4f9d-88aa-9fef347e53c1)

![ss2](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/17fda049-920c-46de-b665-6e4854bb3fc4)

![ss3](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/b8fdb56d-544b-47d6-aa32-bf41769f51c3)

![ss4](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/fc357139-4f47-4c70-94cd-021f89b0e617)


### 2. Hapus satu record dat pada tabel dosen yang telah dirujuk pada tabel mahasiswa

![ss5](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/7c411ca7-40cd-454d-a383-3b39d337832d)

![ss6](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/26ea7635-2d1c-449e-aa5b-145cc8a02e73)


### 3. Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT. 

![ss7](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/e4355c21-5983-4d84-8003-102fbb842cc4)

### 4. Lakukan perubahan data pada tabel dosen (kd_ds).


![ss8](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/d014a093-c7de-46f1-8fdc-9961dc8ac997)


### 5. Lakukan penghapusan data pada tabel dosen, 

![ss10](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/b10a47f1-e140-455c-90a1-a530e92c5cfc)


### 6. Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL 
Untuk Dapat menghapus data kita bisa masukan perintah seperti berikut

***
ALTER TABLE mahasiswa ADD CONSTRAINT FK_Dosen FOREIGN KEY (kd_ds) REFERENCES dosen(kd_ds) ON UPDATE CASCADE ON DELETE SET NULL;
***

### 7. Lakukan penghapusan data pada tabel dosen.

![ss9](https://github.com/FsBagaskorooooo/Praktikum3/assets/130354090/9e3cda41-2777-4830-b227-3c8f0a96e513)



## Evaluasi Dan Pertanyaan

1. Apa bedanya pengguna RESTRICT dan CASCADE ?

RESTRICT dan CASCADE adalah dua opsi yang digunakan dalam konstrain referensial di dalam basis data untuk menentukan bagaimana perilaku pembaruan atau penghapusan akan berpengaruh pada entitas terkait. Berikut adalah perbedaan antara RESTRICT dan CASCADE:

*    RESTRICT: RESTRICT digunakan untuk mencegah pembaruan atau penghapusan entitas yang akan melanggar konstrain referensial. Jika terdapat referensi yang terhubung ke entitas yang akan diubah atau dihapus, operasi tersebut akan ditolak dan menghasilkan error. RESTRICT memastikan keberadaan integritas referensial dan mencegah tindakan yang dapat merusak konsistensi data.

*    CASCADE: CASCADE digunakan untuk mengubah atau menghapus entitas utama beserta entitas terkait secara otomatis. Jika terdapat referensi yang terhubung ke entitas utama yang diubah atau dihapus, aksi CASCADE akan mengubah atau menghapus entitas terkait secara otomatis. Dengan menggunakan CASCADE, perubahan atau penghapusan pada entitas utama akan ditransfer ke entitas terkait tanpa harus melakukan tindakan tambahan secara eksplisit.

2. Berikan kesimpulan

menggunakan CASCADE dapat mempercepat dan menyederhanakan proses karena tidak perlu mengubah entitas terkait secara terpisah. Namun, harus hati-hati dalam penggunaan CASCADE untuk menghindari perubahan atau penghapusan yang tidak disengaja pada entitas. Sedangkan RESTRICT lebih disukai jika ingin memastikan keberadaan integritas referensial dan mengontrol secara langsung perubahan atau penghapusan pada entitas terkait.













