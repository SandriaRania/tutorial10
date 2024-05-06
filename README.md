# tutorial10

1. Take a look at what happened. Capture the result of your execution. Put it in your Readme.md,
   with some explanation why the result is as such. 

<img src="images/Screenshot (441).png">

Di sini terlihat bahwa "Rania's Komputer: hey hey!" diprint lebih duluan dibanding "Rania's Komputer: howdy!" dan 
"Rania's Komputer: done!" hal ini dikarenakan setelah perintah spawn dibuat, ia dipoll untuk dieksekusi oleh executor, lalu baru
howdy! dan done! diprint. Semua hal ini memakan waktu yang lebih lama dari mengeprint hey hey! secara langsung, jadi walaupun
hey hey! dilakukan setelah spawner spawn, ia muncul lebih cepat dari operasi spawn tersebut.

2. Try to remove and put it again. Pay attention to your console. Capture your screen as many as
   needed (but not more than three) and provide explanation why it is like that. Put it in Readme.md

<img src="images/Screenshot (442).png">
<img src="images/Screenshot (445).png">
<img src="images/Screenshot (443).png">

Dalam foto pertama dan kedua, kita melihat bahwa urutan diprintnya done berbeda, walaupun keduanya memiliki kode yang sama. Hal ini dikarenakan  
executor berjalan secara asynchronous, sehingga bisa dianggap ketiga perintah berjalan bersamaan, sehingga tidak bisa ditentukan pasti
mana yang akan muncul duluan. Untuk foto ketiga kita melihat bahwa operasi tidak sepenuhnya berhenti, hal ini dikarenakan kode menganggap
spawner tidak di drop, artinya executor masih dalam state di mana ia menunggu perintah task selanjutnya untuk dijalankan.

3. 