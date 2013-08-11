Originally by Nick Campbell (http://github.com/ncb000gt)

Shoutcast
============

Shoutcast is a popular streaming audio server protocol. NodeJS lends itself very nicely to doing this kind of thing so building an app around it makes sense.


Disclaimer
============

This is alpha software. Since it was abandoned, I am forking so I can
develop it for http://sonicradioboom.com/ without waiting to patch. It is fully
compatible with the centovacast module's public interface (except for connect())


Usage
============

From the CLI

`node shoutcast.js [mp3 directory]`

From Code

    var cast = require('shoutcast');
    var station = cast.Station(conf);

    http.createServer(function (req, res) {
      station.connect(res, function() {
        console.log("Stream ended?");
      });
    }).listen(7000);

    station.start();


License
============

MIT
