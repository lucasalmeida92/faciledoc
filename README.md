# FacileDoc

Another clean, responsive documentation template theme for JSDoc 3.

## Uses

- [the Taffy Database library](http://taffydb.com/)
- [Underscore Template library](http://underscorejs.org/#template)
- [Montserrat](https://fonts.google.com/specimen/Montserrat) & Helvetica Neue


## Install

```bash
$ npm install --save-dev faciledoc
```


## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/faciledoc
```


### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/faciledoc"
}
```


### Example JSDoc Config

```json
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
        "monospaceLinks": true,
        "useLongnameInNav": false,
        "showInheritedInNav": true
    },
    "opts": {
        "destination": "./docs/",
        "encoding": "utf8",
        "private": true,
        "recurse": true,
        "template": "./node_modules/faciledoc"
    }
}
```

Specifying a number for useLongnameInNav it will be the max number of path elements to show in nav (starting from Class).


## License

Licensed under the Apache2 license.

## Credits

A fork of minami (https://github.com/nijikokun/minami)
