# Google SERP API Integration Instructions

Google SERP (Search Engine Results Page) is the results page that users see after entering a query in the Google search engine. It displays organic search results, ads, featured snippets, knowledge graphs, as well as various content such as images and videos, aimed at providing users with the most relevant information.

This article will provide a detailed introduction to the Google SERP API, which can provide results from queries entered in the Google search engine, with results containing many types, such as featured snippets, knowledge graphs, and images.

This document will introduce the integration instructions for the Google SERP API.

## Application Process

To use the Google SERP API, you need to first apply for the corresponding service on the [Google SERP API](https://platform.acedata.cloud/documents/44c86226-8eaa-49bf-85f3-1fae8d2e23f1) page. After entering the page, click the "Acquire" button, as shown in the image:

![](https://cdn.acedata.cloud/q6ytrc.png)

If you are not logged in or registered, you will be automatically redirected to the login page inviting you to register and log in. After logging in or registering, you will be automatically returned to the current page.

During the first application, there will be a free quota provided, allowing you to use the API for free.

## Basic Usage

First, understand the basic usage method, which is to input the type of search resource and keywords to obtain search results. You only need to simply pass the `query` field and specify the corresponding model.

For example, to find information about "apple inc", we can fill in the corresponding content on the interface, as shown in the image:

<p><img src="https://cdn.acedata.cloud/lnqiye.png" width="500" class="m-auto"></p>

Here we can see that we have set the Request Headers, including:

- `accept`: the format of the response result you want to receive, filled in as `application/json`, which is in JSON format.
- `authorization`: the key to call the API, which can be directly selected after application.

Additionally, we have set the Request Body, including:

- `type`: the type of search resource, currently supporting only six types, with the default being `search`.
- `query`: the keyword for the search.
- `country`: the country where the search results are customized to be located, with the default being the United States (US).
- `language`: the language of the search results, with the default being English (en).
- `range`: the time range for the search results, with the default being unlimited.
- `number`: the page size for the search results, with the default being 10.
- `page`: the page number for the search results, with the default being 1.

After selection, you can find that the corresponding code is also generated on the right side, as shown in the image:

<p><img src="https://cdn.acedata.cloud/1j81zr.png" width="500" class="m-auto"></p>

Click the "Try" button to test, as shown in the image above, and we have obtained the following results:
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

The returned result contains multiple fields, described as follows:

- `knowledge_graph`, the knowledge graph of the search result.
- `organic`, detailed information of the search result.
- `people_also_ask`, questions related to the search keyword.
- `related_searches`, related searches for the search keyword.

It can be seen that there is an `organic` field in the returned result, which mainly contains the results of the search keyword.

Additionally, if you want to generate the corresponding interface code, you can directly copy the generated code, for example, the CURL code is as follows:

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

## Custom Search Type

If you customize the type of search resource, we can modify the parameter `type`, which includes ordinary resources `search`, image resources `images`, news resources `news`, map resources `maps`, regional resources `places`, and video resources `videos`. This article will demonstrate using the video resource `videos`.

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

The returned result contains multiple fields, described as follows:

- `news`, the list of video information in the search results.

As you can see, there is a `videos` field in the returned result, which mainly contains the results of the search keywords.

## Customizing the Country of Search Resources

This interface also supports limiting the country of the search results, we can add the `country` parameter to specify the country, with the input parameter being the abbreviation of the country, such as cn (China), us (United States). This article will take China as an example, and the specific information is as follows:

<p><img src="https://cdn.acedata.cloud/gztpwi.png" width="500" class="m-auto"></p>

The output effect is as follows:
```json
{
  "news": [
    {
      "title": "Apple announces iOS 26 beta public roll out set for July",
      "link": "https://www.tv47.digital/apple-announces-ios-26-beta-public-roll-out-set-for-july-105190/",
      "snippet": "Tech giant Apple Inc. has unveiled the latest iterations of its operating systems for iPhone, Mac, and iPad, introducing a significant...",
      "date": "2 hours ago",
      "source": "TV47 Digital",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBNrktH4AWMt8KS3hErOkI1oAeUvRm4Aaq10qnINCa3TmyabOCwiEMvxVWsA&s",
      "position": 1
    },
    {
      "title": "Bragar Eagel & Squire, P.C. Is Investigating Apple, Sable and Abacus and Encourages Investors to Contact the Firm",
      "link": "https://www.tradingview.com/news/reuters.com,2025-06-17:newsml_GNX87dzHl:0-bragar-eagel-squire-p-c-is-investigating-apple-sable-and-abacus-and-encourages-investors-to-contact-the-firm/",
      "snippet": "NEW YORK, June 16, 2025 (GLOBE NEWSWIRE) — Bragar Eagel & Squire, P.C., a nationally recognized shareholder rights law firm,...",
      "date": "10 hours ago",
      "source": "TradingView",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRdcHGK9sZ4M1wtCX6U74yV2ac9ClDX2hTSX4l4Brr1DWTvXfI4dKAn8sDU9g&s",
      "position": 2
    },
    {
      "title": "Apple Inc. (AAPL) Opinions on WWDC Software and AI Announcements",
      "link": "https://www.nasdaq.com/articles/apple-inc-aapl-opinions-wwdc-software-and-ai-announcements",
      "snippet": "Recent discussions on X about Apple Inc. (AAPL) have centered around the company's latest software updates and AI initiatives unveiled at...",
      "date": "17 hours ago",
      "source": "Nasdaq",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSm5mhn6LRgzafnn34CrjlR3LS1_fHPmKNJckasyNgN4eYgBiCqGtulLQIViA&s",
      "position": 3
    },
    {
      "title": "Goldman Sachs Recommends Buying Apple, Expects Stock to Climb",
      "link": "https://finance.yahoo.com/news/goldman-sachs-recommends-buying-apple-042754922.html",
      "snippet": "Apple Inc. (NASDAQ:AAPL) is one of the best next generation dividend aristocrat stocks. Goldman Sachs recently highlighted a group of stocks...",
      "date": "6 hours ago",
      "source": "Yahoo Finance",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS6QgEG6x6t12L8YqJebmoiPNM_RMjmiVUpwam1YXZgKwBUPGe6yn76hR-n0g&s",
      "position": 4
    },
    {
      "title": "Apple threatened with more noncompliance fines after losing Dutch App Store appeal",
      "link": "https://globalcompetitionreview.com/article/apple-threatened-more-noncompliance-fines-after-losing-dutch-app-store-appeal",
      "snippet": "The Netherlands Authority for Consumers and Markets has successfully fended off Apple's appeal against an order to amend its App Store rules...",
      "date": "17 hours ago",
      "source": "Global Competition Review",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ02b47E8UHdyFL6A4Da4Wla_nXXc427Y9aMgE7vVuJpN4CzLQp0ip_G77FwA&s",
      "position": 5
    },
    {
      "title": "Dutch court confirms Apple abused dominant position in dating apps",
      "link": "https://www.reuters.com/sustainability/boards-policy-regulation/dutch-court-confirms-apple-abused-dominant-position-dating-apps-2025-06-16/",
      "snippet": "A Dutch court on Monday confirmed a 2021 consumer watchdog 's ruling saying that Apple had abused its dominant position by imposing unfair...",
      "date": "19 hours ago",
      "source": "Reuters",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLRbz3ypqJL6zJo1LBfMen68-D4csUJbGNNO7w8JODW6fiKliGk0yRyRGfvQ&s",
      "position": 6
    },
    {
      "title": "Can Apple Salvage the AI iPhone in China?",
      "link": "https://www.bloomberg.com/opinion/articles/2025-06-10/can-apple-salvage-the-ai-iphone-in-china",
      "snippet": "If you thought Apple Inc.'s artificial intelligence woes in the US were bad, just know that they could actually be worse. Look at China.",
      "date": "6 days ago",
      "source": "Bloomberg.com",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRzqIqxSek95GHKeeX9ekGIfzlZhz4jdEXqJPlk9Gyi5E8Yzk55iuhR5Soy_Q&s",
      "position": 7
    },
    {
      "title": "Apple requests S. Korea to allow transfer of high-precision map data overseas",
      "link": "https://en.yna.co.kr/view/AEN20250617006800320",
      "snippet": "SEOUL, June 17 (Yonhap) -- U.S. tech giant Apple Inc. has requested the South Korean gover...",
      "date": "5 hours ago",
      "source": "Yonhap News Agency",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS20gcfgCXs4W5Hzu78JWocLIX_9jQPbN1rUUPctbiJ1UKd7R7eotC4CodJdQ&s",
      "position": 8
    },
    {
      "title": "Dutch Court Upholds Ruling Against Apple’s App Store Abuse",
      "link": "https://www.webpronews.com/dutch-court-upholds-ruling-against-apples-app-store-abuse/",
      "snippet": "In a significant blow to Apple Inc., a Dutch court has upheld a 2021 ruling by the Netherlands' Authority for Consumers and Markets,...",
      "date": "13 hours ago",
      "source": "WebProNews",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSVZUsNtxTvIJYDjEGJN53uHWvK5NAGJrf-GS4wnzlSUtAbIYizew6HrYzr_w&s",
      "position": 9
    },
    {
      "title": "Dutch court confirms Apple abused dominant position for dating apps",
      "link": "https://seekingalpha.com/news/4458712-dutch-court-confirms-apple-abused-dominant-position-for-dating-apps",
      "snippet": "A Dutch court confirmed the country's competition agency's ruling that Apple (AAPL) abused its dominant position by imposing unreasonable...",
      "date": "2 hours ago",
      "source": "Seeking Alpha",
      "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSkf9LcqSBxw2DQZaDhfzZyJ0G2VRkkJ6dVHgBJFIGv_fgtPTDo2iAfQ_5fcQ&s",
      "position": 10
    }
  ]
}
```
We can also customize the language of the search results. Here we additionally add the `language` field, with the content being `zh-cn`, which refers to the Simplified Chinese language. Other languages are also supported, but the abbreviation of the language must be entered, such as en (English), fr (French), zh-cn (Chinese (Simplified)), etc., as shown in the figure:

<p><img src="https://cdn.acedata.cloud/yyrssp.png" width="500" class="m-auto"></p>

The corresponding code is as follows:

```shell
curl -X POST 'https://api.acedata.cloud/serp/google' \
-H 'accept: application/json' \
-H 'authorization: Bearer {token}' \
-H 'content-type: application/json' \
-d '{
  "type": "news",
  "query": "apple inc",
  "language": "zh-cn"
}'
```

The running result is as follows:

```json
{
  "knowledge_graph": {
    "title": "苹果",
    "type": "公司",
    "website": "http://www.apple.com/",
    "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRgbY1KzXEpuPeTpcw0GwN6BpQTcg1m06TDUsfdG6P-zW3eWrmu78AXyg&s=0",
    "attributes": {
      "创始人": "史蒂夫·乔布斯、史蒂夫·沃兹尼亚克和罗纳德·韦恩",
      "创立于": "1976 年 4 月 1 日，加利福尼亚洛思阿图斯",
      "总部": "加利福尼亚库比蒂诺"
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
          "title": "Careers at Apple",
          "link": "https://www.apple.com/careers/us/"
        },
        {
          "title": "Store",
          "link": "https://www.apple.com/store"
        },
        {
          "title": "Business",
          "link": "https://www.apple.com/business/"
        },
        {
          "title": "Apple UK",
          "link": "https://www.apple.com/uk/"
        }
      ],
      "position": 1
    },
    {
      "title": "Apple Inc. - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc.",
      "snippet": "Apple Inc. is an American multinational corporation and technology company headquartered in Cupertino, California, in Silicon Valley.",
      "sitelinks": [
        {
          "title": "History",
          "link": "https://en.wikipedia.org/wiki/History_of_Apple_Inc."
        },
        {
          "title": "Litigation involving Apple Inc.",
          "link": "https://en.wikipedia.org/wiki/Litigation_involving_Apple_Inc."
        },
        {
          "title": "Apple Park",
          "link": "https://en.wikipedia.org/wiki/Apple_Park"
        },
        {
          "title": "Apple Watch",
          "link": "https://en.wikipedia.org/wiki/Apple_Watch"
        }
      ],
      "position": 2
    },
    {
      "title": "Apple Inc. | History, Products, Headquarters, & Facts - Britannica",
      "link": "https://www.britannica.com/money/Apple-Inc",
      "snippet": "Apple Inc. is an American multinational technology company that revolutionized the technology sector through its innovation of computer software, ...",
      "position": 3
    },
    {
      "title": "Apple Inc - Company Profile and News - Bloomberg Markets",
      "link": "https://www.bloomberg.com/profile/company/AAPL:US",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables and accessories, and sells a variety of related ...",
      "position": 4
    },
    {
      "title": "Apple Inc. (AAPL) Stock Price, News, Quote & History - Yahoo Finance",
      "link": "https://finance.yahoo.com/quote/AAPL/",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables, and accessories worldwide.",
      "date": "2024年8月27日",
      "position": 5
    },
    {
      "title": "AAPL: Apple Inc Stock Price Quote - NASDAQ GS - Bloomberg",
      "link": "https://www.bloomberg.com/quote/AAPL:US",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables and accessories, and sells a variety of related accessories.",
      "position": 6
    },
    {
      "title": "Apple Inc. (AAPL) Company Profile & Facts - Yahoo Finance",
      "link": "https://finance.yahoo.com/quote/AAPL/profile/",
      "snippet": "See the company profile for Apple Inc. (AAPL) including business summary, industry/sector information, number of employees, business summary, ...",
      "position": 7
    }
  ],
  "people_also_ask": [
    {
      "question": "What is Apple Inc stand for?",
      "snippet": "It was incorporated as Apple Computer, Inc. in January 1977, and sales of its computers, including the Apple II , saw significant momentum and revenue growth for the company. \"Inc.\" is the abbreviation for incorporated. A corporation is a separate legal entity from the person or people forming it.",
      "title": "What does the 'Inc.' in Apple Inc. mean? - Quora",
      "link": "https://www.quora.com/What-does-the-Inc-in-Apple-Inc-mean"
    },
    {
      "question": "Who owns Apple Inc.?",
      "snippet": "Apple (AAPL) Ownership Overview The ownership structure of Apple (AAPL) stock is a mix of institutional, retail and individual investors. Approximately 48.76% of the company's stock is owned by Institutional Investors, 0.11% is owned by Insiders and 51.13% is owned by Public Companies and Individual Investors.",
      "title": "Who owns Apple? AAPL Stock Ownership - TipRanks.com",
      "link": "https://www.tipranks.com/stocks/aapl/ownership"
    },
    {
      "question": "Why did Apple change to Apple Inc?",
      "snippet": "During his keynote speech at the Macworld Expo on January 9, 2007, Jobs announced the renaming of Apple Computer, Inc. to Apple Inc., because the company had broadened its focus from computers to consumer electronics. This event also saw the announcement of the iPhone and the Apple TV.",
      "title": "Apple Inc. - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc."
    },
    {
      "question": "Why Apple Inc is called Apple?",
      "snippet": "With the name Apple, the new computer company would appear ahead of Atari, where Jobs used to work. Jobs confirmed this theory in an 1980 presentation, stating that the name was partly chosen because he liked apples and partly because Apple was ahead of Atari in the phone book.",
      "title": "Why Is Apple Called Apple? - Apple Scoop",
      "link": "https://applescoop.org/story/why-is-apple-called-apple"
    }
  ],
  "related_searches": [
    {
      "query": "apple inc是什么"
    },
    {
      "query": "apple澳门"
    },
    {
      "query": "Apple ID"
    },
    {
      "query": "apple美国"
    },
    {
      "query": "apple官网"
    },
    {
      "query": "apple美国官网"
    },
    {
      "query": "Apple company introduction"
    },
    {
      "query": "apple id官网"
    }
  ],
  "credits": 1
}
```

As can be seen, the results displayed here are all in Simplified Chinese, and the content of the results is similar to the above text.

## Customizing the Time Range of Search Results
This article also allows customizing the time range of search results, which includes five options: `qdr:h` (past hour), `qdr:d` (past day), `qdr:w` (past week), `qdr:m` (past month), and by default, no restrictions. We can pass the corresponding time range through `range`, for example, setting it to `qdr:d` indicates searching for results from the past day, so the input is as follows:

<p><img src="https://cdn.acedata.cloud/qccfib.png" width="500" class="m-auto"></p>

The corresponding code is as follows:

```shell
curl -X POST 'https://api.acedata.cloud/serp/google' \
-H 'accept: application/json' \
-H 'authorization: Bearer {token}' \
-H 'content-type: application/json' \
-d '{
  "range": "qdr:d",
  "query": "apple inc"
}'
```

The result is as follows:

```json
{
  "answer_box": {
    "title": "Tim Cook (Aug 24, 2011–)Apple / CEO",
    "answer": "Tim Cook (Aug 24, 2011–)"
  },
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
          "title": "Apple Leadership",
          "link": "https://www.apple.com/leadership/"
        },
        {
          "title": "Store",
          "link": "https://www.apple.com/store"
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
      "link": "https://www.wsj.com/market-data/quotes/AAPL?gaa_at=eafs&gaa_n=ASWzDAjHf1Jvm_DfBkgGitLxGwlDC2VFfkyeU3ora5VpP1k1gJJfptWjtU4o&gaa_ts=6851a5a8&gaa_sig=FmQcgCrdYtgMPhMwfFTpCtEva8_OZ5j1fx1cEBn0_THBq1EUa8A0Tmo3piNM3OQ488O2rScdH4NuSLly_DIdpQ%3D%3D",
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
      "snippet": "Apple (AAPL) Ownership Overview Approximately 50.57% of the company's stock is owned by Institutional Investors, 0.06% is owned by Insiders, and 49.38% is owned by Public Companies and Individual Investors. The ownership structure of Apple (AAPL) stock is a mix of institutional, retail, and individual investors.",
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
      "question": "Who is the current owner of Apple?",
      "snippet": "Tim Cook (Aug 24, 2011–)\nApple / CEO"
    }
  ],
  "related_searches": [
    {
      "query": "Apple iPhone 13"
    },
    {
      "query": "what is apple inc"
    },
    {
      "query": "Apple Inc full form"
    },
    {
      "query": "Apple Inc address"
    },
    {
      "query": "Apple Inc investor relations"
    },
    {
      "query": "Apple Inc industry"
    },
    {
      "query": "Apple Inc Annual Report"
    },
    {
      "query": "Apple Inc careers"
    }
  ]
}
```

As we can see, we successfully obtained the search results from the past day, and the content of the results is similar to the above.

## Customizing Pagination of Search Results

This API also supports customizing the pagination display of search results, where `number` and `page` represent the page size and page number for pagination. This article will set the format to display 20 search results per page, as shown in the image:

<p><img src="https://cdn.acedata.cloud/dqla1e.png" width="500" class="m-auto"></p>

> Note: When the number of results per page exceeds 10, the deducted points will double.

The code is as follows:
```shell
curl -X POST 'https://api.acedata.cloud/serp/google' \
-H 'accept: application/json' \
-H 'authorization: Bearer {token}' \
-H 'content-type: application/json' \
-d '{
  "query": "apple inc",
  "number": 20,
  "page": 1
}'
```

The result is as follows:

```json
{
  "knowledge_graph": {
    "title": "Apple",
    "type": "Technology company",
    "image_url": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSHmAG45NsvdRfYlNghHFvinM0w2mqjd8A0lXKU2LA&usqp=CAE&s",
    "attributes": {
      "Customer service": "1 (800) 275-2273",
      "Founders": "Steve Jobs, Steve Wozniak, Ronald Wayne",
      "Founded": "April 1, 1976, Los Altos, CA",
      "Stock price": "AAPL (NASDAQ) $198.42 +1.97 (+1.00%)Jun 16, 4:00 PM EDT - Disclaimer",
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
          "link": "https://support.apple.com/",
          "snippet": "iPhone Support - Contact - Billing and Subscriptions - Apple Repair"
        }, {
          "title": "Career Opportunities",
          "link": "https://www.apple.com/careers/us/",
          "snippet": "Work at Apple - Software and Services - Support and Service"
        }, {
          "title": "Business",
          "link": "https://www.apple.com/business/",
          "snippet": "Small Business - Enterprise - Shop for Business - Apple at Work - ..."
        }, {
          "title": "Store",
          "link": "https://www.apple.com/store",
          "snippet": "Shop iPhone - Shop Mac - Shop iPad - App Store - ..."
        },
        {
          "title": "Investor Relations",
          "link": "https://investor.apple.com/investor-relations/default.aspx",
          "snippet": "SEC Filings - Stock Price - Leadership and Governance"
        }
      ],
      "position": 1
    }, {
      "title": "Apple Inc.",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc.",
      "snippet": "Apple Inc. is an American multinational corporation and technology company headquartered in Cupertino, California, in Silicon Valley.",
      "position": 2
    }, {
      "title": "Apple Inc. | History, Products, Headquarters, & Facts",
      "link": "https://www.britannica.com/money/Apple-Inc",
      "snippet": "Apple Inc. is an American multinational technology company that revolutionized the technology sector through its innovation of computer software, personal ...",
      "date": "7 days ago",
      "position": 3
    }, {
      "title": "Apple Inc. (AAPL) Company Profile & Facts",
      "link": "https://finance.yahoo.com/quote/AAPL/profile/",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables, and accessories worldwide.",
      "position": 4
    }, {
      "title": "AAPL: Apple Inc Stock Price Quote - NASDAQ GS",
      "link": "https://www.bloomberg.com/quote/AAPL:US",
      "snippet": "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables and accessories, and sells a variety of related accessories.",
      "position": 5
    }, {
      "title": "Apple Inc. (AAPL) Stock Price Today",
      "link": "https://www.wsj.com/market-data/quotes/AAPL?gaa_at=eafs&gaa_n=ASWzDAgqDxGuyZUvNqcmVhmXBoGHd3y-StLOZpo82befc3s9jFqSwwJzjPmn&gaa_ts=68514b6e&gaa_sig=a-sNk_J7mCIayZx21oIaY6Ge6vifnmxy7A4psXod_wP6ng9689uAwZYvUOUQPv_dxcArYe_RQbKxCkwngcK_bQ%3D%3D",
      "snippet": "Apple Inc. engages in the design, manufacture, and sale of smartphones, personal computers, tablets, wearables and accessories, and other varieties of related ...",
      "position": 6
    }, {
      "title": "Apple",
      "link": "https://www.linkedin.com/company/apple",
      "snippet": "External link for Apple. Industry: Computers and Electronics Manufacturing. Company size: 10,001+ employees. Headquarters: Cupertino, California. Type: Public ...",
      "position": 7
    }, {
      "title": "Apple | AAPL Stock Price, Company Overview & News",
      "link": "https://www.forbes.com/companies/apple/",
      "snippet": "Apple Inc. engages in the design, manufacture, and sale of smartphones, personal computers, tablets, wearables and accessories, and other variety of related ...",
      "position": 8
    }, {
      "title": "Apple Inc. (AAPL) Stock Price, News, Quote & History",
      "link": "https://finance.yahoo.com/quote/AAPL/",
      "snippet": "Find the latest Apple Inc. (AAPL) stock quote, history, news and other vital information to help you with your stock trading and investing.",
      "position": 9
    }, {
      "title": "iCloud",
      "link": "https://www.icloud.com/",
      "snippet": "At iCloud.com, you can access your photos, files, and more from any web browser. Changes you make will sync to your iPhone and other devices.",
      "position": 10
    }, {
      "title": "Apple Inc (AAPL) Stock Price & News - Google Finance",
      "link": "https://www.google.com/finance/quote/AAPL:NASDAQ?hl=en",
      "snippet": "Apple Inc. is an American multinational corporation and technology company headquartered in Cupertino, California, in Silicon Valley.",
      "position": 11
    }, {
      "title": "Apple Inc Company Profile - GlobalData",
      "link": "https://www.globaldata.com/company-profile/apple-inc/",
      "snippet": "Apple Inc (Apple) designs, manufactures, and markets smartphones, tablets, personal computers, and wearable devices. The company offers software applications ...",
      "position": 12
    }, {
      "title": "The Founding of Apple Computer, Inc. - This Month in ...",
      "link": "https://guides.loc.gov/this-month-in-business-history/april/apple-computer-founded",
      "snippet": "Apple Computer, Inc. was founded on April 1, 1976, by college dropouts Steve Jobs and Steve Wozniak, who brought to the new company a vision of changing the ...",
      "position": 13
    }, {
      "title": "Apple Inc",
      "link": "https://vimeo.com/appleinc",
      "snippet": "Apple Inc is a member of Vimeo, the home for high quality videos and the people who love them.",
      "position": 14
    }
  ],
  "people_also_ask": [
    {
      "question": "What is the Apple Inc?"
    }, {
      "question": "Who owns Apple Inc?"
    }, {
      "question": "What is Apple Inc. best known for?",
      "title": "Apple Inc. - Wikipedia",
      "snippet": "It is best known for its consumer electronics, software, and services. Founded in 1976 as Apple Computer Company by Steve Jobs, Steve Wozniak and Ronald Wayne, the company was incorporated by Jobs and Wozniak as Apple Computer, Inc. the following year.",
      "link": "https://en.wikipedia.org/wiki/Apple_Inc.#:~:text=It%20is%20best%20known%20for,%2C%20Inc.%20the%20following%20year."
    },
```
{
      "question": "What is the meaning of Inc in Apple Inc?",
      "title": "Inc. | English meaning - Cambridge Dictionary",
      "snippet": "abbreviation for incorporated: used in the names of US companies that are legally established: Bishop Computer Services, Inc.",
      "link": "https://dictionary.cambridge.org/dictionary/english/inc#:~:text=abbreviation%20for%20incorporated%3A%20used%20in,Bishop%20Computer%20Services%2C%20Inc."
    } ],
  "related_searches": [
    {
      "query": "What is Apple Inc"
    }, {
      "query": "Apple Inc full form"
    }, {
      "query": "Apple Inc address"
    }, {
      "query": "Apple Inc investor relations"
    }, {
      "query": "Apple Inc industry"
    },
    {
      "query": "Apple Inc Annual Report"
    },
    {
      "query": "Apple Inc careers"
    },
    {
      "query": "Apple 17 pro"
    }
  ]
}
```

As can be seen, it displays the search results in a paginated format, showing 20 results per page, and the content of the results is similar to the above text.