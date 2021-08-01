# Scavenger Hunt

*Category: Web Exploitation*

**- URL**

http://mercury.picoctf.net:5080/

**- Description**

There is some interesting information hidden around this site (URL above). Can you find it?

**- Hint**

You should have enough hints to find the files, don't run a brute forcer.

**- Solution**

Mari kita mulai dengan inspek elemendz. Pada source code HTML dapat bagian pertama flag:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/html.png)

Lanjut lihat source code CSS dan dapat bagian kedua flag:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/css.png)

Lanjut ke JS:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/js.png)

Disini, kita dapat sebuah petunjuk yang berkaitan dengan google indexing, tentu saja robots.txt adalah file yang biasa digunakan pada kebanyakan website untuk lalu lintas web.

Dan robots.txt *harus* berada di root path pada website. Langsung saja kita coba buka http://mercury.picoctf.net:5080/robots.txt.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/robots.png)

Mantap, dapat flag part ketiga.

Lanjut, pada robots.txt tadi diberikan petunjuk bahwa web ini menggunakan apache sebagai http servernya dimana apache menggunakan file configurasi *.htaccess*. Langsung saja eksekusi:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/htaccess.png)

Petunjuk yang diberikan selanjutnya adalah pembuat web suka membuat sebuah situs web di *Mac*.

Setelah menganalisis tentang Mac beberapa menit, akhirnya kita dapat sebuah info dimana di setiap direktori pada MAC OS terdapat file *.DS_Store* sebagai informasi dari MAC OS untuk direktori tersebut yang tersembunyi.

Lalu, kita coba membuka http://mercury.picoctf.net:5080/.DS_Store.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Scavenger%20Hunt/DS_Store.png)

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}

![alt text](https://media1.tenor.com/images/bb6aa5121851f1b57a2cb50f73005c66/tenor.gif)
