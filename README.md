# Capstone-K25

# Sistem Pelaporan Perusahaan Berbasis Digital

## A. Deskripsi Program
Sistem Pelaporan ini merupakan aplikasi berbasis Java dengan antarmuka grafis (GUI) yang dirancang khusus untuk mendukung kebutuhan operasional perusahaan. Program ini memiliki tampilan sederhana, intuitif, dan mudah digunakan bahkan oleh pengguna yang tidak memiliki latar belakang teknis sekalipun.
Aplikasi ini dilengkapi dengan fitur utama seperti pengelolaan pemesanan, pembuatan laporan, serta penerbitan nota secara otomatis. Setiap pengguna baik admin, staff, maupun klien dapat mengakses informasi dengan mudah, melakukan input data secara efisien, serta memperoleh hasil informasi yang akurat dan cepat.
Dengan adanya sistem ini, perusahaan dapat mengolah data secara lebih efektif dan menghasilkan informasi yang mendukung pengambilan keputusan strategis. Hal ini diharapkan mampu meningkatkan kualitas layanan, mempercepat proses bisnis, serta membantu perusahaan tetap kompetitif dalam dunia industri modern.

## B. Fitur Program
Program ini memiliki pembagian hak akses berdasarkan jenis pengguna untuk memastikan keamanan dan keteraturan data. Admin memiliki akses penuh untuk mengelola seluruh fitur, meliputi pengelolaan produk, pelaporan, nota, data admin, serta data staff. Staff berperan mengelola transaksi dan laporan, dengan kemampuan membuat, membaca, memperbarui, dan menghapus data nota maupun pelaporan, serta mengakses daftar produk dan mengelola data pemesanan tertentu. Sementara itu, client hanya diberikan akses untuk melihat daftar produk, melakukan pemesanan, serta melihat status pemesanan dan nota. Dengan struktur akses ini, sistem mampu mendukung proses bisnis secara efisien sekaligus menjaga integritas data.

Fitur Sistem Berdasarkan Hak Akses Pengguna:

1. Admin
Admin memiliki akses penuh untuk mengelola data dalam sistem, meliputi:

CRUD produk

CRUD pelaporan

CRUD nota

Read data admin

CRUD staff

2. Staff
Staff berperan dalam mengelola transaksi dan pelaporan, dengan hak akses:

CRUD nota

CRUD pelaporan

Read data produk

Read dan delete pemesanan

3. Client
Client hanya memiliki akses terbatas untuk melakukan pemesanan dan melihat informasi, yaitu:

Read data produk

Create pemesanan

Read pemesanan

Read nota

## Penerapan OOP

## 1. Encapsulation

Encapsulation adalah salah satu pilar utama dalam Object-Oriented Programming (OOP) yang berarti pembungkusan data dan fungsi (method) yang mengakses data tersebut ke dalam satu unit (class). Dengan encapsulation, data di dalam objek dilindungi agar tidak bisa diakses atau diubah secara langsung dari luar class, melainkan harus melalui method khusus (getter & setter).

## Class Pelaporan
<img width="377" height="143" alt="image" src="https://github.com/user-attachments/assets/e0a58261-150a-41d7-8cc5-57b2815bf5f4" />

Semua atribut (id_pelaporan, status_pelaporan, dll) dibuat private, sehingga tidak bisa diakses langsung dari luar class.
Akses dan perubahan data dilakukan melalui getter dan setter, sehingga data lebih aman dan terkontrol:

<img width="1090" height="352" alt="image" src="https://github.com/user-attachments/assets/0c0b764e-389c-413f-b21a-78e008a284b4" />

## Class Nota
<img width="315" height="140" alt="image" src="https://github.com/user-attachments/assets/bce90b73-732e-4283-8550-3577aa0b0487" />

Penerapan encapsulation terlihat dari penggunaan atribut yang bersifat private, seperti id_nota, id_pelaporan, dan lain-lain, sehingga data tidak dapat diakses langsung dari luar class. Untuk mengakses dan mengubah nilainya, class ini menyediakan method getter dan setter, sehingga proses manipulasi data tetap aman dan terkontrol.

getter & setter:

<img width="835" height="352" alt="image" src="https://github.com/user-attachments/assets/1e983326-abc2-453b-a2ec-e8a4330bd245" />

## Class Pemesanan
<img width="381" height="189" alt="image" src="https://github.com/user-attachments/assets/a720a781-f838-491b-a1d9-8bde5fef2fa8" />

Konsep encapsulation diterapkan melalui penggunaan atribut yang bersifat private, seperti id_pemesanan, jumlah_produk, tanggal_pemesanan, dan atribut lainnya, sehingga data tidak bisa diakses langsung dari luar class. Untuk menjaga keamanan dan konsistensi data, class ini menyediakan method getter dan setter sebagai pintu akses dan pengubah nilai atribut.

getter & setter:
<img width="1081" height="488" alt="image" src="https://github.com/user-attachments/assets/9c349357-4806-42ff-9b8a-b78a28df759d" />

## Class Produk
<img width="327" height="138" alt="image" src="https://github.com/user-attachments/assets/940ad4f6-fda1-441d-9ed1-ada6bac01d36" />

Penerapan encapsulation terlihat dari atribut-atribut yang bersifat private seperti id_produk, nama_produk, deskripsi, harga, dan stok. Dengan cara ini, data produk tidak bisa diakses atau diubah secara langsung dari luar class, sehingga keamanan dan konsistensi data tetap terjaga. Untuk memberikan akses yang terkontrol, disediakan method getter dan setter, misalnya getHarga() dan setStok(int stok), yang memungkinkan pengambilan dan perubahan nilai atribut secara aman.

getter & setter:

<img width="852" height="347" alt="image" src="https://github.com/user-attachments/assets/b68c70e4-69c4-42bf-bddb-bacfa2aa7a19" />

## Class staffController
<img width="519" height="78" alt="image" src="https://github.com/user-attachments/assets/fa74d4d8-f8fe-4ed4-b610-0321afaac9f5" />

Atribut pada class tersebut dideklarasikan dengan access modifier private agar tidak memiliki direct access dari luar class. Penggunaan keyword final pada variabel staffModel menunjukkan bahwa reference variable tersebut bersifat immutable, artinya reference-nya tidak dapat di-reassign ke objek lain setelah inisialisasi pertama. Dengan demikian, instance staff yang digunakan oleh controller akan tetap konsisten selama lifecycle staffControlle.

