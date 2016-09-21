
1. Apa itu vector?
2. Bagaimana mengenerate sequence number?
3. Bagaimana menggabungkan dua buah vector?
4. Bagaimana membuat matrix?
5. Apa itu object?
6. Apa itu data frame?
7. Bagaimana mengkombinasikan data vector menjadi data frame?
8. Bagaimana mengakses value dalam sebuah object data frame?
9. Bagaimana membuat subset dari data frame?
10. Bagaimana mengambil data dari file lalu dipindahkan ke dalam obyek data.table?



Jawaban
1. Vektor merupakan kumpulan dari semua nilai yang menunjukan type data yang sama.
buka program R lalu ketikkan kode dibawah ini dan tekan enter :
orangtua_kita <- c("Ayah","Ibu")
huruf c yang berwarna hijau yaitu collection of values yang berarti kumpulan nilai tersebut, tanda  yang berwarna merah <- ini mengartikan kita membaca ruas kanan dahulu baru ruas kiri, jadi cara pembacaan koding diatas ialah Ayah, Ibu merupakan orangtua_kita 
selanjutnya ketikkan koding dibawah ini lalu tekan enter:
orangtua_kita
maka akan muncul secara otomatis seperti dibawah ini :
[1] "Ayah" "Ibu"
untuk mengetahui type data dari koleksi itu ketikan kode dibawah ini lalu tekan enter :
str(orangtua_kita)
str  artinya struktur dari yg didalam kurung 
maka nanti secara otomatis kita dapat hasil output dibawah ini
chr [1:2] "Ayah" "Ibu"
chr  merupakan type data Character
tulisan [1:2] berwarna hijau berarti koleksi nilainya terdiri dari 1 sampai dua koleksi nilai.
tulisan "Ayah" "Ibu" berwarna biru  itu adalah koleksi nilainya, jadi terdapat dua koleksi nilai.


2. R juga mempunyai sejumlah fasilitas untuk membangkitkan (generate) barisan bilangan. Fungsi yang digunakan adalah seq(). Sebagai contoh, untuk menuliskan suatu barisan dari 1 hingga 20, kita tidak perlu menuliskan satu persatu elemen ke dalam vektor, cukup menuliskan 
> seq (1, 20) atau 
> seq (from=1, to=20) 
akan menghasilkan 
[1] 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20
Keterangan: [1] pada sisi paling kiri mengartikan baris ke-1 dari hasil perhitungan di R
 > seq (20, 1) 
Perintah tersebut akan menghasilkan barisan bilangan yang menurun dari 20 ke 1 Barisan bilangan juga dapat dibangkitkan dengan cacah kelipatan tertentu. Misalkan: 
> s3 <- seq(from=-5, to=5, by=.5) atau 
> s3 <- seq(-5,5,by.5) atau 
> s3 <- seq(length=21,from-5,by=.5) 
Ketiga perintah diatas menghasilkan keluaran yang sama. Argumen length menyatakan panjang vektor. 
> s3 
[1] -5.0 -4.5 -4.0 -3.5 -3.0 -2.5 -2.0 -1.5 -1.0 -0.5 0.0 0.5 1.0 1.5 2.0 
[16] 2.5 3.0 3.5 4.0 4.5 5.0 
Pembangkitan barisan bilangan yang elemennya merupakan pengulangan dapat dilakukan dengan menggunakan fungsi rep(), misalkan: 
> s4 <- rep(x,times=5) 
[1] 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 
[16] 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 
akan menyalin sebanyak 5 kali angka 4, sedangkan perintah berikut: 
> s5 <- rep(4,each = 5) 
[1] 11.0 11.0 11.0 11.0 11.0 16.2 16.2 16.2 16.2 16.2 7.2 7.2 7.2 7.2 7.2 
[16] 1.3 1.3 1.3 1.3 1.3 8.3 8.3 8.3 8.3 8.3 
akan menyalin setiap elemen x sebanyak 5 kali.


