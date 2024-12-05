# `@shikijs/markdown-it` WASM + Cloudflare Bug

Requirements:

- Node.js 18+

To reproduce:

1. Clone this repo.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe output:

```
> dev
> npx wrangler dev -c wrangler.toml


 ⛅️ wrangler 3.92.0
-------------------

[wrangler:inf] Ready on http://localhost:3000
⎔ Starting local server...
✘ [ERROR] service core:user:shikijs-markdownit-cloudflare-wasm-bug: Uncaught CompileError: WebAssembly.instantiate(): Wasm code generation disallowed by embedder

    at null.<anonymous> (index.js:5164:26) in getWasmInstance
    at null.<anonymous> (index.js:7263:42)



✘ [ERROR] The Workers runtime failed to start. There is likely additional logging output above.


If you think this is a bug then please create an issue at https://github.com/cloudflare/workers-sdk/issues/new/choose
╭──────────────────────────────────────────────────────────────────────────────────────────────────╮
│  [b] open a browser, [d] open devtools, [l] turn off local mode, [c] clear console, [x] to exit  │
╰──────────────────────────────────────────────────────────────────────────────────────────────────╯
```

