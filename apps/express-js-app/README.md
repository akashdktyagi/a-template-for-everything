# Create an Express JS App

* ```npm init -y ```
* ```npm install express``` ==> this will install express
* Create a app.js file and add below code

```js

const express = require('express');
const app = express();
const port = 3000;
app.get('/', (req, res) => res.send('Hello World!'));
app.listen(port, () => console.log('Example app listening on port ${port}!'));

```

* run command: ```node app.js```

![Alt text](image.png)

![Alt text](image-1.png)