3. Misalnya, kita memiliki dua vektor, yaitu X = dan Y =, maka hasil berbagai operasi hitung biasa di antR juga mempunyai sejumlah fasilitas untuk membangkitkan (generate) barisan bilangan. Fungsi yang digunakan adalah seq(). Sebagai contoh, untuk menuliskan suatu barisan dari 1 hingga 20, kita tidak perlu menuliskan satu persatu elemen ke dalam vektor, cukup menuliskan 

4. > seq (1, 20) atau 

5. > seq (from=1, to=20) 

6. akan menghasilkan 

7. [1] 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20

8. Keterangan: [1] pada sisi paling kiri mengartikan baris ke-1 dari hasil perhitungan di R

9.  > seq (20, 1) 

10. Perintah tersebut akan menghasilkan barisan bilangan yang menurun dari 20 ke 1 Barisan bilangan juga dapat dibangkitkan dengan cacah kelipatan tertentu. Misalkan: 
11. > s3 <- seq(from=-5, to=5, by=.5) atau 
12. > s3 <- seq(-5,5,by.5) atau 
13. > s3 <- seq(length=21,from-5,by=.5) 
14. Ketiga perintah diatas menghasilkan keluaran yang sama. Argumen length menyatakan panjang vektor. 
15. > s3 
16. [1] -5.0 -4.5 -4.0 -3.5 -3.0 -2.5 -2.0 -1.5 -1.0 -0.5 0.0 0.5 1.0 1.5 2.0 
17. [16] 2.5 3.0 3.5 4.0 4.5 5.0 
18. Pembangkitan barisan bilangan yang elemennya merupakan pengulangan dapat dilakukan dengan menggunakan fungsi rep(), misalkan: 
19. > s4 <- rep(x,times=5) 
20. [1] 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 
21. [16] 11.0 16.2 7.2 1.3 8.3 11.0 16.2 7.2 1.3 8.3 
22. akan menyalin sebanyak 5 kali angka 4, sedangkan perintah berikut: 
23. > s5 <- rep(4,each = 5) 
24. [1] 11.0 11.0 11.0 11.0 11.0 16.2 16.2 16.2 16.2 16.2 7.2 7.2 7.2 7.2 7.2 
25. [16] 1.3 1.3 1.3 1.3 1.3 8.3 8.3 8.3 8.3 8.3 
26. akan menyalin setiap elemen x sebanyak 5 kali.
27. Misalnya, kita memiliki dara kedua vektor ini adalah 
> x<-matrix(c(4,5,3,6),4,1) 
> y<-matrix(c(2,4,3,6),4,1) 
> x*y 
[,1] 
[1,] 8 
[2,] 20 
[3,] 9 
[4,] 36 
> x/y 
[,1] 
[1,] 2.00 
[2,] 1.25 
[3,] 1.00 
[4,] 1.00
 
> sum(log(x)) 
[1] 5.886104 
> prod(log(x)) 
[1] 4.39191 
Hasil beberapa operasi vektor atau matriks diperoleh seperti berikut. 
> x%*%t(y)
 [,1] [,2] [,3] [,4]
[1,] 8 16 12 24 
[2,] 10 20 15 30 
[3,] 6 12 9 18 
[4,] 12 24 18 36 

> t(x)%*%y 
             [,1] 
[1,]         73 
>solve(t(x)%*%y) 
                       [,1] 
[1,]     0.01369863 
> x[2] 
[1] 5

28. Matriks merupakan Sebuah koleksi dua dimensi nilai-nilai bahwa semua memiliki tipe yang sama.
Nilai-nilai tersebut diatur dalam baris dan kolom.

Gambar diatas tata letak nilai 1 sampai 9 dimana matrik tersebut berordo 3 x3
coba ketikan kode dibawah ini dan setelah selesai tekan enter :
matrix(1:9,nrow=3,ncol=3)
Tulisan matrix yang berwarna biru perintah untuk membuat matrix 1:9 merupakan untuk membuat koleksi nilai satu sampai sembilan nrow=3 berarti banyaknya baris ada 3 ncol=3 berarti banyaknya kolom ada 3 maka akan menghasilkan output seperti dibawah ini :
     [,1] [,2] [,3]
