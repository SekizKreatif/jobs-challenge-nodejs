# jobs-challenge-nodejs

Senden bir node.js ve index.html örneği hazırlanınızı istiyoruz.
### NODEJS Kullanılacak kütüphaneler
- cluster
- redis
- http
- socket.io
- socket.io-redis
- express
- mongodb


## 1) Kullanıcı kayıt

     POST /user/create 

name

surname

age

email

phone

alınan bilgiler mongodb user tablosuna kayıt edilecek.

## 2) Kullanıcı Bilgisi Getir

    GET /user/{id}

mongodb eklenen kullanıcı bilgisini JSON formatında döndürecek. Redis ile cache yapılacak. (not: Mongodb getirilecen sonuc arrayini, redis set edilecek ve tekrar eden işlemde redis’den  arrayi getirecek.)


### 3)  Kullanıcı kayıt

socket  

    Anahtar usercreate/

*name, surname, age ,email ,phone* alınan bilgiler mongodb *user* tablosuna kayıt edilecek.

### 4) Kullanıcı Bilgisi Getir

socket  

    Anahtar userget/{id}

mongodb eklenen kullanıcı bilgisini JSON formatında döndürecek. Redis ile cache yapılacak.

*(not: Mongodb getirilecek sonuç arrayini, redis set edilecek ve tekrar eden işlemde redis’den  arrayi getirecek.)*

### 5) Kullanıcı Yaş Büyükleri getir

socket  

    Anahtar userageget/

**param:** 
mongodb user tablosu age > param olan verileri getirsin. 
 *(not: Mongodb getirilecen sonuç arrayını, redis set edilecek ve tekrar eden işlemde redis’den  arrayi getirecek.)*

### 6) Kullanıcıları Arama

socket  

    Anahtar usersearch/

param
mongodb user tablosu name ve/veya surname   arama yapılacak. Google tarzında, kelimeye en  yakın olan arattırma yapılacak. 

indexleme: turkish

Örnek kelime: 
- Ahmet Hasan Dursun Batmaz
- Aranan Kelime: 
- Ahmet
- Hasan
- Dursun
- Batmaz
sonuc getirilecek ekranda gösterilecek.

Index.HTML
Kullanılacak kütüphaneler
  
angular veya jquery
socket.io.min.js

Yukarıdaki nodejs methodlarını kullanarak liste şeklinde
 post,get ve socket.io haberleşmesini sağlayın. 

### MONGODB
 user tablosunu index’leme kodlarını yazınız

