## ![logo](http://ww2.sinaimg.cn/large/61ff0de3gw1easknn74dvj2019019t8i.jpg) btc ![npm](https://badge.fury.io/js/btc.png)

a command-line bitcoin price board for geeks

![screenshot](http://ww3.sinaimg.cn/large/61ff0de3gw1easzjzw8d6j20hn0ar74z.jpg)

### Installation
````
$ [sudo] npm install btc -g
````

### Command Line Interface
just run `btc` , prices board will show
````
$ btc 
````
#### Shortcuts
btc cli provides some useful shortcuts for you:
````
[enter]  ->  refresh prices as you wish
[g]      ->  go to current exchange market
[a]      ->  autorefresh the current exchange market every 10 seconds, 
             press [a] to cancel or [enter] to cancel all
[q]      ->  quit
````

### Example
````javascript
var btc = require('btc');

// fetch a prices list
btc.price(function(err, prices){
    console.log(prices);
});

// fetch a seleced exchanger
btc.price('btcchina', function(err, prices){
    console.log(prices);
});
````

### Add your coin's API
please feel free to add new coin's api:
````
$ git clone https://github.com/turingou/btc.git && cd btc
$ vi ./libs/exchangers.js
````
make sure every api has its unique `url` `site` and fill param `currency`.

### API
check this file: `index.js`

btc supports exchanges below:

- [btcchina](https://www.btcchina.com/): the bitcoin largest exchanger in China
- [bitstamp](https://www.bitstamp.net/)
- [btce](https://btc-e.com/)
- [futures796](http://bitcoinwisdom.com/markets/796/futures)
- [coinbase](https://coinbase.com)
- [okcoin](https://www.okcoin.com/)
- [chbtc](https://www.chbtc.com/)
- [fxbtc](http://www.fxbtc.com/)
- [btctrade](http://www.btctrade.com/)
- [btc100](https://btc100.org/)

### Contributors
```
 project  : btc
 repo age : 7 weeks
 active   : 12 days
 commits  : 24
 files    : 11
 authors  :
    14  Guo Yu                  58.3%
     4  Connor Keenan           16.7%
     2  Aleksander Gregorka     8.3%
     2  Glenn Murray            8.3%
     1  Andrew Seidl            4.2%
     1  ekousp                  4.2%
```

### Contributing
- Fork this repo
- Clone your repo
- Install dependencies
- Checkout a feature branch
- Feel free to add your features
- Make sure your features are fully tested
- Open a pull request, and enjoy <3