[1,]    1    4    7
[2,]    2    5    8
[3,]    3    6    9

apabila membuat matriks sembarang tak berurut seperti gambar diatas, maka ketikan kode seperti dibawah ini, setelah diketik tekan enter :
matrix(c(7,12,22,33,9,2,1,23,11),nrow=3,ncol=3)
maka akan muncul output seperti dibawah ini :
     [,1] [,2] [,3]
[1,]    7   33    1
[2,]   12    9   23
[3,]   22    2   11
Perjumlahan dan Pengurangan Matriks
Kita buat dulu matriks dengan objek x dan objek y, ketikan kode dibawah ini, setelah diketik
tekan enter :
x <- matrix(c(2,67,12,21,45,6,7,5,4),nrow=3,ncol=3);y <- matrix(c(32,7,-12,1,-5,6,-7,-5,1),nrow=3,ncol=3)
setelah itu ketikan kode dibawah ini untuk menjumlahkan matriks x dan matriks y, setelah diketik tekan enter :
matrix(x+y,nrow=3,ncol=3)
tulisan bewarna merah untuk menjumlahkan matriks jika diganti jadi x-y akan menjadi pengurangan matriks.
dan hasil output akan terlihat seperti gambar dibawah ini :
     [,1] [,2] [,3]
[1,]   34   22    0
[2,]   74   40    0
[3,]    0   12    5
untuk perkalian matriks bisa diketik kode seperti dibawah ini dan setelah diketik tekan enter :
matrix(x%*%y,nrow=3,ncol=3)
maka akan mucul outputnya seperti dibawah ini :
     [,1] [,2] [,3]
[1,]  127  -61 -112
[2,] 2399 -128 -689
[3,]  378    6 -110

29. Objek pada R adalah simbol atau variable yang mewakili struktur data tertentu pada memori sistem. Objek pada R terdiri dari beberapa tipe / jenis dan tiap tipe tersebut memiliki limitasi dan fungsi yang unik.
Daftar tipe objek yang terdapat pada R adalah sebagai berikut :
a. Vector
b. List
c. Language objects
d. Symbol objects
e. Expression objects
f. Function objects
g. NULL
h. Builtin objects and special forms
i. Promise objects
j. Dot-dot-dot
k. Environments
l. Pairlist objects
m. The “Any” type

30. Frame Data adalah list dengan kelas “data.frame”. Sebagai catatan, ada emapat hal pembatasan suatu list diubah menjadi data frame, yakni:
 − Komponennya harus berupa vektor (numeric, karakter atau logika), faktor, matriks numeric, list, atau data frame lainnya. 
− Matriks, list, dan data frame menyediakan banyak variable untuk data frame sebanyak kolom, elemen atau variable yang dimiliki/didefinisikan sebelumnya.
 − Struktur vektor yang ditampilkan dalam bentuk variable suatu data frame harus memiliki panjang yang sama, struktur matriknya harus mempunyai ukuran baris yang sama. 
Dalam praktiknya, data frame sering digunakan dalam bentuk matriks.

Data frame digunakan untuk menyimpan data tabel (persegi).
Merupakan bentuk khusus dari list, dimana setiap komponennya punya jumlah unsur yang sama
Setiap komponen dari data frame bisa dianggap sebagai kolom, dan panjang (length) dari setiap komponen tsb bisa dianggap sebagai banyaknya baris
Tidak seperti matriks, data frame dapat berisi komponen komponen berbeda jenis.

