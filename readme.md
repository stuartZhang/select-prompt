# select-prompt

**A prompt to an item from a list.**

[![asciicast](https://asciinema.org/a/41541.png)](https://asciinema.org/a/41541)

[![npm version](https://img.shields.io/npm/v/select-prompt.svg)](https://www.npmjs.com/package/select-prompt)
[![dependency status](https://img.shields.io/david/derhuerst/select-prompt.svg)](https://david-dm.org/derhuerst/select-prompt#info=dependencies)
![ISC-licensed](https://img.shields.io/github/license/derhuerst/select-prompt.svg)

*select-prompt* uses [*cli-styles*](https://github.com/derhuerst/cli-styles) and [*prompt-skeleton*](https://github.com/derhuerst/prompt-skeleton) to have a look & feel consistent with [other prompts](https://github.com/derhuerst/prompt-skeleton#prompts-using-prompt-skeleton).


## Installing

```
npm install select-prompt
```

## My contributions

A new option named after <code>timeout</code> has been added. Accompanying <code>{timeout: 2000}</code>,
the CLI program will automatically pick up the active selecting item which the <code>cursor</code>
points at and resume the user interaction in the 2 seconds.

## Usage

```js
const prompt = require('select-prompt')

const colors = [
    {title: 'red',    value: '#f00'},
    {title: 'yellow', value: '#ff0'},
    {title: 'green',  value: '#0f0'},
    {title: 'blue',   value: '#00f'},
    {title: 'black',  value: '#000'},
    {title: 'white',  value: '#fff'}
]

prompt('What is your favorite color?', colors, {cursor: 3, timeout: 2000})
.on('data', (e) => console.log('Interim value', e.value))
.on('abort', (v) => console.log('Aborted with', v))
.on('submit', (v) => console.log('Submitted with', v))
```


## Related

- [`mail-prompt`](https://github.com/derhuerst/mail-prompt)
- [`date-prompt`](https://github.com/derhuerst/date-prompt)
- [`multiselect-prompt`](https://github.com/derhuerst/multiselect-prompt)
- [`number-prompt`](https://github.com/derhuerst/number-prompt)
- [`text-prompt`](https://github.com/derhuerst/text-prompt)
- [`cli-autocomplete`](https://github.com/derhuerst/cli-autocomplete)


## Contributing

If you **have a question**, **found a bug** or want to **propose a feature**, have a look at [the issues page](https://github.com/derhuerst/select-prompt/issues).
