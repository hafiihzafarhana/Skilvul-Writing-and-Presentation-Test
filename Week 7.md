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
  
  <br/> <br/>
     
## 2 Mongo DB
- ### Basic Dari MongoDB
  
  Skema Mongo DB adalah JSON : <br/>
  
  ```json
    {
       field1: value1,
       field2: value2,
       field3: value3,
       ...
       fieldN: valueN
    }
  ```
  
  <br/>
  
  Tipe data skema dari Mongo DB : <br/>
  
  ```md
    Object
      Array

      String

      Number

      Boolean

      UUID

      ObjectId

      Binary Data

      Mixed

      Set

      Dictionary
  ```
  
  <br/>
 
- ### Operasi CRUD Pada MongoDB
  CRUD dengan menggunakan Mongo DB : <br/>
  
  a) Menambah banyak data <br/>
  
  ```js
    db.orang.insertMany(
      [
        {nama:"hafi", umur: "20"},
        {nama:"ihza", umur: "20"}
      ]
    );
  ```
  
  <br/>
  
  b) Menampilkan banyak data <br/>
  
  ```js
    db.orang.find({});
    
    //apabila ada kondisi AND
    const cursor = db.orang.find({
      hafi: 'hafi',
      umur: { $gt: 30 }
    });
    
    //apabila ada kondisi OR
    const cursor = db.orang.find({
      $or: [{ nama: 'hafi' }, { umur: { $gt: 10 } }]
    });
  ```
  
  <br/>
  
  c) Menampilkan data spesifik<br/>
  
  ```js
    db.orang.find({nama:"hafi"});
  ```
  
  <br/>

  e) Menambah satu data<br/>
  
  ```js
    db.orang.insertOne( { nama:"farhana",  umur:"20"} )
    
    //or
    
    db.orang.createIndex( { nama:"farhana",  umur:"20"} )
    
    // kedua hal di atas bisa diakses apabila tidak ada database
  ```
  
  f) Menghapus banyak data <br/>
  
  ```js
    db.orang.deleteMany({})
    
    // terdapat kondisinya
    db.orang.deleteMany({ nama : "hafi" })
  ```
  
  <br/>
  
  g) Menghapus satu data <br/>
  
  ```js
    db.orang.deleteOne( { nama : "hafi" } )
  ```
  
  <br/>

- ### Relasi Pada MongoDB
    
  - #### One-to-One
      Pada contohnya satu pengguna hanya memiliki satu nama saja. <br/>
      
      ```js
        {
            "_id": "ObjectId('AAA')",
            "name": "Joe Karlsson",
            "company": "MongoDB",
            "twitter": "@JoeKarlsson1",
            "twitch": "joe_karlsson",
            "tiktok": "joekarlsson",
            "website": "joekarlsson.com"
        }
      ```
      
      <br/>
      
   - #### One-to-Few
      Pada contohnya satu pengguna memungkinkan memiliki sebuah data yang cukup banyak. Dan data tersebut akan dimasukan ke dalam Array secara bersamaan. <br/>
      
      ```js
        {
            "_id": "ObjectId('AAA')",
            "name": "Joe Karlsson",
            "company": "MongoDB",
            "twitter": "@JoeKarlsson1",
            "twitch": "joe_karlsson",
            "tiktok": "joekarlsson",
            "website": "joekarlsson.com",
            "addresses": [
                { "street": "123 Sesame St", "city": "Anytown", "cc": "USA" },  
                { "street": "123 Avenue Q",  "city": "New York", "cc": "USA" }
            ]
        }
      ```
      
      <br/>
      
  - #### One-to-Many
      Pada contohnya seperti pengguna memiliki banyak catatan dan akan dimodel dengan bentuk reference. <br/> 
      
      `pengguna`
      
      ```js
        {   "_id" : "ObjectID('bos1')",
            "name": "Hafi",
            "parts": ["ObjectID('AAAA')", "ObjectID('BBBB')", "ObjectID('CCCC')"]
        }
      ```
      
      `catatan`
      
      ```js
        {
            "_id" : "ObjectID('AAAA')",
            "name" : "catatan 1"
        },
        {
            "_id" : "ObjectID('BBBB')",
            "name" : "catatan 2"
        },
        {
            "_id" : "ObjectID('CCCC')",
            "name" : "catatan 3"
        }
      ```
      
      <br/>
      
  - #### One-to-Squillions
      </div align="justify">Pada contohnya adalah dibuatkan 2 koleksi yaitu koleksi pengguna dan catatan. Maka setiap catatan akan memiliki id reference dari pengguna. Konsepnya sama dengan One-to-Many, tetapi yang membedakan adalah setiap pengguna akan menyimpan id reference dari catatan. Hal itu sangat buruk karena setiap dokumen hanya akan menampung 16 mb saja. Sehingga apabila catatan semakin banyak, otomatis penyimpanan akan semakin besar. </div> <br/>
      
      `pengguna`
      
      ```js
        {
            "_id" : "ObjectID('bos1')",
            "name": "Hafi",
            "parts": ["ObjectID('AAAA')", "ObjectID('BBBB')", "ObjectID('CCCC')"]
        }
      ```
      
      `catatan`
      
      ```js
        {
            "_id" : "ObjectID('AAAA')",
            "name" : "catatan 1",
            "pengguna" : "ObjectID('bos1')"
        },
        {
            "_id" : "ObjectID('BBBB')",
            "name" : "catatan 2",
            "pengguna" : "ObjectID('bos1')"
        },
        {
            "_id" : "ObjectID('CCCC')",
            "name" : "catatan 3",
            "pengguna" : "ObjectID('bos1')"
        }
      ```
      
      <br/>
      
  - #### Many-to-Many
      </div align="justify">Pada contohnya adalah dibuatkan 2 koleksi yaitu koleksi pengguna dan catatan. Maka setiap koleksi akan memiliki kumpulan id menyilang yaitu banyak pengguna dapat membuat banyak catatan dan banyak catatan dibuat oleh banyak pengguna. </div> <br/>
      
      `pengguna`
      
      ```js
        {
            "_id" : "ObjectID('bos1')",
            "name": "Hafi",
            "parts": ["ObjectID('AAAA')", "ObjectID('BBBB')", "ObjectID('CCCC')"]
        },
        {
            "_id" : "ObjectID('bos2')",
            "name": "Ihza",
            "parts": ["ObjectID('AAAA')", "ObjectID('BBBB')", "ObjectID('CCCC')"]
        }
      ```
      
      `catatan`
      
      ```js
        {
            "_id" : "ObjectID('AAAA')",
            "name" : "catatan 1",
            "pengguna" : ["ObjectID('bos1')", "ObjectID('bos2')"]
        },
        {
            "_id" : "ObjectID('BBBB')",
            "name" : "catatan 2",
            "pengguna" : "ObjectID('bos1')",
            pengguna" : ["ObjectID('bos1')", "ObjectID('bos2')"]
        },
        {
            "_id" : "ObjectID('CCCC')",
            "name" : "catatan 3",
            "pengguna" : "ObjectID('bos1')",
            pengguna" : ["ObjectID('bos1')", "ObjectID('bos2')"]
        }
      ```
      
    <br/><br/>
    
