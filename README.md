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
  
- Cara bikin module sendirii

  ```js
  var http = require('http');
  var dt = require('./myfirstmodule')

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
