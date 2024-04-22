## Reyhan Zada Virgiwibowo
## 2206081723
## Advanced Programming - C
## Modul 8 - Publisher


## a. How many data your publisher program will send to the message broker in one run? 

Publisher akan mengirimkan 5 messages ke message broker dalam satu run, karena tiap kali pemanggilan p.publish_event akan dikirimkan satu message dan ada 5 pemanggilan di dalam main methodnya.

## b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

URL amqp://guest:guest@localhost:5672 diperlukan agar terhubung ke broker AMQP. Pada program publisher dan subscriber, URL tersebut menunjuk ke broker AMQP yang sama yang berjalan di mesin lokal. Dengan url yang digunakan sama oleh subscriber dan publisher, berarti mereka memiliki akses AMQP yang sama sehingga kedua program berkomunikasi melalui broker yang sama.

## Running RabbitMQ as message broker

![RabbitMQ Screenshot](assets/images/running_rabbitmq.png)

## Sending and processing event
![Sending and Processing Screenshot](assets/images/sending_and_processing.png)

Pada saat RabbitMQ berjalan dan kita menjalankan cargo run di Publisher dan Subscriber, maka Publisher akan mengirimkan 5 data event ke message broker yang diterima oleh Subscriber. Ketika Publisher di jalankan kembali, maka Publisher akan mengirimkan 5 data yang sama dengan sebelumnya ke message broker yang diterima oleh Subscriber.

![Monitoring chart based on publisher](assets/images/monitoring_chart.png)

Chart ini menunjukkan tentang message rates, yaitu sebanyak apa message broker menerima data dari Publisher dalam satu detik. Semakin banyak cargo run yang dijalankan pada Publisher, maka data yang dikirim oleh broker akan menjadi lebih banyak sehingga message rates akan meningkat.