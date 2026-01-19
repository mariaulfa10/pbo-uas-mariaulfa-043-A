Judul :
SMARTKOS: Sistem Digital Pengelolaan Kos-Kosan Berbasis Object Oriented Programming (OOP)

 

Maria Ulfa (2400018043)


PROGRAM STUDI INFORMATIKA
FAKULTAS TEKNOLOGI INDUSTRI
UNIVERSITAS AHMAD DAHLAN
TAHUN 2026

a.	Identitas Proyek 
Judul Proyek : SMARTKOS: Sistem Digital Pengelolaan Kos-Kosan Berbasis Object Oriented Programming (OOP)
SMARTKOS: Sistem Digital Pengelolaan Kos-Kosan Berbasis Object Oriented Programming (OOP)
Link Github : Project PBO
Deskripsi Singkat : 
SMARTKOS merupakan aplikasi berbasis Object Oriented Programming (OOP) yang dirancang untuk membantu pemilik kos dalam mengelola data kamar, penghuni, tagihan, serta pembayaran secara terstruktur dan terkomputerisasi.
 



b.	Persoalan Bisnin dan Deskripsi Proyek 
Pemilik kos-kosan harus mengelola berbagai data penting seperti data kamar, data penghuni, tagihan bulanan, dan pembayaran. Selama ini, proses pencatatan masih dilakukan secara manual menggunakan buku atau catatan sederhana. Hal tersebut menimbulkan berbagai permasalahan, seperti data mudah hilang atau rusak, kesulitan dalam pencarian data, serta tidak terdokumentasinya riwayat pembayaran dengan baik. Oleh karena itu, dikembangkan aplikasi SMARTKOS sebagai sistem manajemen kos-kosan berbasis OOP yang mampu membantu pemilik kos dalam mengelola data secara efektif, efisien, dan terstruktur.
c.	Daftar Seluruh Spesifikasi Aplikasi 
Spesifikasi aplikasi SMARTKOS meliputi:
•	Bahasa pemrograman: Java
•	Paradigma: Object Oriented Programming (OOP)
•	Antarmuka: Graphical User Interface (GUI)
•	Fitur utama:
o	Pengelolaan data kamar
o	Pengelolaan data penghuni
o	Mengapus dan menambah calon penghuni kosan 
o	Informasi status kamar (jika penuh tidak bisa menginputkan penghuni lagi)
o	Pemilahan spesifikasi kamar (kosongan / isian )
•	Penyimpanan data: berbasis objek 




d.	Rancangan model Diagram UML 
Perancangan sistem menggunakan diagram UML untuk memodelkan struktur dan hubungan antar kelas. Diagram yang digunakan adalah Class Diagram, yang menggambarkan atribut dan method dari setiap kelas utama dalam sistem.
Kelas – kelas utama yang dirancang di antara lain :
•	Kelas Kamar 
•	Kelas Unitkamar
•	Kelas Penghuni
•	Kelas Booking 
•	Kelas pembayaran 
•	Kelas Kost











e.	Rancangan Antar Muka Berbasis GUI 
Aplikasi dirancang berbasis GUI agar mudah digunakan oleh pengguna. Desain tampilan dibuat sederhana. Rancangan GUI meliputi : 
1.	Bagian Input (Input Booking)
•	Nama Penghuni (TextField): Tempat pengguna mengetikkan nama calon penyewa.
•	Lama Sewa / bulan (TextField): Tempat memasukkan angka durasi sewa dalam satuan bulan.
•	Tipe Kamar (ComboBox/Dropdown): Pilihan kategori kamar (pada gambar terlihat pilihan "Kosongan"). Biasanya ini digunakan untuk menentukan harga atau fasilitas.
2. Panel Kontrol (Tombol Aksi)
Terdapat dua tombol utama di bagian tengah:
•	Tombol Booking: Digunakan untuk memproses input data ke dalam sistem/daftar.
•	Tombol Hapus Terpilih: Digunakan untuk menghapus data yang sudah ada di daftar jika terjadi kesalahan atau pembatalan.
3. Bagian Output (Display Data)
Bagian bawah dibagi menjadi dua area besar untuk menampilkan informasi secara real-time:
•	Daftar Penghuni (List/TextArea): Area di sebelah kiri yang kemungkinan akan menampilkan daftar nama-nama penghuni yang sudah berhasil di-booking.
•	Detail Booking (TextArea): Area di sebelah kanan yang berfungsi sebagai ringkasan atau rekapitulasi. Di sana sudah tersedia label statis:
o	Kamar Isian: Untuk merangkum jumlah atau daftar kamar tipe isian (furnished).
o	Kamar Kosongan: Untuk merangkum jumlah atau daftar kamar tipe kosong

