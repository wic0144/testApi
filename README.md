
## Installation

```bash
git clone https://github.com/wic0144/testApi.git
cd testApi
npm install
heroku login
heroku create {input name project}
heroku git:remote -a {your name project}
git add .
git commit -am "make it better"
git push heroku master

```

## Usage

```node js
const express = require('express')
const app = express()
const path = require('path');
app.listen(process.env.PORT); #static


##### method get
app.get('/', (req, res) => {
  res.send('Hello World')
})

app.listen(3000, () => {
  console.log('Start server at port 3000.')
})
const books = require('./db')

app.get('/books', (req, res) => {
  res.json(books)
})

app.get('/books/:id', (req, res) => {
    res.json(books.find(book => book.id === req.params.id))
  })

```
## Json File
```json
[
    {
      "id": "1",
      "name": "Game of thrones"
    },
    {
      "id": "2",
      "name": "Clash of kings"
    }
]

```
## License
[SoftwareEngineer#7](https://www.facebook.com/neil.armstrong.92/)
