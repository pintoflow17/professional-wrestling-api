
# PROFESSIONAL WRESTLING DOCUMENTATION

The Professional Wrestling API offers extensive access to a wealth of data from the world of professional wrestling, covering major promotions such as AEW and WWE. This API is perfect for developers and fans looking to delve into the intricacies of professional wrestling, providing detailed information about wrestlers, matches, events, and more.

With a variety of endpoints dedicated to different aspects of professional wrestling, the API allows users to retrieve up-to-date statistics, event schedules, match results, and wrestler profiles. Its structured JSON responses facilitate easy integration into various applications, making it an invaluable resource for enhancing wrestling-related platforms and engaging fans with accurate and timely data.

## Authentication
The URL you need to use is the following: `https://professional-wrestling.p.rapidapi.com/`
The API requires the headers listed below:

 - **`x-rapidapi-host`**: `professional-wrestling.p.rapidapi.com`
 - **`x-rapidapi-key`**: `YOUR_API_KEY`

Make sure to replace `YOUR_API_KEY` with your API key. You can register one [here](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/professional-wrestling/pricing).
Some frameworks automatically add extra headers, you have to make sure to remove them in order to get a response from the API.

### Endpoints
The API is configured to accept only **GET** requests. Below are the available endpoints with their descriptions and required parameters.

#### 1. **`GET /search`**
-   **Description**: Searches for wrestling-related news or items based on a query string.

-   **Parameters**:

