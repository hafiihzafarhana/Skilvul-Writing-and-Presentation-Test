# Writing and Presentation Test Week 1
### 1 Unix Command Line

- #### Shell
  <div align="justify">Merupakan sebuah program yang menerima perintah, kemudian meneruskan perintah tersebut ke sebuah sistem untuk dieksekusi atau        dijalankan. Terdapat 2 jenis dari shell yaitu CLI (Command Line Interface) dan GUI (Graphical User Interface).
  </div>
  
- #### CLI (Command Line Interface)
  <div align="justify">Merupakan sebuah antarmuka berbasis teks yang dapat digunakan oleh pengguna untuk menjalankan program, mengelola file pada           komputer, berinteraksi dengan komputer, dan mengerjakan tugas tertentu lainya.
  </div>
  
- #### Mengakses CLI dan menggunakan terminal
  <div align="justify">Terminal merupakan antarmuka berbasis teks dengan mengetikan baris-baris perintah untuk mengerjakan tugas tertentu. <b>Gambar       terminal:</b> <br/><br/>
  <img src="https://user-images.githubusercontent.com/71125093/192132380-fb32659c-eebc-4f51-9db2-b79c15cffffd.png" width="400"/>
  </div>
  
- #### File system structure
  <div align="justify">Merupakan cara untuk menyimpan sebuah data di dalam sistem. Terdapat beberapa hal di dalam file system yaitu memberi nama dan menyimpan data pada sebuah penyimpanan. Adanya file system ini dapat mempermudah dalam membaca sebuah file atau direktori. Ada beberapa atribut dalam file system seperti nama, penanda, lokasi, jenis file, ukuran, dan waktu. Di dalam sistem operasi windows dapat melihat struktur dari file system dengan mengetikan di dalam terminal:                        
  </div>
  <br/>
  
   ```md
      tree
   ```
   
   <div align="justify">Contoh kasus:</div>
   <br/>
   <div align="justify">Bentuk Folder</div>
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192139231-6ad00d37-b368-485e-a323-84c51410c4be.png" width="400"/>
   <br/>
   <div align="justify">Bentuk Struktur File System</div>
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192139235-5b47a59b-e981-4002-9fc3-da77d819a58e.png" width="400"/>
   <br/>

