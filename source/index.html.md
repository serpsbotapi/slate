---
title: SERPSBOT API Docs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - php

toc_footers:
  - <a href='https://serpsbot.com/account/sign-up/' target='_blank'>Get Your API Key</a>

includes:
  - errors

search: false
---

# Introduction

[SERPSBOT](https://serpsbot.com) offers a robust API to get Google SERPs results as JSON data. We offer a highly-reliable API service at an affordable price. This documentation helps you get started using our API service.

# Get SERP Results

> Get SERP results:

```python
import requests

# Your API key
apikey = 'your-api-key-here'
headers = {
  'Authorization': 'Bearer {}'.format(apikey)
}

payload = {
  'q': 'covid19',
  'pages': 2,
  'hl': 'en-US',
  'gl': 'us'
}

res = requests.get('https://serpsbot.com/api/v1/google-serps/', headers=headers, params=payload)

# JSON data
res.json()
```

```shell
# In a terminal, you can use CURL to get SERP results
curl -X GET -H "Authorization: Bearer your-api-key-here" "https://serpsbot.com/api/v1/google-serps/?q=covid19&pages=2&hl=en-US&gl=us"
```

```php
use Guzzle\Client;
$options = [
  'headers' => [
    'Authorization' => 'Bearer your-api-key-here'
  ],
  'params' => [
    'q' => 'covid19',
    'pages' => 2,
    'hl' => 'en-US',
    'gl' => 'us'
  ]
];
$client = new Client();
$res = $client->get("https://serpsbot.com/api/v1/google-serps/", $options);

// JSON data
$json = json_decode($res->getBody()->getContents(), true);
```

> Example Response:

```json
{
    "data": {
        "meta": {
            "pages": 2,
            "results": 17,
            "query": "covid19",
            "gl": "us",
            "duration": null,
            "hl": "en-US",
            "time_taken": 1.7270863056182861,
            "credits_left": 707705
        },
        "results": {
            "organic": [
                {
                    "url": "https://covid19.ca.gov/",
                    "title": "California Coronavirus - CA.gov",
                    "rank": 1,
                    "snippet": "Official website for California Coronavirus (COVID-19) Response daily updates and resources. Stay home - save lives. Find information and services to help you ...",
                    "snippet_html": "<span class=\"st\">\n Official website for California Coronavirus (\n <em>\n  COVID-19\n </em>\n ) Response daily updates and resources. Stay home - save lives. Find information and services to help you\n <wbr/>\n ...\n</span>\n"
                },
                {
                    "url": "https://www.cdc.gov/coronavirus/2019-ncov/index.html",
                    "title": "Coronavirus Disease 2019 (COVID-19) | CDC",
                    "rank": 2,
                    "snippet": "Coronavirus (COVID-19) Home Page.",
                    "snippet_html": "<span class=\"st\">\n Coronavirus (\n <em>\n  COVID-19\n </em>\n ) Home Page.\n</span>\n"
                },
                {
                    "url": "https://covid19.healthdata.org/",
                    "title": "COVID-19",
                    "rank": 3,
                    "snippet": "135,109COVID-19 deaths. projected by August 4, 2020. 0 20k 40k 60k 80k 100k 120k 140k 160k 180k 200k 220k 240k 260k 280k 300k Total deaths Mar 1 Apr ...",
                    "snippet_html": "<span class=\"st\">\n 135,109\n <em>\n  COVID-19\n </em>\n deaths. projected by August 4, 2020. 0 20k 40k 60k 80k 100k 120k 140k 160k 180k 200k 220k 240k 260k 280k 300k Total deaths Mar 1 Apr ...\n</span>\n"
                },
                {
                    "url": "https://www.who.int/emergencies/diseases/novel-coronavirus-2019",
                    "title": "Coronavirus disease 2019 - World Health Organization",
                    "rank": 4,
                    "snippet": "Information on COVID-19, the infectious disease caused by the most recently discovered coronavirus.",
                    "snippet_html": "<span class=\"st\">\n Information on\n <em>\n  COVID-19\n </em>\n , the infectious disease caused by the most recently discovered coronavirus.\n</span>"
                },
                {
                    "url": "https://www.who.int/emergencies/diseases/novel-coronavirus-2019/situation-reports",
                    "title": "Coronavirus Disease (COVID-19) Situation Reports",
                    "rank": 5,
                    "snippet": "The daily Situation Report provides the current COVID-19 epidemiological situation and presents official case and death counts and transmission classifications ...",
                    "snippet_html": "<span class=\"st\">\n The daily Situation Report provides the current\n <em>\n  COVID-19\n </em>\n epidemiological situation and presents official case and death counts and transmission classifications ...\n</span>"
                },
                {
                    "url": "https://www.theatlantic.com/science/archive/2020/06/how-negative-covid-19-test-can-mislead/613246/",
                    "title": "What a Negative COVID-19 Test Really Means - The Atlantic",
                    "rank": 6,
                    "snippet": "1 day ago - Understanding false negatives from COVID-19 tests is especially important because people who do not yet know that they're sick play a major ...",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  1 day ago -\n </span>\n Understanding false negatives from\n <em>\n  COVID-19\n </em>\n tests is especially important because people who do not yet know that they're sick play a major ...\n</span>"
                },
                {
                    "url": "https://www.nih.gov/coronavirus",
                    "title": "Coronavirus (COVID-19) | National Institutes of Health (NIH)",
                    "rank": 7,
                    "snippet": "Resources and news releases from the National Institutes of Health regarding the coronavirus (COVID-19).",
                    "snippet_html": "<span class=\"st\">\n Resources and news releases from the National Institutes of Health regarding the coronavirus (\n <em>\n  COVID-19\n </em>\n ).\n</span>"
                },
                {
                    "url": "https://www.alabamapublichealth.gov/covid19/",
                    "title": "Coronavirus Disease 2019 (COVID-19) | Alabama Department ...",
                    "rank": 8,
                    "snippet": "3 days ago - COVID-19, the infectious disease caused by SARS-CoV-2, is now a pandemic affecting many countries globally. Patients with confirmed COVID- ...",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  3 days ago -\n </span>\n <em>\n  COVID-19\n </em>\n , the infectious disease caused by SARS-CoV-2, is now a pandemic affecting many countries globally. Patients with confirmed\n <em>\n  COVID-\n </em>\n ...\n</span>"
                },
                {
                    "url": "https://www.scdhec.gov/infectious-diseases/viruses/coronavirus-disease-2019-covid-19",
                    "title": "Coronavirus Disease 2019 (COVID-19) | SCDHEC",
                    "rank": 9,
                    "snippet": "DHEC continues to work with federal, state and local partners as it investigates COVID-19 cases in South ...",
                    "snippet_html": "<span class=\"st\">\n DHEC continues to work with federal, state and local partners as it investigates\n <em>\n  COVID-19\n </em>\n cases in South ...\n</span>\n"
                },
                {
                    "url": "https://www.sciencemag.org/news/2020/05/why-do-some-covid-19-patients-infect-many-others-whereas-most-don-t-spread-virus-all",
                    "title": "Why do some COVID-19 patients infect many others, whereas ...",
                    "rank": 10,
                    "snippet": "May 19, 2020 - Science 's COVID-19 reporting is supported by the Pulitzer Center. When 61 people met for a choir practice in a church in Mount Vernon, ...",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  May 19, 2020 -\n </span>\n Science 's\n <em>\n  COVID-19\n </em>\n reporting is supported by the Pulitzer Center. When 61 people met for a choir practice in a church in Mount Vernon, ...\n</span>"
                },
                {
                    "url": "https://mn.gov/covid19/",
                    "title": "Minnesota COVID-19 Response (Coronavirus) / COVID-19 ...",
                    "rank": 11,
                    "snippet": "The state of Minnesota's official website for COVID-19 information. Get information on coronavirus testing sites, Minnesota-specific case data and statistics, ...",
                    "snippet_html": "<span class=\"st\">\n The state of Minnesota's official website for\n <em>\n  COVID-19\n </em>\n information. Get information on coronavirus testing sites, Minnesota-specific case data and statistics, ...\n</span>"
                },
                {
                    "url": "https://www.worldometers.info/coronavirus/",
                    "title": "Coronavirus Update (Live): 9,077,451 Cases and 471,246 ...",
                    "rank": 12,
                    "snippet": "The coronavirus COVID-19 is affecting 213 countries and territories around the world and 2 international conveyances. The day is reset after midnight GMT+0.",
                    "snippet_html": "<span class=\"st\">\n The coronavirus\n <em>\n  COVID-19\n </em>\n is affecting 213 countries and territories around the world and 2 international conveyances. The day is reset after midnight GMT+0.\n</span>"
                },
                {
                    "url": "https://www.apple.com/covid19/",
                    "title": "Coronavirus (COVID-19) - Apple and CDC",
                    "rank": 13,
                    "snippet": "If you think you or a family member have been exposed to COVID-19, evaluate symptoms with our in-home screening tool and understand your next steps.",
                    "snippet_html": "<span class=\"st\">\n If you think you or a family member have been exposed to\n <em>\n  COVID-19\n </em>\n , evaluate symptoms with our in-home screening tool and understand your next steps.\n</span>"
                },
                {
                    "url": "https://www.politico.com/states/florida/story/2020/06/20/desantis-pivots-on-covid-19-surge-says-testing-doesnt-account-for-spike-1293901",
                    "title": "DeSantis pivots on Covid-19 surge, says testing doesn't ...",
                    "rank": 14,
                    "snippet": "2 days ago - TALLAHASSEE — Gov. Ron DeSantis acknowledged on Saturday that the rising number of new Covid-19 cases in Florida cannot be ...",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  2 days ago -\n </span>\n TALLAHASSEE — Gov. Ron DeSantis acknowledged on Saturday that the rising number of new\n <em>\n  Covid-19\n </em>\n cases in Florida cannot be ...\n</span>"
                },
                {
                    "url": "https://www.theatlantic.com/health/archive/2020/06/does-colloidal-silver-work-covid-19/613177/",
                    "title": "Does Colloidal Silver Work for COVID-19? - The Atlantic",
                    "rank": 15,
                    "snippet": "4 hours ago - The pandemic has sparked an interest in dubious cures such as colloidal silver—and some are trying to capitalize on it.",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  4 hours ago -\n </span>\n The pandemic has sparked an interest in dubious cures such as colloidal silver—\n <wbr/>\n and some are trying to capitalize on it.\n</span>"
                },
                {
                    "url": "https://landing.google.com/screener/covid19",
                    "title": "COVID‑19 self-assessment - Google",
                    "rank": 16,
                    "snippet": "This resource can help you decide what kind of medical care you might need for COVID‑19. For informational purposes only. Not a medical diagnosis.",
                    "snippet_html": "<span class=\"st\">\n This resource can help you decide what kind of medical care you might need for COVID‑19. For informational purposes only. Not a medical diagnosis.\n</span>"
                },
                {
                    "url": "https://www.mprnews.org/story/2020/06/22/latest-on-covid19-in-mn",
                    "title": "Latest on COVID-19 in MN: State passes 500K tests | MPR News",
                    "rank": 17,
                    "snippet": "5 hours ago - The total number of completed COVID-19 tests in Minnesota surpassed 500000 over the weekend as the virus' toll continued.",
                    "snippet_html": "<span class=\"st\">\n <span class=\"f\">\n  5 hours ago -\n </span>\n The total number of completed\n <em>\n  COVID-19\n </em>\n tests in Minnesota surpassed 500000 over the weekend as the virus' toll continued.\n</span>"
                }
            ]
        }
    }
}
```

To get SERP results, you need to first get your API key [from here](https://serpsbot.com/account/sign-up/) and then perform a <code>GET</code> request to our API endpoint <code>https://serpsbot.com/api/v1/google-serps/</code>

### Request Headers
Header | Value |
------- | ------- |
Authorization | Bearer your-api-key-here

### Request Parameters

Param | Type | Required | Description
--------- | ----------- | ----------- | -----------
q | string | yes | Search query parameter. All Google search filters like <strong>site:</strong> and others are supported.
pages | integer | no | Number of SERP pages to get based on 10 results per page. Defalts to <strong>1</strong> (i.e. first page).
hl | string | no | Language to get search results for. Defaults to <strong>en-US</strong> (i.e. English USA).
gl | string | no | Country code to get search results for a particular country. Defaults to <strong>us</strong>.
autocorrect | integer | no | Should Google autocorrect your typos? If no, set this to <strong>0</strong>. Defaults to <strong>1</strong>.
duration | string | no | Duration to get results updated during the specified time period. Expected values are <strong>d</strong> (for the last 24 hours), <strong>w</strong> (for the last 7 days), <strong>m</strong> (for the last 1 month), <strong>mn</strong> (for the last <strong>n</strong> months), and <strong>y</strong> (for the last 1 year).

# Get Account Details

You can perform a <code>GET</code> request at our API endpoint <code>https://serpsbot.com/api/v1/account/</code> to get details for your account. The server will return your email address, remaining credits, and a count of your API calls as a JSON response.

### Request Headers
Header | Value |
------- | ------- |
Authorization | Bearer your-api-key-here

> Get account details:

```python
import requests
headers = {
    "Authorization": "Bearer your-api-key-here"
}
res = requests.get("https://serpsbot.com/api/v1/account/", headers=headers)

# JSON data
res.json()
```

```shell
curl -H "Authorization: Bearer your-api-key-here" "https://serpsbot.com/api/v1/account/"
```

```php
require Guzzle\Client;
$options = [
    "headers" => [
        "Authorization" => "Bearer your-api-key-here"
    ]
];
$client = new Client();
$res = $client->get("https://serpsbot.com/api/v1/account/", $options);

# JSON data
$json = json_decode($res->getBody()->getContents(), true);
```

> Example Response:

```json
{
    "account": {
        "email": "user@example.com",
        "credits": 123456789,
        "stats": 123456789
    }
}
```