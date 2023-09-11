# Quick UI Template [2023]
This project can used for quick template generations with a little bit of help, useful for prototyping.
Using **PARCEL** as the bundler and builder for development purposes.

```

Please fork the project to start a new project

```

## Usage
1. develop with browser-sync, allows live preview and autoreload 
```
npm start
```

2. process and copy src files to publish folder for deployment
```
npm run build
```

## starting point
```
./src/index.html
```

## additional note
```
.npmrc
```
this is for pnpm and controlling which node version to run with. But not nesscessary, PARCEL can run with the current starting point.

using: **posthtml-include** package, this allows for html template includes

``` example
<include src="./htmltpl/header-tpl.html"></include>
```


browser-sync start --proxy "localhost:1234" --files "dist/*.*"
