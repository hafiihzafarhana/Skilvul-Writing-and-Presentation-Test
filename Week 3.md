# Writing and Presentation Test Week 1
## 1 Struktur Data Array
   <div align="justify">Array merupakan sekumpulan penyimpanan atau memory untuk sebuah data yang memiliki tipe data yang sama atau berbeda (Ada beberapa bahasa pemrograman yang bisa menampung Array dengan tipe data yang berbeda). Array terbagi menjadi kumpulan-kumpulan index. Hal tersebut merupakan cara untuk mengakses sebuah data di dalam Array. Nilai awal dari Array adalah 0. </div> <br/>
   
   Gambaran tentang array : <br/>
   
   <img src="https://user-images.githubusercontent.com/71125093/194697201-f5b54153-ff75-4bc4-9c54-0fa2e6207305.png" width="300"/> <br/>
   
   Jadi, nilai "mawar" akan berada di index ke 0 karena merupakan nilai yang paling awal. <br/>
   
   Contoh Array di JavaScript : <br/>
   
   ```js
    const value = [1, "Salak", "Nanas", true, null];
   ```
   
   <br/>
   
   Array di JavaScript dapat memiliki tipe data yang berbeda. <br/>
   
   Cara mengakses Array: <br/>
   
   ```js
    const value = [1, "Salak", "Nanas", true, null];
    
    console.log(value[2]); //mendapatkan data di index ke 2 atau data ke 3 (nanas)
    
    value[0] = 2; //merubah data array di index ke 1 (1) menjadi angka 2
    
    value[value.length] = "data"; //menambah data Array secara manual. Data akan dimasukan ke index Array paling akhir
   ```
   
   <br/>
   <div align="justify">
   Array di atas merupakan konsep untuk Array 1 dimensi. Array dapat memiliki banyak dimensi seperti Array 2 dimensi dan 3 dimensi. Konsepnya tetap sama.
   </div> <br/>
   
   Konsep Array 2 dimensi : <br/>
   <img src="https://user-images.githubusercontent.com/71125093/194697955-21b101eb-e5e5-4997-b65d-99a2f28f92dc.png" width="300"/> <br/>
   
   Contoh Array 2 dimensi di JavaScript : <br/>
   
   ```js
    const value = [["Rusa", "Badak"], ["Kijang", "Beruang"], ["Paus", "Singa"], ["Kelinci", "Kucing"]];
   ```
   
   <br/>
   Array 2 dimensi memiliki cara akses yang sama dengan Array 1 dimensi. <br/><br/>
   
   Array memiliki beberapa method yang sangat membantu: <br/>
   
   ```js
     const value = ["Rusa", "Badak", "Kelinci", "Paus", "Kijang", "Buaya"];
     
     value.push("Panda"); //menambahkan value di akhir
     value.pop(); //menghapus data Array yang terakhir
     value.unshift("Kerang"); //menambah value di awal
     value.shift(); //menghapus data Array yang pertama
     
     //method yang penting pada penerapan proyek nyata
     value.forEach((e) => {
        console.log(e); 
     }) //perulangan untuk mendapatkan data Array
     
     value.map((e) => {
        console.log(e); 
     }) //perulangan untuk mendapatkan data Array
     
     let Badak = value.filter(e => {
        return e == "Badak"
     }) //Untuk mendapatkan data yang bernama Badak
   ```
   
   Tentunya masih banyak lagi Built in method untuk Array. 
   
   <br/> <br/>
  
## 2 Struktur Data Object
## 3 Struktur Data Array of Object
## 4 Program Rekursif
## 5 Memanipulasi Data Menggunakan Web Storage
## 6 Asynchronous Pada JavaScript
## 7 Mengambil Data API Menggunakan Fetch


