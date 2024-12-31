# Auto Minify Extension for VSCode

Automatically minify your HTML, CSS, and JS files to optimize space and bandwidth usage.<br>
Ignore stuff below, this turns x.big.y to x.y instead of x.y to x.min.y

## Features

- Automatically generates a `.min.html`, `.min.css`, or `.min.js` file each time you save a `.html`, `.css`, or `.js` file.
  For example: `styles.css` becomes `styles.min.css`.

## Basic Usage

1. Create an `.html`, `.css`, or `.js` file.
2. Press `Ctrl/Cmd` + `S` to save your file.
3. A corresponding `.min.html`, `.min.css`, or `.min.js` file is automatically generated.
4. You will see a temporary "HTML Compiled," "CSS Compiled," or "JS Compiled" message in the status bar.

## Dependencies Utilized

- **HTML:** [html-minifier-terser](https://github.com/terser/html-minifier-terser)
- **CSS:** [clean-css](https://github.com/clean-css/clean-css/)
- **JS:** [terser](https://github.com/terser/terser/)

Please check the changelog for version updates.

## Heads-Up

- This extension was created because the my previously used minifier, [Minify](https://marketplace.visualstudio.com/items?itemName=HookyQR.minify), had not been updated for a while and appears to be abandoned. This is an improved version.
- Any errors encountered during minification are likely caused by the underlying dependencies.
- If you have any feature requests or suggestions, please submit them in the Issues tab; your input is highly appreciated.

**Note:** Any additional options not provided below are defaulted to their respective values in their original code.

### `html-minifier-terser` Options Utilized:
```json
{
    "removeAttributeQuotes": true,
    "removeComments": true,
    "removeEmptyElements": true,
    "removeOptionalTags": true,
    "removeRedundantAttributes": true,

    "collapseWhitespace": true,
    "conservativeCollapse": true,

    "caseSensitive": true,
    "continueOnParseError": true,
    "collapseBooleanAttributes": true,
    "processConditionalComments": true,

    "minifyCSS": true,
    "minifyJS": true,
    "html5": true
}
```

### `clean-css` Options Utilized:
```json
{
	"level": {
		"1": {
			"all": true
		}
	}
}
```

### `terser` Options Utilized:
```json
{
	"mangle": false
}
```