- #### Beberapa Command:
  - #### Melihat current working directory
    <div align="justify">Ketikan : </div>
    <br/>
    
     ```md
      pwd
     ```
     
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192139861-7863df48-06f6-4e03-a445-5d9d602eac66.png" width="400"/>
    <br/>
    
  - #### Melihat isi sebuah directory
    <div align="justify">Ketikan : </div>
    <br/>
    
     ```md
      ls
     ```
     
     <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192139921-dd175c61-9a78-412e-9362-6df096163649.png" width="400"/>
    <br/>

  - #### Berpindah direktori
    <div align="justify">Ketikan : </div>
    <br/>
    
    ```md
      cd
     ```
     
     <br/>
     <div align="justify">Contoh kasus : </div>
     <br/>
     <img src="https://user-images.githubusercontent.com/71125093/192143256-acb9ee92-3440-4c5c-9c65-6ecb81c658fb.png" width="400"/>
     <br/>
  
  - #### Melihat isi files
    <div align="justify">Terdapat 3 cara dalam melihat isi file yaitu dengan menggunakan perintah head, tail, dan cat.</div>
    <br/>
      
      #### a) head
      <div align="justify">Digunakan untuk mendapatkan isi file yang dimulai dari baris paling awal.</div>
      <br/>
      
      ```md
        head "ketikan nama file"
       ```
       
      <br/>
      <div align="justify">Contoh kasus : </div>
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192140263-18c6f116-bfdf-43b1-a834-63ba0b5813fc.png" width="400"/>
      <br/>
    
      #### b) tail
      <div align="justify">Digunakan untuk mendapatkan isi file yang dimulai dari baris paling akhir.</div>
      <br/>
      
      ```md
        tail "ketikan nama file"
       ```
       
      <br/>
      <div align="justify">Contoh kasus : </div>
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192140352-efe0fb79-3629-47e0-bafd-7049003c06c2.png" width="400"/>
      <br/>
      
      #### c) cat
      <div align="justify">Digunakan untuk mendapatkan seluruh isi file.</div>
      <br/>
      
      ```md
        cat "ketikan nama file"
       ```
       
      <br/> 
      <div align="justify">Contoh kasus : </div>
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192140433-af2be1e8-3412-41ba-a14c-ce78e04a8735.png" width="400"/>
      <br/>
    
    ### Pada bagian ini akan dibuatkan studi kasus berurutan
  - #### Membuat file & direktori
      #### a) mkdir
      <div align="justify">Digunakan untuk membuat direktori atau folder.</div>
      <br/>

      ```md
       mkdir "ketikan nama folder"
      ```

      <br/>
      <div align="justify">Contoh kasus : </div>
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192140824-ec5afab1-69d5-4e70-a569-81b5d0de054f.png" width="400"/>
      <br/>
      <div align="justify">Pada gambar di atas menunjukan pembuatan folder bernama "folder".</div>
      <br/>
      
      #### b) touch
      <div align="justify">Digunakan untuk membuat file. Ketikan nama file dengan format tertentu.</div>
      <br/>
      
      ```md
        touch "ketikan nama file"
       ```
       
      <br/> 
      <div align="justify">Contoh kasus : </div>
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192140840-19d1dbe3-aed1-4416-96d2-0118771d08a3.png" width="400"/>
      <br/>
      <div align="justify">Pada gambar di atas menunjukan pembuatan file bernama "file.txt". </div>
      <br/>
      <br/>
    
  - #### Menyalin file & direktori
    <div align="justify">Pada dasarnya menyalin file dan direktori hampir sama, tetapi pada saat menyalin folder harus ditambahkan "-r".</div>
    <br/>
    <div align="justify">Cara menyalin folder :</div>
    </br>
      
      ```md
        cp -r "folder yang disalin" "lokasi untuk menyalin folder"
       ```
    
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192141784-4d6ff24a-d876-49fe-b9cc-8bb470d72704.png" width="400"/>
    <br/>
    <div align="justify">Pada gambar di atas menunjukan hasil salin dari folder bernama "folder". Pada awalnya folder "folder" berada di lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Github
     ```
     
    <br/>
    <div align="justify">Lalu, folder bernama "folder" disimpan di lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Akan dicopy disini
    ```
    
     <br/>
     <div align="justify">Cara menyalin file :</div>
     <br/>
      
      ```md
        cp "file yang disalin" "lokasi untuk menyalin file"
       ```
    
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192142160-a852c381-600f-4809-bd92-285726e3f6c7.png" width="400"/>
    <br/>
    <div align="justify">Pada gambar di atas menunjukan hasil salin dari file bernama "file.txt". Pada awalnya folder "file.txt" berada di lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Github\folder
     ```
    
    <br/>
    <div align="justify">Lalu, folder bernama "folder" disimpan di lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Akan dicopy disini\folder
    ```
    
    <br/>
    
  - #### Memindahkan atau mengganti nama file & direktori
    <div align="justify">Cara memindahkan atau mengganti nama folder :</div>
    </br>
    
    ```md
        mv "folder" "lokasi pemindahan"/(ganti_nama)
    ```
    
    <div align="justify">Catatan : mengganti nama adalah opsional.</div>
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192143949-2df1c27c-a2bf-4218-b543-5b3faacf98a4.png" width="400"/>
    <br/>
    <div align="justify">Pada gambar di atas menunjukan hasil pindah dari folder bernama "Folder yang akan dipindah". Pada awalnya folder tersebut berada di     lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Github\
     ```
     
    <br/>
    <div align="justify">Lalu, folder tersebut berpindah lokasi dan berubah nama menjadi "folder_terpindah" :</div>
    <br/>
    
      ```md
          D:\skilvul\Github Writing\Akan dipindah disini
      ```
      
    <br/>
    
    <div align="justify">Cara memindahkan atau mengganti nama file :</div>
    </br>
    
    ```md
        mv "file" "lokasi pemindahan"/(ganti_nama)
    ```
    
    <div align="justify">Catatan : mengganti nama adalah opsional.</div>
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192144246-523ff36e-3393-450f-9be4-4c600b516c96.png" width="400"/>
    <br/>
    <div align="justify">Pada gambar di atas menunjukan hasil pindah dari file bernama "inifile.txt". Pada awalnya folder tersebut berada di lokasi :</div>
    <br/>
    
    ```md
        D:\skilvul\Github Writing\Github\folfil
     ```
     
    <br/>
    <div align="justify">Lalu, file tersebut berpindah lokasi dan berubah nama menjadi "inifiles.txt" :</div>
    <br/>
    
      ```md
          D:\skilvul\Github Writing\Akan dipindah disini
      ```
      
    <br/>
    
  - #### Menghapus file & direktori
    <div align="justify">Pada dasarnya menghapus file dan direktori hampir sama, tetapi pada saat menyalin folder harus ditambahkan "-r" atau "-d".</div>
    <br/>
    <div align="justify">Cara menghapus folder :</div>
    </br>
      
      ```md
        rm -r "folder yang dihapus"
       ```
    
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192144867-9672ce4d-2eb7-419a-b58b-cf3c7b5347b9.png" width="400"/>
    <br/>
    <div align="justify">Sebelumnya folder bernama "folfil" telah dibuat dan sekarang terhapus.</div>
    
    <br/>
    
    <div align="justify">Cara menghapus file :</div>
    </br>
      
      ```md
        rm "file yang dihapus"
       ```
    
    <br/>
    <div align="justify">Contoh kasus : </div>
    <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192145023-0b3c9d16-63d0-4b46-9910-5820991db2a2.png" width="400"/>
    <br/>
    <div align="justify">Sebelumnya folder bernama "file.txt" telah dibuat dan sekarang terhapus.</div>

    <br/><br/>

    
### 2 Git & GitHub Dasar
- #### Perbedaan Git dan GitHub
  <div align="justify">Git merupakan sebuah tools sebagai Version Control System yang berarti untuk mencatat setiap perubahan file pada suatu proyek yang       dikerjakan sejara individu atau berkelompok. Lalu, GitHub merupakan sebuah cloud base yang digunakan untuk mengupload atau mengelola sebuah file.</div>
  
  <br/>
  
- #### Alasan Git dan GitHub menjadi alat yang wajib digunakan
  <div align="justify">Seorang programmer tidak akan bekerja sendirian. Seorang programmer pasti akan bekerja dengan       tim. Namun, hal ini akan menjadi permasalahan karena programmer akan menyalin ulang seluruh file secara manual dan bahkan akan menunggu rekan tim untuk       menyelesaikan bagianya masing-masing. Hal ini dapat dipecahkan dengan adanya Git dan GitHub karena menjadi media untuk berkolaborasi dengan tim. Adanya Git   dan GitHub memungkinkan programmer bekerja dengan tim tanpa saling menunggu bagianya masing-masing dan tidak perlu meyalin seluruh file, hanya file atau     folder yang terupdate saja.</div>
  
  <br/>
  
 - #### Alur kerja Git dan GitHub
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
   
 - #### Membuat repository Git
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

 - #### Membuat repository Git
   <div align="justify">Masukan seluruh file atau beberapa file dengan mengetikan : </div>
   <br/>
   
   ```md
       git add . 
   ```
   
   <br/>
   <div align="justify">Penulisan di atas menunjukan semua file atau folder akan dimasukan.</div>
   <br/>
   atau
   <br/>
   
   ```md
       git add (file atau folder pilihan) 
   ```
   
   <br/>
   <div align="justify">Penulisan di atas menunjukan hanya beberapa file atau folder akan dimasukan.</div>
   <br/>
   
   Studi kasus:
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192151386-4a04e88d-cbd5-43fb-b2d0-588ad28d367d.png" width="400"/>
   <br/>
   <div align="justify">Pada gambar di atas adalah proses penambahan seluruh file ke dalam fase stagged. Setelaha dilakukan </div>
   
   ```md
       git status 
   ```
   
   <div align="justify">Terlihat beberapa file yang berhasil ditambahkan.</div>
   <br/>
   
 - #### Melakukan commit pada Git
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

 - #### Remote repository antara GitHub dengan lokal
   <div align="justify">Sebelum memasukan proyek ke dalam GitHub, perlu dihubungkan antara lokal dengan GitHub dengan cara :</div>
   <br/>
   
   ```md
       git remote add origin "link GitHub repository"
   ```
   
   Studi kasus :
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192151539-db6c3019-85da-4763-be6f-e404e91ec80f.png" width="400"/>
   <br/>

 - #### Publikasi file atau aplikasi ke dalam GitHub
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
   
 - #### Cloning GitHub ke penyimpanan lokal
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
   
   <br/><br/>
      
### 3 HTML (HyperText Markup Language)
 - #### Peran HTML pada Web Development
   <div align="justify">HTML digunakan untuk membuat kerangka website yang juga menampilkan konten pada browser.
   </div>
   <br/>
   
 - #### Tools pendukung dalam menggunakan HTML
   <div align="justify">Terdapat 2 <i>tools</i> utama untuk mempersiapkan HTML yaitu Browser (Google Chrome, Microsoft Edge, Firefox, Opera, dan lain sebagainya)    dan Code Editor (VS Code, Sublime text, Notepad, dan lain sebagainya.
   </div>
   <br/>

 - #### HTML sederhana
   <div align="justify">Contoh HTML sederhana : </div>
   <br/>
   
   ```html
       <html>
       <head>
         <title>
           Judul Website
         </title>
       <body>
           Konten Website
       </body>
       </html>
   ```
   
   <br/>
   
   Terdapat tag utama di dalam HTML yaitu `<html>` `<head>` `<title>` `<body>` .
   
   <br/>
   
 - #### Menjalankan HTML secara manual dan menggunakan liver server dari VS Code
   Menjalankan HTML secara manual dapat dilakukan dengan cara : 
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192154408-00b91705-035b-4dde-a1bf-0ad791a81453.png" width="400"/>
   <br/>
   <div align="justify">Cara manual sangatlah tidak efektif karena apabila ingin merubah kode HTML harus tetap menyegarkan kembali halaman website agar dapat    berubah</div>
   <br/><br/>
   
   Menjalankan HTML menggunakan live server dari VS Code:
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192154681-85e52f70-5f77-454f-8d8e-59a4c433f598.png" width="400"/>
   <br/>
   <div align="justify">Menggunakan live server untuk pengembangan sangatlah efektif karena tidak perlu menyegarkan website setiap ada perubahan</div>
   <br/>
   
 - #### Implementasi tag HTML yang populer
   a) IMG<br/>
   Tag ini berfungsi untuk menyisipkan sebuah gambar.
   <br/>
   
   ```html
       <img src="https://i.ibb.co/KDM5PPr/OIP-1.jpg" alt="OIP-1" />
   ```
   
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192155410-45c62c48-6641-42c9-8c09-7c96508e4dda.png" alt="OIP-1" width="400" />
   <br/>
   <div align="justify"><i>Source</i> (src) berfungsi untuk memberitahukan sumber gambar. <i>Alternative</i> (alt) berfungsi untuk menampilkan teks apabila      gambar tidak muncul</div>
   <br/>
   
   b) Video<br/>
   Tag ini berfungsi untuk menyisipkan sebuah video.
   <br/>
   
   ```html
       <video controls>
        <source src="videoku.mp4" type="video/mp4"/>
       </video>
   ```
   
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192155895-40d244c4-797c-4478-bcc6-aa63dea29c3f.png" alt="OIP-1" width="400" />
   <br/>
   <div align="justify">Controls berguna untuk mengatur video bisa <i>play</i> / <i>pause</i>. <i>Source</i> (src) untuk memberitahukan sumber video.            <i>Type</i> untuk memberitahukan tipe dari video.</div>
   <br/>

   c) Table <br/>
   Tag ini berfungsi untuk membuat sebuah tabel.
   <br/>
   
   ```html
      <table border="1">
        <tr>
          <th>No</th>
          <th>Nama</th>
          <th>Umur</th>
        </tr>
        <tr>
          <td>1</td>
          <td>Ihza</td>
          <td>14</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Farhana</td>
          <td>15</td>
        </tr>
      </table>
   ```
   
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192156311-43719020-1ca3-4197-b519-aa4e9fcf4a27.png" alt="OIP-1" width="400" />
   <br/>
   
   d) Form <br/>
   Tag ini berfungsi untuk melakukan sebmit data yang ada di dalam input HTML.
   <br/>
   
   ```html
   <form>
    <div>
        <label for="nama">Nama</label>
        <input type="text" placeholder="masukan nama" name="nama" id="nama">
    </div>
    <div>
        <label for="password">password</label>
        <input type="password" placeholder="masukan password" name="password" id="password">
    </div>
   </form>
   ```
   
   <br/>
   <img src="https://user-images.githubusercontent.com/71125093/192156475-dec1cdd4-f32a-48a9-b69c-6451876761de.png" alt="OIP-1" width="400" />
   <br/>
   
 - #### Memahami dan mengimplementasikan semantic HTML
   <div align="justify">Semantic HTML merupakan langkah menggunakan elemen HTML sesuai dengan kebutuhan konten. Kegunaan semantic HTML adalah :<br/>
      a) Meningkatkan Accessibility
      <br/>
      b) Meningkatkan SEO
      <br/>
      c) Lebih mudah untuk pemeliharaan
      <br/>
   </div>
   <br/>
   
   <img src="https://www.w3schools.com/html/img_sem_elements.gif" width="400"/>
   
   <br/>
   
   Beberapa tag semantic HTML :
   <br/>
   Penerapan `<article>` : <br/>
   Digunakan untuk menentukan konten mandiri.
   <br/>
   
   ```html
   <article>
    <h2>Hafi Ihza Farhana</h2>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </article>
   ```
   
   <br/>
   Hasil:
   <article>
    <h2>Hafi Ihza Farhana</h2>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </article>
   
   <br/>
   
   Penerapan `<aside>` :<br/>
   Digunakan untuk membuat konten yang ditempatkan di sisi sebelah.
   <br/>
   
   ```html
   <aside>
    <h4>Hafi Ihza Farhana</h4>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </aside>
   ```
   
   <br/>
   Hasil:
   <br/>
   <aside>
    <h4>Hafi Ihza Farhana</h4>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </aside>
   
   <br/>
   
   Penerapan `<details>` :<br/>
   Digunakan untuk menentukan detail tambahan yang bisa dibuka dan ditutup.
   <br/>
   
   ```html
   <details>
    <summary>Hafi Ihza Farhana</summary>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </details>
   ```
   
   <br/>
   Hasil:
   <br/>
   <details>
    <summary>Hafi Ihza Farhana</summary>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </details>
   
   <br/>
   
   Penerapan `<footer>` :<br/>
   Digunakan untuk mendefinisikan bagian bawah.
   <br/>
   
   ```html
   <footer>
    <p>Author: Hafi Ihza Farhana</p>
   </footer>
   ```
   
   <br/>
   Hasil:
   <br/>
   <footer>
    <p>Author: Hafi Ihza Farhana</p>
   </footer>
   
   <br/>
   
   Penerapan `<header>` :<br/>
   Digunakan untuk mendefinisikan bagian heading pada website.
   <br/>
   
   ```html
   <header>
    <h1>Hafi Ihza Farhana</h1>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </header>
   ```
   
   <br/>
   Hasil:
   <br/>
   <header>
    <h1>A heading here</h1>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </header>
   
   <br/>
   
   Penerapan `<main>` :<br/>
   Digunakan untuk mendefinisikan konten utama.
   <br/>
   
   ```html
   <main>
    <h1>Hafi Ihza Farhana</h1>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </main>
   ```
   
   <br/>
   Hasil:
   <br/>
   <main>
    <h1>Hafi Ihza Farhana</h1>
    <p>Orang keren di UPN Veteran Jawa Timur</p>
   </main>
   
   <br/>
   
   Penerapan `<nav>` :<br/>
   Digunakan untuk mendefinisikan bagian navigasi.
   <br/>
   
   ```html
   <nav>
    <a href="https://www.instagram.com/loker_it/">Instagram</a>
   </nav>
   ```
   
   <br/>
   Hasil:
   <br/>
   <nav>
    <a href="https://www.instagram.com/loker_it/">Instagram</a>
   </nav>
   
   <br/>
   
 - #### Tahap Deployment
   Langkah-langkah:<br/>
   a) Menuju ke link berikut : <a href="https://app.netlify.com/teams/hafiihza6/overview">Klik ini</a><br/>
   b) Cari `<button>` dan pilih "Deploy manually".<br/>
   <img src="https://user-images.githubusercontent.com/71125093/192157627-12086c43-323f-436a-b331-5f1e61dff706.png" alt="OIP-1" width="400" /> <br/>
   c) Masukan folder yang akan di-deploy<br/>
   <img src="https://user-images.githubusercontent.com/71125093/192157789-7c8eaf73-f13d-4528-aea1-02f675c40202.png" alt="OIP-1" width="400" /> <br/>
   d) Hasil berhasil: <br/>
   https://ini-adalah-website-saya.netlify.app
   
   <br/><br/>
   
### 4 CSS (Cascading Style Sheets)
  - #### Peran CSS pada web development <br/>
    CSS merupakan bahasa yang digunakan untuk mendesain halaman website. <br/>
    
  - #### Cara menyisipkan CSS ke HTML
    Ada 3 cara dalam menyisipkan CSS ke dalam HTML: <br/>
    a) Inline (Langsung di dalam element HTML)
    <br/>
    
    ```html
       <p style="color:green;">Hafi Ihza Farhana</p>
    ```
    
    <br/>
    
    b) Internal (Di dalam tag `<style` , tetapi masih di dalam file HTML) 
    <br/>
    
    ```html
       <style>
        p{
         color:red;
        }  
       </style>
    ```
    
    <br/>
    
    c) Eksternal (di luar halaman HTML) <br/>
    <i>Styling</i> dilakukan di luar halaman HTML yang dihubungkan dengan :
    <br/>
    
    ```html
     <head>
       <link rel="stylesheet" href="style.css">
     </head>
    ```
    
    <br/>

  - #### Sintaks dasar CSS <br/>
    Kerangka pada sintaks CSS : <br/>

    ```css
      tag html, .class, #id {
        property : value;
      }    
    ```
    
    <br/>
    Catatan:<br/>
    a) tag html menunjukan nama-nama element di HTML <br/>
    b) .class menunjukan class yang didelarasikan (.class bersifat tidak spesifik) <br/>
    c) #id menunjukan id yang dideklarasikan (#id bersifat spesifik) <br/>
    d) tag html, .class, dan #id merupakan selector
    
    <br/>
    Contoh: <br/>
    
    ```css
      p, .paragraf1, #paragraf2 {
        color : green;
      }    
    ```

  - #### Styling CSS pada halaman HTML
    Langkah styling CSS pada halaman HTML ada 4 cara: <br/>
    - ##### CSS - Tag Name
      <div align="justify">CSS - Tag Name merupakan tag HTML yang diterapkan secara langsung pada CSS. Penggunaan styling ini akan bersifat global yang berarti mempengaruhi       seluruh tag HTML yang dipanggil menggunaka CSS.</div>
      <br/>
      Contoh kasus <br/>
      
      `<HTML>` :
      
      <br/>
      
      ```html
        <!DOCTYPE html>
        <html lang="en">
          <head>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <h1>Hafi Ihza Farhana</h1>
            <h1>UPN Veteran Jawa Timur</h1>
            <h1>Berumur 20 tahun</h1>
          </body>
        </html>
      ```
      
      <br/>
      
      `<CSS>` :
      
      ```css
        h1{
          color: green;
          }
      ```
      
      <br/>
      
      Contoh kasus di atas menunjukan terdapat 3 element HTML dengan tag yang sama yaitu `<h1>` . Ketiga tag tersebut diberikan sebuah <i>styling</i> yang         menyebabkan ketiga tag tersebut berubah warna menjadi hijau.
      
      <br/>
      Hasil: 
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192171947-1864a4ca-66e3-4784-be99-c8266d9440e9.png" alt="OIP-1" width="400" />
      <br/>
      
    - ##### CSS - Class Name
      CSS - Class Name merupakan langkah <i>styling</i> dengan memberikan atribut `class` pada elemen HTML. Apabila ada elemen HTML memiliki nilai `class`         yang sama, maka akan mempunyai <i>styling</i> yang sama.
      <br/>
      Contoh kasus <br/>
      
      `<HTML>` :
      
      <br/>
      
      ```html
        <!DOCTYPE html>
        <html lang="en">
          <head>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <div class="box">
              <p class="teks">Hafi Ihza Farhana</p>
            </div>
          </body>
        </html>
      ```
      
      <br/>
      
      `<CSS>` :
      
      ```css
        .box{
              width: 100px;
              height: 100px;
              background-color: brown;
              display: flex;
              justify-content: center;
              align-items: center;
          }

        .teks{
            color: white;
            text-align: center;
        }
      ```
      
      <br/>
      
      Contoh kasus di atas menunjukan terdapat 2 elemen HTML yaitu `<div>` dengan `class` `box` dan `<p>` dengan class `teks`. Setiap elemen akan dilakukan           <i>styling</i>.
      
      <br/>
      Hasil: 
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192172491-0d91b9ab-0f4a-4e52-b6b7-83fa1d9ab6f8.png" alt="OIP-1" width="400" />
      <br/>
      
    - ##### CSS - Multiple Class
      CSS - Multiple class merupakan langkah <i>styling></i> tetap dengan menggunakan bantuan `class` dan dapat menggunakan lebih dari 1 `class` yangg             berbeda untuk satu elemen HTML.
      
      <br/>
      Contoh kasus <br/>
      
      `<HTML>` :
      
      <br/>
      
      ```html
        <!DOCTYPE html>
        <html lang="en">
          <head>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <p class="warna ukuran">Hafi Ihza Farhana</p>
          </body>
        </html>
      ```
      
      <br/>
      
      `<CSS>` :
      
      ```css
        .warna{
            color: green;
        }

        .ukuran{
            font-size: 36px;
        }
      ```
      
      <br/>
      
      Contoh kasus di atas menunjukan terdapat elemen HTML yaitu `<p>` dengan 2 `class` yaitu `warna` untuk mengatur warna dan `ukuran` untuk mengatur             ukuran.
      
      <br/>
      Hasil : 
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192173096-aac83709-6cfb-47d9-9e5d-f9970835850c.png" alt="OIP-1" width="400" />
      <br/>
      
    - ##### CSS - ID Name
      CSS - ID Name merupakan langkah <i>styling></i> dengan menggunakan atribut `id` . Atribut `id` bernilai spesifik. Jadi hanya akan ada 1 nama `id` pada       elemen HTML.
      
      <br/>
      Contoh kasus <br/>
      
      `<HTML>` :
      
      <br/>
      
      ```html
        <!DOCTYPE html>
        <html lang="en">
          <head>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <div id="box"></div>
          </body>
        </html>
      ```
      
      <br/>
      
      `<CSS>` :
      
      ```css
        #box{
          width: 500px;
          height: 500px;
          background-color: brown;
        }
      ```
      
      <br/>
      
      Contoh kasus di atas menunjukan tag `<div>` yang memiliki `id` bernama `box`. Proses <i>styling</i> pada CSS menggunakan tanda `#` .
      
      <br/>
      Hasil : 
      <br/>
      <img src="https://user-images.githubusercontent.com/71125093/192173461-8236f16c-cd0f-4fd4-81bd-e7c74af7d41b.png" alt="OIP-1" width="400" />
      <br/>
      
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
         
  - #### Responsive web design menggunakan CSS
    <div align="justify">Responsive web design merupakan sebuah halaman website yang dapat digunakan di berbagai macam platform seperti mobile, destop,  dan     tablet. Dalam membuat responsive web design hanya bermodalkan HTML5 dan CSS3. CSS memiliki fitur yang bernama CSS media queries yang hanya berada di         CSS3. <br/>
    CSS media queries dapat melihat : <br/>
      a) lebar dan tinggi viewport <br/>
      b) lebar dan tinggi perangkat <br/>
      c) resolusi <br/>
      d) orientasi <br/>
    </div>
    <br/>
    
    Sintaks dari CSS media queries: <br/>
    ```css
      @media not|only mediatype and (expressions) {
        Kode dari CSS;
      }
    ```
    
    <br/>
    Contoh kasus:
    
    `<html>` :
    
    ```html
      <!DOCTYPE html>
        <html lang="en">
          <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, initial-scale=1.0" />
            <title>Document</title>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <div id="box"></div>
          </body>
        </html>
    ```
    
    <br/>
    
    ```css
      #box{
      width: 1000px;
      height: 100px;
      background-color: brown;
      }

      @media screen and (max-width: 480px) {
          #box {
            background-color: lightgreen;
            width: 50px;
            height: 50px;
          }
        }
    ```
    
    <br/>
    Hasil : <br/><br/>
    Mode destop : <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192185213-377b2bd4-8802-4da8-8dd1-293c16f0c84e.png" alt="OIP-1" width="300" />
    
    <br/>
    Mode mobile : <br/>
    <img src="https://user-images.githubusercontent.com/71125093/192185313-f4dac478-ef2a-4eb8-aa36-e6075579175c.png" alt="OIP-1" width="300" />
    
    <br/>
    
    Penjelasan: <br/>
    Sebelumnya, di mode destop elemen dengan id `box` memilik lebar sebesar 1000px dan tinggi 100px. Apabila lebar diperkecil dengan maksimal lebar layar         480px, maka elemen dengan id `box` akan berubah lebar menjadi 50px dan tinggi 50px.

