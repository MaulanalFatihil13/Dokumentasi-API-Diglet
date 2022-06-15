# Kelompok 11- Dokumentasi API Diglet

| Nama                      | NRP        |
|---------------------------|------------|
| Jovan Surya Bako          | 5027201013 |
| Anisah Farah Fadhilah     | 5027201023 |
| Maulanal Fatihil A.M.     | 5027201031 | 
<br/>

## Base URL
 https://diggie.herokuapp.com

<br/>

| Metode   | End Point                                            | Dokumentasi | Autentikasi | Deskripsi                                |
|----------|------------------------------------------------------|-------------|-------------|------------------------------------------|
| POST     |`https://diggie.herokuapp.com/profile`                |[Register](#large_blue_circle-register-large_blue_circle)|Tidak|Registrasi akun|
| POST     |`https://diggie.herokuapp.com/login`                  |[Login](#large_blue_circle-login-large_blue_circle)|Tidak|Masuk akun dan mendapatkan token|
| PATCH    |`https://diggie.herokuapp.com/profile/saldo`          |[Top Up](##large_blue_circle-profile-large_blue_circle)|Ya|Melakukan topup|
| GET      |`https://diggie.herokuapp.com/profile`                |[Profil](#large_blue_circle-top-up-large_blue_circle)|Ya|Mendapatkan informasi mengenai akun|
| PATCH    |`https://diggie.herokuapp.com/profile/pay`            |[Transaksi](#large_blue_circle-transaksi-large_blue_circle)|Ya|Melakukan pembayaran atas transaksi pembelian yang telah dilakukan|

<br/>

### Register
- Method: `POST`
- URL: https://diggie.herokuapp.com/profile
- Autentikasi: Tidak
- Parameter: 

Atribute | TipeData | Deskripsi
--- | --- | ---
name | string | Nama sebagai informasi atas identitas pengguna
email | string | Menggunakan format email yang sesuai, dengan ketentuan satu email untuk satu akun
password | string | Password dari pengguna, disarankan menyusun password yang aman dan tidak sederhana
confirmpassword | string | Konfirmasi password dari pengguna, disarankan menyusun password yang aman dan tidak sederhana

Contoh:
`POST` https://diggie.herokuapp.com/profile

![image](/img/register1.png)

Respon:

![image](/img/register2.png)
![image](/img/register3.png)

### Login
- Method: `POST`
- URL: https://diggie.herokuapp.com/login
- Autentikasi: Tidak
- Parameter: 

Atribute | TipeData | Deskripsi
--- | --- | ---
email | string | Email dari pengguna
password | string | Password dari pengguna

Contoh:
`POST` https://diggie.herokuapp.com/login

![image](/img/login1.png)

Respon:

![image](/img/login2.png)
![image](/img/login3.png)

### Top Up
- Method: `PATCH`
- URL: https://diggie.herokuapp.com/profile/saldo
- Autentikasi: Ya &rarr; Token yang didapat ketika melakukan login, disimpan pada Authorization Bearer
- Parameter: 

Atribute | TipeData | Deskripsi
--- | --- | ---
jumlah | number | Jumlah atau nominal topup yang akan dilakukan oleh pengguna

Contoh:
`PATCH` https://diggie.herokuapp.com/profile/saldo

![image](/img/topup1.png)

Respon:

![image](/img/topup2.png)

### Profil
- Method: `GET`
- URL: https://diggie.herokuapp.com/profile
- Autentikasi: Ya &rarr; Token yang didapat ketika melakukan login, disimpan pada Authorization Bearer
- Parameter: -

Contoh:
`GET` https://diggie.herokuapp.com/profile

Respon:

![image](/img/profil1.png)

### Transaksi 
- Method: `PATCH`
- URL: https://diggie.herokuapp.com/profile/pay
- Autentikasi: Ya &rarr; Token yang didapat ketika melakukan login, disimpan pada Authorization Bearer
- Parameter: 

Atribute | TipeData | Deskripsi
--- | --- | ---
jumlahBayar | number | Nominal harga barang yang ingin dibeli

Contoh:
`PATCH` https://diggie.herokuapp.com/profile/pay

![image](/img/transaksi1.png)

Respon:

![image](/img/transaksi2.png)