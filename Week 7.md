# Writing and Presentation Test Week 7

## 1 Sequelize
- ### Memahami dan Menggunakan Sequalize
  Langkah menggunakan Sequelize sebagai ORM dari MySQL di Node JS dan Express JS:<br/>
  
  a) Install: <br/>
     Express JS <br/>
     
     ```bash
        npm i express
     ```
     
     <br/>
     
     mysql2 <br/>
     
     ```bash
        npm i mysql2
     ```
     
     <br/>
     
     sequelize <br/>
     
     ```bash
        npm i sequelize
     ```
     
     <br/>
     
     sequelize-cli <br/>
     
     ```bash
        npm i sequelize
     ```
     
     <br/>
     
  b) Lakukan inisialisasi project <br/>
  
     ```bash
        npx sequelize-cli init
     ```
     
     <br/>
     
  c) Konfigurasi database (Harus sudah memiliki MySQL) <br/>
     Berada di `config/config.js` <br/>
     
     ```js
        require("dotenv").config();
        module.exports = {
          development: {
            username: "root", //default
            password: "", //default
            database: "Nama Database Yang Telah Dibuat",
            host: "127.0.0.1", //default
            dialect: "mysql"
          }
        }
     ```
     
     <br/>
     
  d) Generate model <br/>
  
     ```bash
        npx sequelize-cli model:generate --name Noted -- attributes title:string
     ```
     
     <br/>
     
  e) Lakukan migrasi ke dalam database <br/>
  
     ```bash
        npm sequelize-cli db:migrate
     ```
     
     <br/>
     
- ### Membuat API Specification
  
  - ### HTTP
  GET (Mengambil data) <br/>
  POST (Menambah data) <br/>
  PUT (Merubah data) <br/>
  DELETE (Menghapus data) <br/>
  
  <table>
    <thead>
      <th>No</th>
      <th>Method</th>
      <th>Url</th>
      <th>Deskripsi</th>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>Get</td>
        <td>/notes/</td>
        <td>Mendapatkan seluruh data notes</td>
      </tr>
      <tr>
        <td>2</td>
        <td>Get</td>
        <td>/notes/{id}</td>
        <td>Mendapatkan data notes berdasarkan id</td>
      </tr>
      <tr>
        <td>3</td>
        <td>Post</td>
        <td>/notes/</td>
        <td>Mennambah ata notes</td>
      </tr>
      <tr>
        <td>1</td>
        <td>Put</td>
        <td>/notes/{id}</td>
        <td>Mengupdate data notes berdasarkan id</td>
      </tr>
      <tr>
        <td>1</td>
        <td>Delete</td>
        <td>/notes/{id}</td>
        <td>Merubah data notes berdasarkan id</td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
  <table>
    <tbody>
      <tr>
        <td>Get</td>
        <td>/notes/</td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Parameter</td>
      </tr>
      <tr>
        <td>Nama</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>Pembatasan data</td>
        <td><b> Tidak ada </b></td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Response</td>
      </tr>
      <tr>
        <td>Kode</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>200</td>
        <td><b>Berhasil ambil data</b></td>
      </tr>
      <tr>
        <td></td>
        <td><b>application/json</b></td>
      </tr>
      <tr>
        <td>Skema</td>
        <td>
          { <br/>
            id (int), <br/>
            title (string), <br/>
            desc (string), <br/>
            createdAt (date), <br/>
            updatedAt (date) <br/>
          }<br/>
        </td>
      </tr>
      <tr>
        <td>Contoh</td>
        <td>
          { <br/>
            id : "1", <br/>
            title : "Kampungku", <br/>
            desc : "Kampung durian runtuh", <br/>
            createdAt : "2022-11-12", <br/>
            updatedAt : "2022-11-12" <br/>
          }<br/>
        </td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
  <table>
    <tbody>
      <tr>
        <td>Post</td>
        <td>/notes/</td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td>Parameter</td>
        <td><b>Tanpa Parameter</b></td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Response</td>
      </tr>
      <tr>
        <td>Kode</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>200</td>
        <td><b>Berhasil tambah data</b></td>
      </tr>
      <tr>
        <td>Request Body</td>
        <td><b>application/json</b></td>
      </tr>
      <tr>
        <td>Body</td>
        <td>
          { <br/>
            title (string), <br/>
            desc (string), <br/>
          }<br/>
        </td>
      </tr>
      <tr>
        <td>Contoh</td>
        <td>
          { <br/>
            title : "Kampungku", <br/>
            desc : "Kampung durian runtuh", <br/>
          }<br/>
        </td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
  <table>
    <tbody>
      <tr>
        <td>Get</td>
        <td>/notes/{id}</td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Parameter</td>
      </tr>
      <tr>
        <td>Nama</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>Pembatasan data</td>
        <td><b> 1 data </b></td>
      </tr>
      <tr>
        <td>{id}</td>
        <td><b> int </b></td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Response</td>
      </tr>
      <tr>
        <td>Kode</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>200</td>
        <td><b>Berhasil ambil data dengan id {id}</b></td>
      </tr>
      <tr>
        <td></td>
        <td><b>application/json</b></td>
      </tr>
      <tr>
        <td>Skema</td>
        <td>
          { <br/>
            id (int), <br/>
            title (string), <br/>
            desc (string), <br/>
            createdAt (date), <br/>
            updatedAt (date) <br/>
          }<br/>
        </td>
      </tr>
      <tr>
        <td>Contoh</td>
        <td>
          { <br/>
            id : "1", <br/>
            title : "Kampungku", <br/>
            desc : "Kampung durian runtuh", <br/>
            createdAt : "2022-11-12", <br/>
            updatedAt : "2022-11-12" <br/>
          }<br/>
        </td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
  <table>
    <tbody>
      <tr>
        <td>Put</td>
        <td>/notes/{id}</td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Parameter</td>
      </tr>
      <tr>
        <td>Nama</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>Pembatasan data</td>
        <td><b> 1 data </b></td>
      </tr>
      <tr>
        <td>{id}</td>
        <td><b> int </b></td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Response</td>
      </tr>
      <tr>
        <td>Kode</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>200</td>
        <td><b>Berhasil update data dengan id {id}</b></td>
      </tr>
      <tr>
        <td></td>
        <td><b>application/json</b></td>
      </tr>
      <tr>
        <td>Body</td>
        <td>
          { <br/>
            title (string), <br/>
            desc (string), <br/>
          }<br/>
        </td>
      </tr>
      <tr>
        <td>Contoh</td>
        <td>
          { <br/>
            title : "Kampungku", <br/>
            desc : "Kampung durian runtuh", <br/>
          }<br/>
        </td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
  <table>
    <tbody>
      <tr>
        <td>Delete</td>
        <td>/notes/{id}</td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Parameter</td>
      </tr>
      <tr>
        <td>Nama</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>Pembatasan data</td>
        <td><b> 1 data </b></td>
      </tr>
      <tr>
        <td>{id}</td>
        <td><b> int </b></td>
      </tr>
      <tr>
        <td colspan="2"></td>
      </tr>
      <tr>
        <td colspan="2">Response</td>
      </tr>
      <tr>
        <td>Kode</td>
        <td>Deskripsi</td>
      </tr>
      <tr>
        <td>200</td>
        <td><b>Berhasil hapus data dengan id {id}</b></td>
      </tr>
      <tr>
        <td></td>
        <td><b>application/json</b></td>
      </tr>
    </tbody>
  </table>
  
  <br/>
  
