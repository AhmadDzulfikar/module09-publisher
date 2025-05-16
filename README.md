### 1. How much data your publisher program will send to the message broker in one run?
Ada lima event yang dipublikasikan ke message broker, masing-masing mewakili sebuah *UserCreatedEventMessage* dengan data yang berbeda. Setiap `UserCreatedEventMessage` berisi dua field:
- user_id (tipe data String), yang berisi ID pengguna.
- user_name (tipe data String), yang berisi nama pengguna.

Secara rinci, berikut data yang akan dikirimkan:
- 5 pesan, dengan setiap pesan berisi:
    - user_id: string 10-16 karakter
    - user_name: string sekitar 20-30 karakter


 ### The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL amqp://guest:guest@localhost:5672 berarti program publisher dan subscriber akan berkomunikasi dengan broker pesan yang sama, yaitu RabbitMQ yang berjalan di alamat lokal (localhost) pada port 5672 menggunakan protokol AMQP. Berikut penjelasan setiap bagian URL:
- guest:guest: Ini adalah username dan password yang digunakan untuk autentikasi ke broker RabbitMQ. Dalam hal ini, username dan password yang digunakan adalah guest.
- localhost: Ini adalah alamat hostname atau IP dari server tempat RabbitMQ berjalan. Dalam hal ini, "localhost" berarti RabbitMQ berjalan di mesin yang sama dengan aplikasi publisher dan subscriber.
- 5672: Ini adalah port yang digunakan oleh RabbitMQ untuk mendengarkan permintaan AMQP. Port 5672 adalah port default untuk AMQP.
