# Positive Affirmations

I created this fetchable api to be used by whoever needs it to provide several positive affirmations in hopes that it may be used to remind others of their inherent worth. We all need more positivity in our lives and I hope this will help provide the mean to remind others of that.

### Endpoint: https://avyrie.github.io/affirmations-api/affirmations.json

## Fetch Random Affirmation
The following node.js code can fetch a random affirmation:

```js
const fetch = require('node-fetch');
const url = 'https://avyrie.github.io/affirmations-api/affirmations.json';
const randomNum = (arrLength) => {
    return Math.floor(Math.random() * arrLength)
}
const fetchData = () => {
    fetch(url)
    .then(response => response.json())
    .then(data => console.log(data.affirmations[(randomNum(data.affirmations.length))]))
    .catch(err => {
        console.log(err)
    })
}
```

If you are running iOS, there is a [Shortcut to fetch a random affirmation](https://www.icloud.com/shortcuts/88824df962704cb9b2ec73c7b1624895) which can be used as a building block - say in an alarm.


## Contributing
Additional contributions are welcome. If you know of a positive affirmation that would be useful to add, please contribute to this open-source project.

Thank you to our current contributors:
<br />
<br />
<a href="https://github.com/avyrie/affirmations-api/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=avyrie/affirmations-api" />
</a>
