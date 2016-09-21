#### Importing Data pada Command Line 

Secara umum, proses importing data pada R dapat dilakukan dengan dua cara, yaitu menggunakan perintah‐perintah di command line dan menggunakan fasilitas GUI 
R‐Cmdr .  Pada  bagian  ini  akan  dijelaskan  penggunaan perintah pada command line untuk importing data. 

#### <b>Membaca File ASCII </b>

Suatu  file  ASCII  biasanya  terdiri  dari  bilangan‐bilangan  yang  dipisahkan  meng‐gunakan  spasi,  tab,  tanda  akhir  baris  atau  tanda  baris  baru,  serta  pembatas  yang  lain.  Misalkan data file ASCII yang dibuat di NOTEPAD dengan nama latihan5.txt berisi data  seperti berikut ini.

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2012-56-39.png
)

Anggap  bahwa  file  ASCII  dengan  nama  latihan5.txt  ini  sudah  tersimpan  pada  direktori kerja  R.  Proses  impor  data dapat  dilakukan  dengan  perintah  scan  dan  latihan5.txt  sebagai  argumennya.  Apabila  data  tidak berada  pada direktori  kerja R,  maka  tulis juga direktori  tersebut  pada  argumennya.  Berikut  ini  adalah  contoh  proses  impor  data  file ASCII. 
