# Worker Tools

Worker Tools are a collection of TypeScript libraries for writing web servers in [Worker Runtimes][wkrs] such as [Cloudflare Workers][cfws] and [Deno Deploy][dndp]. 

## Tools
- 🧭 [__Worker Router__][router] — Complete routing solution that works across CF Workers, Deno and Service Workers
- 🔋 [__Worker Middleware__][middleware] — A suite of standalone HTTP server-side middleware with TypeScript support
- 📄 [__Worker HTML__][html] — HTML templating and streaming response library
- 📦 [__Storage Area__][kv-storage] — Key-value store abstraction across [Cloudflare KV][cloudflare-kv-storage], [Deno][deno-kv-storage] and browsers.
- 🆗 [__Response Creators__][response-creators] — Factory functions for responses with pre-filled status and status text
- 🎏 [__Stream Response__][stream-response] — Use async generators to build streaming responses for SSE, etc...
- 🥏 [__JSON Fetch__][json-fetch] — Drop-in replacements for Fetch API classes with first class support for JSON.
- 🦑 [__JSON Stream__][json-stream] — Streaming JSON parser/stingifier with 1st class support for WHATWG/web streams.
- 🧱 [__Structured JSON__][structured-json] — Stringify and parse JavaScript values according to Structured Clone Algorithm
- 🍪 [__Request Cookie Store__][request-cookie-store] — An implementation of the Cookie Store API for use in request handlers.
- ⏱ [__Extendable Promise__][extendable-promise] — A promise that can be delayed/extended via repeated calls to `waitUntil`.
<!-- - 🍪 [__Signed Cookie Store__][signed-cookie-store] — An implementation of the Cookie Store API for use in request handlers. -->
<!-- - 🍪 [__Encrypted Cookie Store__][encrypted-cookie-store] — An implementation of the Cookie Store API for use in request handlers. -->
<!-- - ⏱ [__Resolvable Promise__][resolvable-promise] — A promise that is resolvable or rejectable after it was created. -->

Worker Tools also includes a number of polyfills that help bridge the gap between different Worker Runtimes:
- ✏️ [__HTML Rewriter__][html-rewriter] — Cloudflare's HTML Rewriter for use in Deno, browsers, etc...
- 📍 [__Location Polyfill__][location-polyfill] — A `Location` polyfill for Cloudflare Workers.
- 🦕 [__Deno Fetch Event Adapter__][deno-fetch-event-adapter] — Dispatches global `fetch` events using Deno’s native HTTP server.

Worker Tools also maintains a number of (web-) services:
- ⚙️ [__workers.js.org__][wkrs] — Educational site about the state of Worker Runtimes.
- 🦕 [__ghuc.cc__][ghuc] — Import modules directly from GitHub into Deno with a familiar API. 

[router]: https://github.com/worker-tools/router
[middleware]: https://github.com/worker-tools/middleware
[html]: https://github.com/worker-tools/html
[kv-storage]: https://github.com/worker-tools/kv-storage
[cloudflare-kv-storage]: https://github.com/worker-tools/cloudflare-kv-storage
[deno-kv-storage]: https://github.com/worker-tools/deno-kv-storage
[response-creators]: https://github.com/worker-tools/response-creators
[stream-response]: https://github.com/worker-tools/stream-response
[json-fetch]: https://github.com/worker-tools/json-fetch
[json-stream]: https://github.com/worker-tools/json-stream
[request-cookie-store]: https://github.com/worker-tools/request-cookie-store
[extendable-promise]: https://github.com/worker-tools/extendable-promise
[html-rewriter]: https://github.com/worker-tools/html-rewriter
[location-polyfill]: https://github.com/worker-tools/location-polyfill
[deno-fetch-event-adapter]: https://github.com/worker-tools/deno-fetch-event-adapter
[signed-cookie-store]: https://github.com/worker-tools/signed-cookie-store
[encrypted-cookie-store]: https://github.com/worker-tools/encrypted-cookie-store
[resolvable-promise]: https://github.com/worker-tools/resolvable-promise
[structured-json]: https://github.com/worker-tools/structured-json

*[SSE]: Server Sent Events

[wkrs]: https://workers.js.org
[cfws]: https://workers.cloudflare.com
[dndp]: https://deno.com
[ghuc]: https://ghuc.cc
[news]: https://worker-news.deno.dev

***

Worker Tools can be used independently or as a web framework via [__Shed__](https://github.com/worker-tools/shed). 

## How to Use
__Deno__ users can import Worker Tools directly from GitHub as they are written in TypeScript with fully qualified import specifiers:

```js
import * as shed from 'https://ghuc.cc/worker-tools/shed/index.ts'
```

For __other runtimes__ such as module bundlers, webpack or esbuild, Worker Tools are distributed as node-ified modules that can be installed via __npm__ and behave like regular npm modules

```sh
npm install @worker-tools/shed
```
