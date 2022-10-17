# Writing and Presentation Test Week 4
## 1 Git dan GitHub Lanjutan
- ### Alasan Git dan GitHub menjadi alat yang wajib digunakan
  <div align="justify">Seorang programmer tidak akan bekerja sendirian. Seorang programmer pasti akan bekerja dengan tim. Namun, hal ini akan menjadi permasalahan karena programmer akan menyalin ulang seluruh file secara manual dan bahkan akan menunggu rekan tim untuk menyelesaikan bagianya masing-masing. Hal ini dapat dipecahkan dengan adanya Git dan GitHub karena menjadi media untuk berkolaborasi dengan tim. Adanya Git dan GitHub memungkinkan programmer bekerja dengan tim tanpa saling menunggu bagianya masing-masing dan tidak perlu meyalin seluruh file, hanya file atau folder yang terupdate saja.</div>
  
- ### Perbedaan Git dan GitHub
  <div align="justify">Git merupakan sebuah tools sebagai Version Control System yang berarti untuk mencatat setiap perubahan file pada suatu proyek yang         dikerjakan sejara individu atau berkelompok. Lalu, GitHub merupakan sebuah cloud base yang digunakan untuk mengupload atau mengelola sebuah file.</div>
  
- ### Alur kerja Git dan GitHub
   a) Instalasi Git
   <br/>
   b) Atur Git dengan cara mengisi username dan email:
   <br/>
   
   ```md
       git config --global user.name = "(siapa?)"
       git config --global user.email = "(siapa@gmail.com)"
   ```
   
   <br/>
   
   c) Apabila ingin memeriksa instalasi berhasil atau tidak, maka ketikan:
   <br/>
   ```md
       git --version
   ```
   
   <br/>
   
   d) Apabila ingin memeriksa _set up_ Git berhasil, maka ketikan:
   <br/>
   
   ```md
       git config --list
   ```
   
   <br/>
   
   e) Setiap repository hanya berisi 1 direktori saja.
   <br/>
   
   f) Terdapat 3 fase yaitu working directory (modified), staging area (staged), dan commit (committed)
      - Fase working directory (modified) merupakan kondisi perubahan sudah dilakukan, tetapi belum ditandai (untracked) dan belum disimpan di version               control.
        <br/>
      - Fase staging area (stagged) merupakan kondisi perubahan telah ditandai (tracked) dan belum disimpan di version control.
        <br/>
      - fase commit (committed) merupakan kondisi perubahan telah disimpan pada version control.  
        <br/>
      
   g) Pembuatan folder repository di GitHub bertujuan untuk menyediakan ruangan terhadap file yang siap di upload di GitHub dengan remote repository
   <br/>
   
   h) Masukan (push) file pada fase commit ke dalam gitHub
   
- ### Membuat repository Git
   <div align="justify">Buat folder dan beberapa file yang dibutuhkan dalam proyek. Lalu, untuk membuat repository Git ketikan :</div>
   <br/>
   
   ```md
       git init
   ```
   
   <br/>
   Studi kasus:
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192151209-ab5944f5-d6b4-48e7-979b-7b01658c1825.png" width="400"/>
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192151131-4345930b-10be-457d-893b-501a55011cdf.png" width="400"/>
   <div align="justify">Apabila telah berhasil membuat repository Git, maka akan dibuatkan folder bernama "git".</div>
   <br/>
   
- ### Melakukan commit pada Git
   <div align="justify">File yang ada di dalam fase stagged akan dirubah ke fase committed dengan mengetikan </div>
   <br/>
   
    ```md
       git commit -m "tuliskan keterangan"
    ```
    
    <br/>
    Studi kasus:
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192151539-db6c3019-85da-4763-be6f-e404e91ec80f.png" width="400"/>
    <br/>
    <div align="justify">Pada gambar di atas adalah proses melakukan commit untuk beberapa file yang telah ditambahkan. File yang telah ditambahkan telah         memasuki fase committed. Pengguna dapat melihat riwayat commit dengan mengetikan </div>
    <br/>
    
    ```md
       git log
    ```
    
    <br/>
    <div align="justify">Dengan metikan hal tersebut, dapat melihat branch, date, author, id commit, pesan commit, dan hal apa saja yang dirubah di dalam file yang telah dirubah dari commit sebelumnya.</div>
    <br/>
    
