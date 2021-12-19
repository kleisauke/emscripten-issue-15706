# emscripten-issue-15706

See: https://github.com/emscripten-core/emscripten/issues/15706

## Reproduction

```bash
$ git clone https://github.com/kleisauke/emscripten-issue-15706.git && cd emscripten-issue-15706
$ emcc -o vips.js vips.a -O3 --bind -pthread -sWASMFS -lpipefs.js
$ sha256sum vips.wasm
b7110b179c4fb62b1548e139cdb44ffeae654cacac8e4875af9273814fc552e8  vips.wasm
$ emcc -o vips.js vips.a -O3 --bind -pthread -sWASMFS -lpipefs.js
$ sha256sum vips.wasm
18c4c7a71f217a4a24e6c9d6fa03dfca2f7b57cf9facbc5ab91dbf129727ffac  vips.wasm
```
