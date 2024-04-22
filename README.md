## Reyhan Zada Virgiwibowo
## 2206081723
## Advanced Programming - C
## Modul 8 - Publisher


## a. How many data your publisher program will send to the message broker in one run? 

Publisher akan mengirimkan 5 messages ke message broker dalam satu run, karena tiap kali pemanggilan p.publish_event akan dikirimkan satu message dan ada 5 pemanggilan di dalam main methodnya.

## b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

URL amqp://guest:guest@localhost:5672 diperlukan agar terhubung ke broker AMQP. Pada program publisher dan subscriber, URL tersebut menunjuk ke broker AMQP yang sama yang berjalan di mesin lokal. Dengan url yang digunakan sama oleh subscriber dan publisher, berarti mereka memiliki akses AMQP yang sama sehingga kedua program berkomunikasi melalui broker yang sama.