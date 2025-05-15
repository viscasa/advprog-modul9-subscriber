<div align="center">
    <h1>MODULE 9</h1>
</div>

<div align="center">
    <img src="assets/images/burhan_pixel.png" alt="burhan" width="200"/>
</div>

<div align="center">
    <h2>Alwie Attar Elfandra</h2>
    <h2>2306241726</h2>
</div>

# 1. What is `amqp`?

**AMQP (Advanced Message Queuing Protocol)** adalah protokol komunikasi yang distandardisasi dan dirancang untuk pertukaran pesan antar aplikasi. AMQP memungkinkan sistem perangkat lunak yang berbeda—terutama yang berjalan secara terdistribusi atau di cloud—untuk saling berkomunikasi dengan cara yang andal, aman, dan efisien.

Dalam konteks pemrograman, seperti pada kode `main.rs`, AMQP digunakan sebagai sarana untuk terhubung dengan sistem antrean pesan (message queue) seperti **RabbitMQ**. Sistem ini memungkinkan satu bagian aplikasi untuk mengirim pesan ke antrean, dan bagian lainnya untuk membaca serta memproses pesan tersebut secara **asinkron**.

Sebagai contoh, antrean dengan nama `"user_created"` dapat digunakan untuk menerima notifikasi bahwa seorang pengguna baru telah dibuat. Handler seperti `UserCreatedHandler` kemudian akan menangani pesan tersebut begitu diterima.

# 2. What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for?

Format `guest:guest@localhost:5672` merupakan bagian dari **URL koneksi** ke server RabbitMQ, yang menjelaskan bagaimana aplikasi akan terhubung. Berikut adalah penjabaran dari masing-masing komponennya:

* **`guest:guest`**: Ini adalah kombinasi **username** dan **password** yang digunakan untuk autentikasi. Dalam contoh ini, baik nama pengguna maupun kata sandi adalah `"guest"`, yang merupakan kredensial default RabbitMQ. Untuk alasan keamanan, penggunaan akun default ini **tidak disarankan di lingkungan produksi**.

* **`localhost`**: Ini menunjukkan bahwa koneksi dilakukan ke server RabbitMQ yang berjalan di **komputer lokal** (yaitu mesin tempat aplikasi dijalankan).

* **`5672`**: Ini adalah **port default** yang digunakan oleh RabbitMQ untuk menerima koneksi berbasis AMQP.

Secara keseluruhan, `guest:guest@localhost:5672` berarti: terhubung ke server RabbitMQ lokal yang berjalan di port 5672, menggunakan kredensial default "guest" sebagai username dan password.