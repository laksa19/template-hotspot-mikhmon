
## Membuat login Member menjadi default
Edit file login.html di baris 14 menjadi 
```
<body onload="member();">
```

## Input otomatis huruf kecil (auto lowercase)
Edit file login.html 
```
// set password = username
function setpass(){
  var user = username.value		
  password.value = user;
}

username.onkeyup = setpass;

```
menjadi
```
// set password = username
function setpass(){
  var user = username.value	
  user = user.toLowerCase();
  username.value = user;	
  password.value = user;
}

username.onkeyup = setpass; 

```
## Fitur QR Code Scanner

Untuk menggunakan fitur QR CODE SCANNER Anda perlu menambahkan script berikut di MikroTik via Terminal.
```
/ip hotspot walled-garden ip

add action=accept comment="Mikhmon QR Code Scanner" disabled=no dst-host=laksa19.github.io

```
