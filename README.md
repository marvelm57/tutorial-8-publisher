# Tutorial 8 - Crosstown Bus Poc Publisher
AdvPro B - Marvel Martin Everthard - 2206081345

---

## Reflection
1. How many data your publisher program will send to the message broker in one run?
> Publisher program akan mengirim **5 data** ke _message broker_ dalam sekali _run_. Hal ini dapat dilihat pada bagian kode yang memanggil **'publish_event'** sebanyak 5 kali.

2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
> **URL** yang sama pada **subscriber** dan **publisher** menunjukkan bahwa keduanya terhubung dan **berkomunikasi dengan server AMQP yang sama**, serta menggunakan _message broker_ yang sama.

3. Running RabbitMQ as message broker
![Running RabbitMQ as message broker](assets/images/RunningRabbitMQ.png)

4. Sending and processing event
![Sending and processing event](assets/images/SendingProcessingEvent.png)
> Hasil screenshot di atas menunjukkan proses yang terjadi ketika menjalankan `cargo run` pada **publisher**. Ketika `cargo run` dijalankan, **publisher** akan mengirim **5 event** ke _message broker_ yang nantinya akan di-_**consume**_ dan diproses oleh **subscriber**. 

5. Monitoring chart based on publisher
![Monitoring chart based on publisher](assets/images/MonitoringChart.png)
> Hasil screenshot di atas menunjukkan grafik _message rate_ ketika program **publisher** dijalankan. Grafik tersebut menggambarkan seberapa cepat message dikirim **publisher**. Lonjakan(**spike**) yang ada pada grafik mengindikasikan adanya **peningkatan jumlah _message_** yang dikirim **dalam satu periode waktu** akibat dijalankannya program publisher.