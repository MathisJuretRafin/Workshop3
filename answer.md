# Partie B

## Exercice - Simple Hello World Server

### Q1 - Create a simple Hello World Server

We create a JS file with the following content to launch our web server on port 3000 :

```js
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello, World____!');
});

app.listen(port, () => {
  console.log(`Hello World Server listening at http://localhost:${port}`);
});
```

And we launch it with the following command :

```
node hello-world-server.js
```

![image](https://github.com/MathisJuretRafin/Workshop3/assets/148776485/8cee4e91-0dee-4f0e-97bd-3f53b04ae106)

### Q2 - Create a DNS registry

We create a JS file with the following content to launch our dns server on port 3001 :

```js
const express = require('express');
const app = express();
const port = 3001;

// Define a variable to store the server URL
const serverUrl = `localhost:${port}`;

app.get('/getServer', (req, res) => {
  // Respond with the server URL
  res.json({ code: 200, server: serverUrl });
});

app.listen(port, () => {
  console.log(`DNS Registry Server listening at http://localhost:${port}`);
});
```

## Exercice - Simple e-commerce