| Parameter        | Type     | Default               | Description     | Required |
|------------------|----------|-----------------------|-----------------|----------|
| `query` | string | `-` | The search term. | Yes |
| `limit` | string | `10` | The number of results to return. | No |
| `page` | string | `1` | The page number of results. | No |


Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/search?query=John%20Cena', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "totalFound": 2,
  "didYouMean": "john pena",
  "resultTypes": [
    {
      "totalFound": 192018,
      "type": "article",
      "displayName": "Articles"
    },
    {
      "totalFound": 4,
      "type": "clips",
      "displayName": "Clips"
    }
  ],
  "results": [
    {
      "type": "article",
      "totalFound": 10,
      "page": 1,
      "limit": 10,
      "displayName": "Articles",
      "contents": [
        {
          "id": "39769682",
          "nowId": "1-39769682",
          "type": "Story",
          "displayName": "John Cena calls Haaland, and other times soccer and WWE met",
          "link": {
            "web": "https://www.espn.com/soccer/story/_/id/39769682/john-cena-calls-haaland-other-s-soccer-wwe-met"
          },
          "images": [
            {
              "width": 1296,
              "name": "Haaland, John Cena [1296x729]",
              "peers": [
                {
                  "width": 1296,
                  "name": "Haaland, John Cena [1296x1296]",
                  "url": "https://a.espncdn.com/photo/2024/0320/r1307482_1296x1296_1-1.jpg",
                  "height": 1296
                },
                {
                  "width": 1296,
                  "name": "Haaland, John Cena [1296x729]",
                  "url": "https://a.espncdn.com/photo/2024/0320/r1307482_1296x729_16-9.jpg",
                  "height": 729
                },
                {
                  "width": 864,
                  "name": "Haaland, John Cena [864x1296]",
                  "url": "https://a.espncdn.com/photo/2024/0320/r1307482_864x1296_2-3.jpg",
                  "height": 1296
                },
                {
                  "width": 1296,
                  "name": "Haaland, John Cena [1296x864]",
                  "url": "https://a.espncdn.com/photo/2024/0320/r1307482_1296x864_3-2.jpg",
                  "height": 864
                },
                {
                  "width": 1296,
                  "name": "Haaland, John Cena [1296x518]",
                  "url": "https://a.espncdn.com/photo/2024/0320/r1307482_1296x518_5-2.jpg",
                  "height": 518
                }
              ],
              "url": "https://a.espncdn.com/photo/2024/0320/r1307482_1296x729_16-9.jpg",
              "height": 729
            }
          ],
          "...": "..."
        },
        {
          "id": "40510428",
          "nowId": "1-40510428",
          "type": "Story",
          "displayName": "John Cena announces upcoming WWE retirement in 2025",
          "link": {
            "web": "https://www.espn.com/professional-wrestling/story/_/id/40510428/john-cena-announces-upcoming-wwe-retirement-2025-money-bank"
          },
          "images": [
            {
              "width": 1296,
              "name": "John Cena [1296x729]",
              "peers": [
                {
                  "width": 1296,
                  "name": "John Cena [1296x1296]",
                  "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
                  "url": "https://a.espncdn.com/photo/2024/0707/r1355533_1296x1296_1-1.jpg",
                  "height": 1296
                },
                {
                  "width": 1296,
                  "name": "John Cena [1296x729]",
                  "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
                  "url": "https://a.espncdn.com/photo/2024/0707/r1355533_1296x729_16-9.jpg",
                  "height": 729
                },
                {
                  "width": 864,
                  "name": "John Cena [864x1296]",
                  "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
                  "url": "https://a.espncdn.com/photo/2024/0707/r1355533_864x1296_2-3.jpg",
                  "height": 1296
                },
                {
                  "width": 1296,
                  "name": "John Cena [1296x864]",
                  "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
                  "url": "https://a.espncdn.com/photo/2024/0707/r1355533_1296x864_3-2.jpg",
                  "height": 864
                },
                {
                  "width": 1296,
                  "name": "John Cena [1296x518]",
                  "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
                  "url": "https://a.espncdn.com/photo/2024/0707/r1355533_1296x518_5-2.jpg",
                  "height": 518
                }
              ],
              "caption": "John Cena announced that he will be retiring from the WWE next year at Money in the Bank on Saturday night.",
              "url": "https://a.espncdn.com/photo/2024/0707/r1355533_1296x729_16-9.jpg",
              "height": 729
            },
            {
              "width": 576,
              "name": "John Cena announces retirement from WWE",
              "caption": "John Cena announces that Wrestlemania 41 in Las Vegas will be his final Wrestlemania as he is retiring from WWE.",
              "url": "https://a.espncdn.com/media/motion/2024/0706/dm_240706_dm_wwe_cena_retirement_pub2tag_rev1/dm_240706_dm_wwe_cena_retirement_pub2tag_rev1.jpg",
              "height": 324
            }
          ],
          "...": "..."
        },
      
        "..."
      ]
    },
    {
      "type": "clips",
      "totalFound": 4,
      "page": 1,
      "limit": 10,
      "displayName": "Clips",
      "contents": [
        {
          "id": "40510495",
          "guid": "40510495",
          "type": "vod",
          "displayName": "John Cena announces retirement from WWE",
          "subtitle": "John Cena announces that Wrestlemania 41 in Las Vegas will be his final Wrestlemania as he is retiring from WWE.",
          "link": {
            "app": "sportscenter://x-callback-url/showVideo?videoID=40510495",
            "web": "https://www.espn.com/video/clip/_/id/40510495"
          },
          "...": "..."
        },
        {
          "id": "39500631",
          "guid": "39500631",
          "type": "vod",
          "displayName": "John Cena makes Savannah Bananas debut, takes short at-bat",
          "subtitle": "WWE legend John Cena makes a surprise appearance at the Savannah Bananas game and takes the field with a must-see at-bat.",
          "link": {
            "app": "sportscenter://x-callback-url/showVideo?videoID=39500631",
            "web": "https://www.espn.com/video/clip/_/id/39500631"
          },
          "...": "..."
        },
        {
          "id": "36037662",
          "guid": "36037662",
          "type": "vod",
          "displayName": "The best of WrestleMania 39 Night 1",
          "subtitle": "Check out some of the best performances from superstars like Rhea Ripley, Sami Zayn and John Cena from Night 1 of WrestleMania 39.",
          "link": {
            "app": "sportscenter://x-callback-url/showVideo?videoID=36037662",
            "web": "https://www.espn.com/video/clip/_/id/36037662"
          },
          "...": "..."
        },
        {
          "id": "28998798",
          "guid": "28998798",
          "type": "vod",
          "displayName": "McIntyre becomes WWE champion,  The Fiend gets rid of John Cena",
          "subtitle": "Drew McIntyre makes quick work of Brock Lesnar to become the new WWE champion, The Fiend defeats John Cena and Edge pins Randy Orton all in Night 2 of WrestleMania 36.",
          "link": {
            "app": "sportscenter://x-callback-url/showVideo?videoID=28998798",
            "web": "https://www.espn.com/video/clip/_/id/28998798"
          },
          "...": "..."
        }
      ]
    }
  ]
}
```



#### 2. **`GET /aew/news`**
-   **Description**: Fetches the latest news related to All Elite Wrestling (AEW).

-   **Parameters**:

  This endpoint has no parameters.

Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/aew/news', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "newsFeedCount": 19,
  "newsFeed": [
    {
      "id": 17167558,
      "headline": "AEW Profile - Claudio Castagnoli",
      "description": "AEW superstar Claudio Castagnoli's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [],
      "...": "..."
    },
    {
      "id": 17148550,
      "headline": "AEW Profile - Big Bill",
      "description": "AEW superstar Big Bill's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "AEW",
      "video": [],
      "...": "..."
    },
    {
      "id": 17443817,
      "headline": "AEW Profile - Bryan Danielson",
      "description": "AEW superstar Daniel Bryan's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [],
      "...": "..."
    },
    {
      "id": 38803635,
      "headline": "Pro wrestling power rankings: Inside the rise of IYO SKY, L.A. Knight and MJF-Adam Cole",
      "description": "Who are the top wrestlers, regardless of promotion, in the world today? We rank the best male and female wrestlers, plus tag teams.",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [
        {
          "cerebroId": "654405c5be6ab31c01694484",
          "images": [
            {
              "name": "Poster Image",
              "alt": "",
              "width": 576,
              "caption": "",
              "credit": "",
              "url": "https://media.video-cdn.espn.com/images/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
              "...": "..."
            }
          ],
          "thumbnail": "https://a.espncdn.com/media/motion/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
          "ad": {
            "sport": "Other",
            "bundle": "sportscenter"
          },
          "dataSourceIdentifier": "76832824a8d86",
          "keywords": [],
          "...": "..."
        }
      ],
      "...": "..."
    },
    {
      "id": 38803348,
      "headline": "Ric Flair, 74, on new beginnings with AEW, working with Sting and going through tables",
      "description": "Flair returned to professional wrestling with a surprise return to AEW last week, but what does the future hold for \"The Nature Boy\"?",
      "byline": "Marc Raimondi",
      "section": "AEW",
      "video": [
        {
          "cerebroId": "654405c5be6ab31c01694484",
          "images": [
            {
              "name": "Poster Image",
              "alt": "",
              "width": 576,
              "caption": "",
              "credit": "",
              "url": "https://media.video-cdn.espn.com/images/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
              "...": "..."
            }
          ],
          "thumbnail": "https://a.espncdn.com/media/motion/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
          "ad": {
            "sport": "Other",
            "bundle": "sportscenter"
          },
          "dataSourceIdentifier": "76832824a8d86",
          "keywords": [],
          "...": "..."
        }
      ],
      "...": "..."
    },
    {
      "id": 38547792,
      "headline": "Adam Copeland, fka Edge, makes AEW debut at WrestleDream 2023",
      "description": "Adam Copeland made a surprise debut at AEW's WrestleDream 2023 on Sunday night.",
      "byline": "ESPN",
      "section": "AEW",
      "video": [],
      "...": "..."
    },
    "..."
  ]
}
```



