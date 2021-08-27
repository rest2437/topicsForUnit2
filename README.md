# topicsForUnit2 MY Response

Topics covered in unit two's first week

## 1 SQL

- ```sql
  CREATE TABLE movies (
      id SERIAL PRIMARY KEY,
      title TEXT,
      description TEXT,
      rating INTEGER
  );
  ```

---

## 2 NODE

- ```js
  const fs = require("fs");
  fs.readfile("story.txt", "utf8", function (err, data) {
    if (err) {
      consoel.log("there was a problem reading file");
    } else {
      console.log(data);
    }
  });
  ```

---

## 3 Node Packages

- HTTP directory
- ```js
  const http = require("http");
  htttp
    .createServer((req, res) => {
      res.write("hello world");
      res.end();
    })
    .listen(8000);
  ```

---

## 4 Node Package Modules NPM

- Moment json confirmation
- ```json
      {
          "name": "node-introl",
          "verson: "1.0.0",
          "description": "",
          "main": "app.js",
          "scripts": {
              "start": "node app.js"
          },
          "keywords": [],
          "author": "Robert Estrella",
          "license": "ISC",
          "dependencies": {
              "moment": "^2.24.0"
          }
      }
  ```

---

## 5 Express

- ```js
  const express = require("express");
  const app = express();
  app.get("/", function (req, res) {
    res.send("Hello");
  });
  app.listen(8000);
  ```

---

# Classmates response - 1

---

## 1. Mocha

- npm install -g mocha
- //MY RESPONSE - to run mocha

```iterm
➜  deliverables cd challenge-problems-1
➜  challenge-problems-1 git:(main) mocha


  power()
    ✔ should return base to the power of exp

  removeNthLetter()
    ✔ should return the given string with the nth letter removed

  greatestCommonFactor()
    ✔ should return the greatest common factor between num1 and num2

  nickname()
    ✔ should return a nickname string

  oddOnesOut()
    ✔ should return an array of elements that appear in the given array an even number of times

  debug1()
    ✔ should return a string indicating how high the person is jumping

  debug2()
    ✔ should return an array of unique numbers


  7 passing (9ms)

➜  challenge-problems-1 git:(main)
```

---

## 2. PORT

```js
const PORT = process.env.PORT || 8000;
// MY RESPONSE - add LISTEN
app.listen(PORT, () => {
  console.log(`server is running on PORT' ${PORT}`);
});
```

---

## 3. Fetch

```js
const fetch = require("node-fetch");

fetch("https://api.spacexdata.com/v3/capsules")
  .then((response) => {
    console.log(response);
    return response.json();
  })
  .then((data) => {
    console.log(data);
  });

//MY REPSONSE
const axios = require("axios");

let capsules = "Capsules";
axios
  .get(`https://api.spacexdata.com/v3/capsules`)
  .then((response) => {
    console.log(response.data);
  })
  .catch((err) => {
    console.log(err);
  });

async function fetchCapsules(array) {
  for (let i = 0; i < array.length; i++) {
    let capsules = array[i];
    let spacexUrl = `https://api.spacexdata.com/v3/capsules`;
    try {
      const { data } = await axios.get(spacexUrl);
      console.log(data);
    } catch (error) {
      console.log(error);
    }
  }
}
fetchCapsules(capsules);

module.exports = fetchCapsules;
```

---

## 4. Express

```js
const express = require("express");
const app = express();

// MY RESPONSE
//import
const express = require("express");

const app = express();

const PORT = process.env.PORT || 8000;
// assuming we are on production, its gonna look for this port or autmatically set port to 8000

app.get("/", (req, res) => {
  res.send("My express server");
});
// '/' resembles home rout
//req = request
//res = response
app.get("/rob", (req, res) => {
  res.send("Robert Estrella");
});

app.get("/contact", (req, res) => {
  res.send("Contact me at GA");
});

app.listen(PORT, () => {
  console.log(`server is running on PORT' ${PORT}`);
});
```

---

## 5. Axios

```js
const axios = require("axios");

//MY RESPONSE - using axios
const hello = (req, res) => {
  axios.get("https://api.github.com/users/rest2437").then((response) => {
    console.log(response.data);
    const { login, id, node_id } = response.data;
    console.log("login", login);
    console.log("id", id);
    console.log("node_id", node_id);
    res.json({ message: "Hello, welcome to my API", login, id, node_id });
  });
};
```

---

# Classmates response - 2

---

## 1: sql

```sql
SELECT * FROM countries
WHERE region='Southern Europe'
ORDER BY population ASC
LIMIT 5;

// MY RESPONSE -
SELECT language, isofficial FROM countrylanguages WHERE countrycode='VAT';
```

---

## 2: NPM

```iterm
npm init -y

// MY RESPONSE - to run program

npm run start
```

---

## 3: Fetch

```js
const fetchData = async (endpoint) => {
  let response = await fetch(endpoint);
  let data = await response.json();
  return data;
};

fetchData("https://api.spacexdata.com/v3/capsules").then((data) => {
  console.log(data);
});

// MY RESPONSE
const fetch = require("node-fetch");

fetch("https://api.spacexdata.com/v3/capsules")
  .then((response) => {
    console.log(response);
    return response.json();
  })
  .then((data) => {
    console.log(data);
  });
```

---

## 4. Express

```js
const express = require("express");
const app = express();
const PORT = process.env.PORT || 8000;

const about = (req, res) => {
  res.send("<h1>This is a practice app to learn about express routes.</h1>");
};
app.get("/about", about);

app.listen(PORT, () => {
  console.log("Server running on PORT:", PORT);
});

//MY RESPONSE
const express = require("express");
const app = express();
app.get("/", function (req, res) {
  res.send("Hello");
});
app.listen(8000);
```

---

## 5. Javascript algorithms

```js
function removeNthLetter(word, n) {
  const arrWord = word.split("");
  arrWord.splice(n, 1);
  ans = arrWord.join("");
  return ans;
}
//NO REPONSE
```