Data frame adalah struktur data yang paling banyak dipakai dalam R. Gunakan fungsi data.frame() untuk membuatnya.
>Tim <- c (“Persib”,”Arema”,”Persipura”,”SFC”,”Persija”)
>menang <- c (0,1,1,0,0)
>seri <- c (1,0,1,0,1)
>kalah <- c (1,1,0,2,0)
>ILS <- data.frame (tim,menang,seri,kalah)
>ILS



31. Cara mengkombinasikan data vektor menjadi data frame
Contoh vektor
Died.At <- c(22,40,72,41)
Writer.At <- c(16, 18, 36, 36)
First.Name <- c("John", "Edgar", "Walt", "Jane")
Second.Name <- c("Doe", "Poe", "Whitman", "Austen")
Sex <- c("MALE", "MALE", "MALE", "FEMALE")
Date.Of.Death <- c("2015-05-10", "1849-10-07", "1892-03-26","1817-07-18")

a. Data frame harus memiliki variabel yang sama panjang. Periksa apakah Anda telah menempatkan jumlah yang sama dari argumen di semua c ( ) fungsi yang Anda tetapkan untuk vektor dan bahwa Anda telah menunjukkan string dari kata-kata dengan " ".
b. Kombinasikan vektor menjadi data frame dengan menggunakan fungsi data.frame()
writers_df <- data.frame(Died.At, Writer.At, First.Name, Second.Name, Sex, Date.Of.Death) 
c. Perhatikan bahwa ketika Anda menggunakan fungsi data.frame ( ), variabel karakter diimpor sebagai faktor atau variabel kategori. Gunakan fungsi str ( ) untuk mengenal lebih lanjut tentang frame data Anda.
str(writers_df)
## 'data.frame' :     4 obs. of  6 variables:
##  $ Died.At             : num  22 40 72 41
##  $ Writer.At          : num  16 18 36 36
##  $ First.Name       : Factor w/ 4 levels "Edgar","Jane",..: 3 1 4 2
##  $ Second.Name  : Factor w/ 4 levels "Austen","Doe",..: 2 3 4 1
##  $ Sex                     : Factor w/ 2 levels "FEMALE","MALE": 2 2 2 1
##  $ Date.Of.Death : Factor w/ 4 levels "1817-07-18","1849-10-07",..: 4 2 3 1 
d. Catatan bahwa jika Anda lebih tertarik dalam memeriksa baris pertama dan baris terakhir dari frame data Anda, Anda dapat menggunakan fungsi head() dan tail(), masing-masing.
e. Anda melihat bahwa First.Name , Second.Name , Sex dan Date.Of.Death variabel dari frame writers_df data yang semuanya telah dibaca sebagai faktor. Tapi apakah Anda ingin ini?
Untuk variabel First.Name dan Second.Name, Anda tidak ingin ini. Anda dapat menggunakan fungsi I() untuk melindungi mereka. Fungsi ini menghambat interpretasi argumen. Dengan kata lain, hanya dengan sedikit mengubah definisi dari vektor First.Name dan Second.Name dengan penambahan fungsi I() , Anda dapat memastikan bahwa nama-nama yang tepat tidak ditafsirkan sebagai faktor .
Anda dapat menyimpan vektor Sex sebagai faktor, karena hanya ada jumlah terbatas kemungkinan nilai bahwa variabel ini dapat memiliki.
Juga untuk Date.of.Death variabel Anda tidak ingin memiliki faktor. Akan lebih baik jika nilai-nilai terdaftar sebagai tanggal. Anda dapat menambahkan fungsi as.Date ( ) untuk variabel ini untuk memastikan hal ini terjadi.
Died.At <- c(22,40,72,41)
Writer.At <- c(16, 18, 36, 36)
First.Name <- I(c("John", "Edgar", "Walt", "Jane"))
Second.Name <- I(c("Doe", "Poe", "Whitman", "Austen"))
Sex <- c("MALE", "MALE", "MALE", "FEMALE")
Date.Of.Death <- as.Date(c("2015-05-10", "1849-10-07", "1892-03-26","1817-07-18"))
writers_df <- data.frame(Died.At, Writer.At, First.Name, Second.Name, Sex, Date.Of.Death)
str(writers_df) 

