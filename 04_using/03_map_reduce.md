!SLIDE smbullets
### Using Riak
## Map Reduce

- Querying Riak is performed by map/reduce processing
- More closely resembles Hadoop than CouchDB
- Jobs submitted via HTTP POST to ‘/mapred’, described in **JSON**
- Phases: **Map** -> (**Link**) -> **Reduce**

!SLIDE 
### Using Riak
## Map Reduce

    # 'goog' bucket
    {
      "Adj Close":"541.30",
      "Close":"541.30",
      "Date":"2010-02-16",
      "High":"544.13",
      "Low":"534.30",
      "Open":"536.87",
      "Volume":"3654400"
    }


!SLIDE
### Using Riak
## Map Reduce

    {
      "inputs": [
        ["goog","2010-01-04"],
        ["goog","2010-01-05"],
        ["goog","2010-01-06"],
        ["goog","2010-01-07"],
        ["goog","2010-01-08"]
      ],
      "query": [
        {
          "map": {
            "language": "javascript",
            "source": "function(value,keyData,arg){ var data = Riak.mapValuesJson(value)[0]; return [data.High];}",
            "keep": true
          }
        },
        {
          "reduce": {
            "language": "javascript",
            "name": "Riak.reduceMax"
          }
        }
      ]
    }

