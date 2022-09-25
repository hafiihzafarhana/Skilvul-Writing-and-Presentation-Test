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
  <div align="justify">Hal yang menjadi akan hal ini adalah seorang programmer tidak akan bekerja sendirian. Seorang programmer pasti akan bekerja dengan       tim. Namun, hal ini akan menjadi permasalahan karena programmer akan menyalin ulang seluruh file secara manual dan bahkan akan menunggu rekan tim untuk       menyelesaikan bagianya masing-masing. Hal ini dapat dipecahkan dengan adanya Git dan GitHub karena menjadi media untuk berkolaborasi dengan tim. Adanya Git   dan GitHub memungkinkan programmer bekerja dengan tim tanpa saling menunggu bagianya masing-masing dan tidak perlu meyalin seluruh file, hanya file atau     folder yang terupdate saja.</div>
  
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
      - Fase stging area (stagged) merupakan kondisi perubahan telah ditandai (tracked) dan belum disimpan di version control.
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
   <div align="justify">Terdapat 2 _tools_ utama untuk mempersiapkan HTML yaitu Browser (Google Chrome, Microsoft Edge, Firefox, Opera, dan lain sebagainya)    dan Code Editor (VS Code, Sublime text, Notepad, dan lain sebagainya.
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
   a) IMG
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
   
   b) Video
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

   c) Table
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
   
   d) Form
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
   
   Beberapa tag semantic HTML :
   <br/>
   Penerapan `<article>` :
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
   
   Penerapan `<aside>` :
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
   
   Penerapan `<details>` :
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
   
   Penerapan `<footer>` :
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
   
   Penerapan `<header>` :
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
   
   Penerapan `<main>` :
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
   
   Penerapan `<nav>` :
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
   
### 4 CSS

### 5 Algorithm

### 6 JavaScript Dasar