## Class loginController
<img width="324" height="120" alt="image" src="https://github.com/user-attachments/assets/b981e3b8-18e4-4640-85c8-524fc1262640" />

Atribut userRole, userName, dan userId dideklarasikan dengan access modifier private agar data sensitif terkait user yang sedang login tidak dapat diakses atau dimodifikasi secara langsung dari luar class. Akses dan modifikasi terhadap nilai atribut tersebut seharusnya dilakukan melalui method publik (getter/setter) atau melalui mekanisme kontrol di dalam class loginController itu sendiri.

## Class clientController
<img width="543" height="69" alt="image" src="https://github.com/user-attachments/assets/a03a6f84-180a-4e47-97cb-0d5e4da25ff1" />

Deklarasi variabel clientModel menggunakan modifier private dan keyword final menunjukkan penerapan prinsip Encapsulation serta immutability pada reference. Dengan private, instance model hanya dapat diakses oleh clientController. Sementara itu, penggunaan final memastikan bahwa reference clientModel tidak dapat di-reassign ke objek client lain setelah inisialisasi awal. Ini menjaga konsistensi penggunaan model selama lifecycle controller.

## Class adminController
<img width="519" height="67" alt="image" src="https://github.com/user-attachments/assets/e09721b9-7545-4247-b0c8-6279eb5672db" />

Deklarasi variabel adminModel menggunakan modifier private dan keyword final menunjukkan penerapan prinsip Encapsulation serta immutability pada reference objek. Dengan modifier private, instance adminModel hanya dapat diakses oleh kelas adminController, sehingga mencegah akses langsung dari luar kelas dan menjaga keamanan data internal. Sementara itu, penggunaan keyword final memastikan bahwa reference adminModel tidak dapat diubah atau di-reassign ke objek admin lain setelah inisialisasi awal.

## Class produkController
<img width="544" height="68" alt="image" src="https://github.com/user-attachments/assets/f2bc6cde-bc78-49be-9fe2-f06d0008e85e" />

Deklarasi variabel produkModel menggunakan modifier private dan keyword final merupakan penerapan prinsip Encapsulation serta menjaga immutability pada referensi objek. Dengan modifier private, instance produkModel hanya dapat diakses oleh kelas produkController, sehingga data di dalam objek produk terlindungi dari akses atau modifikasi langsung oleh kelas lain. Penggunaan keyword final memastikan bahwa referensi produkModel tidak dapat diubah atau diarahkan ke objek produk lain setelah proses inisialisasi awal.

## Class pemesananController
<img width="619" height="76" alt="image" src="https://github.com/user-attachments/assets/2994a916-3f70-4205-a514-1964176c398d" />

Deklarasi variabel pemesananModel menggunakan modifier private dan keyword final menunjukkan penerapan prinsip Encapsulation serta menjaga immutability pada referensi objek. Dengan modifier private, instance pemesananModel hanya dapat diakses oleh kelas pemesananController, sehingga mencegah akses atau perubahan langsung dari luar kelas dan menjaga integritas data pemesanan. Sementara itu, penggunaan keyword final memastikan bahwa referensi pemesananModel tidak dapat diubah atau diarahkan ke objek pemesanan lain setelah inisialisasi awal.

## Class pelaporanController
<img width="629" height="81" alt="image" src="https://github.com/user-attachments/assets/6286595c-703f-445d-9fc8-45f17029a91a" />

Deklarasi variabel pelaporanModel menggunakan modifier private dan keyword final merupakan penerapan prinsip Encapsulation serta menjaga immutability pada referensi objek. Dengan modifier private, instance pelaporanModel hanya dapat diakses oleh kelas pelaporanController, sehingga mencegah akses langsung dari luar kelas dan menjaga keamanan serta integritas data pelaporan. Penggunaan keyword final memastikan bahwa referensi pelaporanModel tidak dapat diubah atau diarahkan ke objek pelaporan lain setelah inisialisasi awal.

## Class notaController
<img width="508" height="72" alt="image" src="https://github.com/user-attachments/assets/07be3c1d-2ff1-47a9-9d48-2349ff573caf" />

Deklarasi variabel notaModel menggunakan modifier private dan keyword final menunjukkan penerapan prinsip Encapsulation serta menjaga immutability pada referensi objek. Dengan modifier private, instance notaModel hanya dapat diakses oleh kelas notaController, sehingga data di dalam objek nota terlindungi dari akses dan modifikasi langsung oleh kelas lain. Penggunaan keyword final memastikan bahwa referensi notaModel tidak dapat diubah atau diarahkan ke objek nota lain setelah proses inisialisasi awal.

## Class notaDatabase
<img width="545" height="186" alt="image" src="https://github.com/user-attachments/assets/a03c3231-d8f1-4fac-882e-7e4ada7eb0e6" />

Kode pada kelas notaDatabase menerapkan prinsip encapsulation dengan menyembunyikan detail internal koneksi database menggunakan modifier private. Variabel seperti DB_HOST, DB_PORT, DB_NAME, DB_USERNAME, dan DB_PASSWORD hanya dapat diakses di dalam kelas itu sendiri, sehingga data sensitif tidak dapat dimodifikasi atau dilihat langsung oleh kelas lain. Penggunaan final memastikan nilainya tetap dan tidak bisa diubah, sedangkan static membuatnya menjadi milik kelas, bukan objek.

## Class pelaporanDatabase
<img width="619" height="184" alt="image" src="https://github.com/user-attachments/assets/977c9d3e-6711-4a02-9bbf-d01861e671c2" />

Kode pada kelas pelaporanDatabase menerapkan prinsip encapsulation dengan menyembunyikan detail koneksi database menggunakan modifier private. Variabel seperti DB_HOST, DB_PORT, DB_NAME, DB_USERNAME, dan DB_PASSWORD hanya bisa diakses di dalam kelas itu sendiri, sehingga informasi sensitif tidak terekspos ke luar. Penggunaan final memastikan nilai-nilai tersebut tidak dapat diubah, sedangkan static membuatnya menjadi milik kelas, bukan milik objek. Hanya TABLE_PELAPORAN yang bersifat public karena aman untuk diakses oleh kelas lain.

