# tutorial10

1. Take a look at what happened. Capture the result of your execution. Put it in your Readme.md,
   with some explanation why the result is as such. 

<img src="images/Screenshot (441).png">

Di sini terlihat bahwa "Rania's Komputer: hey hey!" diprint lebih duluan dibanding "Rania's Komputer: howdy!" dan 
"Rania's Komputer: done!" hal ini dikarenakan setelah perintah spawn dibuat, ia dipoll untuk dieksekusi oleh executor, lalu baru
howdy! dan done! diprint. Semua hal ini memakan waktu yang lebih lama dari mengeprint hey hey! secara langsung, jadi walaupun
hey hey! dilakukan setelah spawner spawn, ia muncul lebih cepat dari operasi spawn tersebut.

2. 