- ### Melakukan merge pada Git
     Merge digunakan untuk menggabungkan branch cabang ke branch utama untuk digabungkan menjadi proyek yang siap produksi. <br/>
      
     Langkah:
     1) Buat sebuah repository di dalam lokal <br/>
      
       git init
      
     <br/>
     
     2) Lakukan proses ke staging area <br/>
     
       
       git add .
       
     
     <br/>
     
     3) Lakukan commit dengan branch apapun (Contoh kali ini adalah main) <br/>

       git commit -m "awal"
      
     <br/>
      
     4) Buat branch baru (Contoh kali ini adalah fiturA) <br/>

       git branch fiturA
      
     <br/>
     
     5) Pindah dari branch main ke Branch fiturA <br/>

       git checkout fiturA
      
     <br/>
      
     6) Lakukan proses stagged sampai commit dengan branch fiturA <br/>

     7) Setelah selesai, pindah branch fiturA ke branch main <br/>

     8) Lakukan merge dari untuk memasukan branch fiturA ke main <br/>
        
       git merge fiturA
     
     <br/>
     
- ### Langkah menghindari konflik saat berkolaborasi 
     <div align="justify">Menghindari konflik saat berkolaborasi dapat dilakukan dengan berkomunikasi antar anggota yang berkolaborasi mengenai pembagian tugas mana saja yang harus dikerjakan. Dikarenakan apabila anggota mengerjakan file dengan baris yang sama akan menyebabkan sebuah konflik.</div> <br/>
     
     Langkah untuk menyelesaikan konflik: <br/>
     1) Periksa baris kode dan file yang sedang terjadi konflik <br/>
     2) Segera lakukan konfirmasi kepada para anggota yang berkolaborasi <br/>
     3) Anggota yang mengalami konflik harus melakukan pull <br/>

        ```md
          git pull
        ```
        
        <br/>
        
     4) Lakukan merge untuk melihat konfliknya <br/>

         ```md
          git merge (branch yang dituju)
         ```
         
         <br/>
         
     5) Lakukan diskusi dengan kelompok untuk menentukan code mana yang akan dipakai <br/>

     6) Lalu lakukan proses stagged sampai commit, dan push file ke repository <br/> 

 - ### Publikasi file atau aplikasi ke dalam GitHub
   <div align="justify">Setelah seluruh langkah di atas berhasil, maka dapat publikasi file atau aplikasi ke dala GitHub dengan cara :</div>
   <br/>
   
   ```md
       git push -u origin main
   ```
   
   Studi kasus :
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192151539-db6c3019-85da-4763-be6f-e404e91ec80f.png" width="400"/>
   <br/>
   <div align="justify">Gambar di atas adalah kondisi file telah dipublikasi ke dalam GitHub.</div>
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192152261-d3a047f2-6ad8-4d88-8f7c-9ceeff52d4fe.png" width="400"/>
   <br/>
   <div align="justify">Gambar di atas adalah GitHub repository yang telah terisi.</div>
   <br/>
   
 - ### Cloning GitHub ke penyimpanan lokal
   <div align="justify">Cloning merupakan proses menyimpan GitHub repository ke dalam lokal repository yang kita miliki. Sebelumnya akan digunakan GitHub        Repository dengan link dibawah sebagai studi kasus.
   </div>
   <br/>
   
   ```md
       https://github.com/hafiihzafarhana/Wegodev-competition-with-bootstrap-4.5
   ```
   
   <br/>
   Hal yang harus diketikan untuk cloning :
   <br/>
   
   ```md
       git clone "link GitHub repository"
   ```
   
   <br/>
   Studi kasus :
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192152833-5c570708-df37-497d-b655-58aa7ac6a7de.png" width="400"/>
   <br/>
   <div align="justify">Gambar di atas merupakan proses cloning dari GitHub repository dengan link yang dicantumkan di atas.
   </div>
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192152926-ac3ecb52-e4f3-49f8-b5f3-d4b104f536e9.png" width="400"/>
   <br/>
   <div align="justify">Gambar di atas merupakan hasil dari proses cloning dengan link yang dicantumkan di atas.
   </div>
   
   <br/>
   
