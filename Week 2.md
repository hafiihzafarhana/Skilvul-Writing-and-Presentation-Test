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
 
- ### Membuat sebuah fungsi

- ### Penyelesaian error dan bug pada JavaScript Dasar - Scope and Function


## JavaScript Dasar - DOM Manipulation

- ### Memanipulasi HTML dan DOM