### 5 Algorithm
  - #### Perbedaan Algoritma dan Data Structure
    <div align="justify">Algoritma merupakan langkah-langkah yang terstruktur untuk memecahkan sebuah permasalahan, sedangkan struktur data merupakan langkah penyimpanan, pengorganisasian, dan pengaturan banyak data di dalam media penyimpanan komputer sehingga data-data tersebut dapat digunakan secara efisien.</div> <br/>
    
  - #### Manfaat Algoritma dan Data Structure
    <div align="justify">Algoritma dan data struktur memili fungsi untuk memecahkan sebuah permasalahan.</div>
    Manfaat algoritma : </div><br/>
      a) Membuat program menjadi lebih sederhana dari sebelumnya. <br/>
      b) Memudahkan dalam pembuatan program. <br/>
      c) Mengatasi masalah logika secara terurut. <br/>
      d) Meminimalisir penulisan program yang berulang-ulang. <br/>
      e) Program menjadi lebih terstruktur dan rapih. <br/>
      f) Dokumentasi lebih mudah. <br/>
      g) Mudah untuk melakukan pemeliharaan. <br/><br/>
      
      Manfaat Data Structure : <br/>
      a) Memudahkan untuk menyimpan dan mengatur data menjadi lebih efisien, rapih, dan terorganisir. <br/>
      b) Memberikan informasi yang lebih cepat. <br/>
      c) Meningkatkan efektivitas terhadap algoritma. <br/>
      d) Mudah melakukan debugging. <br/>
      e) Mengatur sumber daya dan layanan pada sistem. <br/>
      f) Menciptakan kecepatan dalam pencarian data. <br/>
      g) Menegelola big data sehingga terjamin kualitasnya. <br/><br/>
      
  - #### Membuat Algoritma sederhana
    ```md
    Langkah 1: mulai
    Langkah 2: Deklarasi variabel angka
    Langkah 3: Inisialisasi variabel angka
    Langkah 4: Pengondisian apabila angka dibagi 2 bersisa 0, maka genap. Jika 1 adalah ganjil
    Langkah 5: Tampilkan hasil
    Langkah 6: Selesai
    ```
    
  - #### Menerapkan Algoritma ke dalam bahasa pemrograman
    Menerapkan algoritma bisa menggunakan semua bahasa pemrograman. Pada saat ini menggunakan C++.
    ```c++
    #include <iostream>
    using namespace std;
    
    //mulai
    int main(){
      // deklarasi variabel angka
      int angka;
      
      //inisialisasi variabel angka
      cin>>angka;
      
      //pengondisian
      if(angka % 2 == 0){
        cout<<angka<<" adalah genap"<<endl;
      } else {
        cout<<angka<<" adalah ganjil"<<endl;
        }
      return 0;
    }
    ```
    
    <br/>
    
  - #### Big O Notation
    <div align="justify"> 
    Merupakan penggambaran tingkat kompleksitas dari sebuah sistem yang bisa diterapkan dalam ilmu komputer untuk mengelompokan algoritma dalam tingkat           kesulitanya. Pada penerapanya big O notation untuk tingkat lama waktu proses dan resource yang digunakan berbanding lurus dengan bertambahnya data.</div>     <br/>
  
    <img src="https://miro.medium.com/max/1100/1*RXl6HCx57Eg7T0GGrq0STg.png" alt="OIP-1" width="400" /> <br/>
    Sumber: Medium: Big O Notation ~ D. Husni Fahri Rizal (04 April 2020)
    
    <br/>
    Dari gambar di atas menunjukan apabila kurva berbanding lurus secara horizontal memiliki proses waktu yang lebih baik. 
    
    <br/>
    Terdapat 2 jenis kompleksitas di dalam Big O notation yaitu kompleksitas dalam waktu yang berarti semakin komplek, maka lamanya pemrosesan semakin           bertambah dan kompleksitas dalam ruang yang berarti semakin komplek, maka penyimpanan akan semakin besar.
    
    <br/>
    
    Membaca Big O Notation: <br/>
    a) `O(log n)` yang berarti tingkat kompleksitas berbanding lurus dengan log dari banyaknya jumlah data. <br/>
    b) `O(1)` yang berarti tingkat kompleksitas bersifat konstan terhadap data yang masu.k <br/>
    c) `O(n)` yang berarti tingkat kompleksitas berbanding lurus dengan banyaknya data. <br/>
    d) `O(n+2)` atau O(2n+5) yang berarti tingkat kompleksitas sama dngan `O(n)`
    
    <br/>
    
  - #### Penyelesaian masalah melalui program
    Contoh kasus:
    
    <br/>
    
    ```md
    Buatlah Algoritma untuk menyelesaikan problem ini
    William ingin menampilkan deretan nilai dari 0 sampai N.
    N adalah nilai akhir yang diinputkan.
    Jika William menginput N dengan nilai 100, maka program akan menampilkan deretan nilai 1, 2, 3, 4, 5, … , 100
    ```
    
    <br/>
    Coding dengan JavaScript:
    <br/>
    
    ```js
    let i; 
    let n = 100;
    for(i = 0; i < n; i++){
      console.log(i)
    } 
    ```
    
    <br/>
    
  - #### Menerapkan Algoritma dengan JavaScript
    Contoh soal:<br/>
    
    ```md
      Tulis program untuk menentukan biaya parkir yang dihitung berdasarkan lama parkir. 
      lama parkir dihitung dari selisih jam masuk dan jam keluar diinput.
      Biaya parkir untuk motor adalah 2000 dan biaya parkir untuk mobil adalah 4000.
    ```
    
    <br/>
    
    ```js
      let masuk, keluar, jenis, selisih;
      masuk = prompt("Masuk jam berapa?")
      keluar = prompt("Keluar jam berapa?")
      jenis = prompt("jenis mobil(1) atau motor(2)?")
      selisih = keluar - masuk;
      alert(`selisih jam adalah ${selisih}`)

      if(jenis == 1){
        alert(`Mobil dengan pembayaran sebesar ${selisih * 4000}`)
      } else if(jenis == 2){
        alert(`Motor dengan pembayaran sebesar ${selisih * 2000}`)
      } else{
        alert("Input salah")
      }
    ```
    
  - #### Menerapkan Data Structure dengan JavaScript
    Contoh kasus :
    
    ```md
      Pengguna ingin memasukan sebuah data berbentuk array of object. 
      Di dalam objek terdapat skema data beruba id, nama, dan umur. 
      Bagaimana cara menginputkan data array tersebut ke dalam sebuah array dengan 
      ketentuan penyimpanan data dibebaskan berdasarkan keinginan pengguna. 
      Setelah itu, tampilkan data tersebut.
      
      Catatan: id tidak boleh ditentukan oleh pengguna, tetapi harus otomatis terbuat.
    ```
    
    <br/>
    
    ```js
      let data = []

      let tambahOrang = prompt("Berapa orang yang ingin kamu tambahkan ?")

      if(tambahOrang > 0){
        for(let i = 0; i<tambahOrang; i++){
          let nama = prompt("Masukan nama")
          let umur = parseInt(prompt("berapa umurnya"))
          let id = data.length + 1;
          let obj = {id,nama,umur}
          data.push(obj)
        }
      }

      data.map(e => console.log(e.id + " " + e.nama + " " + e.umur))
    ```
    
    <br/><br/>