## Class pemesananDatabase
<img width="618" height="190" alt="image" src="https://github.com/user-attachments/assets/d270c56c-5790-4ea7-890a-805d81216a6e" />

Deklarasi variabel pada kelas pemesananDatabase menggunakan modifier private dan keyword final static menunjukkan penerapan prinsip Encapsulation serta menjaga immutability pada konfigurasi koneksi database. Dengan modifier private, setiap variabel seperti DB_HOST, DB_PORT, DB_NAME, DB_USERNAME, dan DB_PASSWORD hanya dapat diakses di dalam kelas pemesananDatabase, sehingga informasi sensitif seperti kredensial database terlindungi dari akses langsung oleh kelas lain. Sementara itu, penggunaan keyword final static memastikan bahwa nilai setiap variabel bersifat konstan dan tidak dapat diubah selama program berjalan.

## Class produkDatabase
<img width="561" height="180" alt="image" src="https://github.com/user-attachments/assets/fe67a5fa-c6be-4b90-bb0f-e76172691e4a" />

Deklarasi variabel pada kelas produkDatabase menggunakan modifier private dan keyword final static merupakan bentuk penerapan prinsip Encapsulation untuk melindungi data konfigurasi database. Modifier private memastikan bahwa variabel seperti DB_HOST, DB_PORT, DB_NAME, DB_USERNAME, dan DB_PASSWORD hanya dapat diakses di dalam kelas produkDatabase, sehingga data sensitif tidak dapat dimodifikasi secara langsung oleh kelas lain. Sementara itu, penggunaan keyword final static menjamin bahwa nilai variabel bersifat konstan dan tetap selama program berjalan.

## Class SuperUser
<img width="293" height="208" alt="image" src="https://github.com/user-attachments/assets/4d537a49-a4f7-4d0e-9f77-ce1c6e5d2e06" />

Deklarasi atribut pada kelas SuperUser menggunakan modifier private menunjukkan penerapan prinsip Encapsulation dalam pemrograman berorientasi objek. Dengan menjadikan atribut seperti id_user, password, username, email, no_telp, alamat, nama, dan role bersifat private, data tersebut hanya dapat diakses dan dimodifikasi melalui method getter dan setter yang disediakan di dalam kelas.

## Class client
<img width="314" height="74" alt="image" src="https://github.com/user-attachments/assets/71241589-f1a0-47e1-b930-aeb74bbe0c71" />

<img width="999" height="184" alt="image" src="https://github.com/user-attachments/assets/cbdfc35a-05d6-45ab-83f3-5f1ed773c1e4" />

Kode ini merupakan penerapan prinsip Encapsulation dalam pemrograman berorientasi objek dengan melindungi atribut jumlah_nota, jumlah_pemesanan, dan e_money menggunakan modifier private. Artinya, ketiga variabel tersebut tidak dapat diakses atau dimodifikasi langsung dari luar kelas. Sebagai gantinya, akses terhadap nilai variabel dilakukan melalui getter dan setter seperti getJumlah_nota(), setJumlah_nota(), getJumlah_pemesanan(), setJumlah_pemesanan(), getE_money(), dan setE_money().

## Class staff
<img width="379" height="44" alt="image" src="https://github.com/user-attachments/assets/a7b01fc1-2a2f-4fd8-b716-98248984735b" />

Bagian ini menerapkan Encapsulation, atribut jabatan dibuat private dan hanya bisa diakses lewat method getter & setter. Tujuannya untuk melindungi data, mengontrol cara data diakses dan diubah

## Class adminDatabase
<img width="556" height="187" alt="image" src="https://github.com/user-attachments/assets/7cf17428-f26c-4dce-96a1-8f3fa31918ad" />

Variabel dibuat private, hanya bisa diakses class ini. Gunanya melindungi data konfigurasi database agar tidak bisa diubah sembarangan dari luar class, menjaga keamanan & konsistensi.

## Class clientDatabase
<img width="571" height="184" alt="image" src="https://github.com/user-attachments/assets/b575ad9c-9b92-45e5-b9a9-c645e6807b9e" />

Variabel dibuat private static final, hanya bisa diakses dari class ini. Gunanya menjaga agar informasi koneksi database tidak bisa diubah sembarangan dari luar class dan menjaga konsistensi.

## Class staffDatabase
<img width="570" height="184" alt="image" src="https://github.com/user-attachments/assets/717061df-7dd3-428c-9284-dfed2a81e944" />

Semua variabel dibuat private static final, artinya hanya bisa diakses di class ini dan tidak bisa diubah setelah didefinisikan, gunanya melindungi data sensitif seperti username & password database, serta menjaga keseragaman konfigurasi.

## Class RoundedPanel
<img width="432" height="55" alt="image" src="https://github.com/user-attachments/assets/2636f099-bf81-4999-ab9c-0a3dd840cfb5" />

Variabel cornerRadius:

private → hanya bisa diakses dalam class ini

final → nilainya tidak bisa diganti

Gunanya:
Menjaga nilai radius sudut tetap konsisten dan tidak diubah dari luar class.

## 2. Interface

Interface dalam pemrograman, khususnya dalam OOP (Object-Oriented Programming), adalah sebuah template atau kontrak yang hanya berisi deklarasi method (tanpa implementasi), dan class lain wajib mengisi / mengimplementasikan method-method tersebut.

## CRUDClient
<img width="398" height="189" alt="image" src="https://github.com/user-attachments/assets/38fae60b-d969-4ad9-8dc1-03f3ad3e74d9" />

<img width="548" height="40" alt="image" src="https://github.com/user-attachments/assets/ae0d9771-d48f-4d05-8f25-32f4bcefe49e" />

Interface ini berfungsi sebagai kontrak yang menentukan bahwa setiap class yang mengimplementasikannya harus menyediakan implementasi untuk method createClient(), readClient(), updateClient(int id), dan deleteClient(int id). Dengan cara ini, program menjadi lebih terstruktur, karena interface memastikan bahwa pengelolaan data client memiliki standard fungsi yang konsisten, lalu diterapkan pada class clientController.

## CRUDStaff
<img width="393" height="186" alt="image" src="https://github.com/user-attachments/assets/ad733a63-636f-483a-94f1-cc5abb8e0231" />

<img width="569" height="40" alt="image" src="https://github.com/user-attachments/assets/b4a8a556-cece-4c33-b31a-e571fe678a72" />

