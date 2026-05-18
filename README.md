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

## 2.2. Modifying the websocket port

Setelah mengganti port menjadi 8080 di client.rs, sekarang kita harus mengganti port di fungsi main pada server.rs menjadi 8080 juga, agar koneksi dapat tersambung.

## 2.3 Small changes. Add some information to client

![alt text](image-4.png)

Pada `server.rs`, ganti line pada fungsi handle_connection agar mengirim addr juga kepada para client.
```rust 
if let Some(text) = msg.as_text() {
    println!("From client {addr:?} {text:?}");
    bcast_tx.send(format!("{addr}: {text}"))?;
}
```