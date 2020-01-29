# getheader
Simple http/https detector(get response headers)

[![NPM version](https://img.shields.io/npm/v/getheader.svg)](https://www.npmjs.com/package/getheader)
[![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![npm](https://img.shields.io/npm/dt/getheader.svg)](https://www.npmjs.com/package/getheader)
[![node](https://img.shields.io/node/v/getheader.svg)](https://nodejs.org/en/download/)

```
npm install getheader
const detect = require('getheader');
```

### Example:1 (async/await)
```
(async () => {
    try{
        let info = await detect({
            url: 'https://www.78pan.com/api/stats/hls/2018/05/22/aDeuR3Zp/out005.ts',
            timeout:20000
        });
        console.log(info);
    }catch(e){
        console.log(e);
    }
})();
```

### Example:2 (chain called)
```
detect({
    url: 'https://www.78pan.com/api/stats/hls/2018/05/22/aDeuR3Zp/out005.ts',
    timeout:20000
}).then( (info) => {
    console.log( info );
} ).catch( e => console.log );
```