- ### Cara melakukan kolaborasi dengan GitHub kolaborasi
     a) Cari buttom "plus" / "+" <br/>
     b) Lalu pilih "new organization" <br/>
     c) Pilih "Create a free organization" <br/>
     d) Isi data sampai selesai <br/>
     e) Pilih "Create new repository" <br/>
     f) Sebagai seorang leader, lakukan push file pertama ke dalam repository yang telah dibikin dengan branch utama yaitu `main` atau `master` <br/>
     g) Masukan branch `dev` untuk fase pengembangan <br/>
     h) Invite anggota yang akan diajak untuk berkolaborasi <br/>
     i) Setiap anggota melakukan cloning terhadap repository yang ada <br/>
     j) Saat melakukan push ke dalam GitHub, maka anggota harus menggunakan branch berdasarkan fitur yang dibuat, bukan `dev`, `main`, dan `master` <br/>
     k) Anggota akan membuat pull request <br/>
     l) Leader akan menerima pull request <br/>
     m) Leader akan melakukan merge ke branch `dev` sebagai branch untuk proses pengembangan <br/>
     n) Setelah proses pengembangan selesai, branch `dev` akan di merge ke dalam branch `main` <br/>
     o) Setiap branch yang telah dibuat dapat dihapus <br/>
      
     <br/>
      
     

## 2 Responsive Web Design
- ### Responsive web design
     Responsive web design merupakan desain website yang dapat diakses di device manapun seperti mobile, desktop, dan tablet. Jadi, design di dalam website akan memposisikan dirinya sesuai dengan device yang dipakai. <br/>
      
     Contoh : <br/>
     <img src="https://www.pngitem.com/pimgs/m/140-1404926_et-web-design-free-responsive-joomla-template-responsive.png" width="400" /><br/>
     <i>Sumber : https://contohgambartemplate.blogspot.com/2019/11/template-website-layout-design.html</i> <br/> <br/>
     
     Pada contoh gambar di atas merupakan sebuah website yang responsive terhadap device yang akan dipakai <br/>
      
- ### Tools untuk website responsive
     Tools yang digunakan untuk membantu membuat website responsive adalah web browser masing-masing. Lalu, kita dapat mendeteksi website responsive atau tidak dengan melakukan inspect halaman. <br/>
      
     Shortcut : <br/>
     
     ```md
        ctrl + shift + j
     ```
     
     <br/>
     Lalu, klik icon mobile <br/>
     
     atau <br/>
     
     Bisa menggunakan shortcut : <br/>
     
     ```md
        ctrl + shift + m
     ```
     
     <br/>
      
- ### Menggunakan viewport
      Viewport digunakan untuk mengontrol dimensi halaman di dalam setiap device. <br/>
      Aturan : <br/>
      1) width=device-width, untuk mengatur lebar halaman website berdasarkan lebar layar device. <br/>
      2) initial-scale=1.0, untuk mengatur level perbesaran ketika halaman dimuat. <br/>

      ```html
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
      ```
      
     <br/><br/>
      
