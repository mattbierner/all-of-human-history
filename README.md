```bash
$ npm install all-of-human-history
```

This Node package contains date and blurbs for major historical events covering about the last 5000 years of human history, from the late bronze age to 2015.

```js
// Get array of all events
const history = require('all-of-human-history');

history.filter(event => event.start.year > 1720 && event.start.year < 1723)
----
[ { start: { year: 1721 },
    event: 'Robert Walpole becomes the first Prime Minister of Great Britain (de facto)' },
  { start: { year: 1721 },
    event: 'The Treaty of Nystad is signed, ending the Great Northern War' },
  { start: { year: 1721 },
    event: 'Kangxi Emperor bans Christian missionaries because of Pope Clement XI\'s decree' },
  { start: { year: 1721 },
    event: 'Peter I reforms the Russian Orthodox Church' },
  { start: { year: 1722 },
    event: 'Afghans conquer Iran, overthrowing the Safavid Shah Sultan Husayn' },
  { start: { year: 1722 }, event: 'Kangxi Emperor of China dies' },
  { start: { year: 1722 },
    event: 'Bartholomew Roberts is killed in a sea battle off the African coast' },
  { start: { year: 1722 },
    end: { year: 1723 },
    event: 'Russo-Persian War' },
  { start: { year: 1722 },
    end: { year: 1725 },
    event: 'Controversy over William Wood\'s halfpence leads to the Drapier\'s Letters and begins the Irish economic independence from England movement' } ]
```

## Structure
Events are structured:

```js
{
    "event": STRING Blub about the event,
    "start": {
        "year": NUMBER When the event took place or started. Always present.
    },
    ?"end": {
        "year": NUMBER When the event ended. Only present if the event spanned multiple years.
    } 
}
```

## Source
All of the data in this dataset was initially scraped from Wikipedia from pages like this: https://en.wikipedia.org/wiki/Timeline_of_modern_history

See `./data` for individual datasets that were collected.