Interface CrudStaff pada kode tersebut berfungsi sebagai template atau kontrak untuk operasi CRUD (Create, Read, Update, Delete) khusus pada data staff. Di dalamnya hanya terdapat deklarasi method seperti createStaff(), readStaff(), updateStaff(int id), dan deleteStaff(int id), tanpa detail implementasi. Artinya, setiap class yang mengimplementasikan interface ini wajib menyediakan logika lengkap untuk masing-masing method tersebut, lalu CRUDStaff diterapkan pada class staffController.

## ReadAdmin
<img width="300" height="129" alt="image" src="https://github.com/user-attachments/assets/b3a51f57-2e5e-45b9-b656-26f0d04a5091" />

<img width="558" height="43" alt="image" src="https://github.com/user-attachments/assets/2b35a5c2-0b64-473b-b84f-96678dbacf10" />

Interface ini digunakan untuk memastikan bahwa setiap class yang mengimplementasikannya wajib menyediakan implementasi fungsi untuk membaca atau menampilkan data admin. Tujuannya adalah menjaga konsistensi struktur program, memisahkan definisi dari implementasi, lalu read admin diimplementasikan di class adminController.

## CRUDNota
<img width="384" height="184" alt="image" src="https://github.com/user-attachments/assets/9355635f-804d-439d-806e-0301baf71f39" />

<img width="503" height="38" alt="image" src="https://github.com/user-attachments/assets/222036c2-caf7-4ca4-b158-ca99e01ad83c" />

Interface ini hanya berisi deklarasi method seperti createNota(), readNota(), updateNota(int id), dan deleteNota(int id) tanpa memberikan detail prosesnya. Dengan adanya interface ini, setiap class yang mengimplementasikannya harus menyediakan logika dan cara kerja lengkap untuk masing-masing method, sehingga sistem tetap konsisten, dan mudah dikembangkan. Lalu Interface diimplementasikan di class notaController

## CRUDPelaporan
<img width="416" height="187" alt="image" src="https://github.com/user-attachments/assets/1797960e-dc69-4540-9373-9ea04f6b9d0d" />

<img width="615" height="33" alt="image" src="https://github.com/user-attachments/assets/ecda3c34-3e7f-4869-b7ae-7bae24e58284" />

Di interface ini terdapat deklarasi method seperti createPelaporan(), readPelaporan(), updatePelaporan(int id), dan deletePelaporan(int id), tanpa implementasi langsung. Dengan menggunakan interface ini, setiap class yang mengimplementasikannya diwajibkan menyediakan logika lengkap untuk setiap fungsi tersebut, sehingga pengelolaan data pelaporan tetap konsisten,dan lebih mudah dipelihara. Lalu interface diimplementasikan dalam class pelaporanController.

## CRUDPemesanan
<img width="432" height="180" alt="image" src="https://github.com/user-attachments/assets/bc45bd24-6f0a-43aa-a656-f7a4c676be42" />

<img width="624" height="38" alt="image" src="https://github.com/user-attachments/assets/0df220f4-9d5e-422d-b0c2-b8cfe91b5ab1" />

Interface ini mendefinisikan beberapa method seperti createPemesanan(), readPemesanan(), updateStatusPemesanan(), dan deletePemesanan(int id), tanpa memberikan implementasi langsung. Dengan adanya interface ini, setiap class yang mengimplementasikannya wajib menyediakan logika fungsi sesuai deklarasi tersebut, sehingga pengelolaan data pemesanan menjadi konsisten, terstruktur, dan mudah dipelihara. Lalu interface diimplementasikan dalam class pemesananController.

## CRUDProduk
<img width="389" height="184" alt="image" src="https://github.com/user-attachments/assets/f1d71cd2-eab2-42a9-8f8c-305e7fe16766" />

<img width="550" height="34" alt="image" src="https://github.com/user-attachments/assets/35231213-6e1e-4de4-aef1-e455409d2d31" />

Di interface ini terdapat deklarasi method seperti createProduk(), readProduk(), updateProduk(int id), dan deleteProduk(int id), tanpa implementasi langsung. Dengan pendekatan ini, setiap class yang mengimplementasikan interface tersebut harus menyediakan logika lengkap untuk masing-masing method, sehingga proses pengelolaan data produk menjadi konsisten dan terstruktur. Lalu interface diimplementasikan dalam class produkController.

## 3. Polymorphism
Polymorphism adalah konsep dalam OOP yang memungkinkan satu fungsi atau method memiliki perilaku berbeda tergantung objek yang menggunakannya. Dengan polymorphism, method yang sama bisa dijalankan oleh banyak class, tetapi setiap class dapat memberikan cara kerja yang berbeda sesuai kebutuhannya.

## -overriding
Overriding adalah salah satu bentuk polymorphism, yaitu ketika sebuah class menuliskan ulang method yang sudah didefinisikan di superclass atau interface, lalu memberikan implementasi yang berbeda. Jadi overriding memastikan method yang sama memiliki fungsi yang disesuaikan oleh class masing-masing.

## Class notaController
<img width="277" height="49" alt="image" src="https://github.com/user-attachments/assets/e2a6a58e-6385-492e-b19a-349b834455f9" />
<img width="334" height="46" alt="image" src="https://github.com/user-attachments/assets/aaa7f923-29f0-4aaf-9df5-5d7a671d9ce5" />
<img width="350" height="52" alt="image" src="https://github.com/user-attachments/assets/aaa3202e-35ea-458f-8c7e-7dffae2d815d" />
<img width="344" height="49" alt="image" src="https://github.com/user-attachments/assets/18d26929-daad-4dd6-a4e4-7a88e5d87bd0" />

Pada bagian nota, method createNota(), readNota(), updateNota(int id), dan deleteNota(int id) merupakan implementasi dari interface CrudNota, sehingga class notaController wajib mendefinisikan perilaku masing-masing method. Method createNota() digunakan untuk menambahkan data nota baru ke database sekaligus mengambil ID nota yang di-generate secara otomatis. readNota() berfungsi menampilkan seluruh data nota, updateNota(int id) digunakan untuk memperbarui informasi nota berdasarkan ID tertentu, dan deleteNota(int id) menghapus data nota sesuai ID nota yang diberikan. Penggunaan anotasi @Override menandakan bahwa method-method ini adalah hasil overriding dari interface