- ### Menggunakan relative CSS unit
     Digunakan untuk menentukan panjang relatif terhadap properti panjang lainya. Ukuranya akan tetap. <br/>
      
     Jenis relative CSS unit: <br/>
     1) `em`, akan relatif terhadap ukuran huruf <br/>


     ```css
        p {
          font-size: 16px;
          line-height: 2em; // akan berukuran 16px * 2 = 32px
        }
     ```
        
     <br/>
     
    2) `ex`, akan relatif terhadap tinggi <br/>


      ```css
          // kondisi apabila span berada di dalam div
          div {
            font-size: 60px;
          }

          span {
            font-size: 1ex; // akan menyesuaikan dengan ukuran panjang huruf yang ada di dalam div
          }
       ```

    <br/>
        
     3) `ch`, akan relatif lebar berukuran 0 <br/>

        
        ```css
          body {
            font-size:8px;
          }

          div {
            font-size: 3ch; // akan berukuran 12 px
          }
        ```
        
        <br/>
        
     4) `rem`, akan relatif terhadap element root-nya <br/>

        
        ```css
          html {
            font-size:8px;
          }

          div {
            font-size: 3rem; // akan berukuran 24 px
          }
        ```
        
        <br/>
        
     5) `vw`, akan relatif sebesar 1% lebar viewport <br/>

        
        ```css
          //seandainya lebar viewport adalah 500
          div {
            font-size: 20vw; // 500 * 20 * 1% = 100 px;
          }
        ```
        
        <br/>
        
     
     6) `vh`, akan relatif sebesar 1% tinggi viewport <br/>

        
        ```css
          //seandainya lebar viewport adalah 500
          div {
            font-size: 20vh; // 500 * 20 * 1% = 100 px;
          }
        ```
        
        <br/>
        
        
     7) `vmin`, akan relatif sebesar 1% dari tinggi dan lebar viewport terkecil <br/>
  
        
        ```css
          // seandainya lebar adalah 500 dan tinggi adalah 700
          div {
            font-size: 15vmin; // Akan berukuran 50px
          }
        ```
        
        <br/>
        
        
     7) `vmax`, akan relatif sebesar 1% dari tinggi dan lebar viewport terbesar <br/>
  
        
        ```css
          // seandainya lebar adalah 500 dan tinggi adalah 700
          div {
            font-size: 15vmax; // Akan berukuran 72px
          }
        ```
        
        <br/>
        
        
     8) `%`, akan relatif terhadap parent-nya <br/>
  
        
        ```css
          body{
            font-size:10px;  
          }
          
          div {
            font-size: 100%; // Akan berukuran 10px
          }
        ```
        
        <br/><br/>
        
- ### Menggunakan media query
     Media query digunakan untuk mengatur styling terhadap element HTML sesuai dengan device yang dipakai. <br/>
     Media query dapat digunakan untuk memeriksa :<br/>
     a) Tinggi dan lebar viewport <br/>
     b) Tinggi dan lebar device <br/>
     c) Resolusi <br/>
     d) Orientasi (landscape atau potrait) <br/>
     
     Namun, pada umumnya yang sering digunakan adalah melihat lebar dan tinggi device (screen). <br/>
     
     ```css
        @media only screen and (max-width: 600px) {
          body {
            background-color: red; //element body apabila memiliki lebar kurang dari 600px, maka warna akan berubah menjadi merah
          }
        }
     ```
     
     <br/><br/>

