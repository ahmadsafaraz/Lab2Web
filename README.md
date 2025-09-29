# Lab2Web

# 1. mengubah dan menambah properti dan nilai pada kode CSS
<img width="1862" height="1025" alt="image" src="https://github.com/user-attachments/assets/11d6c311-10dd-424f-a668-4dd2a15ce6ce" />




# 2. Pebedaan Dari Deklarasi `<h1>` dengan Into `<h1>`
deklarasi `<h1>` menargetkan semua element `<h1>` dalam dokumen tanpa syarat


sedangkan into `<h1>` lebih spesifikhanya menarget `<h1>` yang berada di dalam elemen dengan id="intro".

h1 lain di luar elemen tersebut tidak terpengaruh. seperti pada contoh berikut `<h1>` pada belajar css tidak berubah warna seperti `<h1>` pada HELLO MAHASISWA


# 3. deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada element yang sama

Kalau ada lebih dari satu deklarasi CSS yang mengatur elemen yang sama, browser akan menampilkan gaya sesuai dengan urutan prioritas (CSS Specificity & Cascade).

Urutan prioritas CSS:

Inline CSS (ditulis langsung pada atribut style="" di elemen HTML) → paling tinggi.

Internal CSS (<style>...</style> di dalam file HTML).

External CSS (file .css yang dihubungkan dengan <link>).

Jadi, yang ditampilkan di browser adalah Inline CSS jika ada deklarasi yang bentrok pada properti yang sama.

contoh code inline css

```
<p style="color: blue;">
```

contoh code internal css

```
 <style>
    p{
      color: pink;
    }
    
  </style>
```

cotoh code external css

```
p {
  color: green;
}
```


# 4. elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser


elemen HTML punya ID dan Class sekaligus, lalu masing-masing ada deklarasi CSS, maka yang ditampilkan di browser mengikuti aturan Specificity CSS.

Aturan Specificity

Inline CSS → paling tinggi (tidak ada hubungannya dengan pertanyaan, tapi tetap penting).

ID Selector (#id) → lebih tinggi daripada class.

Class Selector (.class), pseudo-class, dan atribut → prioritas di bawah ID.

Tag Selector (p, div, dll) → paling rendah.

Jadi: Jika ada konflik, deklarasi CSS dengan selector ID yang akan dipakai browser.

Contoh Elemen

```
<p id="paragraf-1" class="text-paragraf">
```

kemudian di definisikan css
```
.text-paragraf{
  color: green;      /* class */
}

#paragraf-1 {
  color: red;        /* ID */
```




# penjelasan dari setiap langkah praktikum beserta screenshot


# 1. membuka dokumen HTML


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6b375d99-f88a-415e-983a-54e00eb236e0" />


Halaman web pada gambar tersebut menampilkan hasil dari penggunaan HTML dasar dengan penerapan internal, eksternal dan inline CSS. Struktur halaman terdiri dari judul besar “CSS Internal, eksternal dan Inline CSS”, tautan menuju materi CSS dasar, sebuah heading “Hello MAHASISWA”, serta paragraf yang berisi penjelasan tentang pembelajaran HTML dan CSS di mata kuliah Pemrograman Web di Universitas Pelita Bangsa. Selain itu, terdapat tautan tambahan “Informasi selengkapnya” yang mengarahkan pengguna pada informasi lebih lanjut. Tampilan masih sederhana karena berfokus pada pengenalan dasar penggunaan tag-tag HTML serta CSS.


# 2. Mendeklarasikan CSS Internal

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7d853b85-101c-487a-8ada-002efac8b067" />


Kode HTML tersebut menggunakan CSS internal yang ditulis langsung di dalam tag <style> pada bagian . Dengan pendekatan ini, styling hanya berlaku untuk halaman yang sama. Pada contoh tersebut, beberapa elemen dasar diberikan gaya sederhana, misalnya teks di dalam diberi warna merah, link di dalam diberi warna hijau tua dengan jarak antar-link, dan paragraf pada bagian #intro dibuat lebih rapi dengan margin tambahan. Selain itu, tombol yang dibuat menggunakan class .button diberi latar belakang merah, teks putih, serta sudut membulat agar terlihat lebih menarik, dan ketika diarahkan kursor (hover), warnanya berubah menjadi lebih gelap.



# 3. membuat CSS Eksternal

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9583d832-b931-4b7a-a054-2c18c02835f2" />


Eksternal CSS adalah metode penulisan kode CSS yang dipisahkan dari file HTML dan ditempatkan dalam file khusus dengan ekstensi .css, kemudian dihubungkan ke HTML menggunakan tag di dalam bagian . Cara ini sangat membantu menjaga struktur kode tetap rapi karena gaya tampilan bisa diatur secara terpusat dan dapat digunakan kembali oleh banyak halaman web sekaligus. Dengan eksternal CSS, pengembang web lebih mudah melakukan perubahan tampilan hanya dengan mengedit satu file, tanpa perlu membuka dan mengubah setiap halaman HTML satu per satu.


# 4. membuat Inline CSS

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/35d1bf41-2e66-472f-9497-2d939a5115d1" />


Internal CSS adalah cara menuliskan kode CSS di dalam tag <style> pada bagian sehingga aturan gaya bisa dipakai berulang kali pada beberapa elemen sekaligus, sedangkan Inline CSS ditulis langsung pada atribut style di tiap elemen HTML sehingga efeknya hanya berlaku untuk elemen tersebut saja. Dengan internal CSS, pengaturan tampilan lebih terstruktur dan mudah dikelola, sementara inline CSS biasanya dipakai untuk perubahan cepat atau styling khusus yang sifatnya spesifik. Keduanya sama-sama valid, tapi praktik terbaik adalah memaksimalkan internal (atau eksternal) CSS agar kode tetap rapi, dan inline CSS hanya digunakan bila benar-benar diperlukan.


# 5. membuat CSS Selector

<img width="1862" height="1025" alt="image" src="https://github.com/user-attachments/assets/10dfa230-20e7-4c03-a24b-59e0595e56c9" />



Fungsi utama dari CSS Selector adalah menemukan dan memilih (menargetkan) elemen HTML yang ingin Anda beri gaya. Dengan kata lain, Selector memberi tahu browser elemen mana yang harus diterapkan oleh sekumpulan aturan CSS tertentu.

Anda bisa membayangkan HTML sebagai sekelompok orang di sebuah ruangan dan CSS Selector sebagai instruksi yang sangat spesifik untuk memilih kelompok orang tertentu untuk diberi pakaian yang seragam (gaya).