## Class pelaporanController
<img width="654" height="70" alt="image" src="https://github.com/user-attachments/assets/3fedc825-c10b-470b-932d-6c4196d0156f" />
<img width="455" height="69" alt="image" src="https://github.com/user-attachments/assets/73071a7c-47b9-41ac-a3af-33e98c8f4e42" />
<img width="390" height="53" alt="image" src="https://github.com/user-attachments/assets/bbf30376-1e57-4628-bf8a-da1b36b0d9f5" />
<img width="391" height="52" alt="image" src="https://github.com/user-attachments/assets/b33dc744-8c5e-4bc5-b185-a0b1e2c15671" />

Pada bagian pelaporan, method CRUD seperti createPelaporan(), readPelaporan(), updatePelaporan(), dan deletePelaporan(int id) merupakan implementasi dari interface yang telah ditentukan sehingga controller pelaporan wajib mengisi logikanya. Method createPelaporan() digunakan untuk memasukkan data pelaporan baru ke database, readPelaporan() berfungsi menampilkan seluruh data pelaporan, updatePelaporan() dipakai untuk memperbarui informasi pelaporan berdasarkan ID, dan deletePelaporan(int id) digunakan untuk menghapus data pelaporan dengan parameter ID tertentu. Penggunaan anotasi @Override menandakan bahwa method-method ini adalah bentuk overriding dari interface.

## Class pemesananController
<img width="329" height="50" alt="image" src="https://github.com/user-attachments/assets/13057f10-ff8e-4502-90d6-8f0b7f2b88a5" />
<img width="321" height="44" alt="image" src="https://github.com/user-attachments/assets/60b3aad2-d9ba-4ab2-b318-c40c316db573" />
<img width="382" height="52" alt="image" src="https://github.com/user-attachments/assets/dc2a0686-1161-4c90-a60f-7ad59f403378" />
<img width="388" height="51" alt="image" src="https://github.com/user-attachments/assets/aab9e97e-310e-4a48-84da-045a8cbd858f" />

Pada bagian pemesanan, method seperti createPemesanan(), readPemesanan(), updateStatusPemesanan(), dan deletePemesanan(int id) merupakan implementasi dari interface CrudPemesanan, sehingga controller pemesanan wajib menyediakan logika lengkap untuk setiap proses CRUD. Method createPemesanan() digunakan untuk menambahkan data pemesanan baru ke database, readPemesanan() menampilkan daftar pemesanan, updateStatusPemesanan() berfungsi memperbarui status pemesanan (misalnya dari pending menjadi selesai), dan deletePemesanan(int id) menghapus data pemesanan berdasarkan ID tertentu. Anotasi @Override menunjukkan bahwa method-method ini adalah hasil overriding dari interface

## Class produkController
<img width="309" height="53" alt="image" src="https://github.com/user-attachments/assets/d547484c-fa93-4bbf-a6d7-8f891a89bf8a" />
<img width="269" height="50" alt="image" src="https://github.com/user-attachments/assets/cefa1192-9fb1-4846-8c59-ff656162d524" />
<img width="349" height="49" alt="image" src="https://github.com/user-attachments/assets/44bd2d4c-b6c4-4821-b592-a5e441f22c8e" />
<img width="350" height="48" alt="image" src="https://github.com/user-attachments/assets/0c222186-444b-4627-a70c-e9c196e8553b" />

Pada bagian produk, setiap method CRUD (createProduk(), readProduk(), updateProduk(), dan deleteProduk(int id)) merupakan hasil override dari interface sehingga controller produk wajib menyediakan implementasinya. Method createProduk() berfungsi untuk menambah data produk baru ke database, readProduk() untuk menampilkan seluruh data produk, updateProduk() untuk memperbarui informasi produk berdasarkan ID, dan deleteProduk(int id) digunakan untuk menghapus data produk dari database menggunakan parameter ID. Penggunaan anotasi @Override menunjukkan bahwa method-method ini adalah implementasi spesifik dari kontrak interface

## Class adminController
<img width="270" height="66" alt="image" src="https://github.com/user-attachments/assets/36b99dbb-e278-496c-8f69-33ee51ceff1b" />

Pada method readAdmin(), terjadi proses overriding dari interface yang mewajibkan class controller untuk menyediakan implementasi fungsi pembacaan data admin. Fungsi ini digunakan untuk mengambil dan menampilkan seluruh data admin dari database melalui query SELECT, sehingga data admin dapat dilihat atau ditampilkan dalam aplikasi. Penggunaan anotasi @Override menunjukkan bahwa method ini merupakan bentuk penerapan polymorphism.

## Class clientController
<img width="299" height="51" alt="image" src="https://github.com/user-attachments/assets/4ae36be7-f228-4cdb-9d36-bc8adf4e6650" />
<img width="271" height="52" alt="image" src="https://github.com/user-attachments/assets/ce19e758-088e-4dd2-9847-0d811cb28033" />
<img width="354" height="53" alt="image" src="https://github.com/user-attachments/assets/dbbc172f-92a9-4f18-b5e6-10d34a0046f3" />
<img width="356" height="51" alt="image" src="https://github.com/user-attachments/assets/177f93b0-f7e0-4183-855d-a57dfc7f3846" />

Pada fitur CRUD Client, setiap method seperti createClient(), readClient(), updateClient(int id), dan deleteClient(int id) merupakan bentuk polymorphism melalui method overriding. Seluruh fungsi tersebut berasal dari interface yang sudah kamu definisikan, lalu di-override dalam class controller agar memiliki implementasi khusus untuk data Client. createClient() digunakan untuk menambahkan data client baru ke database, readClient() menampilkan seluruh data client, updateClient(int id) memperbarui data client berdasarkan ID tertentu, dan deleteClient(int id) menghapus data client sesuai ID yang diterima. Dengan adanya @Override pada tiap method, sistem memastikan bahwa fungsi-fungsi ini berjalan sesuai kontrak interface.

## Class staffController
<img width="304" height="48" alt="image" src="https://github.com/user-attachments/assets/43766b72-c466-47ae-9b99-c01288e891b5" />
<img width="262" height="54" alt="image" src="https://github.com/user-attachments/assets/0f57ff62-a2d5-472a-9c0b-5817311ad5bc" />
<img width="341" height="52" alt="image" src="https://github.com/user-attachments/assets/e21b25c9-17f8-4ffc-8cc9-0166b181d01a" />
<img width="358" height="49" alt="image" src="https://github.com/user-attachments/assets/aa2c95a6-ca28-42f3-b08c-6ecb68065f52" />

