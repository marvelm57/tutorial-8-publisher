# Tutorial 8 - Crosstown Bus Poc Publisher
AdvPro B - Marvel Martin Everthard - 2206081345

---

## Reflection
1. How many data your publisher program will send to the message broker in one run?
> Publisher program akan mengirim **5 data** ke _message broker_ dalam sekali _run_. Hal ini dapat dilihat pada bagian kode yang memanggil **'publish_event'** sebanyak 5 kali.

2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
> **URL** yang sama pada **subscriber** dan **publisher** menunjukkan bahwa keduanya terhubung dan **berkomunikasi dengan server AMQP yang sama**, serta menggunakan _message broker_ yang sama.
