## Edit background
Edit background backcground.css  (css/background.css )

bagian background-image: url(...)

convert gambar ke base64 http://base64online.org/encode/

centang pada Format as Data URL

## Membuat login Member menjadi default
Edit file login.html di baris 15 menjadi 
```
<body class="background" onload="member()">
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

## Warna background yang tersedia 

Diletakkan di class element
```
<div class="bg-dark"></div>
```

```
bg-primary
bg-secondary
bg-success
bg-info
bg-warning 
bg-danger
bg-light
bg-dark
bg-blue
bg-indigo
bg-purple
bg-pink
bg-red
bg-orange
bg-yellow
bg-green
bg-teal
bg-cyan
bg-white
bg-grey
bg-grey-dark
bg-light-blue

```
## Fitur QR Code Scanner

Untuk menggunakan fitur QR CODE SCANNER Anda perlu menambahkan script berikut di MikroTik via Terminal.
```
/ip hotspot walled-garden ip

add action=accept comment="Mikhmon QR Code Scanner" disabled=no dst-host=laksa19.github.io

```
Centang HTTP PAP di hotspot server profile.