### 6 JavaScript Dasar
  - #### Peran JavaScript dalam web development
    <div align="justify">
    Peran JavaScript dalam pengembangan sebuah website untuk membuat website menjadi lebih interaktif dan dinamis. Interaktif dalam artian dapat memanipulasi     elemen HTML dan CSS. Lalu, disebut dinamis juga karena tidak ada ketentuan tipe data seperti di beberapa variabel harus menggunakan String atau Number.       Pada saat ini, JavaScript tidak hanyak digunakan untuk kepentingan Front end, tetapi bisa untuk back end  
  <br/>
    </div>
    
    <br/>
    
  - #### Menjalankan JavaScript
    <div align="justify">
    Cara menjalankan JavaScript hanya dengan membuka sebuah teks editor seperti VS Code dan browser seperti Firefox, Chrome, Microsoft Edge, dan lain             sebagainya. Namun, tidak hanya itu, JavaScript harus dihubungkan terlebih dahulu dengan halaman HTML. JavaScript dihubungkan dengan 2 cara yaitu secara       internal (diletakan ke dalam tag script) dan eksternal (diletakan di luar halaman HTML).
    </div>
    
    <br/>
    Internal :
    <br/>
    
    ```html
       <!DOCTYPE html>
        <html lang="en">
          <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, initial-scale=1.0" />
            <title>Document</title>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <script>
              console.log("check");
            </script>
          </body>
        </html>
    ```
    
    <br/>
    Eksternal :
    <br/>
    
    ```html
       <!DOCTYPE html>
        <html lang="en">
          <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, initial-scale=1.0" />
            <title>Document</title>
            <link rel="stylesheet" href="style.css" />
          </head>
          <body>
            <script src="app.js"></script>
          </body>
        </html>
    ```
    
    <br/>
    
    halaman `app.js` :
    
    <br/>
    
    ```js
    console.log("hai")
    ```
    
  - #### Jenis tipe data di JavaScript
    Tipe data di dalam JavaScript dibedakan menjadi 2 jenis yaitu tipe data primitif dan tipe data non primitif.
    <br/>
    
    Tipe data primitif: <br/>
      - #### String
        Tipe data ini akan bernilai teks yang dibuktikan dengan adanya tanda kutip (".....").<br/>
      
      - #### Number
        Tipe data ini akan bernilai angka, tanpa tanda kutip. <br/>

      - #### Boolean
        Tipe data ini akan bernilai kebenaran yaitu true (1) atau false (0). <br/>

      - #### Undefined
        Tipe data ini akan muncul apabila nilai dari suatu variabel belu diinisialisasi.

      - #### Null
        Tipe data ini akan muncul apabila sebuah variabel diinisialisasi dengan `null`. Namun, bukan berarti tidak memiliki nilai seperti `undefined`.<br/><br/>
      
    Tipe data non primitif: <br/>
      - #### Object
        Tipe data ini menyimpan sebuah nilai (properti) dan fungsi (method). Object bisa dibangun dengan mendeklarasikan variabel lalu diikuti dengan kurung         kurawal `{}`. Di dalam kurung kurawal tersebut bisa terdiri dari berbagai macam tipe data lainya seperti `String`, `Number`, dan lain-lain. <br/>
        
      - #### Array
        Tipe data ini hampir sama dengan Object yang dapat menyimpan banyak data dan beragam tipe data (untuk JavaScript dan bahasa pemrograman yang                 mendukung banyak data yang bisa menyimpan tipe data yang berbeda). Namun, tidak memiliki properti dan method, maka dari itu mendapatkan data dari             `array` menggunakan indeks yang dimulai dari angka 0. <br/>

      - #### RegExp
        Tipe data ini berbentuk string teks yang digunakan untuk mencari pola pencarian. <br/><br/>

  - #### Operator di JavaScript
    JavaScript memiliki 6 jenis operator:
      - #### Operator aritmatika
      
          ```md
           Operator (+) untuk penambahan
           Operator (-) untuk pengurangan
           Operator (*) untuk pengalian
           Operator (**) untuk pangkat
           Operator (/) untuk pembagian
           Operator (%) untuk mencari hasil bagi
           Operator (++) untuk menambahkan 1
           Operator (--) untuk mengurangi 1
          ```
          
          <br/>
          
      - #### Operator penugasan
        
        ```md
           Operator (=)   contoh : x = y
           Operator (+=)  contoh (x += y) == (x = x + y)
           Operator (-=)  contoh (x -= y) == (x = x - y)
           Operator (*=)  contoh (x *= y) == (x = x * y)
           Operator (/=)  contoh (x /= y) == (x = x / y)
           Operator (%=)  contoh (x %= y) == (x = x % y)
           Operator (**=) contoh (x **= y) == (x = x ** y)
          ```
          
          <br/>

      - #### Operator perbandingan

        ```md
           Operator (==)   digunakan untuk membandingkan kesamaan sebuah nilai
           Operator (===)  digunakan untuk membandingkan kesamaan sebuah nilai dan tipe data dari nilai
           Operator (!=)   digunakan untuk membandingkan ketidaksamaan sebuah nilai
           Operator (!==)  digunakan untuk membandingkan ketidaksamaan sebuah nilai dan tipe data dari nilai
           Operator (>)    digunakan untuk membandingkan lebih besar
           Operator (<)    digunakan untuk membandingkan lebih kecil
           Operator (>=)   digunakan untuk membandingkan lebih besar atau sama dengan
           Operator (<=)   digunakan untuk membandingkan lebih kecil atau sama dengan
           Operator (?)    merupakan operator ternari
          ```
          
          <br/>

      - #### Operator logika
        
        ```md
           Operator (&&)   logika AND
           Operator (||)   logika OR
           Operator (!)    logika NOT
          ```
          
          <br/>

      - #### Operator tipe
         ```md
           Operator typeof       mengembalikan jenis tipe data
           Operator instanceof   mengembalikan TRUE apabila bertipe objek
          ```
          
          <br/>
        
    
  - #### Control flow (looping & conditional)
    Control flow ada 2 yaitu looping untuk pengulangan dan conditional untuk pengondisian. <br/>
    Contoh looping di JavaScript:<br/>
      
      - #### for
        Di dalam pengulangan for terdapat komponen utama yaitu initial statement, test expression, dan update statement. <br/>
        
        ```js
          for(initial statement; test expression; update statement){
            pernyataan ...
          }
        ```
        
        <br/>
        Contoh:
        
        ```js
          for(let i = 0; i < 5; i++){
            console.log(i);
          }
        ```
        
        <br/>
        
      - #### while
        Pengulangan while akan dieksekusi apabila pengondisianya sesuai. <br/>
        
        ```js
          while(kondisi) {
             pernyataan ...
          }
        ```
        
        <br/>
        Contoh:
        
        ```js
          let i = 0;
          while(i<5){
            console.log(i);
            i++;
          }
        ```
        
        <br/>
        
      - #### for in
        Melakukan pengulangan melalui properti pada objek. <br/>

        ```js
          for(key in object){
            pernyataan ...
          }
        ```
        
        <br/>
        Contoh:
        
        ```js
          let data = {nama1:"Hafi", nama2:"Ihza"}
          for(let x in data) {
            console.log(data[x])
          }
        ```
        
        <br/>

      - #### for of
        Melakukan pengulangan di atas nilai dari setiap iterasi. <br/>
        
        ```js
          for(variabel of iterable){
            pernyataan ...
          }
        ```
        
        <br/>
        Contoh:
        
        ```js
          let data = ["Hafi", "Ihza"]
          for(let x of data) {
            console.log(data[x])
          }
        ```
        
        <br/>

      - #### do while
        Pengulangan ini setidaknya akan mengeksekusi 1 pernyataan meskipun kondisinya salah.
        
        ```js
          do{
            pernyataan ...
          } while(kondisi)
        ```
        
        <br/>
        Contoh:
        
        ```js
          let i = 0
          do{
            console.log("hai")
            i++
          } while(i<5)
        ```

    <br/><br/>
    
    Contoh conditional di JavaScript
      - #### if..else if..else
        
        ```js
          
          if(kondisi 1){
            pernyataan 1 ...
          } else if(kondisi 2) {
              pernyataan 2 ...
            } else{
                pernyataan sisa ...
              }
          
        ```
        
        <br/>
        Contoh:
        <br/>
        
        ```js
          let a = 1;
          if(a == 1){
            console.log("benar")
          } else if(kondisi 2) {
              console.log("salah")
            } else{
                console.log("error")
              }
        ```
        
        <br/>

      - #### switch

        ```js
          switch(ekspresi) {
            case x:
              pernyataan ...
              break;
            case y:
              pernyataan ...
              break;
            default:
              pernyataan ...
          }
        ```
        
        <br/>
        Contoh:
        <br/>
        
        ```js
          let a = 1;
          switch(a) {
            case 1:
              console.log("benar")
              break;
            case 2:
              console.log("salah")
              break;
            default:
              console.log("error")
          }
        ```