Pada fitur CRUD Staff, method seperti createStaff(), readStaff(), updateStaff(int id), dan deleteStaff(int id) merupakan penerapan polymorphism melalui method overriding dari interface CrudStaff. Setiap method di-override dalam class controller untuk memberi logika spesifik sesuai proses pengelolaan data staff. Method createStaff() berfungsi untuk menambahkan data staff baru ke database, readStaff() membaca dan menampilkan seluruh data staff, updateStaff(int id) digunakan untuk mengubah data staff berdasarkan ID yang dipilih, dan deleteStaff(int id) menghapus data staff tertentu sesuai dengan ID yang diberikan. Adanya anotasi @Override memastikan bahwa class ini mengikuti kontrak interface dan mengimplementasikan fungsi CRUD sesuai kebutuhan tabel staff.

## Class NotaHelper
<img width="628" height="241" alt="image" src="https://github.com/user-attachments/assets/2563a2af-025c-4e27-9070-e967eb98f836" />

Method printNota() dioverride untuk mengisi logika mencetak nota berdasarkan ID, sementara hitungTotal() juga dioverride untuk memberikan perhitungan total harga dasar (harga × jumlah barang). Dengan overriding, subclass NotaHelper memberikan implementasi nyata dari method yang sebelumnya hanya dideklarasikan abstrak, sehingga fungsi pencetakan dan perhitungan nota bisa berjalan sesuai kebutuhan program.

## 4. Abstraction
Abstraction pada pilar OOP adalah konsep menyembunyikan detail kompleks dari sebuah proses dan hanya menampilkan bagian penting yang diperlukan oleh pengguna. Tujuannya agar program lebih mudah dipahami, dikelola, dan digunakan tanpa harus mengetahui cara kerja internalnya secara rinci.

<img width="362" height="430" alt="image" src="https://github.com/user-attachments/assets/384dd960-fa0c-43e2-bf07-322bc061af1c" />

Class SuperUser dideklarasikan sebagai abstract, artinya class ini berfungsi sebagai kerangka dasar yang tidak dapat dibuat objeknya secara langsung, tetapi hanya dapat diwarisi oleh class lain seperti client, admin, atau staff. Dengan abstraction, hanya informasi penting yang ditampilkan (misalnya struktur umum data user seperti id_user, username, email, alamat, dan role), sementara detail implementasi dan perilaku spesifik dibiarkan untuk class turunannya.

## 5. Inheritance
Inheritance adalah salah satu konsep utama dalam OOP yang memungkinkan sebuah class untuk mewarisi atribut dan method dari class lain. Class yang mewarisi disebut child class, sedangkan class yang diwarisi disebut parent class.

<img width="414" height="73" alt="image" src="https://github.com/user-attachments/assets/a004d222-8c5c-4a2a-b619-81ffce08577f" />

Public class client extends SuperUser menunjukkan bahwa class client merupakan turunan dari class SuperUser. Ini adalah penerapan konsep inheritance dalam OOP, di mana client mewarisi seluruh atribut dan method yang dimiliki SuperUser, seperti nama, email, password, dan informasi user lainnya. Dengan pewarisan ini, kode menjadi lebih efisien karena tidak perlu menulis ulang properti umum pengguna, serta memudahkan pengembangan sistem ketika nanti ada jenis user lain seperti admin atau staff yang juga dapat mewarisi struktur yang sama.
## C. Struktur Package
<img width="592" height="841" alt="image" src="https://github.com/user-attachments/assets/d9fdcc9a-2a3f-4a54-9321-8caca3a217bb" />
<img width="591" height="798" alt="image" src="https://github.com/user-attachments/assets/34c2e91b-1e47-4152-a00a-a654c5753ab1" />
<img width="581" height="204" alt="image" src="https://github.com/user-attachments/assets/655b63c8-94e2-4141-a562-1cae08fd11ee" />

Package Model berisi class data, abstract class, interface, dan akses ke database, sementara package Controller berisi logika proses baik untuk fitur utama maupun user management. Bagian tampilan GUI ditempatkan pada package capstone, serta terdapat tambahan folder pendukung seperti music dan icon untuk media aplikasi. Pemisahan struktur ini membantu program lebih mudah dikelola, dipahami, dan dikembangkan.

## D. Library/framework

## Penerapan MVC
<img width="592" height="841" alt="image" src="https://github.com/user-attachments/assets/d9fdcc9a-2a3f-4a54-9321-8caca3a217bb" />
<img width="591" height="798" alt="image" src="https://github.com/user-attachments/assets/34c2e91b-1e47-4152-a00a-a654c5753ab1" />
<img width="581" height="204" alt="image" src="https://github.com/user-attachments/assets/655b63c8-94e2-4141-a562-1cae08fd11ee" />

Program ini menerapkan konsep MVC (Model-View-Controller) dengan jelas. Model menangani struktur data dan koneksi database, View menangani tampilan aplikasi melalui form Swing, dan Controller menjadi penghubung yang menerima input dari View, memproses logika, lalu berkomunikasi dengan Model untuk mengolah data. Dengan arsitektur MVC ini, program menjadi lebih terstruktur, serta memudahkan maintenance dan pengembangan fitur baru tanpa mengganggu komponen lain.

## E. Cara Menggunakan
<img width="1247" height="863" alt="image" src="https://github.com/user-attachments/assets/89ffda97-19c8-4bd6-9898-15974e736fc5" />

Pada saat aplikasi dijalankan, pengguna akan disambut dengan halaman awal EnergiSync yang menampilkan logo, nama aplikasi. Halaman ini berfungsi sebagai tampilan pembuka sebelum masuk ke sistem, untuk mulai menggunakan aplikasi, pengguna cukup menekan tombol Start, kemudian aplikasi akan mengarahkan ke halaman login untuk proses autentikasi sebelum mengakses fitur utama.

<img width="1248" height="820" alt="image" src="https://github.com/user-attachments/assets/f5a6ed46-5f79-47e2-8089-8084c9e950c0" />

