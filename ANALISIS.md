# 📊 System Analysis (Minggu 2)

## 📌 Project Title  
academic-system  

## 👥 Prepared By  
siti ramadhon ainun 

## 📅 Periode  
23–29 April 2026  

## 📄 Kegiatan  
Analisis Kebutuhan Sistem  

---

<h1>SYSTEM ANALYSIS – PROJECT CARTER</h1>

<h2>1. Deskripsi Sistem</h2>
<p>
Project Carter adalah sistem informasi akademik berbasis web yang dirancang untuk membantu mahasiswa dalam mengelola berbagai aktivitas akademik dalam satu platform. Sistem ini mencakup fitur pengisian KRS, evaluasi dosen (EDOM), konsultasi bimbingan akademik, pengajuan revisi nilai, dan akses tagihan kuliah.
</p>

<h2>2. Latar Belakang</h2>
<p>
Dalam proses akademik di perguruan tinggi, masih banyak kegiatan yang dilakukan secara terpisah atau manual, seperti pengisian KRS, konsultasi dengan dosen, hingga pengajuan revisi nilai. Hal ini sering menyebabkan keterlambatan, kesalahan data, serta kurang efisiennya waktu.
Selain itu, mahasiswa juga kesulitan dalam mengakses informasi seperti tagihan kuliah dan hasil evaluasi dosen. Oleh karena itu, dibutuhkan sistem terintegrasi yang dapat mengelola seluruh proses akademik secara digital agar lebih efektif dan efisien.
</p>

<h2>3. Identifikasi Masalah</h2>
<ul>
<li>Pengisian KRS masih membingungkan dan rawan kesalahan</li>
<li>Evaluasi dosen belum terkelola dengan baik</li>
<li>Konsultasi akademik sulit dilakukan</li>
<li>Pengajuan revisi nilai tidak terstruktur</li>
<li>Informasi tagihan kuliah sulit diakses</li>
</ul>

<h2>4. Tujuan Sistem</h2>
<ul>
<li>Mempermudah mahasiswa dalam mengelola aktivitas akademik</li>
<li>Mengintegrasikan semua layanan akademik dalam satu sistem</li>
<li>Meningkatkan efisiensi dan akurasi data</li>
<li>Memberikan akses informasi yang cepat dan mudah</li>
</ul>

<h2>5. Solusi Sistem</h2>
<ul>
<li>KRS online</li>
<li>EDOM (evaluasi dosen)</li>
<li>Konsultasi bimbingan akademik</li>
<li>Pengajuan revisi nilai</li>
<li>Informasi tagihan kuliah</li>
</ul>

<h2>6. Analisis Kebutuhan Sistem</h2>

<h3>A. Kebutuhan Fungsional</h3>
<ul>
<li>Mahasiswa dapat login ke sistem</li>
<li>Mahasiswa dapat mengisi dan menyimpan KRS</li>
<li>Mahasiswa dapat mengisi EDOM</li>
<li>Mahasiswa dapat melakukan konsultasi akademik</li>
<li>Mahasiswa dapat mengajukan revisi nilai</li>
<li>Mahasiswa dapat melihat tagihan kuliah</li>
<li>Dosen dapat merespon konsultasi</li>
<li>Admin dapat mengelola seluruh data sistem</li>
</ul>

<h3>B. Kebutuhan Non-Fungsional</h3>
<ul>
<li>Sistem mudah digunakan (user friendly)</li>
<li>Sistem dapat diakses 24 jam</li>
<li>Keamanan data terjamin</li>
<li>Sistem memiliki performa yang cepat</li>
</ul>

<h2>7. Aktor Sistem</h2>
<ul>
<li>Mahasiswa : pengguna utama</li>
<li>Dosen : memberikan respon & evaluasi</li>
<li>Admin : mengelola sistem</li>
</ul>

<h2>8. Analisis Proses Sistem</h2>
<p>
1. KRS<br>
Mahasiswa login - memilih mata kuliah - sistem validasi - data disimpan<br><br>

2. EDOM<br>
Mahasiswa mengisi form evaluasi - sistem menyimpan hasil<br><br>

3. Konsultasi Akademik<br>
Mahasiswa mengirim pesan - dosen membalas - tersimpan di sistem<br><br>

4. Revisi Nilai<br>
Mahasiswa mengajukan revisi - dosen memproses - status diperbarui<br><br>

5. Tagihan Kuliah<br>
Mahasiswa membuka menu - sistem menampilkan tagihan
</p>

<h2>9. Kesimpulan</h2>
<p>
Project Carter merupakan solusi sistem informasi akademik yang terintegrasi untuk mempermudah proses administrasi dan aktivitas mahasiswa. Dengan sistem ini, diharapkan semua proses akademik menjadi lebih efisien, cepat, dan terstruktur.
</p>

<hr>

<h1>DATABASE SYSTEM – PROJECT CARTER</h1>

<h2>1. Deskripsi Database</h2>
<p>
Database Project Carter digunakan untuk menyimpan dan mengelola seluruh data akademik mahasiswa seperti KRS, EDOM, bimbingan akademik, revisi nilai, dan tagihan kuliah. Database ini dirancang menggunakan model relasional agar data saling terhubung dan terstruktur dengan baik.
</p>

<h2>2. Struktur Tabel</h2>

