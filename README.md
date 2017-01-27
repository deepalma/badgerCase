# badger case

Badger case is a naming convention for functions that plays well with functional programming style.

The basic idea is to have determininistic way to name a function starting from its accepted parameters and its returned value.

Here's some examples:

```javascript
const aTOb = a => b;

const aTObTOc = a => b => c;

const aANDbTOc = (a, b) => c;

const aANDbTOcTOd = (a, b) => c => d;
```
Then you can:

```javascript
const aTOb = a => b;

const bTOcTOd = c => d;

const aTOd = pipe(aTOb, bTOcTOd);

```
or:

```javascript
const aANDbTOcTOd = (a, b) => c => d;

const cTOd = aANDbTOcTOd(a, b);
```
