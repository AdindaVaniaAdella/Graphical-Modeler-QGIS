# Graphical-Modeler-QGIS
Graphical Modeler QGIS
adalah aplikasi yang dapat digunakan untuk membuat, mengedit, dan mengelola model. Graphical Modeler dapat membuat suatu model yang kompleks menggunakan antarmuka (User Interface) yang sederhana dan mudah digunakan. Dalam melakukan analisis dengan SIG, biasanya terdapat beberapa tahap yang harus dilakukan dan memakai banyak tools dari Processing Toolbox. Dengan menggunakan Graphical Modeler tahapan-tahapan tersebut dapat digabungkan ke dalam satu proses, sehingga membentuk satu alur kerja dengan serangkaian input yang berbeda. Banyaknya tahapan dan algoritma yang dipakai, model dijalankan sebagai algoritma tunggal sehingga dapat menghemat waktu bagi para pengguna terutama untuk model yang lebih besar (QGIS Documentation, 2022). Kegunaan model ini dapat digunakan untuk memecahkan analisis spasial yang menggunakan banyak tools dalam pengerjaannya sehingga mempermudah untuk mengerjakan analisis spasial yang serupa dan tidak perlu melakukan proses dari awal (Gunawan, 2018). Dari model yang telah dirancang nantinya akan dihasilkan sebuah tools baru. Salah satu contoh tool yang akan penulis bahas disini adalah Tool Perhitungan Debit Limpasan.
# Pengenalan Tool Perhitungan Debit limpasan
Tool Perhitungan Debit Limpasan adalah model Graphical Modeler yang dirancang untuk menghitung besarnya debit limpasan dari suatu Catchment Area. Perhitungan debit limpasan ini merujuk pada persamaan Metode Rasional, yang dapat ditunjukkan dibawah ini:

![image](https://user-images.githubusercontent.com/124231433/217170643-0ff46dd5-bb4c-4e50-a0e2-fc95b7137019.png)

Q	=  Debit limpasan (m3/detik)

0,278	=  Konstanta

C	=  Koefisien limpasan

I	=  Intensitas curah hujan (mm/jam)

A	=  Luas DAS (km2)

Nilai Koefisien Limpasan (C) pada Tool ini ditentukan berdasarkan tabel berikut yang diambil dari berbagai referensi:

![image](https://user-images.githubusercontent.com/124231433/217183004-94e841d6-77e1-461e-913b-4705b0a29c95.png)

Data yang dibutuhkan untuk melakukan perhitungan debit limpasan menggunakan tool ini adalah sebagai berikut:
1) Data Raster berupa Digital Elevation Model (DEM).
2) Data vektor berupa Shapefile Tutupan Lahan dan Batas Wilayah Catchment Area.
3) Nilai Intensitas Curah Hujan dalam satuan mm/jam.

