# Belajar Node JS

### Basic Node JS

- Cara manggil node js dengan cara bikin lokal web server

  ```js
  var http = require('http');

  http.createServer(function (req, res) {
      res.writeHead(200, { 'Content-Type': 'text/html' });
      res.write("Halo gais");
      res.end();
  }).listen(8080);

  ```

- Cara run node js make terminal
  ```ssh
  node contohFile.js
  ```
  nanti lokal web server bakal jalan, kalo matiinnya make **CTRL + C**

- Modules
  Modules bisa dianggap sebagai library seperti halnya dalam javascript, yakni merupakan satu set fungsi yang ingin digunakan pada aplikasi anda

- Modul bawaan
  Dalam node js ada modul bawaan yang bisa digunakan tanpa instalasi lebih lanjut
  
- Cara manggil modul

  ```js
  var http = require('http');
  ```
  
- Cara bikin modul sendirii

  ```js
  var http = require('http');
  var dt = require('./lokasiFile')

  http.createServer(function (req, res) {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('Sekarang tanggal : ' + dt.myDateTime());
  }).listen(8080);

  ```
  
  ```js
  // bikin modul 
  exports.myDateTime = function () {
    return Date();
  };
  ````
