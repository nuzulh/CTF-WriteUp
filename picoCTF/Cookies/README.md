
# Cookies
*Category: Web Exploitation*

**URL**

http://mercury.picoctf.net:54219/

**Desciption**

Who doesn't love cookies? Try to figure out the best one. 

**Solution**

Berikut tampilan awal web.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/tampilan-web.png)

Dijelaskan bahwa autor sangat suka kue (cookie), kira-kira seberapa banyak jenis kue yang disukai beliau?
Dari sini, kita dapat petunjuk yang pasti bahwa ada lebih dari 1 jenis cookie yang valid.

Setelah kita coba menginput text ngasal di search bar, lalu ditampilkan pesan bahwa inputan kita tadi adalah cookie yang tidak valid.

Tentu saja tidak lupa sambil membuka inspeq elementz, di bagian network, kita melihat di Request Header terdapat:

```
Cookie: name=-1
```

Sekarang saatnya membuka alat tempur BurpSuite untuk memanipulasi header. Disini kita mencoba mengubah value name dari '-1' menjadi '1'.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/ubah-name.png)

Dan, hasilnya:

(berhasil.png)

Setelah berhasil mendapatkan 1 kue kesukaan autor, maka kita akan mencari kue-kue lainnya dengan cepat menggunakan BurpSuite.

Tambahkan dulu hasil respon di HTTP History tadi ke Intruder, dan pada position, tandakan bagian value dari name sebagai parameter untuk di attack:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/position.png)

Lalu, kita coba create 100 angka dulu untuk parameternya dengan Python3:

```
hhylh2@hhylh2-com:~$ python3
Python 3.8.10 (default, Jun  2 2021, 10:49:15) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> for i in range(100):
...     print(i)
...
```

copy hasil print tersebut, lalu paste ke Payload Options:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/payload-options.png)

Klik start attack, lalu tunggu, hirrup qalem sampai ada sebuah respon yang janggal.

Pada request ke 19 dengan payload 18 terdapat kejanggalan, dimana length dari respon yang diberikan sangat berbeda yaitu lebih sedikit sekitar setengah dari length pada respon dari payload lainnya.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/length-janggal.png)

Dan, inilah flag nya:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Cookies/flag.png)

picoCTF{3v3ry1_l0v3s_c00k135_96cdadfd}

![alt text](https://media.giphy.com/media/lgcUUCXgC8mEo/giphy.gif)
