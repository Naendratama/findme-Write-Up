# findme-Write-Up
![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/findme%201.png)

Category: Web Exploitation

Level: Medium

Author: Geoffrey Njogu

Decription: Help us test the form by submiting the username as test and password as test!

Hints: any redirections?

Recoon:
Web tersebut ternyata adalah web yang berbentuk form login, dan kita harus memasukkan input Username=test dan Password=test!
![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/Screenshot%202026-02-26%20171025.png)
kita coba submit

Ternyata kita dibawa ke sebuah website baru
![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/Screenshot%202026-02-26%20171047.png)

Namun ini hanya web pengalihan, karena sebelum masuk ke website ini, ada sebuah url yang mencurigakan, mari kita balik ke url sebelumnya.

![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/Screenshot%202026-02-26%20171118.png)
Ditemukan sebuah string yang sudah terenkripsi base64, namun sepertinya ini belum lengkap, mari kita balik lagi ke url sebelumnya.

![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/Screenshot%202026-02-26%20171142.png)
Dan yap kita menemukan sebuah string yang mencurigakan lago, sepertinya ini sudah terenkripsi base64 dan memiliki hubungan dengan url sebelumnya.

Mari kita gabungkan kedua strings tersebut, yang hasilnya adalah = cGljb0NURntwcm94aWVzX2FsbF90aGVfd2F5X2RmNDRjOTRjfQ==

Setelah itu ayo kita decode menggunakan base64
![ss](https://github.com/Naendratama/findme-Write-Up/blob/main/flag%20findme.png)

Dan yap flag telah ditemukann!
Flag : picoCTF{proxies_all_the_way_df44c94c}

