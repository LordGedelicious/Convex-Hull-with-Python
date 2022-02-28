# Implementasi _Convex Hull_ untuk Visualisasi Tes _Linear Separability Dataset_ dengan Algoritma _Divide and Conquer_

> Program dalam format `.ipynb` untuk membangun _convex hull_ pada sklearn.datasets.load_iris() dan sklearn.datasets.load_wine()
> sebagai Tugas Besar 2 IF2211 Strategi Algoritma

## Daftar Isi
- [Deskripsi](#deskripsi)
- [Penggunaan](#penggunaan)
- [Identitas](#identitas)

## Deskripsi
_Convex Hull_ adalah sebuah bentuk convex terkecil yang memuat seluruh data di dalamnya. Bentuk _convex_ sendiri dapat diartikan sebagai sebuah bentuk yang untuk setiap sembarang dua titik di dalamnya, dapat ditarik garis lurus antara dua titik tersebut dan setiap segmen garis tersebut berada di dalam bentuk tersebut. 
Terdapat banyak manfaat dari penggunaan _convex hull_ ini, khususnya di bidang _data science_. Salah satu penggunaannya adalah dalam pengujian _linear separability dataset_. _Linear separability dataset_ adalah pengujian untuk mengetahui apakah dua _dataset_ terpisah atau independen terhadap satu sama lain. Pengujian ini dilakukan dengan cara memetakan kedua _dataset_ ke dalam suatu bidang planar berdimensi dua dan melihat apakah bisa ditarik sebuah garis linear yang memisahkan kedua _dataset_ tersebut. Bila bisa dipisahkan, maka kedua _dataset_ terpisah secara linear. Dengan menggunakan _convex hull_, maka cukup dilihat apakah sisi dari kedua _convex hull dataset_ saling tumpang-tindih (_overlapping_) atau tidak. Bila iya, maka kedua dataset tidak linear terpisah. 
_Convex Hull_ pada program yang didesain penulis dibuat dengan mengimplementasikan algoritma _divide and conquer_. Algoritma _divide and conquer_ adalah algoritma yang membagi sebuah persoalan menjadi beberapa sub-persoalan yang lebih kecil sampai mencapai sebuah ukuran tertentu yang mudah diselesaikan dan menggabungkan hasil dari semua upa-persoalan yang sudah digabungkan. Program ini mengimplementasikan konsep tersebut dengan cara membagi kumpulan titik menjadi dua bagian setiap kali ditemukan sebuah titik terluar yang dapat menjadi ujung _convex hull_. Begitu tidak ada lagi ujung _convex hull_ yang ditemukan, keseluruhan titik akan digabungkan secara terurut sehinga dapat menjadi sebuah kesatuan utuh _convex hull_.

Isi direktori adalah sebagai berikut:
```
├── docs  [laporan tugas kecil]
├── test  [laporan tugas kecil]
    ├── dataset_list.txt  [file txt yang berisikan semua dataset dan atribut yang diujikan pada pembuatan _convex hull_]
├── src   
    ├── main.ipynb [file utama yang dijalankan untuk menghasilkan _convex hull_ ]
```

## Penggunaan
**[RECOMMENDED]** Disarankan menggunakan Visual Studio Code sebagai compiler dari `main.ipynb` dengan adanya extension `Jupyter Notebook Renderers v1.0.6`, `Jupyter Keymap`, dan `Jupyter` dari Microsoft

1. Buka direktori `src` dan buka file `main.ipynb` pada Visual Studio Code
2. Run dua balok kode pertama secara berurutan sampai muncul tanda centang pada pojok kiri bawah. Tidak disarankan menggunakan fitur "Run All" karena adanya beberapa balok kode yang meminta query input
3. Pada section sklearn.datasets.load_iris(), lakukan run code (atau Ctrl + Enter) untuk memunculkan _convex hull_ load_iris. Akan diminta query untuk memilih atribut yang dihasilkan _convex hull_-nya. Dapat juga dibandingkan dengan _convex hull_ dari _library_ scipy dengan melakukan run code pada balok kode di bawahnya dan memasukkan query yang sama dengan yang diatas.
4. Pada section sklearn.datasets.load_wine(), lakukan run code (atau Ctrl + Enter) untuk memunculkan _convex hull_ load_wine. Akan diminta query untuk memilih atribut yang dihasilkan _convex hull_-nya. Dapat juga dibandingkan dengan _convex hull_ dari _library_ scipy dengan melakukan run code pada balok kode di bawahnya dan memasukkan query yang sama dengan yang diatas.

## Identitas
- <a href = "https://github.com/LordGedelicious">Gede Prasidha Bhawarnawa (13520004 - K01)</a>