- ### membuat web server dan RESTFul API

  `/config/config.js`
  
  ```js
    require("dotenv").config();
    module.exports = {
      development: {
        username: process.env.DB_USERNAME,
        password: process.env.DB_PASSWORD,
        database: process.env.DB_NAME,
        host: process.env.DB_HOSTNAME,
        dialect: process.env.DB_DIALECT
      }
    }
  ```
  
  <br/>
  
  `/models/m_notes.js`
  
  ```js
    module.exports = (sequelize, DataTypes) => {
    const Notes = sequelize.define(
        "Notes",
        {
            id:{
                type:DataTypes.INTEGER,
                primaryKey: true,
                autoIncrement: true,
                allowNull: false
            },
            title:{
                type:DataTypes.STRING(40),
                allowNull:false
            },
            desc:{
                type:DataTypes.TEXT
            },
            createdAt:{
                type:DataTypes.DATE,
                allowNull:false
            },
            updatedAt:{
                type:DataTypes.DATE,
                allowNull:false
            }
        },
        {
            tableName:"notes" //sesuaikan dengan nama table di database
        }
    );

    return Notes; 
  }
  ```
  
  <br/>
  
  `index.js`
  
  ```js
    require("dotenv").config();
    const express = require('express');
    const cookieParser = require('cookie-parser');

    const app = express()

    app.use(express.json())
    app.use(express.urlencoded({extended:true}))
    app.use(cookieParser())

    const listRoute = require('./routes')

    app.use(listRoute)

    app.listen(process.env.PORT, (err, res) => {
        if(err) throw err
        console.log(`Berjalan di port ${process.env.PORT}`)
    })
  ```
  
  <br/>
  
  `/routes/r_notes.js`
  
  ```js
    const express = require('express');
    const router = express.Router();

    const {getAllPosts, getPostById, postData, updateData, hapusData} = require('./../controller/c_notes')

    // GET ALL DATA
    router.get('/', getAllPosts)

    // GET DATA BY ID
    router.get("/:id", getPostById);

    // POST DATA
    router.post('/', postData)

    // UPDATE DATA
    router.put("/:id", updateData);

    // DELETE
    router.delete("/:id", hapusData);

    module.exports = router
  ```
     
## 2 Mongo DB
## 3 Mongoose
## 4 Docker
## 5 API with Post Man