#### 3. **`GET /wwe/news`**
-   **Description**: Fetches the latest news related to World Wrestling Entertainment (WWE).

-   **Parameters**:

  This endpoint has no parameters.

Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/wwe/news', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "newsFeedCount": 19,
  "newsFeed": [
    {
      "id": 17167558,
      "headline": "AEW Profile - Claudio Castagnoli",
      "description": "AEW superstar Claudio Castagnoli's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [],
      "...": "..."
    },
    {
      "id": 17148550,
      "headline": "AEW Profile - Big Bill",
      "description": "AEW superstar Big Bill's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "AEW",
      "video": [],
      "...": "..."
    },
    {
      "id": 17443817,
      "headline": "AEW Profile - Bryan Danielson",
      "description": "AEW superstar Daniel Bryan's bio, career highlights and notes",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [],
      "...": "..."
    },
    {
      "id": 38803635,
      "headline": "Pro wrestling power rankings: Inside the rise of IYO SKY, L.A. Knight and MJF-Adam Cole",
      "description": "Who are the top wrestlers, regardless of promotion, in the world today? We rank the best male and female wrestlers, plus tag teams.",
      "byline": "ESPN.com",
      "section": "WWE",
      "video": [
        {
          "cerebroId": "654405c5be6ab31c01694484",
          "images": [
            {
              "name": "Poster Image",
              "alt": "",
              "width": 576,
              "caption": "",
              "credit": "",
              "url": "https://media.video-cdn.espn.com/images/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
              "...": "..."
            }
          ],
          "thumbnail": "https://a.espncdn.com/media/motion/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
          "ad": {
            "sport": "Other",
            "bundle": "sportscenter"
          },
          "dataSourceIdentifier": "76832824a8d86",
          "keywords": [],
          "...": "..."
        }
      ],
      "...": "..."
    },
    {
      "id": 38803348,
      "headline": "Ric Flair, 74, on new beginnings with AEW, working with Sting and going through tables",
      "description": "Flair returned to professional wrestling with a surprise return to AEW last week, but what does the future hold for \"The Nature Boy\"?",
      "byline": "Marc Raimondi",
      "section": "AEW",
      "video": [
        {
          "cerebroId": "654405c5be6ab31c01694484",
          "images": [
            {
              "name": "Poster Image",
              "alt": "",
              "width": 576,
              "caption": "",
              "credit": "",
              "url": "https://media.video-cdn.espn.com/images/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
              "...": "..."
            }
          ],
          "thumbnail": "https://a.espncdn.com/media/motion/2023/1102/dm_231102_aew_flair_interview/dm_231102_aew_flair_interview.jpg",
          "ad": {
            "sport": "Other",
            "bundle": "sportscenter"
          },
          "dataSourceIdentifier": "76832824a8d86",
          "keywords": [],
          "...": "..."
        }
      ],
      "...": "..."
    },
    {
      "id": 38547792,
      "headline": "Adam Copeland, fka Edge, makes AEW debut at WrestleDream 2023",
      "description": "Adam Copeland made a surprise debut at AEW's WrestleDream 2023 on Sunday night.",
      "byline": "ESPN",
      "section": "AEW",
      "video": [],
      "...": "..."
    },
    "..."
  ]
}
```



#### 4. **`GET /aew/champions`**
-   **Description**: Fetches the current champions in All Elite Wrestling (AEW).

-   **Parameters**:

  This endpoint has no parameters.

Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/aew/Champions', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
{
  "dataSourceIdentifier": "5d0a9ecdfc336",
  "keywords": [],
  "description": "Full title histories and details behind every champion to hold any of the active titles in All Elite Wrestling.",
  "video": [
    {
      "cerebroId": "6136975bbe6ab365c9a9dcba",
      "images": [
        {
          "name": "Poster Image",
          "alt": "",
          "width": 576,
          "caption": "",
          "credit": "",
          "url": "https://media.video-cdn.espn.com/images/2021/0906/dm_210906_AEW_Presser_Bryan_Danielson/dm_210906_AEW_Presser_Bryan_Danielson.jpg",
          "...": "..."
        }
      ],
      "thumbnail": "https://a.espncdn.com/media/motion/2021/0906/dm_210906_AEW_Presser_Bryan_Danielson/dm_210906_AEW_Presser_Bryan_Danielson.jpg",
      "ad": {
        "sport": "Other",
        "bundle": "sportscenter"
      },
      "keywords": [
        "Bryan Danielson"
      ],
      "timeRestrictions": {
        "embargoDate": "2021-09-06T22:31:45Z",
        "expirationDate": "2025-09-09T22:31:45Z"
      },
      "...": "..."
    }
  ],
  "type": "Story",
  "title": "AEW current world champions and title history",
  "...": "..."
}
```



