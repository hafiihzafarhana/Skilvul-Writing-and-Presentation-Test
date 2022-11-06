# Writing and Presentation Test Week 5
## 1 Web Servers & Restful API
- ### Konsep Web Server
  <div align="justify">Web server terdiri dari 2 komponen penting yaitu software dan hardware. Di sisi hardware berfungsi untuk menyimpan web server software dan komponen file website seperti HTML, CSS, dan JS. Di sisi software terdapat HTTP server yang memahami alamat website dan HTTP.</div> <br/>
  <div align="justify">Konsep dari web server adalah apabila ada request dari sisi client atau browser, maka file atau HTTP server akan memberikan response terhadap client. Terdiri dari 2 jenis yaitu static sites dan dynamic sites, static sites hanya request navigasi halaman oleh pengguna dan dynamic sites bisa berupa request data di dalam halaman website dengan menggunakan database.</div>
- ### Konsep Restful API
  <div align="justify">Sebelum memahami konsep Restful API, terdapat sebuat Rest yang merupakan gaya arsitektur yang memudahkan sistem untuk berkomunikasi dengan yang lainya sebagai standart sistem komputer dan website. Lalu, Restfull API merupakan konsep untuk memisahkan antar server dan klien. </div> <br/>
  <div align="justify">Di dalam konsep Rest, implementasi antar klien dan server dapat berdiri sendiri tanpa mengetahui satu sama lain. Hal ini bermaksud segala sesuatu di sisi server dapat berubah sewaktu-waktu tanpa adanya komunikasi dengan sisi klien. </div> <br/>
  <div align="justify">Pembuatan request di Restfull API terdapat beberapa jenis, tetapi yang paling sering digunakan adalag GET untuk mendapatkan data, POST untuk mengirim data, PUT untuk mengupdate data, dan DELETE untuk menghapus data. Juga ada path sebagai endpoint alamat url yang bisa diakses.</div> <br/><br/>

## 2 Node JS
- ### Fundamentarl Node JS
  <div align="justify">Node JS merupakan open source dan back end JavaScript runtime environment yang berjalan di V8 engine dan mengeksekusi JavaScript di luar Web Browser. Node JS sendiri berguna untuk menjalankan script server side yang membuat website menjadi dinamis.</div> <br/>
  <div align="justify">Node JS menggunakan konsep single thread. Namun, seakan-akan Node JS seperti menggunakan konsep multiple thread dengan cara event loop yang berarti memeriksa perintah secara terus menerus apabila ada perintah baru.</div><br/>

- ### Node JS untuk Back End
  <div align="justify">Untuk membantu Node JS dalam menjalankan sebuah Back End diberikan beberapa module populer seperti : </div> <br/>
  
  ```md
    console, digunakan sebagai debug
    process, digunakan untuk menampilkan dan mengontrol process di node.js
    os, digunakan untuk memberikan informasi mengenai sistem operasi komputer
    util, digunakan untuk kebutuhan API di node js
    errors, digunakan untuk mendefinisikan error
    buffer, digunakan untuk mengakses tipe data bytes dan raw
    fs, digunakan untuk berinteraksi dengan file yang ada di luar code
    timers, digunakan untuk mengatur sebuah waktu
  ```
  
  <br/>
  
- ### Membuat Program Node JS
  
  Program dasar untuk Node JS :
  
  ```js
    const http = require('http')
   
    const reqHandler = (req, res) => {
      res.end("Halo dunia");
    }
    
    const server = http.createServer(reqHandler);
    
    server.listen(3001, "localhost", err => {
      if(err){
      return "Salah"
      }
      
      console.log("Server berjalan di port 3001")
      
    })
  ```
  
  <br/> <br/>

## 3 Express Routing & Middleware
- ### Membuat Routing
  <div align="justify">Routing merupakan manajemen endpoint dari sebuah aplikasi atau website untuk melakukan request dan memberikan response oleh client. Terdapat banyak sekali method untuk mengakses routing yaitu : </div> <br/>
  
  ```md
    GET, mendapatkan data
    POST, mengirim data
    PUT, mengupdate data
    DELETE, menghapus data
  ```
  
  <br/>
  
  Cara routing : <br/>
  
  ```js
    app.get('/', (req, res) => {
      res.send("Halo dunia")
    })
    
    app.post('/', (req, res) => {
      res.send("Telah ditambahkan")
    })
    
    app.put('/', (req, res) => {
      res.send("Telah diupdate")
    })
    
    app.delete('/', (req, res) => {
      res.send("Telah dihapus")
    })
    
    app.get('/siswa', (req, res) => {
      res.send("Dapat data siswa")
    })
    
    app.get('/siswa/:id', (req, res) => {
      res.send("Dapat data siswa dengan id")
    })
    
  ```
  
  <br/>

- ### Membuat Middleware
  <div align="justify">Middleware merupakan fungsi yang terdiri dari 3 parameter yaitu req (untuk mendapatkan data), res (memberikan response), dan next (untuk melanjutkan ke route lain yang berhubungan). </div> <br/>
  
  Bentuk middleware : <br/>
  
  ```js
    // application level middleware
    const middle1 = (req,res,next) => {
      console.log("middle 1")
      next()
    }
    
    app.use(middle1)
    
    // router level middleware
    const express = require('express')
    const Router = express.Router()
    const middle2 = (req,res,next) => {
      console.log("middle 2")
      next()
    }
    Router.user(middle2)
    
    // error handling level middleware
    const express = require('express')
    const Router = express.Router()
    const middle3 = (err,req,res,next) => {
      console.log("middle 3")
      next()
    }
    Router.user(middle3)
  ```
  
  <br/><br/>

## 4 Design database with MySQL
  Akan ada sebuah studi kasus : <br/>
  
  ```md
    Peminjaman buku perpustakaan oleh seorang mahasiswa.
    1) Mahasiswa dapat meminjam banyak buku di perpustakaan dan banyak buku dapat dipinjam oleh banyak mahasiswa
    2) Apabila mahasiswa telat mengembalikan sebuah buku akan dikenakan denda untuk tiap bukunya
  ```
  
  <br/>
  
- ### Membuat Diagram Entity
  ![github drawio](https://user-images.githubusercontent.com/71125093/198930036-8b9d8b7f-fec8-4f5b-b710-c45fe09e4167.png)
  
  <br/>
   <div align="justify">Terdapat 3 entitas utama yaitu Mahasiswa, Buku, dan Denda yang memiliki 2 entitas konjungsi yaitu pinjam (Berisi data peminjaman buku) dan bayar (Berisi data pembayaran denda).</div> <br/>
  
- ### Menentukan Atribut Entity
 ![github drawio (1)](https://user-images.githubusercontent.com/71125093/198931539-9276d306-a1f8-4c53-a111-edba948bae65.png)

- ### Menentukan dan Membuat Relasi Entity
  ![github drawio (2)](https://user-images.githubusercontent.com/71125093/198931659-a6843998-aedb-4352-8c12-be38f65099d2.png)