## 'data.frame':    4 obs. of  6 variables:
##  $ Died.At      : num  22 40 72 41
##  $ Writer.At    : num  16 18 36 36
##  $ First.Name   :Class 'AsIs'  chr [1:4] "John" "Edgar" "Walt" "Jane"
##  $ Second.Name  :Class 'AsIs'  chr [1:4] "Doe" "Poe" "Whitman" "Austen"
##  $ Sex          : Factor w/ 2 levels "FEMALE","MALE": 2 2 2 1
##  $ Date.Of.Death: Date, format: "2015-05-10" "1849-10-07" ... 
f. Jika Anda menggunakan fungsi lain seperti read.table() atau fungsi lain yang digunakan untuk input data, seperti read.csv() dan read.delim(), bingkai data dikembalikan sebagai hasilnya. Dengan cara ini, file yang terlihat seperti ini di bawah atau file yang memiliki pembatas lainnya, akan dikonversi ke data frame setelah mereka membaca ke R dengan fungsi-fungsi ini.
22, 16, John, Doe, MALE, 2015-05-10
40, 18, Edgar, Poe, MALE, 1849-10-07
72, 36, Walt, Whitman, MALE, 1892-03-26
41, 36, Jane, Austen, FEMALE, 1817-07-18
32. Ada dua cara untuk mengakses nilai-nilai ini data frame, yaitu:
a. Through The Variable Names
1) Pertama, dapat mencoba untuk mengakses hanya dengan memasukkan nama frame data dalam kombinasi dengan nama variabel:
writers_df$Age.As.Writer
2) Catatan bahwa jika Anda mengubah salah satu nilai di Era vektor bahwa perubahan ini tidak akan dimasukkan ke dalam frame data :
3) Pada akhirnya , dengan metode ini mengakses nilai-nilai , Anda hanya membuat copy dari variabel tertentu ! Itu sebabnya setiap perubahan variabel tidak mengubah variabel frame data ini
b. Through The [,] and $ Notations
1) Mengakses value dari data frame juga dapat dilakukan dengan notasi [,]:
writers_df [1:2,3] #Value located on the first and second row, third column
2) Gives
## [1] "John"  "Edgar"
writers_df[, 3] #Values located in the third column
3) Gives
## [1] "John"  "Edgar" "Walt"  "Jane"
writers_df[3,] #Values located in the third row
4) Gives
##   Age.At.Death Age.As.Writer Name Surname Gender      Death
## 3           72            36 Walt Whitman   MALE 1892-03-26
5) Ingat bahwa dimensi data frame ' didefinisikan sebagai baris dengan kolom. Alternatif notasi [,] adalah dengan notasi $
writers_df$Age.At.Death
6) Gives
## [1] 22 40 72 41
writers_df$Age.At.Death[3] #Value located on third row of the column `Age.At.Death`
7) Gives
## [1] 72 

33. Untuk memanipulasi data frame dalam R kita dapat menggunakan notasi braket untuk mengakses indeks untuk pengamatan dan variabel. Hal ini paling mudah untuk berpikir dari frame data sebagai persegi panjang data dimana baris adalah pengamatan dan kolom adalah variabel. Sama seperti dalam matriks aljabar, indeks untuk persegi panjang data mengikuti prinsip RXC; dengan kata lain, indeks pertama adalah untuk Baris dan indeks kedua adalah untuk Kolom [R, C]. Ketika kita hanya ingin subset variabel (atau kolom) kita menggunakan indeks kedua dan meninggalkan indeks kosong pertama.Meninggalkan kosong indeks menunjukkan bahwa Anda ingin menyimpan semua elemen dalam dimensi itu. Pada contoh pertama kita membuat frame datahsb3 hanya berisi variabel id , membaca dan menulis , tetapi semua pengamatan dari aslinya frame data hsb2.small . Untuk mengetahui variabel yang sesuai dengan yang nomor indeks kita menggunakan nama-nama fungsi, yang akan daftar nama-nama variabel dalam urutan di mana mereka muncul dalam frame data. Dari daftar ini kita melihat bahwa id adalah variabel 1, membaca adalah variabel 7 dan menulis adalah variabel 8. Kita tidak bisa mengacu pada variabel dengan nama mereka sendiri sampai kita telah terpasang data.
hsb2.small  <-  read.csv ( "http://www.ats.ucla.edu/stat/data/hsb2_small.csv" )

