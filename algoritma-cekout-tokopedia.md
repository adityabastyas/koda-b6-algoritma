# Algoritma

## Analisa Proses Checkout Tokopedia

## Deskriptif

1. Mulai
2. Pengguna buka aplikasi Tokopedia
3. Pengguna memilh produk yang mau dibeli
4. Sistem mengecek stok produk, apakah ada atau habis
5. Jika stok habis, maka tampilkan "Produk tidak tersedia" kembali ke langkah 3
6. Jika stok ada, pengguna memasukkan produk ke keranjang atau langsung beli
7. Muncul halaman keranjang belanja
8. Pengguna mengecek jumlah barang dan detailnya
9. Pengguna meng klik tombol checkout
10. Sistem mengecek apakah ada alamat pengiriman?
11. jika tidak ada alamat, pengguna mengisi alamat pengiriman
12. Jika ada, sistem menampilkan alamat yang udah kesimpan
13. Pengguna memilih jasa pengiriman
14. Pengguna memilih cara pembayaran transfer, COD, atau yang lain
15. Menampilkan ringkasan pesanan dan total harga yang harus dibayar
16. Pengguna menekan tombol bayar
17. Sistem memproses pembayaran
18. Jika pembayaran gagal, maka menampilkan "Pembayaran gagal" kembali ke langkah 14
19. Jika pembayaran berhasil, maka menampilkan "Pembayaran berhasil"
20. Sistem mengirimkan notifikasi konfirmasi pesanan ke pengguna
21. Selesai

## Flowchart

```mermaid
flowchart TD
    A@{shape: circle, label: "Mulai"}
    B@{shape: rect, label: "Buka Tokopedia"}
    C@{shape: lean-r, label: "Input: produk"}
    D@{shape: rect, label: "stok = x"}
    E@{shape: diamond, label: "stok > 0?"}
    F@{shape: lean-r, label: "Output : 'Produk tidak tersedia'"}
    G@{shape: rect, label: "keranjang = produk"}
    H@{shape: lean-r, label: "Output : Halaman keranjang"}
    I@{shape: rect, label: "Cek detail produk"}
    J@{shape: rect, label: "Klik checkout"}
    K@{shape: rect, label: "alamat = y"}
    L@{shape: diamond, label: "alamat == null?"}
    M@{shape: lean-r, label: "Input : alamat"}
    N@{shape: lean-r, label: "Output : alamat tersimpan"}
    O@{shape: lean-r, label: "Input : jasaKirim"}
    P@{shape: lean-r, label: "Input : metodeBayar"}
    Q@{shape: lean-r, label: "Output : ringkasan, totalHarga"}
    R@{shape: rect, label: "Klik bayar"}
    S@{shape: rect, label: "status = z"}
    T@{shape: diamond, label: "status == 'success'?"}
    U@{shape: lean-r, label: "Output : 'Pembayaran gagal'"}
    V@{shape: lean-r, label: "Output : 'Pembayaran berhasil'"}
    W@{shape: rect, label : "Kirim notifikasi"}
    X@{shape: dbl-circ, label: "Selesai"}

    A --> B
    B --> C
    C --> D
    D --> E
    E --True--> G
    E --False--> F
    F --> C
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
    L --True--> M
    L --False--> N
    M --> O
    N --> O
    O --> P
    P --> Q
    Q --> R
    R --> S
    S --> T
    T --True--> V
    T --False--> U
    U --> P
    V --> W
    W --> X
```
