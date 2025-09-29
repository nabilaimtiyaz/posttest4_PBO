# posttest4_PBO

**Nama: Nabila Imtiyaz Agustin**

**NIM: 2409116011**

**Kelas: A 2024**

# Tema

Sistem Pencatatan Hasil Panen Kebun, dirancang untuk membantu pencatatan, pengelolaan, serta pencarian data hasil panen petani. Program ini menggunakan encapsulation, inheritance, dan polymorphism/overriding untuk memudahkan pengembangan serta pemeliharaan kode.

Dalam sistem ini, hasil panen dikelompokkan menjadi dua kategori utama, yaitu sayur dan buah. Masing-masing kategori memiliki atribut umum seperti nama, berat, dan kualitas, serta atribut khusus (misalnya cara penyimpanan untuk sayur dan lama simpan untuk buah). Pengguna dapat melakukan berbagai operasi melalui menu.

# <sub>Penjelasan kode</sub>


<img width="1091" height="624" alt="image" src="https://github.com/user-attachments/assets/dfd8f90b-b9f1-4d0f-a6e6-4a79630fb3a7" />


<img width="1041" height="380" alt="image" src="https://github.com/user-attachments/assets/83b101f9-f80a-46de-9ca8-2b20e6d449a8" />


Class itemPanen berperan sebagai superclass yang mempresentasikan data umum dari sebuah hasil panen. Didalamnya terdapat properti utama seperti 'nama', 'beratkg', dan 'kualitas'. Menerapkan encapsulation dengan menjadikan atribut private lalu menyediakan getter dan setter agar data hanya bisa diakses melalui method yang sudah disediakan. Memiliki constructor untuk memudahkan pembuatan objek hasil panen baru. Ada juga method tampilkanInfo() yang nantinya bisa di-override oleh subclass untuk menampilkan detail khusus.


<img width="475" height="151" alt="image" src="https://github.com/user-attachments/assets/cbb9695c-e2a0-4f52-b428-4f59bee53ba8" />


Class buah adalah subclass dari itemPanen yang mempresentasikan hasil panen khusus katefori buah. Menambahkan atribut khusus seperti lamaSimpan untuk menyimpan informasi ketahanan buah. Menggunakan constructor untuk mengisi data buah sekaligus memanggil constructor superclass. Melakukan overriding pada method tampilkanInfo() agar selain menampilkan atribut umum juga menampilkan informasi lama simpan.


<img width="1080" height="628" alt="image" src="https://github.com/user-attachments/assets/8c831c71-4b92-4b51-81c4-f06157ecc8aa" />


Class sayur merupakan subclass dari itemPanen, tapi khusus untuk kategori sayur. Menambahkan atribut tambahan seperti caraSimpan. Constructor dibuat untuk menginisialisasi data sayur dan tetap memanggil constructor superclass. Method tampilkanInfo() juga di-override sehingga informasi khusus sayur ikut tampil selain atribut umum.


<img width="1035" height="673" alt="image" src="https://github.com/user-attachments/assets/07f9b6d3-37ea-4f20-a9fb-cc4b63a91952" />


<img width="1147" height="775" alt="image" src="https://github.com/user-attachments/assets/0a6baf50-9c55-4a6e-b86a-77af40538fe4" />


<img width="1147" height="782" alt="image" src="https://github.com/user-attachments/assets/78aefc21-8d67-47a7-b61b-1a79ab9b0a01" />


<img width="865" height="779" alt="image" src="https://github.com/user-attachments/assets/2bbfe549-54de-4952-8455-682bff60293b" />


<img width="1202" height="324" alt="image" src="https://github.com/user-attachments/assets/65fca370-97af-4244-ab30-4fe09d8bb569" />


Class panenService berguna untuk mengatur logika CRUD  dan pengelolaan data panen. Menyimpan data hasil panen dalam sebuah ArrayList<itemPanen>. Memiliki method untuk melakukan operasi: 
1. tambahItem(), menambahkan data baru (baik buah maupun sayur).
2. tampilkanItem(), menampilkan seluruh data panen, memanggil method.
3. tampilkanInfor(), hasil overriding dari subclass.
4. editItem(), mengubah data berdasarkan index pilihan pengguna.
5. hapusItem(), menghapus item dari daftar panen.
6. cariItem(), fitur tambahan untuk encari panen berdasarkan nama.
Class ini menjadi penghubung utama antara input pengguna dan data yang dikelola.

