# vite react

> 做了如下初始化, tailwind css + react + vite

[eslint-config-react-app](https://www.npmjs.com/package/eslint-config-react-app)
[vite](https://cn.vitejs.dev/)
[tailwindcss](https://www.tailwindcss.cn/)

1.  初始化项目, 继承 CRA 的 eslint 风格

    ```
    npm i -D eslint-config-react-app
    ```

    根目录新增 `.eslintrc.json`

    ```json
    {
      "extends": "react-app"
    }
    ```

2.  在项目内

    ```
    npm i -D tailwindcss postcss autoprefixer

    npx tailwindcss init -p
    ```

    根目录初始化得到一个`tailwind.config.cjs`文件.配置如下

    ```js
    module.exports = {
      content: ['./index.html', './src/**/*.{vue,js,ts,jsx,tsx}'],
      theme: {
        extend: {},
      },
      plugins: [],
    }
    ```

3.  `index.css`(在 main.js 引入)文件新增
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```
