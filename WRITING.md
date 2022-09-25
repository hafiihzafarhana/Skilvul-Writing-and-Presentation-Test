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

    
### 2 Git & Github Dasar

### 3 HTML

### 4 CSS

### 5 Algorithm

### 6 JavaScript Dasar
