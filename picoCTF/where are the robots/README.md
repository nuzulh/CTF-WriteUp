# where are the robots

*Category: Web Exploitation*

**- URL**

http://jupiter.challenges.picoctf.org:36474/

**- Description**

Can you find the robots?

**- Hint**

What part of the website could tell you where the creator doesn't want you to look?

**- Solution**

Tanpa berlama-lama, langsung gas ke (url)/robots.txt sebagaimana deskrispi dan judul challenge.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/where%20are%20the%20robots/robots.png)

Benar saja, file tersebut tersedia, isinya adalah:

```
User-agent: *
Disallow: /477ce.html
```

Berdasarkan *hint*, kita harus menuju ke (url)/477ce.html, karena halaman tersebut kemungkinan adalah yang dimaksud *hint*.

![alt text](https://raw.githubusercontent.com/nuzulh/CTF-WriteUp/main/picoCTF/where%20are%20the%20robots/flag.png)

picoCTF{ca1cu1at1ng_Mach1n3s_477ce}

Jangan lupa closing

![alt text](https://media.giphy.com/media/lgcUUCXgC8mEo/giphy.gif)
