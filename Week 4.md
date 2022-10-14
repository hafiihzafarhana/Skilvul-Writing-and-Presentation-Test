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
     

## 2 Responsive Web Design

## 3 Bootstrap
