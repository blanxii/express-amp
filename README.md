# express-amp
> :zap: Express middleware to convert website to Google AMP

## Installation

```sh
npm install --save express-amp
```

## Preview
```js
/**
 * Overriding the render method
 * You can use that to avoid use renderAMP
 * With that you can transform all /path in AMP pages
 */

import express from 'express';
import expressAMP from 'express-amp';

const app = express();

app.use(expressAMP({
  override: true
}));

app.get('/', (req, res) => {
  res.render('index', {});
});

```

```js
// Using renderAMP method

import express from 'express';
import expressAMP from 'express-amp';

const app = express();

app.use(expressAMP({
  override: false
}));

app.get('/', (req, res) => {
  res.renderAMP('index', {});
});

```

## Usage

expressAMP({ [override] });
<!-- {.font-large} -->
where:

- `override` (optional): It brings you the possibility to override the method render or use renderAMP method.

## License

MIT © [Jordi López](http://jlopezxs.github.io)
