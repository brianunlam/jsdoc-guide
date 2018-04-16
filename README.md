# Jsdoc micro-guide

Fast configuration of jsdoc.

## Getting Started

These instructions will configure jsdoc with a pretty template.

### Installing

Install jsdoc

To install the latest version on npm globally
```
npm install -g jsdoc
```
To install the latest version on npm locally and save it in your package's package.json file:
```
npm install --save-dev jsdoc
```
Install the tui-jsdoc-template

```
npm i -D tui-jsdoc-template
```


### Configuring

To make it simple, create conf.json file in root directory

```
{
    "plugins": [],
    "recurseDepth": 10,
    "source": {
        "includePattern": ".+\\.js(doc|x)?$",
        "excludePattern": "(^|\\/|\\\\)_"
    },
    "sourceType": "module",
    "opts": {
      "template": "node_modules/tui-jsdoc-template"
    },
    "tags": {
        "allowUnknownTags": true,
        "dictionaries": ["jsdoc","closure"]
    },
    "templates": {
        "name": "Tui JSDoc Template",
        "footerText": "My awesome footer text",
        "cleverLinks": false,
        "monospaceLinks": false
    }
}
```
For more details refer to:
([*jsdoc page - configuration*](http://usejsdoc.org/about-configuring-jsdoc.html#incorporating-command-line-options-into-the-configuration-file))
([*tui-jsdoc-template*](https://github.com/nhnent/tui.jsdoc-template))


## Creating the docs:

Execute jsdoc from commmand-line

```
jsdoc -c /path/to/conf.json fileToBeDocumented.js
```
In opt folder you will find the generated docs.

## For more information on how to style your code

([* jsdoc style-guide *](https://github.com/shri/JSDoc-Style-Guide))

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details


