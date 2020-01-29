# httpdetector
Simple http/https detector(get response headers)

[![NPM version](https://img.shields.io/npm/v/httpdetector.svg)](https://www.npmjs.com/package/httpdetector)
[![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![npm](https://img.shields.io/npm/dt/httpdetector.svg)](https://www.npmjs.com/package/httpdetector)
[![node](https://img.shields.io/node/v/httpdetector.svg)](https://nodejs.org/en/download/)

```
npm install httpdetector
const detect = require('httpdetector');
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