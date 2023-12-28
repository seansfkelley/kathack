From http://kathack.com/js/kh.js.

Updated to not require jQuery. This means you can paste the entire implementation into any page without having to do script injection, which browsers intentionally make a little annoying.

Bookmarklet:

```
javascript:s=document.createElement('script');s.src='https://cdn.jsdelivr.net/gh/seansfkelley/kathack@v1/kh.js';document.body.appendChild(s);void(0);
```

Or in the browser console:

```
s=document.createElement('script');s.src='https://cdn.jsdelivr.net/gh/seansfkelley/kathack@v1/kh.js';document.body.appendChild(s);
```

Or just paste `kh.js` verbatim into the browser console.

## Doing a "Release"

jsdelivr _never_ refreshes a reference once fetched, so the `main` branch URL is forever poisoned. (Oops.) Instead, push a new tag and use `@<tag>` in the URL to fetch it.
