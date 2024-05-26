name: Build redocly HTML file
on: push
permissions:
  contents: read
jobs:
  run-redocly-cli:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          sparse-checkout: 外部設計/API定義/OpenAPI.yml
          sparse-checkout-cone-mode: false
      - uses: actions/setup-node@v3
        with:
          node-version: 18
      - run: npx -y @redocly/cli build-docs 外部設計/API定義/OpenAPI.yml -o output/redocly-static.html
      - uses: actions/upload-artifact@v3
        with:
          name: redocly-html
          path: output/redocly-static.html