#### 5. **`GET /wwe/schedule`**
-   **Description**: Fetches the upcoming schedule of events for World Wrestling Entertainment (WWE).

-   **Parameters**:

  This endpoint has no parameters.

Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/wwe/schedule', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
[
  {
    "date": "Oct. 21, 2024",
    "name": "Raw",
    "location": "Philadelphia",
    "venue": "<strong>Raw,</strong>",
    "city": "Wells Fargo Center"
  },
  {
    "date": "Oct. 25, 2024",
    "name": "SmackDown",
    "location": "Brooklyn",
    "venue": "<strong>SmackDown,</strong>",
    "city": "Barclays Center"
  },
  {
    "date": "Oct. 28, 2024",
    "name": "Raw",
    "location": "Hershey",
    "venue": "<strong>Raw,</strong>",
    "city": "Giant Center"
  },
  {
    "date": "Nov. 2, 2024",
    "name": "Crown Jewel",
    "location": "Riyadh",
    "venue": "<strong>Crown",
    "city": "Jewel,</strong> Kingdom Arena"
  },
  {
    "date": "Nov. 8, 2024",
    "name": "SmackDown",
    "location": "Buffalo",
    "venue": "<strong>SmackDown,</strong>",
    "city": "KeyBank Center"
  },
  {
    "date": "Nov. 11, 2024",
    "name": "Raw",
    "location": "Grand Rapids",
    "venue": "<strong>Raw,</strong>",
    "city": "Van Andel Arena"
  },
  "..."
]
```



#### 6. **`GET /aew/schedule`**
-   **Description**: Fetches the upcoming schedule of events for All Elite Wrestling (AEW).

-   **Parameters**:

  This endpoint has no parameters.

Example request:
```javascript
fetch('https://professional-wrestling.p.rapidapi.com/aew/schedule', { 
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'professional-wrestling.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:
```json
[
  {
    "event": "AEW Dynamite: Salt Lake City",
    "date": "Oct. 23, 2024",
    "arena": "Maverik Center",
    "isPPV": false
  },
  {
    "event": "AEW Rampage: Salt Lake City",
    "date": "Oct. 25, 2024",
    "arena": "Maverik Center",
    "isPPV": false
  },
  {
    "event": "AEW Collision: Cedar Rapids",
    "date": "Oct. 26, 2024",
    "arena": "Alliant Energy PowerHouse",
    "isPPV": false
  },
  {
    "event": "AEW Dynamite: Cleveland",
    "date": "Oct. 30, 2024",
    "arena": "Wolstein Center",
    "isPPV": false
  },
  {
    "event": "AEW Rampage: Cleveland",
    "date": "Nov. 1, 2024",
    "arena": "Wolstein Center",
    "isPPV": false
  },
  {
    "event": "AEW Collision: Philadelphia",
    "date": "Nov. 2, 2024",
    "arena": "Liacouras Center",
    "isPPV": false
  },
  "..."
]
```



## Error Handling
The API returns standard HTTP status codes to indicate the success or failure of API requests. Below are common errors and suggestions for handling them.

|Status Code|Message|Description|Suggested Handling|
|--|--|--|--|
| **400** | Bad Request | The request was malformed or missing required parameters (e.g., `domain` parameter not provided). | Verify that all required parameters are included and correctly formatted. |
| **401** | Unauthorized | Invalid or missing API key in the request headers. | Check that a valid API key is included in `x-rapidapi-key`. |
| **403** | Forbidden | Access to the requested resource is denied, possibly due to rate limits or restricted access. | Review rate limits and ensure API permissions. Retry after a delay if the rate limit is exceeded. |
| **404** | Not Found | The requested domain information could not be found (e.g., domain does not exist). | Check the spelling or availability of the domain. |
| **429** | Too Many Requests | The API rate limit has been exceeded. | Implement rate-limiting logic and retry after the specified rate limit reset time. |
| **500** | Internal Server Error | A server error occurred while processing the request. | Retry the request after a few seconds. If the error persists, contact API support. |
| **503** | Service Unavailable | The API service is temporarily unavailable (e.g., due to maintenance). | Retry the request later or check the API status page for maintenance alerts. |
