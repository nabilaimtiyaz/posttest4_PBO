# posttest4_PBO

**Nama: Nabila Imtiyaz Agustin**

**NIM: 2409116011**

**Kelas: A 2024**

# Tema

Sistem Pencatatan Hasil Panen Kebun, dirancang untuk membantu pencatatan, pengelolaan, serta pencarian data hasil panen petani. Program ini menggunakan encapsulation, inheritance, dan polymorphism/overriding untuk memudahkan pengembangan serta pemeliharaan kode.

Dalam sistem ini, hasil panen dikelompokkan menjadi dua kategori utama, yaitu sayur dan buah. Masing-masing kategori memiliki atribut umum seperti nama, berat, dan kualitas, serta atribut khusus (misalnya cara penyimpanan untuk sayur dan lama simpan untuk buah). Pengguna dapat melakukan berbagai operasi melalui menu.

# <sub>Penjelasan kode</sub>


<img width="475" height="151" alt="image" src="https://github.com/user-attachments/assets/cbb9695c-e2a0-4f52-b428-4f59bee53ba8" />

Pada program ini, konsep Abstraction diterapkan melalui class ItemPanen yang berada di packages model. Class ini berfungsi sebagai representasi umum dari seluruh hasil panen. Dengan adanya class induk ini, detail implementasi dari setiap jenis panen tidak perlu diketahui pengguna, cukup melalui method umum seperti tampilkanInfo().


<img width="834" height="185" alt="image" src="https://github.com/user-attachments/assets/d10250d9-502d-4370-8cea-646e8083f6d3" />


Selain abstraction, program ini juga menerapkan Polymorphism dalam dua bentuk, yaitu overriding dan overloading. Penerapan overriding terlihat pada subclass Buah dan Sayur yang menuliskan ulang method tampilkanInfo() milik ItemPanen.

Meskipun method yang dipanggil sama, hasil yang ditampilkan berbeda sesuai jenis objek yang digunakan.


<img width="844" height="192" alt="image" src="https://github.com/user-attachments/assets/4fe5591c-4f61-467b-9f68-563cbac2818b" />


Penerapan Polymorphism overriding pada subclass Sayur yang menuliskan ulang method tampilkanInfo() milik ItemPanen.


# <sub>Penjelasan Alur Program</sub>


<img width="405" height="228" alt="image" src="https://github.com/user-attachments/assets/c84a31e9-675b-430c-bc2a-46565961b128" />


Ketika program pertama kali dijalankan, pengguna akan langsung melihat menu utama yang menampilkan beberapa pilihan, yaitu Tambah Item, Lihat Item, Edit Item, Hapus Item, Cari Item (berdasarkan nama), Cari Item (berdasarkan kategori), dan Keluar.


<img width="411" height="352" alt="image" src="https://github.com/user-attachments/assets/30b9ed8e-a799-4844-8109-d6536fec5674" />


Jika pengguna memilih opsi 1 (Tambah Item), maka sistem akan menanyakan detail hasil panen seperti kategori (buah atau sayur), nama item, berat dalam kilogram, kualitas, serta informasi tambahan sesuai kategori. Setelah data dimasukkan, program akan menyimpan objek baru ke dalam daftar panen, lalu menampilkan pesan bahwa data berhasil ditambahkan.


<img width="553" height="250" alt="image" src="https://github.com/user-attachments/assets/25b83d24-52db-4008-a7bb-651aa072a3b7" />


Jika pengguna memilih opsi 2 (Lihat Item), maka sistem akan menampilkan seluruh daftar hasil panen yang sudah tersimpan. Pada tahap ini, method tampilkanInfo() yang ada di setiap objek (buah atau sayur) akan dipanggil. Hasilnya, data yang tampil bisa berbeda tergantung kategori panen, karena ada penerapan overriding. Jika daftar masih kosong, program akan menampilkan pesan bahwa belum ada data.


<img width="552" height="253" alt="image" src="https://github.com/user-attachments/assets/b0de730f-e51f-4f1b-a80a-51b6eaf51b75" />


Jika pengguna memilih opsi 3 (Edit Item), terlebih dahulu sistem akan menampilkan daftar hasil panen. Setelah itu, pengguna diminta memilih nomor item yang ingin diubah. Jika nomor valid, sistem meminta data baru (kategori, nama, berat, kualitas, dan atribut tambahan) lalu memperbarui data yang ada. Setelah selesai, akan muncul pesan bahwa item berhasil diedit. Jika pengguna memilih nomor yang tidak valid, akan keluar pesan peringatan.


<img width="623" height="302" alt="image" src="https://github.com/user-attachments/assets/149dd32f-0b89-4070-aeda-1d9448aee32f" />


Jika pengguna memilih opsi 4 (Hapus Item), daftar hasil panen kembali ditampilkan agar pengguna tahu nomor item yang ingin dihapus. Setelah memilih nomor, sistem akan menghapus data yang sesuai dan memberikan pesan konfirmasi bahwa item berhasil dihapus. Jika input salah, sistem menampilkan pesan bahwa nomor tidak valid.


<img width="1267" height="77" alt="image" src="https://github.com/user-attachments/assets/454a07dd-6cf1-4dba-99c9-47c1f9625fec" />



Jika pengguna memilih opsi 5 (Cari Item (berdasarkan nama)), program akan meminta pengguna mengetikkan nama item yang ingin dicari. Sistem kemudian melakukan pencarian dalam daftar panen. Jika data ditemukan, detail hasil panen akan ditampilkan sesuai namanya. Jika tidak ditemukan, sistem akan menampilkan pesan bahwa item tidak ada dalam daftar.

<img width="1077" height="71" alt="image" src="https://github.com/user-attachments/assets/f704e9d8-d15f-4c2e-b003-328dcfca65ce" />


Jika pengguna memilih opsi 6 (Cari Item (berdasarkan kategori)), program akan meminta pengguna mengetikkan kategori item yang ingin dicari. Sistem kemudian melakukan pencarian dalam daftar panen. Jika data ditemukan, detail hasil panen akan ditampilkan sesuai kategorinya. Jika tidak ditemukan, sistem akan menampilkan pesan bahwa item tidak ada dalam daftar.


<img width="351" height="230" alt="image" src="https://github.com/user-attachments/assets/ceba2a39-611e-4b52-b238-9f72e04ee2b5" />


Jika pengguna memilih opsi 7 (Keluar), maka sistem menampilkan pesan ucapan terima kasih, lalu program berhenti berjalan.
