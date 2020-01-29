# getheader
Simple http/https detector(get response headers)

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