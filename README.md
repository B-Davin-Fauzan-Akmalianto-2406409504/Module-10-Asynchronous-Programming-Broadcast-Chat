# Reflection Notes

## 2.1. Original code of broadcast chat.

![alt text](image.png)

Image run server ^

![alt text](image-1.png)

Image run client1 ^

![alt text](image-2.png)

Image run client2 ^

![alt text](image-3.png)

Image run client3 ^

Untuk menjalankan server, cukup ketik

`cargo run --bin server`

dan untuk client, cukup ketik

`cargo run --bin client` untuk setiap client yang ingin dijalankan.

Ketika mengetik sesuatu di client, itu akan mengirim pesan ke server, kemudian server akan mengirim balik pesan tersebut ke semua client.