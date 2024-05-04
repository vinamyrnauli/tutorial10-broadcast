# Tutorial 10 (TBROADCAST)
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