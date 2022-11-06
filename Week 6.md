# Writing and Presentation Test Week 6

## 1 MySQL Basic
- ### Memahami database
  <div align="justify">Database merupakan kumpulan informasi yang disimpan di dalam komputer secara sistematik dan saling berelasi. Lalu, informasi di dalam database akan diolah yang kemudian menjadi sebuah data dan akan dikelolah oleh sistem. Dalam mengakses database diperlukan sebuah DBMS (Database Management System) yang merupakan media komunikasi antara pengguna dengan data yang ada di dalam media penyimpanan. </div> <br/>
  
  Konsep DBMS sebagai media komunikasi antar pengguna dengan database : <br/> <br/>
  <img src="https://2.bp.blogspot.com/-rFEgVEyHhWQ/Wplq0GGPKoI/AAAAAAAABOs/mIq324r3bC4aTGEXztEbUEF3u7G-Wi-cQCLcBGAs/s1600/5.png" width="500"/> <br/>
  Sumber : <i>https://aisaturrahmah.blogspot.com/2018/03/konsep-desain-software-database.html</i>

- ### Memahami Relational Database
  <div align="justify">Relasi database merupakan hubungan antara beberapa tabel yang ada di dalam sebuah database. Relasi antar tabel dihubungkan antara primary key dan foreign key. Primary key merupakan atribut unik dan mewakili satu entitas, sedangkan foreign key merupakan atribut yang melengkapi relasi dan menunjukan hubungan antara tabel induk dan anak. </div> <br/>
  
  Contoh hubungan antar tabel: <br/><br/>
    <img src="https://user-images.githubusercontent.com/71125093/200154679-ebaf0a48-0f1d-4299-b601-cea7755461fb.png" width="200"/> <br/><br/>
  
- ### Memahami Tipe Data Pada MySQL
  <div align="justify">Tipe data pada MySQL digunakan untuk mengidentifikasi jenis tipe yang dipakai di dalam setiap kolom di dalam sebuah tabel.</div> <br/>
  
  Jenis tipe data (Tipe data populer): <br/>
  A) Tipe data nomor (number) : <br/>
  
  ```sql
    - TINYINT(size), nilai berukuran dari 0 - 255
    - BOOLEAN, nilai bernilai TRUE atau FALSE
    - MEDIUMINT(size), nilai berukuran dari 0 - 16777215
    - INTEGER(size) / INT(size), nilai berukuran dari 0 - 4294967295
    - BIGINT(size), nilai berukuran 0 - 18446744073709551615
    - FLOAT(size, d), nilai memberikan nilai desimal
    - DOUBLE PRECISION(size, d), nilai memberikan nilai desimal
  ```
  
  <br/>
  B) Tipe data teks (string) : <br/>
  
  ```sql
    - CHAR(size), karakter memiliki panjang dari 0 - 255
    - VARCHAR(size), karakter memiliki panjang dari 0 - 65535
    - TINYTEXT, karakter memiliki panjang maksimum 255
    - TEXT(size), karakter memiliki panjang sebesar 65,535
    - ENUM(val1, val2, val3, ...), bernilai pemilihan kata
  ```
  
  <br/>
  C) Tipe data waktu (date & time) : <br/>
  
  ```sql
    - DATE, tipe data yang berformat YYYY-MM-DD
    - DATETIME(fsp), tipe data yang berformat YYYY-MM-DD hh:mm:ss
    - TIMESTAMP(fsp), tipe data yang berformat YYYY-MM-DD hh:mm:ss
    - TIME(fsp), tipe data yang berformat dari -838:59:59 sampai 838:59:59
    - YEAR, tipe data yang berformat YYYY
  ```
  
  <br/>
  
