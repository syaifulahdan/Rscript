
#### Importing Data File Excel 

Data  file  Excel  dengan  ekstensi  .XLS  dapat  diimpor  secara  langsung  meng‐gunakan fasilitas GUI R‐Cmdr (lihat bagian sebelumnya).  Untuk dapat diimpor ke dalam 
R  dengan  fasilitas  command  line,  maka  data  file  Excel  harus  terlebih  dulu  diubah menjadi format Text Tab Delimited (ekstensi .TXT) atau CSV comma delimited (ekstensi 
.CSV).  Setelah  itu,  data  ini  dapat  diimpor  menggunakan  perintah  <b>read.table</b>  atau <b>read.csv.</b> 

 
Misalkan  saja  data  file  Excel  yang  akan  diimpor  adalah  seperti  pada  gambar berikut ini dan telah disimpan menjadi file data1.txt atau data1.csv.

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2013-04-57.png)

Proses  impor data1.txt dapat dilakukan dengan perintah read.table, sedangkan, impor data1.csv  dilakukan  dengan  perintah  read.csv.  Argumen  optional  header=T  digunakan dengan  tujuan  agar  R  menggunakan  baris  pertama  dari  file  sebagai  header  atau  nama dari variabel. Seperti pada bagian sebelumnya, apabila data tidak berada pada direktori  kerja R, maka tulis juga direktori tersebut pada argumennya. Berikut ini adalah contoh proses impor data file dengan ekstensi .TXT dan .CSV. 

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2013-08-25.png)
