# Writing and Presentation Week 2
## JavaScript Dasar - Scope and Function

- ### Pemahaman tentang scope
  <div align="justify">Scope merupakan cakupan JavaScript untuk mendefinisikan wilayah yang bisa diakses oleh ekspresi dan nilai. Terdapat 3 jenis scope di dalam JavaScript: </div> <br/>
  
  a) Block Scope <br/>
     Setelah tahun 2015, ES6 memperkenalkan `let` dan `const`. Kedua keyword yang digunakan untuk mendeklarasikan variabel memberikan block scope pada                JavaScript. Pada contohnya variabel yang berada di `{}` tidak dapat diakses keluar. Contoh: <br/>
     
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
  c) Function Scope
 
- ### Membuat sebuah fungsi

- ### Penyelesaian error dan bug pada JavaScript Dasar - Scope and Function


## JavaScript Dasar - DOM Manipulation

- ### Memanipulasi HTML dan DOM
