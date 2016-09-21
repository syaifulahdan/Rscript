 ### Importing Data dari Paket Statistik
 
 R  mempunyai  paket  atau  library  foreign  untuk  melakukan  importing  data  dari file dalam format paket statistika yang lain. Sampai saat ini yang tersedia pada R adalah 
importing data file dari paket‐paket statistika berikut :

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2013-12-51.png)

Pada  bagian  ini  akan  diberikan  contoh  hanya  untuk  mengimpor  data  file  SPSS dan MINITAB yang seringkali digunakan dalam analisis data statistik. Misalkan data file 
SPSS  yang  sudah  dimiliki  diberi  nama  WORLD95.SAV  dan  telah  disimpan  di  direktori kerja R. Proses impor data ini ke dalam R dengan menggunakan perintah command line 
adalah sebagai berikut. 

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2013-14-18.png)

Perintah  use.value.labels=TRUE  digunakan  untuk  mendapatkan  variabel  yang  bertipe FACTOR dengan “value label” seperti yang ada pada data file di SPSS.  Berikut ini adalah proses impor data file MINITAB dalam ekstensi .MTP ke dalam R dengan menggunakan perintah command line. Misalkan data file MINITAB yang sudah dimiliki adalah FA.MTW dan telah disimpan ke dalam ekstensi .MTP menjadi FA.MTP.  

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-21%2013-18-13.png)

