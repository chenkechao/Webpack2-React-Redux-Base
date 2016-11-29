环境搭建时碰到的问题解决如下：
1.\Webpack2-React-Redux-Base\node_modules\babel.js doesn't exist
  新版本的babel用babel-loader代替babel，npm install babel-loader babel-core babel-preset-es2015 --save-dev
  用法：loader: 'babel-loader?presets[]=es2015'
  所以修改webpack/loaders.js下loaders: ["babel"]为loaders: ["babel-loader?presets[]=es2015"]
2.Webpack2-React-Redux-Base\node_modules\sass\sass.js doesn't exist or is not a directory
  修改webpack/loaders.js下SassLoader：去掉!sass