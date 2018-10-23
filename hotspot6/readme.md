
## Membuat login Member menjadi default
Edit file login.html di baris 15 menjadi 
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
