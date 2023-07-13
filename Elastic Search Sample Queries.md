Query for a term match:


GET /my_index/_search
{
  "query": {
    "term": {
      "field_name": "search_term"
    }
  }
}
Query for a match phrase:


GET /my_index/_search
{
  "query": {
    "match_phrase": {
      "field_name": "search phrase"
    }
  }
}
Query for a range of values:


GET /my_index/_search
{
  "query": {
    "range": {
      "field_name": {
        "gte": 10,
        "lte": 100
      }
    }
  }
}
Query for a fuzzy search:


GET /my_index/_search
{
  "query": {
    "fuzzy": {
      "field_name": {
        "value": "search_term",
        "fuzziness": "AUTO"
      }
    }
  }
}
Query for a boolean combination:


GET /my_index/_search
{
  "query": {
    "bool": {
      "must": [
        { "term": { "field_name1": "value1" } },
        { "term": { "field_name2": "value2" } }
      ],
      "must_not": [
        { "range": { "field_name3": { "gte": 10 } } }
      ],
      "should": [
        { "term": { "field_name4": "value4" } }
      ]
    }
  }
}
Query for aggregations:


GET /my_index/_search
{
  "aggs": {
    "agg_name": {
      "terms": {
        "field": "field_name",
        "size": 10
      }
    }
  }
}