# Menggunakan nama fungsi untuk melihat nama-nama variabel dan yang kolom 
# data yang mereka sesuai 
nama (hsb2.small)
## [1] "id" "perempuan" "ras" "ses" "schtyp" "prog" "membaca"   
## [8] "menulis" "matematika" "ilmu" "socst"
(hsb3  <-  hsb2.small [,  c ( 1 ,  7 ,  8 )])
## Id baca tulis
## 1 70 57 52
## 2 121 68 59
## 3 86 44 33
## 4 141 63 44
## 5 172 47 52
## 6 113 44 52
## 7 50 50 59
## 8 11 34 46
## 9 84 63 57
## 10 48 57 55
## 11 75 60 46
## 12 60 57 65
## 13 95 73 60
## 14 104 54 63
## 15 38 45 57
## 16 115 42 49
## 17 76 47 52
## 18 195 57 57
## 19 114 68 65
## 20 85 55 39
## 21 167 63 49
## 22 143 63 63
## 23 41 50 40
## 24 20 60 52
## 25 12 37 44
Jika variabel kita ingin berada di kolom berturut-turut, kita dapat menggunakan notasi colon daripada daftar mereka menggunakan c fungsi. Pada contoh berikut kita membuat frame data hsb4 yang berisi empat variabel pertama hsb2.small .
(hsb4  <-  hsb2.small [,  1 : 4 ])
## Id ses ras perempuan
## 1 70 0 4 1
## 2 121 1 4 2
## 3 86 0 4 3
## 4 141 0 4 3
## 5 172 0 4 2
## 6 113 0 4 2
## 7 50 0 3 2
## 8 11 0 1 2
## 9 84 0 4 2
## 10 48 0 3 2
## 11 75 0 4 2
## 12 60 0 4 2
## 13 95 0 4 3
## 14 104 0 4 3
## 15 38 0 3 1
## 16 115 0 4 1
## 17 76 0 4 3
## 18 195 0 4 2
## 19 114 0 4 3
## 20 85 0 4 2
## 21 167 0 4 2
## 22 143 0 4 2
## 23 41 0 3 2
## 24 20 0 1 3
## 25 12 0 1 2
2. pengamatan Subsetting
Kami subset pengamatan juga menggunakan notasi bracket tapi sekarang kita menggunakan indeks pertama dan meninggalkan indeks kedua kosong. Hal ini menunjukkan bahwa kita ingin semua variabel untuk pengamatan tertentu. Pada contoh pertama kita membuat frame data hsb5 , yang berisi 10 pengamatan pertama hsb2.small .
(hsb5  <-  hsb2.small [ 1 : 10 ,])
## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 1 70 0 4 1 1 1 57 52 41 47 57
## 2 121 1 4 2 1 3 68 59 53 63 61
## 3 86 0 4 3 1 1 44 33 54 58 31
## 4 141 0 4 3 1 3 63 44 47 53 56
## 5 172 0 4 2 1 2 47 52 57 53 61
## 6 113 0 4 2 1 2 44 52 51 63 61
## 7 50 0 3 2 1 1 50 59 42 53 61
## 8 11 0 1 2 1 2 34 46 45 39 36
## 9 84 0 4 2 1 1 63 57 54 58 51
## 10 48 0 3 2 1 2 57 55 52 50 51
Kami juga dapat subset pengamatan berdasarkan tes logis. Pada contoh berikut kita membuat frame data hsb6 , yang hanya berisi pengamatan yang ses= 1. Untuk kesetaraan logis kita perlu menggunakan notasi tanda sama ganda. Kita juga perlu merujuk ke variabel, ses dalam frame data hsb2.small , yang kami menggunakan $ .
(hsb6  <-  hsb2.small [hsb2.small $ ses  ==  1 ,])
## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 1 70 0 4 1 1 1 57 52 41 47 57
## 15 38 0 3 1 1 2 45 57 50 31 56
## 16 115 0 4 1 1 1 42 49 43 50 56
Pada contoh sebelumnya kita menggunakan tes logis untuk subset pengamatan, tetapi kami hanya diuji untuk satu variabel yang sama dengan nilai tunggal.Kami juga dapat subset menggunakan uji logis yang akan menguji satu variabel yang sama dengan unsur-unsur dalam daftar, dan kami melakukan ini dengan menggunakan % di% fungsi. Pada contoh berikut kita membuat frame data hsb7 , yang berisi pengamatan di mana id sama dengan 11, 12, 20, 48, 86 atau 195.
(hsb7  <-  hsb2.small [hsb2.small $ id  % di%  c ( 12 ,  48 ,  86 ,  11 ,  20 ,  195 ),])
## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 3 86 0 4 3 1 1 44 33 54 58 31
## 8 11 0 1 2 1 2 34 46 45 39 36
## 10 48 0 3 2 1 2 57 55 52 50 51
## 18 195 0 4 2 2 1 57 57 60 58 56
## 24 20 0 1 3 1 2 60 52 57 61 61
## 25 12 0 1 2 1 3 37 44 45 39 46
Hal ini juga memungkinkan untuk menggabungkan tes logis. Pada contoh berikut kita membuat frame data hsb8 , yang hanya berisi pengamatan mana ses= 3 dan perempuan = 0. Di sini untuk menghindari jenis hsb2.small beberapa kali, kita menggunakan dengan fungsi untuk membiarkan R tahu bahwa itu harus mencari ses dan perempuan dalam hsb2.small frame data.
(hsb8  <-  hsb2.small [ dengan (hsb2.small, ses  ==  3  &  perempuan  ==  0 ),])
## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 3 86 0 4 3 1 1 44 33 54 58 31
## 4 141 0 4 3 1 3 63 44 47 53 56
## 13 95 0 4 3 1 2 73 60 71 61 71
## 14 104 0 4 3 1 2 54 63 57 55 46
## 17 76 0 4 3 1 2 47 52 51 50 56
## 19 114 0 4 3 1 2 68 65 62 55 61
## 24 20 0 1 3 1 2 60 52 57 61 61

