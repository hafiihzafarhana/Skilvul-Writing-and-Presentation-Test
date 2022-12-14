# Writing and Presentation Week 2
## JavaScript Dasar - Scope and Function

- ### Pemahaman tentang scope
  <div align="justify">Scope merupakan cakupan JavaScript untuk mendefinisikan wilayah yang bisa diakses oleh ekspresi dan nilai. Terdapat 3 jenis scope di     dalam JavaScript: </div> <br/>
  
  a) Block Scope <br/>
     Setelah tahun 2015, ES6 memperkenalkan `let` dan `const`. Kedua keyword yang digunakan untuk mendeklarasikan variabel memberikan block scope pada            JavaScript. Pada contohnya variabel yang berada di `{}` tidak dapat diakses keluar. Contoh: <br/>
     
     Untuk let:<br/>
     
     ```js
        {
          let nama = "Hans";
          console.log("dapat diakses disini")
        }
        
        console.log("tidak dapat diakses disini")
        
        Error: Uncaught ReferenceError: x is not defined
     ```
     
     <br/>
     
     Untuk const:<br/>
     
     ```js
        {
          let nama = "hans";
          console.log("dapat diakses disini")
        }
        
        console.log("tidak dapat diakses disini")
        
        Error: Uncaught ReferenceError: x is not defined
     ```
     
     <br/>
     
     Untuk var:<br/>
     
     ```js
        {
          let nama = "hans";
          console.log("dapat diakses disini")
        }
        
        console.log("dapat diakses disini")        
     ```
     
     Catatan: keyword `var` tidak akan error karena tidak memiliki block scope.
     <br/>
     
  b) Global Scope
     Merupakan variabel yang dideklarasi di luar function. Variabel global dapat dideklarasikan dimanapun. Variabel dengan keywords `var`, `let`, dan `const      ` dapat dideklarasikan secara global. <br/>
     
     ```js
        var a = "keren sekali" //dideklarasikan secara global
        let b = "hebat sekali" //dideklarasikan secara global
        const b = "mantap sekali" //dideklarasikan secara global
     ```
     
     <br/>
     Namun, ada sedikit perbedaan apabila ingin mendeklarasikan variabel tanpa sebuah keyword, maka variabel tersebut akan bertipe global.
     <br/>
     
     ```js
        hasil()
        
        console.log(tanpaKeywords) // berhasil
     
        function hasil(){
          tanpaKeywords = "tanpa keywords"
        }
     ```
     
     <br/>
     Hal seperti itu tidak disarankan dan dapat menyebabkan masalah nantinya. Dapat diselesaikan dengan cara : <br/>
     
     ```js
      "use strict" //dideklarasikan di awal baris;
     ```
     
  c) Function Scope
     Merupakan cakupan yang hanya dapat mendeklarasikan variabel di dalam sebuah fungsi. Tidak dapat diakses di luar fungsi tersebut. Contoh:
     <br/>
     
     ```js
      function data(){
        var a = "hai"
        console.log(a + "berhasil")
      }
      
      console.log("gagal") //gagal
      
      data()
     ```
     
     <br/>
 
- ### Membuat sebuah fungsi
  <div align="justify">Fungsi (function) di dalam pemrograman merupakan program yang melakukan tugas tertentu (block code) dan dapat dipanggil terus menerus. Biasanya setiap bahasa pemrograman memiliki fungsi sendiri (built-in functions). Namun, dapat membuat sebuah fungsi sendiri.</div>
  <br/>
  
  Cara membuat fungsi di javaScript ada 2: <br/>
  Normal function: <br/>
  
  ```js
    function data(param1, param2){
      let jumlah = param1 + param2;
      return jumlah;
    }
    
    let hasil = data(5,5);
    console.log(hasil);
  ```
  
  <br/>
  Arrow function: <br/>
  
  ```js
    const data = (param1,param2) => {
      let jumlah = param1 + param2;
      return jumlah;
    }
    
    let hasil = data(5,5);
    console.log(hasil);
  ```
  
  <br/>
  Hal yang membedakan dari kedua jenis fungsi tersebut adalah sintaksnya. <br/>
  
  Catatan:<br/>
  1) Pada normal function awal deklarasi menggunakan `function`, sedangkan arrow function menggunakan keywords `let`, `const`, dan `var`. <br/>
  2) Di dalam `()` pada fungsi disebut parameter. <br/>
  3) Di dalam `{}` pada fungsi merupakan function scope. <br/>
  4) Di dalam fungsi terdapat `return` digunakan untuk mengembalikan sebuah nilai. <br/>
  5) Variabel di dalam fungsi tidak dapat dipanggil di luar fungsi tersebut. <br/>
  <br/>
  
  Selain ada fungsi yang dapat dibuat sendiri, juga terdapat fungsi yang dipanggil berdasarkan library yaitu built in function. <br/>
  Contoh:<br/>
  
  ```js
    int a = 10;
    console.log(a.toString()); // digunakan untuk merubah angka menjadi sebuah string
  ```
  
  <br/>