- ### Memahami dan melakukan Manipulasi Query Sederhana
  Manipulasi Query ada 4 yaitu mendapatkan, menambah, mengupdate, dan menghapus data. <br/>
  
  a) Mendapatkan data : <br/>
  
  ```sql
    SELECT * FROM nama_tabel;
  ```
  
  <br/>
  
  b) Menambah data : <br/>
  
  ```sql
    INSERT INTO nama_tabel (nama_entitas_1, nama_entitas_2, nama_entitas_n+1) VALUES(value_1, value_2, values_n+1);
  ```
  
  <br/>
  
  C) Mengupdate data : <br/>
  
  ```sql
    UPDATE nama_tabel SET nama_entitas1=value_1, nama_entitas_n+1=value_n+1 WHERE id_value=values_id;
  ```
  
  <br/>
  
  D) Menghapus data : <br/>
  
  ```sql
    DELETE FROM nama_tabel WHERE id_value=values_id;
  ```
  
  <br/><br/>

## 2 MySQL Lanjutan
- ### Memahami Dan Melakukan Manipulasi Query Tingkat Lanjut yang Sering Digunakan
  Manipulasi tingkat lanjut dari MySQL: <br/>
  
  A) Menggabungkan tabel yang saling berelasi : <br/>
  
  - #### INNER JOIN
    <div align="justify">Semua row akan diambil selama kolom cocok dengan kondisi yang ditentukan.</div> <br/>
    
    ```sql
      SELECT * FROM pengguna INNER JOIN asal ON pengguna.id_asal = asal.pengguna.id_asal
    ```
    
    <br/>
    
  - #### LEFT JOIN
    <div align="justify">Semua record dari tabel sisi kiri akan dipilih. Apabila kondisi tidak cocok, maka akan bernilai NULL</div> <br/>
    
    ```sql
      SELECT * FROM pengguna LEFT JOIN asal ON pengguna.id_asal = asal.pengguna.id_asal
    ```
    
    <br/>
    
  - #### RIGHT JOIN
    <div align="justify">Semua record dari tabel sisi kanan akan dipilih. Apabila kondisi tidak cocok, maka akan bernilai NULL</div> <br/>
    
    ```sql
      SELECT * FROM pengguna RIGHT JOIN asal ON pengguna.id_asal = asal.pengguna.id_asal
    ```
    
    <br/>
    
  B) Fungsi Aggregate <br/>
     Fungsi ini akan mengambil satu nilai setelah dilakukan penghitungan dari kumpulan data. Jenis fungsinya : <br/>
     
     - #### MAX (Mendapatkan nilai terbesar) <br/>

       ```sql
        SELECT MAX(id_user) FROM pengguna;
       ```
       
       <br/>
       
     - #### MIN (Mendapatkan nilai terkecil) <br/>

       ```sql
        SELECT MIN(id_user) FROM pengguna;
       ```
       
       <br/>
       
     - #### SUM (Menambahkan seluruh nilai) <br/>

       ```sql
        SELECT MAX(sub_total) as total FROM pesanan;
       ```
       
       <br/>
       
     - #### COUNT (Menghitung jumlah baris) <br/>

       ```sql
        SELECT COUNT(id_user) FROM pengguna;
       ```
       
       <br/>
       
     - #### AVG (Menghitung rata-rata nilai) <br/>

       ```sql
        SELECT AVG(sub_total) as total FROM pesanan;
       ```
       
       <br/>
       
     - #### UNION (Menggabungkan hasil dari pernyataan SELECT) <br/>

       ```sql
        SELECT * FROM data1
        UNION
        SELECT * FROM data2
       ```
       
       <br/>
  
     - #### GROUP BY (Mengelompokan baris yang memiliki nilai yang sama ke dalam baris ringkasan) <br/>

       ```sql
        SELECT * FROM pengguna GROUP BY id_user;
       ```
       
       <br/>
       
     - #### HAVING (Pengganti WHERE apabila berjalan dengan GROUP BY) <br/>

       ```sql
        SELECT * FROM pengguna GROUP BY id_user HAVING id_user > 10;
       ```
       
       <br/>
