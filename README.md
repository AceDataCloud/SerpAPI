# Search Engine API

Search Engine Results Page (SERP) related API.

API home page: [Ace Data Cloud - Search Engine](https://platform.acedata.cloud/services/a9af5926-e8d8-4c5e-bdef-bbebf19cdbc3)

## Get Started


Google SERP (Search Engine Results Page) is the results page that users see after entering a query in the Google search engine. It displays organic search results, ads, featured snippets, knowledge graphs, as well as various content such as images and videos, aimed at providing users with the most relevant information.

This article will provide a detailed introduction to the Google SERP API, which can provide results for queries entered in the Google search engine, and the results include many types, such as featured snippets, knowledge graphs, and images.

This document will introduce the integration instructions for the Google SERP API.

### Application Process

To use the Google SERP API, you need to first apply for the corresponding service on the [Google SERP API](https://platform.acedata.cloud/documents/44c86226-8eaa-49bf-85f3-1fae8d2e23f1) page. After entering the page, click the "Acquire" button, as shown in the image:

![](https://cdn.acedata.cloud/q6ytrc.png)

If you are not logged in or registered, you will be automatically redirected to the login page inviting you to register and log in. After logging in or registering, you will be automatically returned to the current page.

During the first application, there will be a free quota provided, allowing you to use the API for free.

### Basic Usage

First, understand the basic usage method, which is to input the type of search resource and keywords to obtain search results. You only need to simply pass the `query` field and specify the corresponding model.

For example, to find information about "apple inc," we can fill in the corresponding content on the interface, as shown in the image:

<p><img src="https://cdn.acedata.cloud/lnqiye.png" width="500" class="m-auto"></p>

Here, we can see that we have set the Request Headers, including:

- `accept`: the format of the response result you want to receive, filled in as `application/json`, which means JSON format.
- `authorization`: the key to call the API, which can be selected directly after application.

Additionally, the Request Body is set, including:

- `type`: the type of search resource, currently supporting only six types, with the default being `search`.
- `query`: the search keyword.
- `country`: the country where the search results are located, with the default being the United States (US).
- `language`: the language of the search results, with the default being English (en).
- `range`: the time range for the search results, with the default being unlimited.
- `number`: the page size of the search results, with the default being 10.
- `page`: the page number of the search results, with the default being 1.

After selection, you can find that the corresponding code is also generated on the right side, as shown in the image:

<p><img src="https://cdn.acedata.cloud/1j81zr.png" width="500" class="m-auto"></p>

Click the "Try" button to conduct a test, as shown in the image above, and we obtained the following results:
```json
{
  "knowledge_graph": {
    "title": "Apple",
    "type": "Technology company",
    "website": "http://www.apple.com/",
    "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5ITHsQzdzkkFWKinRe1Y4FUbC_Vy3R_M&s=0",
    "description": "Apple Inc. is an American multinational corporation and technology company headquartered in Cupertino, California, in Silicon Valley. It is best known for its consumer electronics, software, and services.",
    "description_source": "Wikipedia",
    "description_link": "https://en.wikipedia.org/wiki/Apple_Inc.",
    "attributes": {
      "Customer service": "1 (800) 275-2273",
      "Founders": "Steve Jobs, Steve Wozniak, and Ronald Wayne",
      "Founded": "April 1, 1976, Los Altos, CA",
      "Headquarters": "Cupertino, CA",
      "CEO": "Tim Cook (Aug 24, 2011–)"
    }
  },
  "organic": [
    {
      "title": "Apple",
      "link": "https://www.apple.com/",
      "snippet": "Discover the innovative world of Apple and shop everything iPhone, iPad, Apple Watch, Mac, and Apple TV, plus explore accessories, entertainment, ...",
      "sitelinks": [
        {
          "title": "Support",
          "link": "https://support.apple.com/"
        },
        {
          "title": "Career Opportunities",
          "link": "https://www.apple.com/careers/us/"
        },
        {
          "title": "Business",
          "link": "https://www.apple.com/business/"
        },
        {
          "title": "Store",
          "link": "https://www.apple.com/store"
        },
        {
          "title": "Investor Relations",
          "link": "https://investor.apple.com/investor-relations/default.aspx"
        }
      ],
      "position": 1
    },
    {
      "title": "Apple Inc. - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc.",
      "snippet": "Apple Inc. is an American multinational corporation and technology company headquartered in Cupertino, California, in Silicon Valley.",
      "position": 2
    },
    {
      "title": "Apple Inc. | History, Products, Headquarters, & Facts - Britannica",
      "link": "https://www.britannica.com/money/Apple-Inc",
      "snippet": "American manufacturer of personal computers, smartphones, and tablet computers. Apple was the first successful personal computer company and ...",
      "date": "7 days ago",
      "position": 3
    },
    {
      "title": "Apple Inc. (AAPL) Company Profile & Facts - Yahoo Finance",
      "link": "https://finance.yahoo.com/quote/AAPL/profile/",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables, and accessories worldwide. The company offers iPhone, a line ...",
      "position": 4
    },
    {
      "title": "AAPL: Apple Inc Stock Price Quote - NASDAQ GS - Bloomberg",
      "link": "https://www.bloomberg.com/quote/AAPL:US",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables and accessories, and sells a variety of related accessories.",
      "position": 5
    },
    {
      "title": "Apple Inc. (AAPL) Stock Price Today - WSJ",
      "link": "https://www.wsj.com/market-data/quotes/AAPL?gaa_at=eafs&gaa_n=ASWzDAiLDLUKmLSxoaZi5n84id-eGDp9gI99K5VU1R7pK3SzSi_PbdpD61P1&gaa_ts=685148c8&gaa_sig=mGk3lG_2W7ZqrXfXSXv7GAP78KUi_uJEadAXuv2bgYJ8Ah42GhIZxrsN4ynbNg_oKD_7NZS1lRPSglUNacIheQ%3D%3D",
      "snippet": "Apple Inc. engages in the design, manufacture, and sale of smartphones, personal computers, tablets, wearables and accessories, and other varieties of related ...",
      "position": 6
    }
  ],
  "people_also_ask": [
    {
      "question": "What is the Apple Inc?",
      "snippet": "Apple Inc., originally Apple Computer, Inc., is a multinational corporation that creates and markets consumer electronics and attendant computer software, and is a digital distributor of media content. Apple's core product lines are the iPhone smartphone, iPad tablet computer, and the Mac personal computer.",
      "title": "History of Apple Inc. - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/History_of_Apple_Inc."
    },
    {
      "question": "Who owns Apple Inc?",
      "snippet": "Apple (AAPL) Ownership Overview The ownership structure of Apple (AAPL) stock is a mix of institutional, retail, and individual investors. Approximately 50.57% of the company's stock is owned by Institutional Investors, 0.06% is owned by Insiders, and 49.38% is owned by Public Companies and Individual Investors.",
      "title": "Who owns Apple? AAPL Stock Ownership - TipRanks.com",
      "link": "https://www.tipranks.com/stocks/aapl/ownership"
    },
    {
      "question": "What is Apple Inc. best known for?",
      "snippet": "It is best known for its consumer electronics, software, and services. Founded in 1976 as Apple Computer Company by Steve Jobs, Steve Wozniak and Ronald Wayne, the company was incorporated by Jobs and Wozniak as Apple Computer, Inc. the following year.",
      "title": "Apple Inc. - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc."
    },
    {
      "question": "What is the meaning of Inc in Apple Inc?",
      "snippet": "abbreviation for incorporated: used in the names of US companies that are legally established: Bishop Computer Services, Inc.",
      "title": "Inc. | English meaning - Cambridge Dictionary",
      "link": "https://dictionary.cambridge.org/dictionary/english/inc"
    }
  ],
  "related_searches": [
    {
      "query": "Apple iPhone 13"
    },
    {
      "query": "apple inc คืออะไร"
    },
    {
      "query": "Apple Inc full form"
    },
    {
      "query": "Apple Inc address"
    },
    {
      "query": "Apple Inc industry"
    },
    {
      "query": "Apple Inc investor relations"
    },
    {
      "query": "Apple Inc Annual Report"
    },
    {
      "query": "Apple Store"
    }
  ]
}
```

The return result contains multiple fields, described as follows:

- `knowledge_graph`, the knowledge graph of the search result.
- `organic`, detailed information of the search result.
- `people_also_ask`, questions related to the search keyword.
- `related_searches`, related searches for the search keyword.

It can be seen that there is an `organic` field in the returned result, which mainly contains the results of the search keyword.

In addition, if you want to generate the corresponding interface code, you can directly copy the generated code, for example, the CURL code is as follows:

```shell
curl -X POST 'https://api.acedata.cloud/serp/google' \
-H 'accept: application/json' \
-H 'authorization: Bearer {token}' \
-H 'content-type: application/json' \
-d '{
  "query": "apple inc"
}'
```

The Python interface code is as follows:

```python
import requests

url = "https://api.acedata.cloud/serp/google"

headers = {
    "accept": "application/json",
    "authorization": "Bearer {token}",
    "content-type": "application/json"
}

payload = {
    "query": "apple inc"
}

response = requests.post(url, json=payload, headers=headers)
print(response.text)
```

### Custom Search Type

If you customize the type of search resource, we can modify the parameter `type`, which includes ordinary resources `search`, image resources `images`, news resources `news`, map resources `maps`, regional resources `places`, video resources `videos`, this article will demonstrate with video resources `videos`.

Now let's demonstrate the specific operation.

First, set the `type` parameter to `videos`, and normally pass the `query` parameter, as shown in the figure:
<p><img src="https://cdn.acedata.cloud/czlt12.png" width="500" class="m-auto"></p>

The corresponding code is as follows:

```shell
curl -X POST 'https://api.acedata.cloud/serp/google' \
-H 'accept: application/json' \
-H 'authorization: Bearer {token}' \
-H 'content-type: application/json' \
-d '{
  "type": "videos",
  "query": "apple inc"
}'
```

You can get the following response:

```json
{
  "videos": [
    {
      "title": "Healthcare",
      "link": "https://www.apple.com/healthcare/",
      "snippet": "More ways to shop: Find an Apple Store or other retailer near you. Or call 1-800-MY-APPLE (1-800-692-7753). United States. Copyright © 2025 Apple Inc. All ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRQzUYLXB37srVLPW8JbVzhIlP9-SxMe3A8M98Eb7362as4&s",
      "source": "Apple",
      "date": "Apr 16, 2025",
      "position": 1
    },
    {
      "title": "Apple",
      "link": "https://www.youtube.com/apple",
      "snippet": "Our first ever spatial computer. · A Gift for Mom | Shot on iPhone in Spatial Video | Experienced on Apple Vision Pro · Metallica — Official Trailer | Apple ...",
      "position": 2
    },
    {
      "title": "Is Apple FINALLY taking risks again?",
      "link": "https://www.youtube.com/watch?v=JNZV9i5BwH0",
      "snippet": "Taking into account how Microsoft did , and continue to struggle I will said moving the Mac to ARM was a \"killed the company if we fail\" kind of ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR0zvbxg3ozbeHNUJojmyRBhi3J-TviJQRinIS4DZiF-EM8&s",
      "video_url": "https://encrypted-vtbn0.gstatic.com/video?q=tbn:ANd9GcTfNZRuifDZb4zgj0d6wDxoHLI8yUr-8SIPNw",
      "duration": "13:04",
      "source": "YouTube",
      "channel": "Luke Miani",
      "date": "2 days ago",
      "position": 3
    },
    {
      "title": "What Apple Didn't Talk About At WWDC 25 & Why It Matters!",
      "link": "https://www.youtube.com/watch?v=2LTc3mzNh08",
      "snippet": "I'm slowly unfollowing YouTubers that create rage bait videos to follow the hate trend. Apple is far from perfect but these subjects have ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTgGUJwgxdH-WHBmGOk6XgvijwnYX2H_D2Cl23aNab8CKyT&s",
      "video_url": "https://encrypted-vtbn0.gstatic.com/video?q=tbn:ANd9GcRTtYLkgIrCxERepA5KmCJDbZ7lTUa0OBHqzw",
      "duration": "13:05",
      "source": "YouTube",
      "channel": "Brian Tong",
      "date": "7 hours ago",
      "position": 4
    },
    {
      "title": "Apple",
      "link": "https://www.youtube.com/user/Apple",
      "snippet": "Our first ever spatial computer. · A Gift for Mom | Shot on iPhone in Spatial Video | Experienced on Apple Vision Pro · Metallica — Official Trailer | Apple ...",
      "position": 5
    },
    {
      "title": "Apple Watch Ultra 2",
      "link": "https://www.apple.com/apple-watch-ultra-2/",
      "snippet": "Designed in partnership with Huish Outdoors, the Oceanic+ app turns Ultra 2 into a fully capable dive computer running a Bühlmann decompression algorithm.",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSvZ58COtZS4zIIJDd1-Tl0GIKbFqoffFlhLa20OtLcILDR&s",
      "source": "Apple",
      "date": "Sep 12, 2023",
      "position": 6
    },
    {
      "title": "Apple at Work - Success Stories - BDC",
      "link": "https://www.apple.com/business/enterprise/success-stories/financial-services/bdc/",
      "snippet": "Apple Business Manager and AirWatch Mobile Device Management allow BDC to effortlessly deploy and manage devices and apps across the company entirely zero-touch ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRDQuxFNiitOIuPizPvTHwzQqyuLuypH_UNPqcZ-bGUAFy2&s",
      "source": "Apple",
      "date": "Nov 2, 2021",
      "position": 7
    },
    {
      "title": "Higher Education - Institutions",
      "link": "https://www.apple.com/education/higher-education/",
      "snippet": "More ways to shop: Find an Apple Store or other retailer near you. Or call 1-800-MY-APPLE (1-800-692-7753). United States. Copyright © 2025 Apple Inc. All ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSIZRPg0iWQmiRPY-Ro1XmdUQYbwGmIxUgMjjL8TqdyutHF&s",
      "source": "Apple",
      "date": "Jun 8, 2018",
      "position": 8
    },
    {
      "title": "Apple: The Trillion Dollar Betrayal | The Truth About Your ...",
      "link": "https://www.youtube.com/watch?v=wmfuE-RM7Rg",
      "snippet": "Apple is the most valuable company in the world and has a role in our lives like no other. From smartphones to smart watches, ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSvqw0lj-kWlq1HnowgEqzFxk5npWRpod2w1gogX-Dt4-jk&s",
      "video_url": "https://encrypted-vtbn0.gstatic.com/video?q=tbn:ANd9GcSG7N1JPdVZhrbuDckiwnYuWIQsXg_tdcmlvA",
      "duration": "52:40",
      "source": "YouTube",
      "channel": "Moconomy",
      "date": "Dec 4, 2024",
      "position": 9
    },
    {
      "title": "Apple at Work - Success Stories - SAP",
      "link": "https://www.apple.com/business/enterprise/success-stories/tech/sap/",
      "snippet": "SAP has found that offering its employees this choice goes far beyond letting people pick their computer. Mac unleashes their full potential. At a glance. 105K+ ...",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSaplpBsRWWCJNlPtXsFX-jr3yw0mexpI6RtFKN6-TJAqrW&s",
      "source": "Apple",
      "date": "Apr 13, 2022",
      "position": 10
    }
  ]
}
```

The returned result has multiple fields, described as follows:

- `news`, the list of video information in the search results.

As you can see, there is a `videos` field in the returned result, which mainly contains the results of the search keywords.


## More

For more info, please check below APIs and integration documents.

| API | Path | Integration Guidance |
| ---- | ---- | ------------ |
| [Google SERP API](http://platform.acedata.cloud/documents/44c86226-8eaa-49bf-85f3-1fae8d2e23f1) | `/serp/google` | [Google SERP API Integration Guide](http://platform.acedata.cloud/documents/cc2ce913-df8f-4d22-a051-93fa33b2e51b) |

Base URL: [https://api.acedata.cloud](https://api.acedata.cloud)

## Support

If you meet any issue, check our from [support info](https://platform.acedata.cloud/support).