- ### Penyelesaian error dan bug pada JavaScript Dasar - Scope and Function
  Error merupakan sebuah program yang gagal untuk berjalan, sedangkan bug merupakan kesalahan yang terdapat pada sebuah sistem yang menyebabkan program         tidak berjalan secara normal. Lalu, untuk menyelesaikan error dapat menggunakan `try{....} catch(error){....}` dan untuk mengatasi sebuah bug dapat           dilakukan dengan metode debugging.<br/>
      
  Konsep penyelesain error dengan `try{....} catch(error){....}` : <br/>
  
  ```js
    try{
      penambahan(5,5);
    } catch(error){
      console.log(error.message);
    }
  ```
      
  <br/>
  Pada program di atas akan menghasilkan sebuah error karena fungsi `penambahan()` belum dideklarasikan. <br/>
  
  Catatan: <br/>
  1) Pernyataan `try{....}` digunakan untuk menjalankan sebuah program. <br/>
  2) Pernyataan `catch(error){....}` digunakan untuk mencari tahu atau mendapatkan sebuah error jika hal tersebut terjadi. <br/><br/>

  Properti yang digunakan pada saat menangani sebuah error dengan `try{....} catch(error){....}` : <br/>
  1) `name` akan mengembalikan jenis error. <br/>
  2) `message` akan mengembalikan pesan error. <br/>

  Jenis-jenis nama pada error : <br/>
  1) `EvalError` terjadi pada fungsi `eval()`. <br/>
  2) `RangeError` terjadi karena angka yang melebihi jarak angka yang ditetapkan. <br/>
  3) `ReferenceError` terjadi karena terdapat variabel yang belum dideklarasikan <br/>
  4) `SyntaxError` terjadi karena sintaks salah. <br/>
  5) `TypeError` terjadi karena sebuah nilai yang tidak sesuai dengan tipe nya. <br/>
  6) `URIError` terjadi karena menggunakan karakter yang dilarang di dalam URI.

  <br/><br/>
  
  Lalu, untuk mengatasi bug dapat dilakukan dengan debugging. Debugging dapat memberikan informasi kepada programmer lokasi program untuk berjalan dan berhenti. Di dalam JavaScript ada 2 cara yaitu: <br/>
  
  ```js
    console.log("debug");
    
    atau
    
    debugger;
  ```
  
  <br/>
  Adanya hal itu, dapat mengetahui lokasi pemrograman dimulai dan berhenti.
  
  <br/><br/>

## JavaScript Dasar - DOM Manipulation