- ### Memahami dan Membuat Relational Antar Table
  Sebelum memasuki relasi database, harus memahami jenis relasi terlebih dahulu : <br/>
  
  A) Relasi ONE to MANY <br/>
     Relasi ini menghubungkan 1 tabel dengan banyak tabel yang akan dituju <br/>
  
  B) Relasi ONE to ONE <br/>
     Relasi ini menghubungkan 1 tabel dengan 1 tabel yang dituju. <br/>
     
  C) Relasi MANY to MANY <br/>
     Relasi ini menghubungkan banyak tabel dengan banyak tabel yang dituju. <br/>
     
  <div align="justify">Lalu, setelah memahami hal di atas perlu juga memahmi PRIMARY KEY (Menjadi acuan utama dari setiap tabel) dan FOREIGN KEY (Merupakan PRIMARY KEY yang telah dihubungkan dengan tabel yang dituju). </div> <br/> 

  Cara menghubungkan ke dua tabel di SQL : <br/>
  
   ```sql
      SELECT * FROM pengguna INNER JOIN asal ON pengguna.id_asal = asal.pengguna.id_asal
    ```
    
    <br/>
    JOIN merupakan langkah yang digunakan untuk menghubungkan atau berelasi antar tabel. <br/><br/>
    
## 3 Authentication & Authorization
- ### Memahami Beberapa Variasi Authentication dan Authorization
   - #### Jenis Autentikasi
     a) Single Factor Authentication <br/>
     <div align="justify">Autentikasi yang sangat sederhana dan banyak digunakan di masa sekarang. Autentikasi ini berupa memasukan sebuah identitas seperti password dan username. </div> <br/>
     
     b) Two Factor Authentication <br/>
     <div align="justify">Autentikasi ini dibuat setelah Single Factor Authentication dipakai yaitu adanya tambahan autentikasi seperti OTP dan sidik jari atau wajah.</div> <br/>
     
     c) Multi Factor Authentication <br/>
     <div align="justify">Autentikasi yang mewajibkan pengguna untuk memverifikasi 3 jenis identitas seperti ID pengguna (password dan username), sidik jari, dan beberapa pertanyaan yang berhubungan dengan pengguna. </div> <br/>
     
- ### Memahami Perbedaan Authnentication, Authorization, dan Encryption
   - #### Authentication
        <div align="justify">Merupakan metode terhadap seorang pengguna mengkonfirmasi sebagai pengguna valid yang dapat mengakses sebuah akun atau informasi tertentu</div> <br/>
        
   - #### Authorization
        <div align="justify">Merupakan proses penentuan terhadap pengguna yang terautentikasi tersebut diizinkan atau ditolak untuk melakukan satu atau lebih akses terhadap sistem.</div> <br/>
        
   - #### Encryption 
        <div align="justify">Merupakan proses pengubahan data menjadi format yang tidak bisa dibaca terkecuali apabila ada seseorang yang memiliki kunci untuk mengubah kembali data yang terenkripsi</div> <br/>
        
- ### Membuat Authentication dan Authorization
  Untuk penerapanya bisa menggunakan Express JS dengan bantuan module `jsonwebtoken`. <br/>
  
  ```js
      const express = require("express");
      const app = express();

      const PORT = 3000;

      app.use(express.json());
      
      const users = [
        { id: 1, email: "hafi@gmail.com", password: "hafi" },
        { id: 2, email: "ihza@gmail.com", password: "ihza" },
      ];
      
      const KEY = "IblisHanyaTidakSujudKepadaAdamTetapiTidakDengan Allah";

      // Proses autentikasi
      app.get("/auth", (req, res) => {
        const { email, password } = req.body;
        const userData = users.find(
          (item) => email === item.email && password === item.password
        );
        const token = jwt.sign(
          {
            id: userData.id,
          },
          KEY
        );

        if (userData) {
          res.json({
            message: "success login",
            token,
          });
        } else {
          res.status(401).json({
            message: "email or password are incorrect",
          });
        }
      });
      
      // Proses autorisasi
      app.get("/films/:id/subscribe", (req, res) => {
        try {
          const auth = req.headers.authorization;
          const token = auth.split(" ")[1];

          jwt.verify(token, KEY);

          res.json({
            message: "subscribe moviess",
          });
        } catch (error) {
          res.status(500).json({
            message: error.message
          });
        }
      })

      app.listen(PORT, () => {
        console.log("server running on port ", PORT);
      });
  ```
## 4 Sequelize
- ### Memahami dan Menggunakan Sequalize
