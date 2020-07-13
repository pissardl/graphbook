GRAPHBOOK
--- 
www.packt.com
https://github.com/PacktPublishing/Hands-on-Full-Stack-Web-Development-with-GraphQL-and-React
--- 
md graphbook
cd graphbook
npm init
npm install --save react react-dom
npm install --save-dev @babel/core babel-eslint babel-loader @babel/preset-env @babel/preset-react clean-webpack-plugin css-loader eslint file-loader html-webpack-plugin style-loader url-loader webpack webpack-cli webpack-dev-server @babel/plugin-proposal-decorators @babel/plugin-proposal-function-sent @babel/plugin-proposal-export-namespace-from @babel/plugin-proposal-numeric-separator @babel/plugin-proposal-throw-expressions @babel/plugin-proposal-class-properties
npx install-peerdeps --dev eslint-config-airbnb
Creare file ".eslintrc"
Creare file "webpack.client.config.js"

con "package.json" :
"scripts": {
    "client": "webpack-dev-server --devtool inline-source-map --hot --config webpack.client.config.js",
si puo eseguire
npm run client

Controllo degli Head con React Helmet
npm install --save react-helmet


Build di PRODUCTION con webpack

npm install --save-dev mini-css-extract-plugin

con "package.json" :
"scripts": {
    "client:build": "webpack --config webpack.client.build.config.js",
si puo eseguire
npm run client:build
(genera sotto /dist/)

Strumenti
https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi

npm install --save-dev webpack-bundle-analyser
con
  "scripts": {
    "stats": "webpack --profile --json --config webpack.client.build.config.js > stats.json",
    "analyze": "webpack-bundle-analyzer stats.json",
npm run stats
npm run analyze