## 3 Mongoose
- ### Membuat API Specification

| Atrributes    | Tipe Data | Deksripsi                     |
| ------------- | --------- | ----------------------------  |
| pengguna      | String    | nama akun pengguna            |
| pesan         | String    | untuk menambah pesan pengguna |
| likes         | Integer   | untuk menambah pesan pengguna |
| editable      | Boolean   | untuk mengetahui pesan bisa diedit atau tidak            |
| balasan       | Array     | data diri pengguna            |

  - #### Skema Tambah Data
  
  | Atrributes    | Tipe Data | Deksripsi                     |
| ------------- | --------- | ----------------------------  |
| pengguna      | String    | nama akun pengguna            |
| pesan         | String    | untuk menambah pesan pengguna |
| likes         | Integer   | untuk menambah pesan pengguna |
| editable      | Boolean   | untuk mengetahui pesan bisa diedit atau tidak            |

Request :

- Method : POST
- Endpoint : /tambah-data
- Header :
  - Content-Type : application/json
  - Accept : application/json

- Body : <br/>

```javascript
    {
        "pengguna" : "string",
        "pesan" : "string",
        "likes" : "integer",
        "editable" : "boolean",
    }
```

<br/>

- Response : <br/>

```javascript
    {
        "msg" : "Berhasil Tambah Data",
    }
```

<br/>

  - #### Skema Dapat Pesan Baru
  
Request :

- Method : GET
- Endpoint : /quis/get-more-data
- Header :
  - Accept : application/json

- Response : <br/>

```js
  {
        "_id" : "string",
        "pengguna" : "string",
        "pesan" : "string",
        "likes" : "integer",
        "editable" : "boolean",
        "balasan": [{
          "pengguna":"string",
          "pesan":"string",
          "likes":"integer",
        }]
```

<br/>

  - #### Skema Tambah Sub Pesan Baru
  
Request :

- Method : PUT
- Endpoint : /tambah-sub-komen
- Header :
  - Accept : application/json

- Body : <br/>

```javascript
    {
        "pengguna" : "string",
        "pesan" : "string",
        "likes" : "integer",
        "editable" : "boolean",
    }
```

- Response : <br/>

```javascript
   "msg" : "berhasil dirubah"
```

<br/>

  - #### Skema Hapus Pesan

Request :

- Method : DELETE
- Endpoint : /hapus-komen
- Header :
  - Accept : application/json

- Body : <br/>

```javascript
    {
      "_id":string
    }
```

- Response : <br/>

```javascript
   "msg" : "berhasil dihapus"
```
  

- ### Membuat Web Server dan RESTFul API Menggunakan Mongoose

## 4 Docker
- ### Container Pada Docker
- ### Basic Dari Docker

## 5 API with Post Man
- ### Manfaat Postman
- ### Testing API dengan Postman
- ### API Documentation dengan Postman
