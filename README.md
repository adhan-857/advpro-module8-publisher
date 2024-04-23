### a) How many data your publlsher program will send to the message broker in one run? 
**5 kali**. Hal ini berdasarkan kode pada *main function* di file `main.rs`, dibuat sebuah *publisher* dimana *publisher* tersebut akan mengirimkan 5 pesan ke *message broker*. Pengiriman pesan oleh *publisher* ditandai oleh adanya pemanggilan fungsi `publish_event` sebanyak 5 kali.
<br>
<br>

### b) The url of: `“amqp://guest:guest@localhost:5672”` is the same as in the subscriber program, what does it mean?
Kedua URL antara program publisher dan subscriber sama berarti bahwa kedua program tersebut terhubung ke server RabbitMQ yang sama menggunakan protokol AMQP. Protokol AMQP digunakan untuk memfasilitasi komunikasi antara aplikasi yang berbeda dengan cara yang aman dan efisien. Bagian `"guest:guest@localhost:5672"` dalam URL menunjukkan bahwa keduanya menggunakan akun *default* `"guest"` dengan password `"guest"` untuk mengakses server RabbitMQ yang berjalan di `localhost` pada port 5672.

Dalam konteks ini, *publisher* menggunakan URL untuk mengirim pesan ke *queue*, sementara *subscriber* menggunakan URL yang sama untuk mendengarkan atau mengambil pesan dari *queue* tersebut. Dengan demikian, mereka berada dalam sistem yang sama dan dapat berinteraksi melalui *message broker* yang sama.
<br>
<br>

### Running RabbitMQ as message broker
![image](https://github.com/adhan-857/my-first-repo/assets/119088782/3b81a3a9-192c-4ab9-b57b-0d9602a22f8c)