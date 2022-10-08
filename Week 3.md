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
   <div align="justify">Object merupakan tipe data yang terdiri dari method (function) dan property (variabel). Sama dengan Array, Object dapat menampung banyak data dengan tipe data yang berbeda. </div> <br/>

   Strukur dari Object dan cara aksesnya: <br/>
   
   ```js
      let data = {
         id:1,
         nama:"Hafi Ihza Farhana",
         menikah:false,
         sayHai:() => {
            console.log("Hai")
         }
      }
      
      console.log(data.nama); //mendapatkan data nama dengan dot natation
      console.log(data.sayHai()); //mendapatkan method sayHai dengan pesan "Hai"
      
      data.nama="Karl Marx"; //mengganti property nama dari "Hafi Ihza Farhana" ke "Karl Marx"
      
      data.umur = 20; //menambah property umur yang bernilai 20
      
      delete data.umur; //menghapus property umur
   ```
   
   <br/>
   Apabila Array disimpan di dalam kurung siku `[]`, maka Object disimpan di dalam kurung kurawal `{}`. Selain itu, Object dapat diakses dengan 2 cara yaitu dot notation `.` dan bracket notation `[]`. <br/>
   
   Juga terdapat nested object atau object di dalam object : <br/>
   
   ```js
      let data = {
         id:1,
         nama:"Hafi Ihza Farhana",
         menikah:false,
         sayHai:() => {
            console.log("Hai")
         },
         detail:{
            pendidikan:"S1",
            jurusan:"Informatika"
         }
      }
      
      //Cara akses
      console.log(data.detail.pendidikan)
   ```
   
   <br/><br/>
   
## 3 Struktur Data Array of Object
   <div align="justify">Merupakan Object atau sekumpulan Object yang ada di dalam Array. Array of object biasanya di dapatkan saat mengerjakan sebuah proyek dengan menggunakan JSON.</div> <br/>
   
   cara akses Array of Object:
   
   ```js
      let data = [
         {
            id:1,
            nama:"Hafi"
         },
         {
            id:2,
            nama:"Ihza"
         },
         {
            id:3,
            nama:"Farhana"
         }
      ]
      
      //cara akses manual
      console.log(data[0].nama) //mendapatkan index Array ke 0 dengan key nama akan menghasilkan "hafi"
      
      //cara akses dengan looping
      data.map((e) => {
         return e.id +" "+ e.nama;
      })
      
      //cara akses looping tidak hanya dengan menggunakan map, bisa menggunakan perulangan for, forEach, dll
   ```
   
   <br/>
   Perbedaan dari Array sebelumnya, Array sebelumnya menyimpan data primiif tanpa objek, sedangkan Array of Object akan menyimpan data di dalam Object.
   
   <br/><br/>

## 4 Program Rekursif
   <div align="justify">Merupakan sebuah fungsi yang memanggil dirinya sendiri sampai kondisi tertentu. Apabila tidak ada kondisi yang menghentinkanya, maka akan terjadi looping forever yang menyebabkan stack overflow (memory yang dipakai melampaui batas). </div> <br/>
   
   Ketentuan dari rekursif: <br/>
   1) Harus memiliki kondisi untuk menyatakan berhenti.<br/>
   2) Memanggil dirinya sendiri dengan cara dikurangi. <br/>

   Contoh rekursif: <br/>
   
   ```js
      function faktorial(n){
        if(n == 1){
          return 1;
        } else{
          return n * faktorial(n-1)
        }
      }

      console.log(faktorial(5));
   ```
   
   <br/>
   Fungsi di atas merupakan fungsi rekursif untuk menjadi nilai faktorial. 
   
   <br/><br/>

## 5 Memanipulasi Data Menggunakan Web Storage
## 6 Asynchronous Pada JavaScript
## 7 Mengambil Data API Menggunakan Fetch


