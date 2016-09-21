Matriks  atau  data  array  dua  dimensi  adalah  salah  satu  tipe  data  yang  banyak 
digunakan dalam pemrograman statistik. Sebagian besar fungsi‐fungsi statistik dalam R 
dapat  dianalisis  dengan  menggunakan  bentuk  matriks.  Bentuk  matriks  ini  juga  banyak 
digunakan pada operasi fungsi‐fungsi built‐in untuk aljabar linear dalam R, seperti untuk 
penyelesaian suatu persamaan linear. 
Proses  entry  data  matriks  dilakukan  dengan  menggunakan  fungsi  matrix. 
Argumen  yang  diperlukan  adalah  elemen‐elemen  dari  matriks,  dan  argumen  optional 
yaitu  banyaknya  baris  nrow  dan  banyaknya  kolom  ncolom.    Sebagai  contoh,  gunakan 
perintah‐perintah berikut ini pada R‐console.

> matriks.1 = matrix(c(1,2,3,4,5,6),nrow=2,ncol=3) 
> matriks.2 = matrix(1:6,nrow=2,ncol=3) 
> matriks.3 = matrix(1:6,nrow=2) 
> matriks.4 = matrix(1:6,2) 
> matriks.1


[,1] [,2] [,3] 
[1,]    1    3    5 
[2,]    2    4    6

Keempat perintah diatas akan menghasilkan matriks yang sama. Untuk mengetahuinya 
ketikkan  matriks.2,  matriks.3,  matriks.4,  dan  kemudian  enter  untuk  masing‐masing 
perintah tersebut.

Pada R, data secara default akan diisikan kolom perkolom seperti yang terlihat 
pada contoh berikut ini. 


> data=c(6.4,8.8,7.5,5.3,7.6,9.5) 
> data 
<b>[1] 6.4 8.8 7.5 5.3 7.6 9.5 </b>
 
> matriks.a=matrix(data,nrow=3,ncol=2) 
> matriks.a 
<b>     [,1] [,2] 
[1,]  6.4  5.3 
[2,]  8.8  7.6 
[3,]  7.5  9.5 
</b>