- ### Memanipulasi HTML dan DOM
  <div align="justify">DOM (Document Object Model) merupakan cara untuk memanipulasi style, konten, dan element pada website. Setelah website dimuat, maka akan ada DOM yang terbentuk menjadi sebuah pohon dan terdiri dari parent & child.</div> <br/>
  
  <img src="https://user-images.githubusercontent.com/71125093/193417882-ecb42f58-a910-4145-adec-ffc3f7a89734.png" width="400" />
  <br/>
  
  DOM juga merupakan objek yang terdiri dari properties dan method. Lalu, cara untuk mendapatkan element HTML : <br/>
  
  ```md
    a) document.getElementById(id) // mendapatkan element berdasarkan id. Akan mendapatkan 1 element spesifik
    b) document.getElementsByTagName(name) // mendapatkan banyak element (collections) berdasarkan tag name
    c) document.getElementsByClassName(name) // mendapatkan banyak element (collections) berdasarkan class name
    d) document.querySelector(css selector) //mendapatkan satu element berdasarkan CSS selector
    e) document.querySelectorAll(css selector) // mendapatkan banyak element (collections) berdasarkan CSS selector
    f) parentElement // digunakan untuk menyeleksi parent dari suatu elemen 
    g) nextElementSibling // digunakan untuk menyeleksi elemen setelahnya dalam 1 parent
    h) previousElementSibling // digunakan untuk menyeleksi elemen sebelumnya dalam 1 parent
  ```
  
  <br/>
  Praktek:
  
  `<html>`
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <p id="para1">Hai</p> <!-- berdasarkan id -->
        
        <h1>Halo</h1> <!-- berdasarkan tag name -->
        <h1>Keren</h1>
        
        <ul>
          <li class="item">1</li> <!-- berdasarkan class nname -->
          <li class="item">2</li>
          <li class="item">3</li>
          <li class="item">4</li>
        </ul>
        
        <div class="box"></div> <!-- berdasarkan css selector -->
        
        <p class="orang">Hafi Ihza Farhana</p>
        <p class="orang">Hafi Ihza</p>
        <p class="orang">Hafi</p>
        
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    let a = document.getElementById("para1") // berdasarkan id
    
    let b = document.getElementsByTagName("h1") //berdasarkan tag name
    
    let c = document.getElementsByClassName("item") //berdasarkan class name
    
    let d = document.querySelector("div.box") // berdasarkan css selector (hanya mendapatkan 1 element HTML)
    
    let d = document.querySelectorAll("p.orang") // berdasarkan css selector (mendapatkan banyak element HTML)
  ```
  
  <br/>
  Cara merubah konten HTML: <br/>
  
  `<html>`
  
  <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <div id="para1">Hai</div>
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    document.getElementById("para1").innerHTML  = "<h1>teks baru</h1>"
  ```
  
  <br/>
  Catatan: merubah konten dengan `innerHTML` tidak hanya merubah teks, melainkan bisa saja merubah element HTML. <br/>
  
  Cara merubah nilai pada atribut HTML : <br/>
  
  `<html>`
  
  <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <img src="pony1.png" id="img1"/>
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    document.getElementById("img1").src  = "pony2.png"
    
    // struktur
    // document.getElementById("img1").attribute   = nilai
  ```
  
  <br/>
  Cara menambah langsung element pada HTML dengan JavaScript : <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <p>Hai</p>
          <script>
            document.write("Hafi Ihza Farhana")
          </script>
        <p>Selamat tinggal</p>
      </body>
    </html>
  ```
  
  <br/>
  Cara memanipulasi element HTML : <br/>
  
  ```md
    a) document.createElement(e) // membuat element HTML
    b) document.removeChild(e) // menghapus element HTML
    c) document.appendChild(e) // menggabungkan element HTML
    d) document.replaceChild(baru, tua // mengubah element HTML yang lam dengan yang baru
  ```
  
  Praktek Kasus:
  <br/>
  
  `<html>`
  
  ```html
           <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
      </head>
      <body>
          <div class="kontainer">
              <form action="">
                  <input type="text" id="nama" placeholder="isi nama">
                  <button type="submit" id="add">Tambah</button>
              </form>
              <ul class="todo" id="todo">
                  <li>Item</li>
              </ul>
          </div>
          <script src="script.js"></script>
      </body>
      </html>
  ```
  
  ```js
    let tambahButton = document.getElementById("add")
      let inputNama = document.getElementById("nama")

      tambahButton.addEventListener("click", (e) => {
          e.preventDefault()
          let valueInputNama = inputNama.value
          if(valueInputNama){
              tambahData(valueInputNama)
          }
      })

      let tambahData = (data) => {
          let list = document.getElementById("todo")
          // create li
          let item = document.createElement('li')
          item.innerText = data
          console.log(list.childNodes)
          list.insertBefore(item, list.childNodes[0])
      }
  ```
  
  <br/>
  Pada contoh kasus di atas merupakan langkah untuk melakukan set data denga JavaScript.
  
 <br/>
 
 Hasil:<br/>
 
 ![Screenshot (180)](https://user-images.githubusercontent.com/71125093/193437664-091b79e9-dd5a-4e7f-b4d9-84e114fd1d03.png)


  Memanipulasi Atribut : <br/>
  
  ```md
  1) setAttribute //untuk menetapkan atribut dengan nilai tertentu
  2) getAttribute //untuk mendapatkan nilai sebuah atribut
  3) removeAttribute //untuk menghapus atribut
  4) hasAttribute // memeriksa element tersebut memilik atribut atau tidak
  ```
  
  <br/>
  Memanipulasi element styling : <br/>
  
  ```md
  1) style.property // untuk mengatur element styling tertentu
  2) getComputedStyle // untuk mendapatkan style
  ```
  
  <br/>
  Events merupakan sebuah kejadian yang dilakukan berdasarkan interaksi pengguna pada webiste. Ada beberapa event, dan ini merupakan yang populer : <br/>
  
  ```md
  1) onchange // Terpicu ketika element dirubah
  2) onclick // Terpic ketika element di klik
  3) ondblclick // Terpicu ketika element di double click
  4) ondrag // Terpicu ketika element di seret
  5) onkeyup // Terpicu ketika key-up ditekan
  6) onload // Terpicu ketika website di load
  ```
  
  <br/>
  Dan masih banyak lagi
  