- ### Menggunakan flexbox dan Grid
   - #### Flexbox
    Flexbox merupakan langkah untuk mengatur layout. Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis. Flexbox memiliki <i>parent</i> dan     banyak <i>child</i>.
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192174973-f40f486a-3f21-4f40-9add-8f947596dfb2.png" alt="OIP-1" width="300" />
    
    <br/>
    
    - #### Ordering dan orientation:
    
         a) `flex-direction` digunakan untuk mengatur letak child item. Ada 4 jenis <i>value</i>:
       
             row untuk membentuk sebuah baris dari kiri ke kanan.

             row-reverse untuk membentuk baris dari kanan ke kiri.

             column untuk membentuk baris dari atas ke bawah.

             column-reverse untuk membentuk baris dari bawah ke atas.

         <img src="https://user-images.githubusercontent.com/71125093/192175866-4bd37129-2e0c-44e7-9e7a-da6a4af3908e.png" alt="OIP-1" width="300" />
          <br/>
       
         b) `flex-wrap` digunakan untuk membuat tatal letak item <i>children</i> dalam satu tata letak saja. Ada 3 jenis <i>value</i>:

             no-wrap artinya tidak menggunakan flex-wrap.

             wrap artinya memiliki beberapa line dari atas ke bawah  jika space dalam 1 line sudah full width.

             wrap-reverse artinya memiliki beberapa line dari bawah ke atas  jika space dalam 1 line sudah full width.

      
         c) `flex-flow` merupakan gabungan dari `flex-wrap` dan `flex-direction`. <br/>
      
         d) `order` digunakan untuk memposisikan <i>item</i> yang akan diatur berdasarkan urutan order. Apabila semakin kecil, maka akan diposisikan paling           awal. Namun, apabila `order` bernilai 0 tidak akan berubah karena merupakan <i>default value</i>. <br/>
      
     - #### Alignment:
   
         a) `justify-content` digunakan untuk mengatur tata letak dan jarak antar <i>item child</i> secara horizontal dan vertikal. Ada 6 jenis:

             flex-start untuk memposisikan item di awal kontainer.

             flex-end untuk memposisikan item di akhir kontainer.

             center untuk memposisikan item di tengah kontainer.

             space-between untuk memposisikan antar ruang di setiap item.

             space-around memiliki jarak sebelum, setelah, dan setelah di tiap item.

             space-evenly memiliki posisi yang sama dengan `space-around` .
             

          <br/>
          
     
         b) `align-self` digunakan untuk mengatur <i>align</i>. Ada 5 jenis:

             flex-start untuk memposisikan item di awal kontainer.

             flex-end untuk memposisikan item di akhir kontainer.

             center untuk memposisikan item di tengah kontainer.

             baseline memiliki kesamaan dengan flex-start .

             stretch untuk memposisikan item dengan full kontainer.
             

          <br/>
          
        
         c) `align-content` memiliki kesamaan dengan `justify-content` . Hanya saja yang membedakan pada `align-content` terdapat <i>value</i> `stretch` .
         
         d) `align-items` digunakan untuk mengatur <i>align</i> dari item child secara vertikal. Ada 5 jenis:
         
             flex-start untuk memposisikan item di awal kontainer.

             flex-end untuk memposisikan item di akhir kontainer.

             center untuk memposisikan item di tengah kontainer.

             baseline memiliki kesamaan dengan flex-start .

             stretch untuk memposisikan item dengan full kontainer.
             
          <br/>
     
     - #### Flexibility:
         a) `flex-grow` digunakan untuk mengatur ukuran suatu <i>item child</id> pada flexbox. Nilai harus angka dan tidak boleh minus.
         
         b) `flex-shrink` digunakan untuk membuat ukuran suatu <i>item child</i> mengecil secara relatif terhadap <i>item child</i> lainya. Nilai harus angka          dan tidak boleh minus. Semakin besar nilainya, maka semakin kecil ukuran dari suatu <i>item child</i>.
         
         c) `flex-basis` digunakan untuk menentukan lebar dari <i>item child</i>. Flexbox tidak bisa menggunakan properti `min-width` dan `max-width`. Ada 4          nilai dari `flex basis` :
         
            auto akan menyesuaikan dengan kontenya
            
            angka (bisa menggunakan satuan)
            
            initial adalah bentuk default
            
            inherit akan diturunkan dari <i>parent</i>
            
          <br/>
    
 - #### Grid
   Grid merupakan sistem tata letak untuk element HTML dengan menggunakan baris dan kolom. Kolom dari setiap baris akan berjumlah 12.<br/>
       
   <img src="https://1.bp.blogspot.com/-U3rHRyiwlSA/XjonukZGY3I/AAAAAAAAJ_U/-K_pNt8tpIoXKLI_zoYhApo_GdmE0T4mwCLcBGAsYHQ/s1600/css-grid-module.png" width="400"/> <br/><br/>
   <i><a href="https://www.anythinglearn.com/2020/02/what-is-grid-layout-in-css.html">Sumber gambar</a></i> <br/>
   
   Properti pada Grid: <br/>
   1) `display` <br/>
      
      ```css
        .grid-container1{
            display:inline-grid; //untuk membuat display grid dengan level block
         }
         
        .grid-container2{
            display:inline-grid; //untuk membuat display grid dengan level inline
         }
      ```
      
      <br/>
   
   2) `gap`, digunakan untuk memberi spasi tiap baris dan kolom antar item <br/>
      
      ```css
        .grid-container1{
            gap:10px; //akan memberikan jarak spasi baris dan kolom tiap item sebesar 10px
         }
      ```
      
      <br/>
      
   3) `column-gap`, digunakan untuk memberi spasi kolom antar item <br/>
      
      ```css
        .grid-container1{
            column-gap:10px; //akan memberikan jarak spasi kolom tiap item sebesar 10px
         }
      ```
      
      <br/>
      
   4) `row-gap`, digunakan untuk memberi spasi baris antar item <br/>
      
      ```css
        .grid-container1{
            row-gap:10px; //akan memberikan jarak spasi baris tiap item sebesar 10px
         }
      ```
      
      <br/>
      
   5) `grid-column-start` dan `grid-column-end` <br/>
      
      ```css
        .item1{
            grid-column-start:1;
            grid-column-end:3;
         }
         
         // item1 akan selebar 2 kolom
      ```
      
      <br/>
      
   6) `grid-row-start` dan `grid-row-end` <br/>
      
      ```css
        .item1{
            grid-row-start:1;
            grid-row-end:3;
         }
         
         // item1 akan selebar 2 baris
      ```
      
      <br/>
      
   7) `grid-template-column`, digunakan untuk memberikan ukuran ruang untuk tiap kolom  <br/>
      
      ```css
        .container1{
            grid-template-column:auto auto auto //setiap baris akan memiliki 3 kolom auto
         }
         
      ```
      
      <br/>
      
   8) `grid-template-rows`, digunakan untuk memberikan ukuran ruang untuk tiap baris  <br/>
      
      ```css
        .container1{
            grid-template-column:80px 200px // baris pertama memiliki lebar dan tinggi 80px, sedangkan barus ke dua memiliki lebar dan tinggi 200px
         }
         
      ```
      
      <br/>
      
  9) `grid-column`, merupakan shortcut dari `grid-column-start` dan `grid-column-end`  <br/>
      
      ```css
        .item{
            grid-column:1 / 5; // akan memberikan jarak sampai 5 kolom
         }
         
      ```
      
      <br/>
      
  10) `grid-rows`, merupakan shortcut dari `grid-rows-start` dan `grid-rows-end`  <br/>
      
      ```css
        .item{
            grid-row:1 / 5; // akan memberikan jarak sampai 5 baris
         }
         
      ```
      
      <br/><br/>
      
