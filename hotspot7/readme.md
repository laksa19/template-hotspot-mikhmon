
## Membuat login Member menjadi default
Konfigurasi login.html
```
var config = {
    loginvc : "Masukkan Kode Voucher kemudian klik login.",
    loginup : "Masukkan Username dan Password <br> kemudian klik login.",
    voucherCode : "Kode Voucher",
    setCase : "uppercase", // lowercase, uppercase or false
    defaultMode : "voucher", // voucher or member

}
```
## Fitur QR Code Scanner

Untuk menggunakan fitur QR CODE SCANNER Anda perlu menambahkan script berikut di MikroTik via Terminal.
```
/ip hotspot walled-garden ip

add action=accept comment="Mikhmon QR Code Scanner" disabled=no dst-host=laksa19.github.io

```
Centang HTTP PAP di hotspot server profile.