Setelah menekan tombol start, pengguna akan masuk ke halaman Login, pengguna diminta untuk memasukkan akun yang telah terdaftar sebelum dapat mengakses sistem. Tersedia kolom untuk mengisi username dan password, serta tombol Login untuk melanjutkan proses autentikasi. Jika pengguna belum memiliki akun, tersedia opsi Sign Up untuk melakukan registrasi terlebih dahulu.

<img width="1271" height="959" alt="image" src="https://github.com/user-attachments/assets/ab0527c4-e4c9-4cee-b60e-2d3702af0a56" />

Pada halaman Sign Up, pengguna dapat melakukan pendaftaran akun baru untuk mengakses aplikasi. Pengguna diminta mengisi data diri seperti nama, username, email, nomor telepon, alamat, dan password pada form yang telah disediakan. Setelah semua informasi terisi dengan benar, tekan tombol Register untuk menyimpan data dan membuat akun baru. Jika pengguna sudah memiliki akun sebelumnya, tersedia tombol Sign In untuk kembali ke halaman login.

## Dashboard Client
<img width="1727" height="1018" alt="image" src="https://github.com/user-attachments/assets/7b5001f2-6c44-461f-a6c1-ebbf7fecc59f" />

Jika memilih menu client maka akan masuk ke dashboard client, dashboard client ada fitur sistem pemesanan bahan bakar. Di bagian kiri terdapat panel navigasi yang berisi menu Dashboard, Pemesanan, Nota, Top Up, serta tombol Logout. Pada bagian atas halaman ditampilkan informasi pengguna seperti username dan ID user sebagai identitas akun yang sedang login. Bagian tengah menampilkan daftar produk bahan bakar dalam bentuk kartu yang berisi nama produk, deskripsi singkat, stok yang tersedia, serta harga per liter. Di bawahnya terdapat tabel pemesanan yang nantinya menampilkan riwayat transaksi pengguna, seperti ID pemesanan, jumlah produk, tanggal, status, dan total harga. Secara keseluruhan, halaman ini sudah berfungsi sebagai pusat informasi bagi user untuk melihat produk, memantau pesanan, dan mengakses fitur lainnya dalam aplikasi.
<img width="1733" height="1022" alt="image" src="https://github.com/user-attachments/assets/5712f632-e896-41ef-a5b2-939b7cf048ff" />

Jika memilih menu pemesanan maka akan masuk ke halaman yang digunakan oleh client untuk melakukan pembelian produk BBM. Client mengisi nama, memilih jenis produk, dan menentukan jumlah liter yang ingin dipesan. Sistem akan otomatis menampilkan harga produk serta menghitung total biaya berdasarkan pilihan jumlah dan jenis produk. Selain itu, halaman ini juga menampilkan saldo pelanggan, sehingga user dapat memastikan saldo mencukupi sebelum melakukan pemesanan.
<img width="1728" height="1020" alt="image" src="https://github.com/user-attachments/assets/af9adad8-0dbe-4dc3-af23-f42e8616ad86" />

Jika memilih menu nota, maka akan masuk ke halaman nota yang berfungsi sebagai tempat bagi client untuk melihat ringkasan pemesanan yang telah selesai diproses.
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/57a893d9-a11f-4940-96f5-ddc4209ef5a9" />

## Dashboard Staff
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/02eb4a56-0428-4b06-8388-a1d3055cde14" />

Jika login sebagai staff maka akan masuk ke dashboard staff yang berfungsi sebagai pusat kendali bagi staf untuk memantau aktivitas operasional. Setelah staf berhasil login, sistem menampilkan informasi akun staf, daftar produk beserta stok dan harga, serta rangkuman aktivitas terbaru. Di bagian atas, staf dapat melihat tiga jenis produk BBM lengkap dengan ketersediaan dan harga untuk memudahkan pengecekan sebelum memproses pemesanan. Bagian tengah menampilkan ringkasan pemesanan dan pelaporan, termasuk status apakah masih menunggu, disetujui, atau ditolak. Selain itu, terdapat tabel nota dan pelaporan yang telah disetujui sebagai hasil akhir transaksi. Menu di sisi kiri memudahkan staf berpindah ke halaman pemesanan, pelaporan, nota, dan informasi lainnya.
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/14884a23-5057-45f3-a2eb-9db1c5264bf7" />

Jika memilih menu pemesanan maka akan masuk ke dashboard pemesanan yang berfungsi untuk mengelola data pemesanan produk BBM dari para user. Pada halaman ini ditampilkan seluruh daftar pemesanan beserta detailnya, seperti jumlah produk, tanggal pemesanan, status, produk yang dipesan, total harga, dan ID user. Staff dapat melakukan filter berdasarkan status pemesanan (misalnya disetujui atau menunggu) untuk memudahkan pengecekan pesanan sesuai tahap proses. Selain itu, tersedia fitur Edit/Delete berdasarkan ID pemesanan untuk memperbarui atau menghapus data pemesanan tertentu. Tombol Filter Menunggu digunakan untuk menampilkan hanya pesanan yang belum diproses, sedangkan tombol Non Filter akan menampilkan seluruh data kembali.
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/44fcc3ba-62f6-42eb-8b7f-49cc514bb134" />

Jika memilih menu pelaporan akan masuk ke dashbord pelaporan yang berfungsi untuk membuat, mengelola, dan memproses laporan atas pemesanan yang sudah dilakukan client. Pada bagian atas, staff dapat memasukkan ID Client dan ID Pemesanan untuk membuat laporan baru terkait transaksi tertentu, lalu menekan tombol New untuk menyimpan data pelaporan tersebut. Di bagian kiri ditampilkan tabel daftar pemesanan yang sudah disetujui sebagai referensi, sehingga staff dapat memilih pemesanan mana yang perlu dibuatkan laporan. Sementara itu, tabel di sebelah kanan menampilkan daftar pelaporan beserta statusnya, apakah masih menunggu, disetujui, atau ditolak. Staff juga dapat menghapus data pelaporan tertentu melalui kolom edit/delete (id) dan tombol Delete.
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/3eefe063-d382-4a68-b33c-fc5a5aa40454" />

