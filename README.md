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
- [✔] https://webpack.js.org/guides/code-splitting/
    - 코드를 다양한 번들로 분할한 다음 요청시 로드하거나 병렬로 로드할 수 있음
    - 더 작은 번들을 달성하고 올바르게 사용하면 로드시간에 큰 영향을 미칠 수 있는 리소스 로드 우선 순위를 제어하는데 사용할 수 있음
    - 코드 분할 세가지 접근 방식
        1. Entry Point: Manualy split
        2. Prevent Duplication
            - Entry depencies
                - 단일 HTML, 여러 진입점 optimization - runtimeChunk: 'single'
            - SplitChunksPlugin
        3. Dynamic Imports: 인라인 함수 호출을 통해 분할
            - import() : ECMAScript 준수, 권장
    - Prefetching/Preloading
        - prefetching: 향후 리소스가 필요할 수 있음
        - preloading: 현재 탐색 중에도 리소스가 필요함
    - Bundle Analysis
- [✔] https://webpack.js.org/guides/caching/
    - webpack 컴파일로 생성 된 파일이 내용이 변경되지 않는 한 캐시 된 상태로 유지되도록 하는 데 필요한 구성에 중점
    - Output Filenames
        - `output.filename` 대체 설정
    - Extracting Boilerplate
        - optimization - splitChunks - vendor - node_modules
    - Module Identifiers