f.	Skrip Program dan penjelasannya 
Aplikasi SMARTKOS dikembangkan menggunakan konsep OOP dengan beberapa kelas utama, yaitu : 
 
Class Kamar digunakan untuk merepresentasikan jenis kamar dalam kost, seperti kamar isian dan kamar kosongan. Class ini menyimpan informasi tipe kamar, harga sewa, serta daftar unit kamar yang tersedia. Selain itu, class ini memiliki fungsi untuk melakukan booking pada unit kamar yang masih kosong.






Class UnitKamar merepresentasikan satu unit kamar secara spesifik dengan kode kamar tertentu. Class ini menyimpan status apakah kamar sedang terisi atau tidak, serta data booking yang menempatinya. Class ini bertanggung jawab untuk menambah dan menghapus booking pada unit kamar





Class Booking merupakan abstract class yang digunakan sebagai kerangka dasar untuk semua jenis pemesanan kamar. Class ini menyimpan informasi umum booking seperti data penghuni, lama sewa, tipe kamar, dan harga per bulan. Selain itu, class ini menyediakan method untuk menghitung total biaya sewa dan method abstract yang harus diimplementasikan oleh class turunan sebagai bentuk penerapan konsep abstraksi dalam PBO.





Class Penghuni digunakan untuk menyimpan data penyewa kost. Class ini berisi informasi dasar berupa nama penghuni dan berfungsi sebagai representasi objek penghuni yang melakukan booking kamar.
 
Class Pembayaran digunakan untuk menangani proses perhitungan pembayaran sewa kamar. Class ini menghitung total pembayaran berdasarkan jumlah bulan sewa dan harga per bulan, sehingga memisahkan logika pembayaran dari proses booking utama.
 
Class Kost merepresentasikan sistem pengelolaan kost secara keseluruhan. Class ini menyimpan data kamar dan daftar penghuni yang tinggal di kost. Selain itu, class ini menyediakan method untuk menambahkan penghuni dan menampilkan data kost beserta daftar penghuninya.
 
Class BookingOnline merepresentasikan proses pemesanan kamar yang dilakukan secara online. Class ini menyimpan data penghuni, lama sewa, dan kamar yang dipilih, serta menyediakan method untuk menghitung total biaya berdasarkan lama sewa dan harga kamar. Class ini berperan sebagai penghubung antara data penghuni dan data kamar dalam satu transaksi booking.

g.	Penjelasan Screenshot Tampilan Aplikasi 
•	Form input data kamar dan penghuni 








•	Tampilan saat sudah menginput data penghuni 







•	Ada pesan reminder kalo kamar penuh 











•	Ada untuk mengahpus data calon penghuni juga misalnya dia tidak jadi booking 






h.	Penjelasan Screenshot Status Ungah di Github/Gitlab 
Proyek SMARTKOS telah berhasil diunggah ke GitHub/GitLab hingga tahap final. Repository berisi seluruh source code aplikasi, dokumentasi, dan commit terakhir sebagai bukti penyelesaian proyek.
 
i.	Analisis pengerjaan proyek 
•	Waktu pengerjaan 
Kami mengerjakan project ini kurang lebih sekitar 2 minngu sebelum di tenggat 
•	Ketercapaian spesifikasi 
Berdasarkan spesifikasi awal yang telah ditetapkan, sistem SMARTKOS telah berhasil memenuhi sebagian besar kebutuhan fungsional. Sistem mampu mengelola data kamar, penghuni, booking, secara terstruktur menggunakan pendekatan Object Oriented Programming (OOP).
•	Biaya yang di butuhkan 
Tidak ada 
•	Kendala 
Kendala nya yaitu penulisan program yang kadang suka eror 
Kesulitan dalam merancang struktur kelas dan hubungan antar objek agar sesuai dengan konsep OOP.
Tantangan dalam merancang ke dalam GUI yang sederhana namun aga sulit 
•	Tantangan masa depan 
ke depan, sistem SMARTKOS masih memiliki peluang pengembangan yang cukup besar. Tantangan utama adalah meningkatkan kompleksitas sistem agar lebih mendekati kebutuhan nyata, seperti penambahan fitur notifikasi pembayaran, pencatatan riwayat transaksi, serta keamanan data. Selain itu, sistem dapat dikembangkan menjadi berbasis web atau mobile agar lebih fleksibel dan mudah diakses. Pengembangan GUI yang lebih interaktif dan integrasi dengan database juga menjadi tantangan sekaligus peluang untuk meningkatkan kualitas sistem SMARTKOS di masa depan.


			
