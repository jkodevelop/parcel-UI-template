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

3. start browser-sync (open new terminal)
```
browser-sync start --proxy "localhost:1234" --files "dist/*.*"
```

## starting point
```
./src/index.html
```

## parcel notes
```
parcel src/index.html --open
```
option `--open` opens default browser when starting

## additional note
```
.npmrc
```
this is for pnpm and controlling which node version to run with. But not nesscessary, PARCEL can run with the current starting point.

using: **posthtml-include** package, this allows for html template includes

``` example
<include src="./htmltpl/header-tpl.html"></include>
```

# adding tailwindcss

source:
https://tailwindcss.com/docs/guides/parcel

1. install tailwindcss and postcss

```
npm install -D tailwindcss
npm install -D postcss
```

2. add .postcssrc

3. path to source in "content" in tailwind.config.js

4. add directive to main CSS file
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5. use tailwind css classes
https://tailwindcomponents.com/cheatsheet/

## How do I use tailwindcss with SASS/SCSS

source:
https://stackoverflow.com/questions/76233402/how-to-use-scss-with-tailwind-css

**note: sample config below assumes all code files are somewhere inside a folder named "src" under project's root.**

```
[label tailwind.config.js]
/** @type {import('tailwindcss').Config} */
module.exports = {
  mode: "jit",
  module: {
    rules: [
      {
        test: /\.scss$/,
        use: [
          'style-loader',
          'css-loader',
          'sass-loader',
        ],
      },
    ],
  },
  content: [
    "./src/**/*.{html,js,ts,jsx,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```


### final note:
look through files for reference and usage