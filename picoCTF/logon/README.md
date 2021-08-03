# logon

*Category: Web Exploitation*

**- URL**

http://jupiter.challenges.picoctf.org:13594/

**- Description**

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at?

**- Hint**

Hmm it doesn't seem to check anyone's password, except for Joe's?

**- Solution**

Pertama-tama dan yang paling utama, cek lalu lintas network melalui inspect element -> network.

Kita coba login dengan username & password ngasal dulu, hasilnya:

(login-ngasal.png)

Pada cookie request header ternyata tersedia 'admin=False', langsung gas ke BurpSuite untuk manipulasi request header tersebut.

(admintrue.png)

Setelah ubah admin=False menjadi admin=True, begini hasil respon-nya:

(flag.png)

picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}

=)

![alt text](https://media.tenor.com/images/196511013b8250ec3b163882ac988bdf/tenor.gif)
