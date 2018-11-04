# Bookshelf theme

JSDoc theme for [bookshelfjs.org](http://bookshelfjs.org).

Forked from [Minami](https://github.com/Nijikokun/minami).

## Uses

- [the Taffy Database library](http://taffydb.com/)
- [Underscore Template library](http://documentcloud.github.com/underscore/#template)

## Install

```bash
$ npm install --save-dev bookshelf-jsdoc-theme
```

## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/bookshelf-jsdoc-theme
```

### Styles

Stlyes must be compiled if edited:

```bash
$ npm run styles
```

### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "./node_modules/bookshelf-jsdoc-theme"
}
```

### Example JSDoc Config

```js
{
  "tags": {
    "allowUnknownTags": true,
    "dictionaries": ["jsdoc"]
  },
  "source": {
    "include": ["lib", "package.json", "README.md"],
    "includePattern": ".js$",
    "excludePattern": "(node_modules/|docs)"
  },
  "plugins": [
    "plugins/markdown"
  ],
  "templates": {
    "cleverLinks": false,
    "monospaceLinks": true
  },
  "opts": {
    "destination": "./docs/",
    "encoding": "utf8",
    "private": true,
    "recurse": true,
    "template": "./node_modules/bookshelf-jsdoc-theme"
    "whitelist": ['Optional', 'List', 'Of', 'Top', 'Level', 'Classes']
    "changelog": './path-to/CHANGELOG.md',
    "title": "Bookshelf.js"
  }
}
```

## License

Licensed under the Apache2 license.