Class mainProgram adalah entry point atau titik awal eksekusi program. Class ini menyediakan menu interaktif berupa pilihan angka agar pengguna dapat melakukan operasi CRUD, menggunakan objek dari panenService untuk menjalankan logika pengelolaan data.


# <sub>Penjelasan Alur Program</sub>


<img width="326" height="200" alt="image" src="https://github.com/user-attachments/assets/955095c4-c815-432e-ac8d-1def05413453" />


Ketika program pertama kali dijalankan, pengguna akan langsung melihat menu utama yang menampilkan beberapa pilihan, yaitu Tambah Item, Lihat Item, Edit Item, Hapus Item, Cari Item, dan Keluar.


<img width="411" height="352" alt="image" src="https://github.com/user-attachments/assets/30b9ed8e-a799-4844-8109-d6536fec5674" />


Jika pengguna memilih opsi 1 (Tambah Item), maka sistem akan menanyakan detail hasil panen seperti kategori (buah atau sayur), nama item, berat dalam kilogram, kualitas, serta informasi tambahan sesuai kategori. Setelah data dimasukkan, program akan menyimpan objek baru ke dalam daftar panen, lalu menampilkan pesan bahwa data berhasil ditambahkan.


<img width="553" height="250" alt="image" src="https://github.com/user-attachments/assets/25b83d24-52db-4008-a7bb-651aa072a3b7" />


Jika pengguna memilih opsi 2 (Lihat Item), maka sistem akan menampilkan seluruh daftar hasil panen yang sudah tersimpan. Pada tahap ini, method tampilkanInfo() yang ada di setiap objek (buah atau sayur) akan dipanggil. Hasilnya, data yang tampil bisa berbeda tergantung kategori panen, karena ada penerapan overriding. Jika daftar masih kosong, program akan menampilkan pesan bahwa belum ada data.


<img width="552" height="253" alt="image" src="https://github.com/user-attachments/assets/b0de730f-e51f-4f1b-a80a-51b6eaf51b75" />


Jika pengguna memilih opsi 3 (Edit Item), terlebih dahulu sistem akan menampilkan daftar hasil panen. Setelah itu, pengguna diminta memilih nomor item yang ingin diubah. Jika nomor valid, sistem meminta data baru (kategori, nama, berat, kualitas, dan atribut tambahan) lalu memperbarui data yang ada. Setelah selesai, akan muncul pesan bahwa item berhasil diedit. Jika pengguna memilih nomor yang tidak valid, akan keluar pesan peringatan.


<img width="623" height="302" alt="image" src="https://github.com/user-attachments/assets/149dd32f-0b89-4070-aeda-1d9448aee32f" />


Jika pengguna memilih opsi 4 (Hapus Item), daftar hasil panen kembali ditampilkan agar pengguna tahu nomor item yang ingin dihapus. Setelah memilih nomor, sistem akan menghapus data yang sesuai dan memberikan pesan konfirmasi bahwa item berhasil dihapus. Jika input salah, sistem menampilkan pesan bahwa nomor tidak valid.


<img width="625" height="250" alt="image" src="https://github.com/user-attachments/assets/506af8bf-a193-491d-a9f7-de284adeed9e" />


Jika pengguna memilih opsi 5 (Cari Item), program akan meminta pengguna mengetikkan nama item yang ingin dicari. Sistem kemudian melakukan pencarian dalam daftar panen. Jika data ditemukan, detail hasil panen akan ditampilkan sesuai kategorinya. Jika tidak ditemukan, sistem akan menampilkan pesan bahwa item tidak ada dalam daftar.


<img width="351" height="230" alt="image" src="https://github.com/user-attachments/assets/ceba2a39-611e-4b52-b238-9f72e04ee2b5" />


Jika pengguna memilih opsi 6 (Keluar), maka sistem menampilkan pesan ucapan terima kasih, lalu program berhenti berjalan.


