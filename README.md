## Webpack

### Webpack Core Concepts
1. Entry
2. Output
3. Loaders
4. Plugins
5. Mode

### Webpack Getting Started
- webpack-demo
- [✔] https://webpack.js.org/guides/getting-started/
- [✔] https://webpack.js.org/guides/asset-management/
    - Loading CSS
        - Chained Loader
        - Executed reverse order
        - 'style-loader' first!
    - Loading Images
    - Loading Fonts
    - Loading Data
        - csv-loader, xml-loader
        - Customize parser of JSON modules
            - toml
            - yaml
            - json5
    - Global Assets
- [✔] https://webpack.js.org/guides/output-management/
    - index.html 수동관리 어려움 <= 파일이름에 해시 사용, 여러개 번들을 출력
    - entry 추가 또는 이름변경
    - 플러그인으로 쉽게 관리, `HtmlWebpackPlugin`
    - Cleaning up the `/dist` folder
    - The Manifest: 웹팩과 플러그인이 생성되는 파일을 "인식"하는 방식 `WebpackManifestPlugin`
- [✔] https://webpack.js.org/guides/development/
    - mode
    - bundle된 소스에서 error 찾기 어려움 -> 찾아주는 source maps
    - devtool: `inline-source-map`
    - development tool - webpack-dev-server

