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
