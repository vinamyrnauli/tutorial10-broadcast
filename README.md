# Tutorial 10 (BROADCAST)
Nama: Vina Myrnauli Abigail Siallagan<br>
NPM: 2206825776<br>
Kelas: Pemrograman Lanjut - A<br>

---
## REFLEKSI 2

###### 2.1. Original code of broadcast chat.
![](images/1.png)  
![](images/2.png)
* Server dijalankan dengan perintah `cargo run --bin server`. Setiap klien dijalankan dengan perintah `cargo run --bin client`.
* Setiap klien dan server menerima *broadcast* dari setiap klien lainnya. Ketika klien mengetikkan pesan di baris perintah, *string* tersebut akan dikirimkan ke server.
* Server akan meneruskan pesan tersebut ke semua klien yang terhubung kepadanya. Dengan begitu, setiap klien akan menerima pesan dari klien lainnya melalui server. Semua pesan yang diketikkan oleh klien akan disebarkan kepada semua klien yang terhubung ke server.
<br>

###### 2.2. Modifying the websocket port.
![](images/3.png)  
![](images/4.png)
* Ketika port yang digunakan oleh klien dan server adalah sama, aplikasi akan tetap berjalan dengan baik seperti sebelumnya, seperti yang ditunjukkan dalam gambar di atas.

![](images/5.png)  
![](images/6.png)
* Jika misalnya hanya satu dari port tersebut yang diubah, seperti port klien, maka akan terjadi kesalahan pada sisi klien karena menurut klien, port tersebut tidak terhubung dan program akan mengalami kegagalan ketika perintah `cargon run --bin client` dijalankan sepertipada gambar di atas.
<br>

###### 2.3. Small changes. Add some information to client.
![](images/7.png)
* Tampilan yang terlihat dalam foto di atas berhasil dicapai dengan melakukan perubahan kode dalam bin/server.rs menjadi seperti berikut.

![](images/8.png)
* Perubahan dilakukan untuk memastikan bahwa ketika `bcast.tx` (yang bertindak sebagai *sender*) mengirimkan pesan kepada setiap klien, ia juga akan menyediakan alamat IP *sender* dari teks melalui variabel addr.