Tampilan Antarmuka (User Interface) Tool Perhitungan Debit Limpasan :
![image](https://user-images.githubusercontent.com/124231433/217182701-1ed660db-0708-42a8-9d21-e057efebd176.png)
# Input Parameters
![image](https://user-images.githubusercontent.com/124231433/217182318-6beff197-5b95-42ab-8f57-5ec550fc4301.png)
# Outputs
![image](https://user-images.githubusercontent.com/124231433/217182346-048f1ebe-c401-445c-9f4d-3576550a964c.png)

Output Layers :

![image](https://user-images.githubusercontent.com/124231433/217185901-801d8478-41fd-4d4c-96b8-6c1e35fe901c.png)

Attribute Table Pada Output "Intersection" :

![image](https://user-images.githubusercontent.com/124231433/217185224-68974bf9-66d2-45df-9cef-ffe5809a94a5.png)

Attribute Table Pada Output "Total Debit Limpasan" :

![image](https://user-images.githubusercontent.com/124231433/217184894-7c48ba08-566f-426a-9b21-4c1f1f14061e.png)

# Visualisasi Pengolahan Data Pada Tool
![image](https://user-images.githubusercontent.com/124231433/217182076-ae643d88-98ad-4a9e-bc30-398f90845385.png)
![image](https://user-images.githubusercontent.com/124231433/217188141-37a03290-6475-41a5-81a7-b66effc802a6.png)

Dengan menggunakan Persamaan Metode Rasional, maka didapatlah nilai Debit Limpasan (Q) seperti yang terlihat pada gambar berikut:

![image](https://user-images.githubusercontent.com/124231433/217188431-e204ff41-9ed4-42d8-9475-be1f96e3d0f4.png)

# Tutorial Mengunduh File Model Tool Perhitungan Debit Limpasan
1) Pada tampilan repository "Graphical Modeler-QGIS" klik pada bagian Code lalu klik Download ZIP, maka seluruh file yang terdapat pada repository tersebut akan terunduh dalam format ZIP.
![image](https://user-images.githubusercontent.com/124231433/217441270-6c8e6a3b-544d-4b92-879f-6a535e6c1283.png)

2) Jika hanya ingin mengunduh salah satu file pada repository, misalnya hanya ingin mengunduh file Model Tool Perhitungan Debit Limpasan saja, maka klik pada file yang ingin diunduh.
![image](https://user-images.githubusercontent.com/124231433/217443576-23096e45-dc61-4746-9808-20a496fa6655.png)

   Setelah itu, klik kanan pada Raw lalu klik Simpan tautan sebagai... atau Save link as... seperti yang terlihat pada gambar berikut.
   ![image](https://user-images.githubusercontent.com/124231433/217443802-06d80c73-add8-4f86-8812-f2caac5e5a7b.png)

   Pilih folder pada device Anda untuk menyimpan file yang akan diunduh lalu tekan Save.
   ![image](https://user-images.githubusercontent.com/124231433/217744475-656e6b65-1c00-4798-a98d-92ae26ed6662.png)

# Tutorial Menggunakan Tool Perhitungan Debit Limpasan Pada QGIS
Sebagai contoh, disini penulis akan menghitung Besarnya Debit Limpasan dari Sub DAS Krueng Seulimuem. Berikut adalah langkah-langkahnya:

A. Menambahkan Data Spasial

1) Memasukkan data vektor. Klik pada tombol ![image](https://user-images.githubusercontent.com/124231433/217445075-a426ceaf-2c3e-455c-ab5a-6ad426ab83cb.png) pada Manage Layer Toolbar atau melalui Menu Bar --> Layer --> Add Layer --> Add Vector Layer.
   ![image](https://user-images.githubusercontent.com/124231433/217445491-96e37d23-712a-44fb-9176-69024b9edc8f.png)

2) Kemudian akan muncul kotak dialog yang memperbolehkan Anda untuk memilih file yang akan ditambahkan ke dalam proyek QGIS Anda. Klik Source Type File dan dan tentukan Source Vector Dataset-nya dengan menekan tombol ![image](https://user-images.githubusercontent.com/124231433/217445557-1b6c6685-22c9-4ea3-a09c-4bb76a25e04d.png) dan pilih data dengan format .shp.
   ![image](https://user-images.githubusercontent.com/124231433/217446079-040fc097-f0f5-49a9-aff4-0ad40b6723af.png)

3) Data yang dimasukkan ke dalam QGIS yaitu data dengan format shapefile atau .shp. sebagai contoh seperti dibawah ini. Lalu klik Open dan Add data. Data tersebut akan muncul di Map Canvas QGIS.
   ![image](https://user-images.githubusercontent.com/124231433/217744521-b6aaafd8-1d5f-4f49-922e-939154237874.png)

4) Maka akan tampil pada Map Canvas data vektor yang sudah Anda pilih. Selanjutnya klik kanan pada layer shapefile pilih Propreties untuk melakukan pengelompokan dari setiap data atribut pada shapefile.
   ![image](https://user-images.githubusercontent.com/124231433/217744563-7133691a-cfaa-4f54-8a4e-5550c3f4cae5.png)

5) Pada Single Symbol, ubah ke Categorized. Pada Value pilihlah nama Field yang berisikan data atribut. Lalu klik Classify dan Apply.
   ![image](https://user-images.githubusercontent.com/124231433/217744748-160da4ea-c577-4271-8c6a-018b8b1dd7cb.png)
   ![image](https://user-images.githubusercontent.com/124231433/217746611-dca4f6b6-9c90-4205-8284-3fb730fe840b.png)

6) Selanjutnya memasukkan data raster. Klik pada tombol ![image](https://user-images.githubusercontent.com/124231433/217446425-bc8f5e01-1b30-4167-830e-9252fd2da175.png) pada Manage Layer Toolbar atau melalui Menu Bar --> Layer --> Add Layer --> Add Raster Layer.
    ![image](https://user-images.githubusercontent.com/124231433/217746836-0cbb5a90-8fb8-4a2a-9eb9-847ed45000b1.png)
    
7) Kemudian akan muncul kotak dialog yang memperbolehkan Anda untuk memilih file yang akan ditambahkan ke dalam proyek QGIS Anda. Klik Source Type File dan dan tentukan Source Raster Dataset-nya dengan menekan tombol ![image](https://user-images.githubusercontent.com/124231433/217446610-c9680743-978b-45a1-bbbd-698311e132a1.png) dan pilih data dengan format .tif.
   ![image](https://user-images.githubusercontent.com/124231433/217747193-e488143b-ab78-45f4-8bac-45232360aacb.png)

8) Data yang dimasukkan ke dalam QGIS yaitu data dengan format Temporary Instruction File Format atau .tif sebagai contoh seperti dibawah ini. Lalu klik Open dan Add data. Data tersebut akan muncul di Map Canvas QGIS.
   ![image](https://user-images.githubusercontent.com/124231433/217747622-3fcbcb72-a8bb-4d90-8aec-27e1e9deb3ef.png)

9) Maka akan tampil pada Map Canvas data raster yang sudah Anda pilih.
   ![image](https://user-images.githubusercontent.com/124231433/217747936-6f077647-5051-4b83-ad17-e6e034deb587.png)

B. Menambahkan Data Model Tool Pada QGIS

1) Setelah semua data spasial dimasukkan ke Software QGIS, selanjutnya kita dapat menggunakan Tool Perhitungan Debit Limpasan yang telah disediakan penulis. Pertama-tama, klik tombol Toolbox ![image](https://user-images.githubusercontent.com/124231433/217750321-d000df2e-d3be-41bb-a0a4-c1a726ee799e.png) pada Toolbar.

2) Maka akan tampil panel pencarian Toolbox. Selanjutnya, klik pada tombol ![image](https://user-images.githubusercontent.com/124231433/217750439-bc85a4d0-32a1-4f0d-a921-d6410ee2b72b.png), lalu pilih Add Model to Toolbox.
   ![image](https://user-images.githubusercontent.com/124231433/217750549-37a6ee28-4c9d-4739-8b77-33758dc3e08a.png)

3) Data yang dimasukkan ke dalam QGIS yaitu data dengan format .model3 sebagai contoh seperti dibawah ini. Lalu klik Open.
   ![image](https://user-images.githubusercontent.com/124231433/217750667-a6d15eae-aa3e-45ee-a182-ce9a5dcdc01e.png)

4) Selanjutnya, ketikkan pada kolom Search dengan Keyword “Model” lalu pilih Tool “Perhitungan Debit Limpasan” .
   ![image](https://user-images.githubusercontent.com/124231433/217750770-68a987dc-f42e-4ed1-b03a-1d2aedb50b6f.png)

5) Maka muncul Tampilan Antarmuka (User Interface) dari Tool Perhitungan Debit Limpasan. Selanjutnya, masukkan parameter-parameter yang dibutuhkan dari data spasial yang kita miliki.
   * Pada Input DEM Layer masukkan Layer DEM.
   * Lalu pada Input Feature Land Use masukkan Layer Tutupan Lahan.
   * Pada Intensitas Curah Hujan masukkan nilai nya berupa angka dengan satuan mm/jam. Berdasarkan penelitian dari Putri dkk (2019), intensitas curah hujan pada Sub        DAS Krueng Seulimuem adalah sebesar 8,64 mm/jam.
   * Yang terakhir pada Input Feature Catchment Area masukkan Layer Batas Wilayah Catchment Area. Apabila  hanya ingin menggunakan salah satu dari Sub DAS saja, maka      harus ditandai terlebih dahulu wilayah polygon tersebut dengan menggunakan Select Feature by Area or Single Click ![image](https://user-images.githubusercontent.com/124231433/217755087-556dbdd4-4ddd-47bc-ad63-d20fad795486.png), lalu arahkan kursok dan klik pada wilayah polygon yang diinginkan. Setelah       itu kembali pada User Interface Tool, centang pada kotak Selected features only.

6) Langkah terakhir, simpan data output secara permanen dengan menekan tombol ![image](https://user-images.githubusercontent.com/124231433/217751111-e93de5c7-e156-45c5-809d-4f33249af696.png) dan pilih Save to File. Berikan nama file sesuai dengan keinginan. Sebagai contoh disini penulis menuliskan nama file sebagai “Total Debit Limpasan”. Lakukan langkah yang sama pada Output kedua. Pada Output kedua, penulis menamakan “Intersection”. Kemudian klik Run. Tunggu sampai running data selesai lalu klik Close.
   
   ![image](https://user-images.githubusercontent.com/124231433/217757521-59c24d88-f6e9-4a76-a564-62ef8a0f8a5f.png)

7) Maka akan muncul Outputs dari Tool pada Canvas QGIS.

   * Output "Total Debit Limpasan"
   ![image](https://user-images.githubusercontent.com/124231433/217757559-a6739064-5203-4a64-9998-84625c92055f.png)
   
   * Output "Intersection"
   ![image](https://user-images.githubusercontent.com/124231433/217757583-116afe7a-41a7-446a-902f-2c29f73571df.png)   

   Untuk melihat hasil dari perhitungan debit limpasan, dapat dibuka pada  tabel atribut dengan cara klik kanan pada layer Outputs dan pilih Open Attribute Table.        Kemudian akan muncul tampilan data atribut dalam data tersebut.
   ![image](https://user-images.githubusercontent.com/124231433/217758008-d97ea4dc-0a0a-4e1f-9a0d-52b829720410.png)

   * Attribute Table pada Output "Total Debit Limpasan"
   ![image](https://user-images.githubusercontent.com/124231433/217758158-cdd8f782-785e-46d1-a98e-f37eefe74c3e.png)

   * Attribute Table pada Output "Intersection"
   ![image](https://user-images.githubusercontent.com/124231433/217758258-9e0d1fb9-0655-4f81-bb33-2aeb4a4233f3.png)

# Referensi
Gautama, R. S. 2019. Sistem Penyaliran Tambang. Bandung: ITB Press.

Gunawan, R. 2018. Implementasi Sistem Informasi Geografis (SIG) Pada Penyebaran Lokasi Kuliah Kerja Nyata (KKN). Jurnal Simetris Volume 9 No.1. Teknik Informatika.            Universitas Siliwangi. Tasikmalaya.

Hussein, S. 2012. Pemanfaatan Sistem Informasi Geografis (SIG) Berbasis Open Source Untuk Analisis Kerentanan Air Permukaan Subdas Blongkeng. Universitas Gadjah Mada          Bulaksumur.

Putri, I. R. P., Rusdi, M., Basri, Hairul. 2019. Evaluasi Debit Puncak Sub DAS Krueng Seulimeuem Kabupaten Aceh Besar. Universitas Syiah Kuala. Kota Banda Aceh.

QGIS Documentation.	2022.	QGIS Dekstop 3.22 User Guide. https://docs.qgis.org/3.22/en/docs/user_manual/processing/modeler.html. 

Wisconsin department of transportation (WDOT). 1979. Facilities Development Manual (July, 1979). Procedure 13-10-5.

Wisconsin department of transportation (WDOT). 2012. Facilities Development Manual.
