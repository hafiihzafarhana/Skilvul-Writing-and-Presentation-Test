# Writing and Presentation Test Week 6
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
- ### Membuat Middleware

## 4 Design database with MySQL
- ### Membuat Diagram Entity
- ### Menentukan Atribut Entity
- ### Menentukan dan Membuat Relasi Entity
