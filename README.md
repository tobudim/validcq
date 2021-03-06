Validation des codes NIR - NIRPP - Numéro de sécurité sociale
------

![CI Script](https://github.com/tobudim/validcq/workflows/CI%20Script/badge.svg)

Validation des numéros de sécurité sociale, basé sur la [définition wikipedia](https://fr.wikipedia.org/wiki/Num%C3%A9ro_de_s%C3%A9curit%C3%A9_sociale_en_France#lien_F)
> Parse and validate the french NIR, based on the [wikipedia definition](https://fr.wikipedia.org/wiki/Num%C3%A9ro_de_s%C3%A9curit%C3%A9_sociale_en_France#lien_F).


## Install
```
$ npm install validcq
```

## Usage
```js
const { validate } = require('validCq');

validate('255081416802538');
// => true

validate('255081416802539');
// => false

validate('2 55 08 14 168 025 38');
// => true
```

### Options

*shouldClean* - set this to `false` to become white-space and case sensitive (default is true)


```js
validate('2 55 08 14 168 025 38', { shouldClean: false });
// => false
```

```js
validate('2 55 08 14 168 025 38', { shouldClean: true });
// => true
```