## 3 Bootstrap
- ### Alasan dan kapan menggunakan Bootstrap?
     Alasan menggunakan Bootstrap untuk mempermudah pekerjaan dalam membuat elemen secara instan. Bootstrap harus digunakan apabila telah memahami prinsip responsive web design, flexbox, dan grid. Dikarenakan kunci utama dari menggunakan Bootstarp adalah 3 poin tersebut. <br/>
     
- ### Menggunakan layout pada Bootstrap 
     Layout di dalam Bootstrap merupakan langkah untuk  memberikan struktur terhadap susunan komponen agar rapi. <br/>
     
     a) Forms <br/>
     
     ```html
        <form>
          <input class="form-control" type="text" placeholder="Pencarian ..." />
          <button class="btn btn-success" type="submit">Masukan</button>
        </form>
     ```
     
     <br/>
     
     b) Utilitas Margin <br/>
     
     ```html
        <div class="mb-3">
          <input class="form-control" type="text" placeholder="Pencarian ..." />
          <button class="btn btn-success" type="submit">Masukan</button>
        </div>
     ```
     
     <br/>
     
     c) Form Grid <br/>
     
     ```html
        <div class="row">
          <div class="col-md-4 col-12 col-sm-6">
            <input class="form-control" type="text" placeholder="Pencarian ..." />
            <button class="btn btn-success" type="submit">Masukan</button>
          </div>
        </div>
     ```
     
     <br/>
     
     d) Gutters <br/>
     
     ```html
        <div class="row g-3">
          <div class="col-12">
            <input class="form-control" type="text" placeholder="Pencarian ..." />
            <button class="btn btn-success" type="submit">Masukan</button>
          </div>
          
          <div class="col-12">
            <input class="form-control" type="text" placeholder="Pencarian ..." />
            <button class="btn btn-success" type="submit">Masukan</button>
          </div>
        </div>
     ```
     
     <br/>
     
