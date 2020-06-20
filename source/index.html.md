---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

includes:
  - errors

search: true
---

# Introduction

Welcome to the Qurix API! You can use our API to access HIMS and PRM endpoints, which can get information on patients, episodes, beds and billing in our database.

You can view code examples in the dark area to the right.


# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization:  "
```

> Make sure to replace ` ` with your API key.

Qurix uses API keys to allow access to the API. You can register a new API key at our [developer portal](http://example.com/developers).

API key is expected to be included in all API requests to the server in a header that looks like the following:

`Authorization:  `

<aside class="notice">
You must replace <code> </code> with your personal API key.
</aside>

# Masters

## Get Common Data Masters


```shell
curl "http://qurix.io/hims/openapi/masterdetails/commondata?locid=83"
  -H "Authorization:"
```

> The above command returns JSON structured like this:

```json
[
  { 

   "all_countries":[], 
   "all_districts":[], 
   "all_states":[], 
   "all_titles":[], 
   "patient_categories":[], 
   "all_tpas":[], 
   "episode_types":[], 
   "payment_types":[], 
   "referal_sources":[], 
   "all_sponsors":[] 

  } 
]
```

This endpoint retrieves all masters.

### HTTP Request

`http://qurix.io/hims/openapi/masterdetails/commondata?locid=83`


<aside class="notice">
Areas aren't part of common data masters.
</aside>

## Get Areas

```shell
curl "http://qurix.io/hims/openapi/geo/allareas?districtid=583"
  -H "Authorization:  "
```

> The above command returns JSON structured like this:

```json
{
}
```

### HTTP Request

`http://qurix.io/hims/openapi/geo/allareas?districtid=583`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Area to retrieve

## Get RateSheetMappers(Sponsors)


```shell
curl "http://qurix.io/hims/openapi/masterdetails/ratesheetmappers?locationid=83"
  -X DELETE
  -H "Authorization:  "
```

> The above command returns JSON structured like this:

```json
[
    { 

        "patientCategoryId": 3, 

        "patientCategoryName": "Corporate", 

        "sponsorId": 73, 

        "sponsorName": "Microsoft", 

        "tpaId": null, 

        "tpaName": null, 

        "planId": 11, 

        "planName": "Microsoft Executive HealthCheck", 

        "ratesheetId": 208 

    }, 

    { 

        "patientCategoryId": 3, 

        "patientCategoryName": "Corporate", 

        "sponsorId": 74, 

        "sponsorName": "Infosys", 

        "tpaId": null, 

        "tpaName": null, 

        "planId": 9, 

        "planName": "Infosys Pre-employement Check", 

        "ratesheetId": 208 

    }, 

    { 

        "patientCategoryId": 1, 

        "patientCategoryName": "General", 

        "sponsorId": 3, 

        "sponsorName": "General", 

        "tpaId": null, 

        "tpaName": null, 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 1 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 37, 

        "sponsorName": "Bajaj Allianz General Insurance Co. Ltd", 

        "tpaId": 8, 

        "tpaName": "Good Health Insurance TPA Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 122 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 39, 

        "sponsorName": "Cholamandalam MS General Insurance Co. Ltd.", 

        "tpaId": 6, 

        "tpaName": "Family Health Plan Insurance TPA Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 123 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 44, 

        "sponsorName": "Future Generali India Insurance Co. Ltd.", 

        "tpaId": 15, 

        "tpaName": "Medi Assist Insurance TPA Private Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 124 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 46, 

        "sponsorName": "HDFC ERGO General Insurance Co.Ltd.", 

        "tpaId": 15, 

        "tpaName": "Medi Assist Insurance TPA Private Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 124 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 47, 

        "sponsorName": "ICICI LOMBARD General Insurance Co. Ltd.", 

        "tpaId": 6, 

        "tpaName": "Family Health Plan Insurance TPA Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 141 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 48, 

        "sponsorName": "IFFCO TOKIO General Insurance Co. Ltd.", 

        "tpaId": 6, 

        "tpaName": "Family Health Plan Insurance TPA Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 123 

    }, 

    { 

        "patientCategoryId": 5, 

        "patientCategoryName": "Insurance", 

        "sponsorId": 63, 

        "sponsorName": "The New India Assurance Co. Ltd", 

        "tpaId": 8, 

        "tpaName": "Good Health Insurance TPA Limited", 

        "planId": null, 

        "planName": null, 

        "ratesheetId": 125 

    } 
]    
```

### HTTP Request

`GET http://qurix.io/hims/openapi/masterdetails/ratesheetmappers?locationid=83`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Sponsor to retrieve

