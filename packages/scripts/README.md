## Draft

Possible `package.json`

```json
{
	"name": "@wpw/scripts",
	"version": "0.0.0",
	"description": "@wpws/scripts is a single dependency for using WordPress webpack script.",
	"main": "index.js",
	"repository": "https://github.com/swashata/wp-webpack-script",
	"author": "Swashata Ghosh",
	"license": "MIT",
	"private": false,
	"dependencies": {
		"@babel/core": "^7.1.0",
		"@babel/plugin-proposal-class-properties": "^7.1.0",
		"@babel/plugin-proposal-object-rest-spread": "^7.0.0",
		"@babel/preset-env": "^7.1.0",
		"@babel/preset-react": "^7.0.0",
		"autoprefixer": "^9.1.5",
		"babel-loader": "^8.0.2",
		"browser-sync": "^2.24.7",
		"clean-webpack-plugin": "^0.1.19",
		"cross-env": "^5.2.0",
		"css-loader": "^1.0.0",
		"mini-css-extract-plugin": "^0.4.3",
		"optimize-css-assets-webpack-plugin": "^5.0.1",
		"postcss-loader": "^3.0.0",
		"sass-loader": "^7.1.0",
		"style-loader": "^0.23.0",
		"uglifyjs-webpack-plugin": "^2.0.1",
		"webpack": "^4.19.1",
		"webpack-dev-middleware": "^3.3.0",
		"webpack-hot-middleware": "^2.24.0"
	},
	"publishConfig": {
		"access": "public"
	}
}
```