#leefetch polyfill

`fetch()` 函数用于封装请求接口，其中包含 fetch.get() / fetch.post() / fetch.push() / fetch.delete()。

## Installation

```
npm install leefetch --save

const fetch = require('leefetch');
```

## Usage

For a more comprehensive API reference that this polyfill supports,refer to
https://github.com/xxxxx/leefetch

### Importing

Importing will automatically polyfill `window.fetch` and related APIs:

```javascript
import 'leefetch';
```

### GET JSON

```javascript
fetch.get('http://jsonplaceholder.typicode.com/users').then(users => {
    console.log(users);
});
```

### Post JSON

```javascript
var users={
    name:'Kulas Light',
    age:'25'
};

fetch.post('/users',users).then(res => console.log(res));
```

### PUT JSON

```javascript
var users={
    name:'Kulas Light',
    age:'25'
};

fetch.put('/users/:id',users).then(res => console.log(res));
```

### DELETE JSON

```javascript
var users={
    name:'Kulas Light',
    age:'25'
};

fetch.delete('/users/:id').then(res => console.log(res));
```
