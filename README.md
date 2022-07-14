# steps

add `node_modules` to `.gitignore`

create project & install webpack

```sh
npm init -y
npm install -d webpack-cli 
```

execute webpack, create src/index.js and index.html

```sh
./node_modules/.bin/webpack
```

(error because no src is found)

```sh
mkdir src
touch src/index.js
```

edit index.js

```js
function main() {
	console.log('main');
}

main();
```

execute webpack

```sh
./node_modules/.bin/webpack
```

look at `./dist/main.js`

```js
console.log("main");
```

(code is minified)

add `/dist` to `.gitignore`, add `script` to `package.json`

```sh
npm run build
```

add an index.html

```sh
touch ./index.html
```

edit index.html

```html
<html>
<head>
</head>
<body>
	<script type="text/javascript" src="./dist/main.js"></script>
</body>
</html>
```

start a local server

```sh
python -m SimpleHTTPServer
```

open [http://0.0.0.0:8000](http://0.0.0.0:8000) and open the development console

![](doc-images/00_screenshot.png)

examine the network activity and console output
