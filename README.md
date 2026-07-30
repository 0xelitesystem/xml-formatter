# XML Formatter

Format, minify, and validate XML in your browser. One HTML file, no network, nothing leaves your machine.

**Live demo:** https://0xelitesystem.github.io/xml-formatter/

## Use

1. Open the live demo or `index.html` from disk.
2. Paste XML into the Input pane (or press **Sample** to load an example).
3. Press **Format** to pretty print, **Minify** to collapse to one line, or **Validate** to check well-formedness only.
4. Choose the indent width (2 spaces, 4 spaces, or Tab). Tick **Strip comments on minify** to drop comments from minified output.
5. Press **Copy** to put the result on your clipboard. **Ctrl+Enter** in the input formats without reaching for the mouse.

When the XML is well-formed you get a green summary (element count, nesting depth, attribute count, size). When it is not, you get the exact line and column, a plain-language reason, and a small code frame pointing at the problem.

It is a real parser, not a wrapper around the browser. It checks tag matching and nesting, a single root element, valid XML names, quoted and non-duplicated attributes, balanced comments and CDATA, processing instructions, the DOCTYPE prolog, and unescaped `<` or `&` in text. Attributes keep their original quote characters and text content is preserved verbatim, so formatting never changes what your document means. Pretty printing normalizes only the insignificant whitespace between elements.

## Why this exists

Most online XML tools paste your document into someone else's server, wrap it in trackers, and pull megabytes of framework code over the wire. This is one static file with zero dependencies and zero analytics. It loads instantly, works on a plane, and you can read every line of what it does. MIT licensed, so fork it and keep it.

## Privacy

Everything runs in your browser. Your XML is never uploaded, logged, or sent anywhere. There are no network requests, no cookies, no analytics, and no third-party scripts. Open the page once and you can disconnect from the internet and keep using it.

## Run locally

```sh
git clone https://github.com/0xelitesystem/xml-formatter.git
cd xml-formatter
```

Then either open `index.html` directly in any browser, or serve the folder:

```sh
python -m http.server 8000
# then visit http://localhost:8000
```

## Build

No build step. No bundler, no dependencies, no package manager. The entire tool is a single `index.html` with inline CSS and JavaScript. Edit the file, refresh the page.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. See [LICENSE](LICENSE).

## Related

- [json-formatter](https://github.com/0xelitesystem/json-formatter)
- [jwt-inspector](https://github.com/0xelitesystem/jwt-inspector)