The bagian fungsi dengan pernyataan logis akan membiarkan Anda subset frame data dengan observasi. Pada contoh berikut write.50 frame data hanya memiliki satu pengamatan yang nilai-nilai variabel menulis lebih besar dari 50. Perhatikan bahwa salah satu fitur yang mudah dari bagian fungsi, adalah R mengasumsikan nama variabel berada dalam frame data menjadi bagian, sehingga tidak perlu untuk memberitahu R di mana untuk mencari tulis .
(write.50  <-  bagian (hsb2.small, menulis  >  50 ))


## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 1 70 0 4 1 1 1 57 52 41 47 57
## 2 121 1 4 2 1 3 68 59 53 63 61
## 5 172 0 4 2 1 2 47 52 57 53 61
## 6 113 0 4 2 1 2 44 52 51 63 61
## 7 50 0 3 2 1 1 50 59 42 53 61
## 9 84 0 4 2 1 1 63 57 54 58 51
## 10 48 0 3 2 1 2 57 55 52 50 51
## 12 60 0 4 2 1 2 57 65 51 63 61
## 13 95 0 4 3 1 2 73 60 71 61 71
## 14 104 0 4 3 1 2 54 63 57 55 46
## 15 38 0 3 1 1 2 45 57 50 31 56
## 17 76 0 4 3 1 2 47 52 51 50 56
## 18 195 0 4 2 2 1 57 57 60 58 56
## 19 114 0 4 3 1 2 68 65 62 55 61
## 22 143 0 4 2 1 3 63 63 75 72 66
## 24 20 0 1 3 1 2 60 52 57 61 61