- ### Menggunakan content pada Bootstrap
    Konten pada Bootstrap merupakan langkah untuk memberikan isi pada halaman website.  <br/>
      
    a) Reebot <br/>
     Merupakan berbagai macam koleksi element CSS. <br/>
    
    b) Typography <br/>
     Merupakan teks yang akan ditampilkan di dalam sebuah website. <br/>
     Contoh: <br/>
       - `<h1>` ... `<h6>` <br/>
       - `<p>` <br/>
  
     Ada beberapa styling milik Bootstrap yang digunakan oleh teks <br/>
       
   ```html
     <p class="h1">Ini Bootstrap</p> // memberikan heading 1
          
     <p class="lead"> //membuat teks menonjol
       ini Bootstrap
     </p>
        
     <blockquote class="blockquote">
       <p>Ini Bootstrap </p> //memberikan mode quoting   
     </blockquote>
          
     <div>
      <p class="text-center">Ini Bootstrap </p> // membuat teks rata tengah
      <p class="text-start">Ini Bootstrap </p> //membuat teks rata kiri
      <p class="text-end">Ini Bootstrap </p> //membuat teks rata kanan
     </div>
              
    ```
      
     <br/>
  
    c) Image <br/>
     Merupakan langkah pengelolah gambar di dalam bootstrap <br/>
  
     Ada beberapa styling di dala image : <br/>
  
    ```html
       <img src="..." class="img-fluid" alt="..."> //tinggi maksimal dan lebar auto
       <img src="..." class="img-thumbnail" alt="..."> //membuat tinggi dan lebar sebesar 200px dengan border-radius sebesar 1px
    ```
  
     <br/>
  
    d) Table <br/>
       Merupakan langkah pembuatan table dengan styling versi bootstrap <br/>
      
       Table umum milik Bootstrap : <br/>
  
     ```html
     <table class="table">
        <thead>
            <tr>No</tr>
            <tr>Nama</tr>
        </thead>
        <tbody>
            <td>1</td>
          <td>Hafi</td>
        </tbody>
      </table>
    ```
  
    <br/>
  
  e) Figures <br/>
     Merupakan langkah pembuatan gambar dengan didampingin oleh teks. <br/>
       
     ```html
        <figure class="figure">
          <img src="..." class="figure-img img-fluid rounded" alt="...">
          <figcaption class="figure-caption">Ini adalah gambar Saya.</figcaption>
        </figure>
     ```
     
     <br/>
      
- ### Menggunakan component pada Bootstrap
   Merupakan komponen HTML yang telah dibuat secara instan oleh Bootstrap. <br/>
      
   Ada banyak contoh salah satunya adalah pembuatan `button` <br/>
   
   ```html
      <button class="btn btn-success">Klik</button>
   ```
   
   <br/>
  
- ### Membuat website responsif menggunakan Bootstrap
      <a href="https://github.com/hafiihzafarhana/Company-Profile-Website-Nusantaraya-with-Bootstrap">Klik Bootstrap Saya</a>
  <br/><br/>
  
## 4 Mengambil Data API Menggunakan Fetch
   Fetch API merupakan langkah untuk mengambil sebuah data dengan menggunakan Fetch(). <br/>
   
   Cara: <br/>
   
   ```js
      const api_url = 
      "https://reqres.in/api/users";
  
      fetch(api_url)
        .then(e => e.json())
        .then(e => console.log(e))
   ```
