# Pengantar Teknologi Informasi
## Algoritma Desicions Tree

### Desicion Tree Data Mining Algoritm

* Desicion Tree merupakan salah satu cara data processing dalam memprediksi masa depan dengan cara membangun klasifikasi atau regresi model dalam bentuk struktur pohon. Hal tersebut dilakukan dengan cara memecah terus ke dalam himpunan bagian yang lebih kecil lalu pada saat itu juga sebuah pohon keputusan secara bertahap dikembangkan. Hasil akhir dari proses tersebut adalah pohon dengan node keputusan dan node daun. Sebuah node keputusan (misalnya, Cuaca/ Outlook) memiliki dua atau lebih cabang (misalnya, Panas, Berawan dan Hujan).

* Decision Tree juga berguna untuk dieksplorasi data, menemukan hubungan antara sejumlah calon variabel input dengan sebuah variabel target. Pohon keputusan eksplorasi data dan pemodelan yang salah langkah pertama yang sangat baik dalam proses pemodelan yang digunakan sebagai model akhir untuk beberapa teknik lainnya.

* Kelebihan lain dari metode ini adalah mampu mengeliminasi perhitungan atau data-data yang tidak diperlukan. Karena sampel yang ada biasanya hanya diuji berdasarkan kriteria atau kelas tertentu.

* Meski memiliki banyak kelebihan, namun bukan berarti ini tidak memiliki kekurangan. Pohon keputusan ini mungkin tumpang tindih, terutama jika kelas dan kriteria yang digunakan sangat sering dapat meningkatkan waktu pengambilan keputusan sesuai dengan kapasitas memori yang diperlukan.

### Algoritme

* Algoritme adalah urutan langkah logis yang digunakan untuk memecahkan masalah. Singkatnya, masalah harus terdiri dari beberapa langkah logis

### Fungsi 

* Fungsi pembuatan algoritma digunakan dalam pemecahan masalah pemrograman yang kompleks. Algoritma dapat menyelesaikan program sederhana dan kompleks. Keuntungan lain menggunakan algoritme adalah algoritme dapat digunakan berulang kali. Algoritma juga membuat program menulis lebih sederhana bagi pemrogram. Anda dapat menggunakan algoritme untuk mengimplementasikan strategi top-down dan divide-and-conquer.

* Selain itu, algoritma tersebut dapat digunakan untuk mengurangi kesalahan pada program yang berulang. Algoritma sering digunakan sedemikian rupa sehingga masalah dapat diselesaikan secara logis dan berurutan. Dengan menggunakan algoritma yang tepat, program yang ada pun akan rapi, teratur, dan mudah dibuat. Jika terjadi kesalahan, Anda dapat segera menemukannya.

### Contoh Decision Tree Pada Algoritma

Kondisi berikut harus dipenuhi untuk memutuskan apakah akan bermain tenis atau tidak:

```-Climate
-Wind
-Kelembaban
-Temperatur udara
```

Solusi data per objek data, yang dikenal dengan atribut tujuan, merupakan salah satu atribut -> misalnya atribut “play” dengan nilai “key” atau “not playing” adalah salah satu atributnya.

“Contoh” adalah arti dari atribut.

Asumsikan atribut “Weather” memiliki tiga kemungkinan nilai: cerah, bersalju, dan hujan

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/3-1.jpg" height="500"/> 
  </p>

Berdasarkan informasi pada tabel di atas, akan dibuat tabel keputusan untuk memutuskan bermain tenis berdasarkan ramalan cuaca, suhu, kelembaban, dan kondisi angin.

* Algoritma secara umum:
```-Buat Cabang untuk setiap nilai -Pilih atribut sebagai root
-Ulangi prosedur untuk setiap cabang sampai semua kasus di cabang memiliki kelas yang sama.
-Memilih atribut berdasarkan nilai “gain” tertinggi dari atribut-atribut yang ada.
```

* Perhitungan Gain

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/5.jpg" height="100"/> 
  </p>

Keterangan: 
```S: Himpunan
A: Atribut
n: Jumlah Partisi Atribut A
|Si|: Jumlah Kasus Pada Partisi ke-i
|S|: Jumlah Kasus Dalam S
```
* Menghitung Nilai Entropy

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/6.jpg" height="100"/> 
  </p>

Keterangan:
```S : himpunan kasus
A : fitur
n : jumlah partisi S
pi : proporsi dari Si terhadap S
```
#### Perincian algoritme (langkah 1)

Hitung jumlah total kasus dan jumlah keputusan “Ya” atau “Tidak”.

Menggunakan atribut “Outlook”, “Temperature”, “Humidity”, dan “Windy”, ukur entropi semua instance yang terbagi.

Hitung perolehan untuk setiap atribut secara terpisah.

#### Perhitungan

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/7.jpg" height="500"/> 
  </p>

#### Perhitungan total entropy

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/8.png" height="300"/> 
  </p>

#### Menghitung gain pada baris Outlook

<p align="left"> 
  <img src="https://github.com/irwanx/pti/blob/master/9.jpg" height="300"/> 
  </p>

Hitung penguatan untuk suhu, kelembapan, dan kondisi berangin.

Kelembaban -> 0,37 ditemukan sebagai atribut dengan Gain tertinggi, seperti yang ditunjukkan pada tabel.

Kelembaban kemudian menjadi simpul akar.

Kelembaban dibagi menjadi dua kategori: “Tinggi” dan “Normal”.

Kelembaban -> “Alami” telah mengategorikan kasus ke dalam salah satu dari dua kategori: ya atau tidak.

Untuk humidity -> “High” msh perlu dilakukan perhitungn lagi (karena masih terdapat “yes” dan “no”)

Pohon keputusan Node 1
