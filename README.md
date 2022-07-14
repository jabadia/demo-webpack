# steps

add node_modules to .gitignore

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
