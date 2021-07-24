# Message of the day (message-of-the-day)
A database of beautiful message for each day.

In movies, novels, song lyrics, we have lots of well created, touched and polished dialogues and statements.
And we have lots of creations to study and explore, too.
So here is the plan for this repo:
for each day, having some dialogues or statements from a movie, a novel, or a song lyric, to a specfic date.
To express the beauty of human being's creation, and to dedicate it to that specific day.

## Database (or data format in messages.jsonn)

The `messages.json` holds the overall data, as the following:

```json
  {
    "01-01": {
      "month": 1,
      "day": 1,
      "messages": []
    },
    "01-02": {
      "month": 1,
      "day": 2,
      "messages": []
    },
    "01-03": {
      "month": 1,
      "day": 3,
      "messages": []
    },
    ...
    "12-31": {
      "month": 12,
      "day": 31,
      "messages": []
    }
  }
```

The message object in `messages` is:

```json
  {
    "type": "[movie|book|song]",
    "title": {
      "en": "the title of a movie, a book, or some creation in English",
      "zh-TW": "電影/書/作品的中文名稱"
    },
    "text": {
      "en": "the text containing the specific date to match the containing object",
      "zh-TW": "有包含這個日期的中文，可能是台詞，書的一個段落，..."
    },
    "timecode": "[optional for movie or song] 00:00:00.000"
  }
```

Here is an example of messages.json:

```json
  {
    "01-01": {
        "month": 1,
        "day": 1,
        "messages": [
            {
                "type": "movie",
                "title": {
                    "en": "Cosmos: A SpaceTime Odyssey"
                },
		"season": 1,
		"episode": 1,
                "timecode": "00:28:21.930",
                "text": {
                    "en": "January 1st, the Big Bang."
                }
            }
        ]
    }
  }
```

## License

The code from this repo is MIT licensed.
