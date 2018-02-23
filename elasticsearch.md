
# Usage

## Total number of docs for a certain index

``` bash
curl localhost:9200/_stats?pretty | jq .indices.<index>.total.docs.count
```