<h3>2.1 Tabel User</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_user</td><td>Int (Pk,Al)</td><td>Id_user</td></tr>
<tr><td>Nama</td><td>Varchar(100)</td><td>Nama</td></tr>
<tr><td>Email</td><td>Varchar(100)</td><td>Email</td></tr>
<tr><td>Password</td><td>Varchar(225)</td><td>Password</td></tr>
<tr><td>Role</td><td>Enum</td><td>Mahasiswa,Dosen,admin</td></tr>
</table>

<h3>2.2 Tabel Mahasiswa</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Nim</td><td>Varchar(15) (Pk)</td><td>Nim</td></tr>
<tr><td>Id_user</td><td>Int (Fk)</td><td>Relasi user</td></tr>
<tr><td>Jurusan</td><td>Varchar(100)</td><td>Jurusan</td></tr>
<tr><td>Angkatan</td><td>Int</td><td>Tahun masuk</td></tr>
</table>

<h3>2.3 Tabel Dosen</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Nidn</td><td>Varchar(15) (Pk)</td><td>ID Dosen</td></tr>
<tr><td>Id_user</td><td>Int (Fk)</td><td>Relasi ke user</td></tr>
<tr><td>Prodi</td><td>Varchar(100)</td><td>Program Studi</td></tr>
</table>

<h3>2.4 Tabel Mata Kuliah</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Kode_mk</td><td>Varchar(10)</td><td>Kode MK</td></tr>
<tr><td>Nama_mk</td><td>Varchar(100)</td><td>Nama Mata Kuliah</td></tr>
<tr><td>Sks</td><td>Int</td><td>Jumlah SKS</td></tr>
<tr><td>Nidn</td><td>Varchar(15)</td><td>Dosen Pengampu</td></tr>
</table>

<h3>2.5 Tabel KRS</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_krs</td><td>Int (Pk,Al)</td><td>Id KRS</td></tr>
<tr><td>Nim</td><td>Varchar(10) (Fk)</td><td>Mahasiswa</td></tr>
<tr><td>Kode_mk</td><td>Varchar(10) (Fk)</td><td>Mata Kuliah</td></tr>
<tr><td>Semester</td><td>Int</td><td>Semester</td></tr>
</table>

<h3>2.6 Tabel EDOM</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_edom</td><td>Int (Pk,Al)</td><td>Id</td></tr>
<tr><td>Nim</td><td>Varchar(15) (Fk)</td><td>Mahasiswa</td></tr>
<tr><td>Nidn</td><td>Varchar(15) (Fk)</td><td>Dosen</td></tr>
<tr><td>Nilai</td><td>Int</td><td>Nilai evaluasi</td></tr>
<tr><td>Komentar</td><td>Text</td><td>Saran</td></tr>
</table>

<h3>2.7 Tabel Bimbingan</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_bimbingan</td><td>Int (Pk,Al)</td><td>Id</td></tr>
<tr><td>Nim</td><td>Varchar(15) (Fk)</td><td>Mahasiswa</td></tr>
<tr><td>Nidn</td><td>Varchar(15) (Fk)</td><td>Dosen</td></tr>
<tr><td>Pesan</td><td>Text</td><td>Isi konsultasi</td></tr>
<tr><td>Tanggal</td><td>Date</td><td>Tanggal</td></tr>
</table>

<h3>2.8 Tabel Revisi Nilai</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_revisi</td><td>Int (Pk,Al)</td><td>Id</td></tr>
<tr><td>Nim</td><td>Varchar(15) (Fk)</td><td>Mahasiswa</td></tr>
<tr><td>Kode_mk</td><td>Varchar(15) (Fk)</td><td>Mata Kuliah</td></tr>
<tr><td>Alasan</td><td>Text</td><td>Alasan revisi</td></tr>
<tr><td>Status</td><td>Enum</td><td>Pending/disetujui/ditolak</td></tr>
</table>

<h3>2.9 Tabel Tagihan</h3>
<table>
<tr><th>Field</th><th>Tipe Data</th><th>Keterangan</th></tr>
<tr><td>Id_tagihan</td><td>Int (Pk,Al)</td><td>Id</td></tr>
<tr><td>Nim</td><td>Varchar(15) (Fk)</td><td>Mahasiswa</td></tr>
<tr><td>Jumlah</td><td>Decimal(10,2)</td><td>Total tagihan</td></tr>
<tr><td>Status</td><td>Enum</td><td>Lunas/belum</td></tr>
<tr><td>Tanggal</td><td>Date</td><td>Tanggal tagihan</td></tr>
</table>

<h2>3. Relasi Antar Tabel</h2>
<ul>
<li>Users : Mahasiswa (1:1)</li>
<li>Users : Dosen (1:1)</li>
<li>Mahasiswa : KRS (1:M)</li>
<li>Mahasiswa : EDOM (1:M)</li>
<li>Mahasiswa : Bimbingan (1:M)</li>
<li>Mahasiswa : Revisi Nilai (1:M)</li>
<li>Mahasiswa : Tagihan (1:M)</li>
<li>Dosen : Mata Kuliah (1:M)</li>
<li>Dosen : Bimbingan (1:M)</li>
</ul>

<h2>4. Kesimpulan</h2>
<p>
Database Project Carter dirancang untuk mendukung seluruh proses akademik dalam satu sistem terintegrasi. Dengan struktur tabel dan relasi yang jelas, data dapat dikelola dengan lebih efektif, mengurangi kesalahan, serta mempermudah akses informasi bagi pengguna.
</p>

</body>
</html>
