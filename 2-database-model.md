## Database Planning

### Database MongoDB



> Mongodb adalah sebua document database dengan skalabiliti dan fleksibiliti dengan query dan indexing yang anda inginkan.



Mongodb adalah database NoSQL (nosequel), disebut database Non Relational System.

Didalam database Mongodb terdapat kumpulan Collections (Table).

​	misalnya:

```
blog
users
reviews
```



Didalam Collection terdapat kumpulan Documents (Row).

​	misalnya: 

	- post
	- user
	- review
	- dll



Gambaran antara Collections dan Documents sbb:

```
blog ----------------------> post
users ---------------------> user
reviews -------------------> review
```



**Document based** Mongodb disebut database berbasis Document: Karena data disimpan didalam document berbentuk key-value pair data structur (NoSQL/No Relational) atau pasangan field dan value, seperti format JSON. Database Normal (Tradisional Database) disimpan di Row dalam Table.

**Scalable** Mudah di distribusikan pada beberapa hardware dengan data besar dan berkembang pesat.

**Flexible** Tidak memerlukan data schema, karena setiap document bisa punya jumlah field dan type field yang berbeda.

**Performan** Embeded data models, sharding, flexible documents, native duplication dsb.

**Free & Open-source**, published dengan SSPL License.



#### Diagram Mongodb & RDBMS

![](images/mongodb1.PNG)



#### Install Database

Lihat tutorial Mediocademy

#### Create Local Database

Lihat tutorial Mediocademy

#### CRUD Creating Documents

Lihat tutorial Mediocademy

#### CRUD Querying (Reading) Documents

Lihat tutorial Mediocademy

#### CRUD Deleting Documents

Lihat tutorial Mediocademy

#### Menggunakan Compass App untuk CRUD Operations

Mongodb Compass adalah GUI Tools sebagai Database Manager untuk operasi tanpa menggunakan Terminal (lebih mudah).

Download Mongodb Compass disini : https://www.mongodb.com/try/download/compass

Sebelum download pilih dulu OS yang anda gunakan.



**Menjalankan Compass**

Sebelum membuat koneksi localhost database, jangan lupa untuk menjalankan Server Mongodb dulu dengan perintah pada Terminal.

```
mongod
```

kemudian buka tab baru pada Terminal, test dengan perintah:

```
mongo
```

perintah ini akan membuka mongo console dan anda dapat melakukan operasi CRUD database disitu via Terminal.

Selanjutnya kembali ke Compass dan langsung klik Connect, dengan form default nya (jangan isi apapun).

Pada project ini kita tidak akan menggunakan database lokal, melainkan database Host pada Cloud Server.



#### Mongodb Atlas

https://www.mongodb.com/cloud/atlas

Untuk yang belum buat akun silahkan klik Try Free button dan isi form register.

Bagi yang sudah punya akun langsung login saja.

**Membuat Project baru**

Kllik tombol "New Project"

Berinama sesuai dengan project kamu.

Contoh beri nama : bentour-app

Klik "Next"

Klik "Create Project"

Setelah Project dibuat kemudia saat nya membuat "Cluster".

Klik "Build a Cluster"

Lanjut Pilih Free Cluster, **M0 Sanbox**  (kecuali jika client mau bayar). 

Cluster Name :  Namanya samain aja dengan nama project supaya gak bingung.

Klik Create Cluster.

Tunggu proses......



#### Konek ke Host database

Klik Cluster pada dashboard mongodb.

Klik Connect button

Klik "Add Your Current IP Address"

Create Mongodb User

username dan password

Klik "Create Mongodb User"

Copy user name dan password nya

Buka file config-env pada project VCS kamu buat seperti ini:

```
...

...

DATABASE_PASSWORD=<paste_password_database_tadi>

```

Kembali ke mogodb atlass, pilih "Connect with Mongodb Compass".

Klik "I have Compass" buat yang sudah donwload compass.

Pilih yang terbaru dari pilihan: "Choose your version of Compass"

Copy the connection string.

Klik "Close".



Kemudian buka Compass kembali

Di menu Top pilih "Connect to..."

Jika muncul popup "Mongodb connection string detected" Klik YES.

Paste kan password mongodb atlas kamu.

Dan klik "CONNECT"



**Membuat database baru**

Klik "CREATE DATABASE"

Beri nama Database: misalnya "bentour".

Collection Name: tours

Lanjut

Klik database bentour

Klik collection tours

Dan kemudian mulia masukan data nya disitu seperti : 

* nama paket tour  : "Lombok".
* price : ....
* rating :
* dst



Kembali ke mongodb atlas

Klik nama cluster yang sudah kamu buat

Klik Tab Collections

Kamu lihat database yang kamu buat tadi di Compass sudah masuk ke Host Mongodb Atlas.



**Pilihan Access Management atau WhiteList IP address**

Pada mongodb atlas menu disamping kiri

Klik Security.

Pilih Tab IP Whitelist.

Klik "ADD IP ADDRESS".

Klik "ALLOW ACCESS FROM ANYWHERE".

 Klik "Confirm".



**Pilihan: Konek mongodb shell **

Mengkoneksikan Terminal (mongodb shell) dengan Host.

Klik button "CONNECT" pada Clusters

Pilih "Connect with Mongo Shell"

Klik "I have the Mongo Shell Installed"

Copy connection string nya

Buka mongo shell pada Terminal

Dan paste string tsb di Terminal, ENTER.

Masukan password anda di Mongodb Atlas

Dan Terminal anda sudah terkoneksi dengan shell Host mongodb atlas.



selesai lanjut bab berikutnya













 

