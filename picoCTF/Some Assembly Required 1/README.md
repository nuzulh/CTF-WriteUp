# Some Assembly Required 1

*Category: Web Exploitation*

**- URL**

http://mercury.picoctf.net:37669/index.html

**- Description**

ga ada

**- Solution**

Setelah mencoba inspect web tersebut, terdapat sebuah file js bernama *G82XCw5CX3.js*.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Some%20Assembly%20Required%201/beautify.png)

Script js tersebut tertulis dengan cara yang aneh walaupun telah di-beautify. Karena malas membaca source code tersebut, kita coba lihat-lihat dulu lalu lintas networknya, siapa tau ada kecelakaan disana.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Some%20Assembly%20Required%201/network-get.png)

Nah, disini web server memberi respons berbentuk file dengan nama *JIFxzHyW8W*.

Langsung gas download, lalu analisis file tersebut dengan beberapa perintah di terminal:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Some%20Assembly%20Required%201/flag.png)

Untung belum perpusing ria dengan souce code *G82XCw5CX3.js* tadi, ternyata jawabannya ada di *JIFxzHyW8W*.

picoCTF{a8bae10f4d9544110222c2d639dc6de6}

![alt text](https://i.kym-cdn.com/photos/images/original/001/779/959/5ac.png)