Tidak ada batas untuk berapa banyak pernyataan logis dapat dikombinasikan untuk mencapai subsetting yang diinginkan. Frame data write.1 hanya memiliki satu pengamatan yang nilai-nilai variabel menulis lebih besar dari 50 dan untuk yang variabel membaca lebih besar dari 60.
(write.1  <-  bagian (hsb2.small, menulis  >  50  &  baca  >  60 ))

## Id perempuan ras ses schtyp prog baca tulis matematika socst ilmu
## 2 121 1 4 2 1 3 68 59 53 63 61
## 9 84 0 4 2 1 1 63 57 54 58 51
## 13 95 0 4 3 1 2 73 60 71 61 71
## 19 114 0 4 3 1 2 68 65 62 55 61
## 22 143 0 4 2 1 3 63 63 75 72 66


Hal ini dimungkinkan subset kedua baris dan kolom menggunakan bagian fungsi. The pilih Argumen memungkinkan Anda bagian variabel (kolom). Frame data write.2 hanya memiliki satu variabel menulis dan membaca dan kemudian hanya pengamatan kedua variabel mana nilai-nilai variabel menulis lebih besar dari 50 dan nilai-nilai dari variabel membaca lebih besar dari 65.
(write.2  <-  bagian (hsb2.small, menulis  >  50  &  baca  >  60 ,  pilih  =  c (write, read)))

## tulis baca
## 2 59 68
## 9 57 63
## 13 60 73
## 19 65 68
## 22 63 63


Dalam frame data write.3 hanya memiliki satu pengamatan di variabel baca melalui ilmu pengetahuan yang nilai-nilai dalam variabel ilmu kurang dari 55.
(write.3  <-  bagian (hsb2.small, ilmu  <  55 ,  pilih  = baca : ilmu))


## Baca tulis ilmiah matematika
## 1 57 52 41 47
## 4 63 44 47 53
## 5 47 52 57 53
## 7 50 59 42 53
## 8 34 46 45 39
## 10 57 55 52 50
## 11 60 46 51 53
## 15 45 57 50 31
## 16 42 49 43 50
## 17 47 52 51 50
## 20 55 39 57 53
## 25 37 44 45 39


3. Subsetting kedua variabel dan pengamatan
Kita bisa subset variabel dan pengamatan dengan hanya menggabungkan dua metode di atas dari subsetting. Kami melakukannya dengan subsetting menggunakan kedua indeks pada saat yang sama. Pada contoh berikut kita membuat frame data hsb9 di mana kita tetap hanya variabel id , perempuan ,ras , ses dan membaca dan hanya pengamatan mana ses = 3. Perhatikan lagi bahwa karena kita tidak menggunakan bagian , kita harus membiarkan R tahu di mana untuk menemukan variabel ses oleh eksplisit menunjuk ke hsb2.small .


# Menggunakan nama fungsi untuk melihat nama-nama variabel dan yang kolom 
# data yang mereka sesuai 

nama (hsb2.small)


## [1] "id" "perempuan" "ras" "ses" "schtyp" "prog" "membaca"   
## [8] "menulis" "matematika" "ilmu" "socst"
(hsb9  <-  hsb2.small [hsb2.small $ ses  ==  3 ,  c ( 1 : 4 ,  7 )])
## Ses ras id perempuan baca
## 3 86 0 4 3 44
## 4 141 0 4 3 63
## 13 95 0 4 3 73
## 14 104 0 4 3 54
## 17 76 0 4 3 47
## 19 114 0 4 3 68
## 24 20 0 1 3 60
