# Insp3ct0r

*Category: Web Exploitation*

**- URL**

http://jupiter.challenges.picoctf.org:41511

**- Description**

Kishor Balan tipped us off that the following code may need inspection: (URL above)

**- Hint**

*1. How do you inspect web code on a browser?*

*2. There's 3 parts*

**- Solution**

Karena kali ini berkaitan dengan inspect, maka membuka inspeqk elemendt pada web target adalah langkah awalnya.

Pada source code HTML nya pun terdapat bagian pertama flag:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Insp3ct0r/js.png)

Karena pemilik website menulis bahwa cara dia bikin web ini dengan '3' bahasa (html, css, js), kita menduga bahwa pesan itu berkaitan dengan *hint* poin ke 2.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Insp3ct0r/how.png)

Setelah periksa HTML web dan mendapatkan bagian pertama flag, maka lanjut ke source code css:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Insp3ct0r/js.png)css.png)

Dapat bagian kedua :)

Lanjut ke js:

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/Insp3ct0r/js.png)js.png)

Done.

picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?832b0699}

![alt text](https://media.giphy.com/media/lgcUUCXgC8mEo/giphy.gif)
