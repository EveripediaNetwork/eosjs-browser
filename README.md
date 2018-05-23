# EOS.js for the Browser

This repo contains a browser-friendly version of the [eosjs](https://github.com/EOSIO/eosjs) npm module. 

To use, copy the `eosjs-browser.js` into your web frontend's `js` folder and insert the script into your HTML. Replace `path/to` with the path to the directory containing `eosjs-browser.js`:

```
<body>
    ...
    <script src="path/to/eosjs-browser.js"></script>
    <script>
        // eosjs module is available under the global variable `EOS`
        eos = EOS.Testnet();
        eos.getBlock(1).then(result => {console.log(result)})
    </script>
```

The current version of eosjs is `12.0.0` with support for Dawn 4.1. We will update this as newer versions come out. 

See the eosjs [Github](https://github.com/EOSIO/eosjs) for tutorials. 

## Custom Versions

To compile a newer version of `eosjs-browser.js` file, run the following commands. If you want to use an older version, specify the version in `package.json` before running these commands. 

```
npm install -g browserify # try with sudo if this fails
npm install 
browserify main.js > eosjs-browser.js
```


## CDN Support

We are working on CDN support for the `eosjs-browser.js` file. If anybody can help make this happen, please create an issue to contact us. 
