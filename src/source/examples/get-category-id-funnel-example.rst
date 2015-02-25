.. code-block :: javascript

    GET /category/{id}/funnel?cpc=50
    Accept: application/sellside.funnel-v1+json, application/json

    200 OK
    Content-Type: application/sellside.funnel-v1+json

    {
      "cpc": 50,
      "pageNumber": 1,
      "averageClicks": 100,
      "averageCpc": 0,
      "averageImpressions": 300,
      "averageUrlClicks": 400,
      "ctr": 3.5,
      "urlCtr": 1.2,
      "maxCpc": 250,
    }