Jika memilih menu nota akan masuk ke halaman nota yang digunakan untuk menghasilkan dan mengelola bukti transaksi akhir setelah pelaporan disetujui. Pada bagian atas, staf dapat memasukkan ID Pelaporan yang telah disetujui untuk dibuatkan nota, kemudian mengisi Total Harga, Pembayaran, dan ID User terkait transaksi tersebut. Tombol New berfungsi untuk membuat nota baru, sementara Edit digunakan untuk memperbarui data nota yang sudah ada, dan Delete untuk menghapusnya berdasarkan ID. Untuk memudahkan pengecekan data, halaman ini juga menampilkan tiga tabel sekaligus: daftar pemesanan yang sudah disetujui, daftar pelaporan yang sudah diproses, serta daftar nota yang telah dibuat.
<img width="1734" height="1080" alt="image" src="https://github.com/user-attachments/assets/030dcd57-d611-4524-88a1-9da9cea5d321" />

Jika memilih menu nota maka akan masuk ke halaman Pelaporan yang Disetujui menampilkan daftar khusus laporan yang telah melalui proses penilaian dan dinyatakan disetujui. Data yang ditampilkan meliputi ID Pelaporan, status pelaporan, tanggal pelaporan, ID Pemesanan, dan ID User. Halaman ini berfungsi sebagai referensi bagi staf untuk memantau laporan mana saja yang sudah selesai diproses dan siap dilanjutkan ke tahap berikutnya

## Dashboard Admin
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/fbd48a3d-c958-449d-a82e-d2ecd2fbaef9" />

Jika login sebagai admin akan masuk ke bagian utama dashboard admin ini, dashboard menampilkan kartu ringkasan produk yang menunjukkan jenis bahan bakar (seperti VLSFO, Biosolar, dan HSFO) lengkap dengan deskripsi singkat, jumlah stok yang tersedia, dan harga per liter. Di bawahnya, terdapat beberapa tabel kecil dengan judul Informasi Pelaporan, Nota, Pelaporan, dan Staff, yang menyajikan data terbaru secara ringkas untuk memantau aktivitas sistem secara real-time. Setiap tabel juga dilengkapi tombol “View All” untuk melihat detail data secara lengkap. Secara keseluruhan, halaman ini berfungsi sebagai pusat kontrol yang memudahkan admin memantau stok produk, pelaporan, transaksi nota, serta data user dalam satu tempat dengan tampilan ringkas dan informatif.
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/9ada59bc-867e-435d-893c-1fdaba7cda14" />

Jika memilih menu produk maka akan masuk ke halaman menu produk dalam aplikasi admin yang digunakan untuk mengelola data produk bahan bakar. Pada bagian utama, terdapat form input yang memungkinkan admin memasukkan atau mengubah informasi produk, seperti Nama Produk, Harga per kg, Deskripsi, dan Stok. Terdapat juga kolom untuk Edit/Delete berdasarkan ID sehingga data dapat dimodifikasi secara spesifik. Tombol New, Edit, dan Delete disediakan sebagai fungsi CRUD untuk menambah, memperbarui, dan menghapus produk. Di bawahnya, terdapat tabel yang menampilkan daftar produk beserta detailnya, sehingga admin dapat melihat data stok dan harga secara langsung.
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/f29e4e8e-0791-460d-a9a9-ccddeba6f9c6" />

Jika memilih menu pelaporamn maka akan masuk ke halaman pelaporan pada aplikasi yang digunakan admin untuk mengelola data laporan hasil pemesanan. Pada bagian utama, tersedia form input dengan field seperti Status Pelaporan, Tanggal Pelaporan, ID Pemesanan, dan ID User, serta kolom Edit/Delete menggunakan ID, yang memudahkan admin untuk memasukkan atau mengubah data laporan. Terdapat tombol New, Edit, Delete, dan tombol khusus Filter Hanya Menunggu untuk menampilkan laporan yang masih dalam status “menunggu”. Di bagian bawah, ditampilkan dua tabel: tabel Pemesanan untuk melihat detail pesanan, dan tabel Pelaporan untuk melihat daftar laporan yang sudah dibuat.
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/5942ea64-52b1-49b7-9d30-46f21913e324" />

Jika memilih menu nota maka akan masuk ke halaman nota pada yang digunakan untuk mengelola data nota pembayaran. Pada bagian utama, terdapat form input yang berisi field seperti ID Pelaporan, Total Harga, ID untuk Edit/Delete, Pembayaran, dan ID User. Admin dapat melakukan aksi New untuk membuat nota baru, Edit untuk memperbarui data nota berdasarkan ID, dan Delete untuk menghapus nota tertentu. Di bagian bawah tersedia tiga tabel berurutan: tabel Pemesanan, tabel Pelaporan, dan tabel Nota, yang menampilkan riwayat dan hubungan data antar modul, sehingga admin dapat melihat detail transaksi mulai dari pesanan, laporan, hingga nota akhir.
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/c68a713b-f7f9-40ca-8d33-1110c49a54d0" />

Jika memilih menu staff akan ada menu staff yang tersedia kolom untuk memasukkan ID sebagai referensi saat melakukan edit atau delete data. Di bawah form terdapat tiga tombol tindakan yaitu New untuk menambah staff baru, Edit untuk mengubah data staff yang sudah ada, dan Delete untuk menghapus data staff berdasarkan ID. Pada bagian bawah halaman ditampilkan tabel yang memuat daftar staff lengkap dengan kolom ID User, Nama, Username, Email, Nomor Telepon, Alamat, Role, dan Jabatan, sehingga admin dapat melihat serta mengelola data staff dengan mudah.
<img width="1861" height="1080" alt="image" src="https://github.com/user-attachments/assets/7efc4005-ff1f-44af-baa0-2fb0a6368106" />

terakhir jika memilih menu admin ada sebuah tabel yang berisi daftar admin yang terdaftar dalam sistem. Informasi yang ditampilkan mencakup ID User, Nama, Username, Email, Nomor Telepon, Alamat, Role, serta Status Admin. Setiap admin ditampilkan dalam baris data, menunjukkan bahwa fitur read data dari database sudah berjalan dengan baik. Tampilan ini berfungsi sebagai pusat manajemen informasi administrator, sehingga admin dapat melihat seluruh data admin yang aktif dalam sistem.

<img width="1247" height="863" alt="image" src="https://github.com/user-attachments/assets/89ffda97-19c8-4bd6-9898-15974e736fc5" />

Jika memilih log out maka akan kembali ke menu awal yaitu home page.
