# Description


# Configuration

# Usage

```json
"request_statistics": {
    "headers": {
        "user-agent": "curl/7.19.7 (x86_64-redhat-linux-gnu) libcurl/7.19.7 NSS/3.14.0.0 zlib/1.2.3 libidn/1.18 libssh2/1.4.2",
        "clientid": "cada@birdstep.com",
        "accept": "*/*",
        "host": "localhost:8101"
    },
      "uri": "/credentials/wifi?requestor=android&wispr=1",
      "session_id": "6b2eff3d258f1b48780df8c214b751de"
    }
}
```

## Select all

``` bash    
jq '.'
```    

## Select in nested json structure

``` bash
jq '.request_statistics
```

Results in:  
```json
"headers": {
    "user-agent": "curl/7.19.7 (x86_64-redhat-linux-gnu) libcurl/7.19.7 NSS/3.14.0.0 zlib/1.2.3 libidn/1.18 libssh2/1.4.2",
    "clientid": "cada@birdstep.com",
    "accept": "*/*",
    "host": "localhost:8101"
    },
        "uri": "/credentials/wifi?requestor=android&wispr=1",
        "session_id": "6b2eff3d258f1b48780df8c214b751de"
}
```


## Select specific value in nested json structure

```
	jq '.request_statistics.headers.host'
    output
    "localhost:8101"
```


## Use together with tail

```
tail -f | jq .
```

### Hide null values
When using jq to grep from log files the tool will by default show lines with no matches for the query. To remove empty lines use the following syntax

``` bash
jq '.request_statistics.headers.host //empty'
```

Note that the query needs to be enclosed by quotation marks.

## Compactify output

  * By default jq returns prettified multi line json content. To get compactified content use the following switch.
  :-c


## Remove quotes from result

When piping the result from jq to other tools it is handy to be able to strip quotes from the reply use the below switch.

```
--raw-output / -r
```

## Inbox
### Filter structlog based on log-level
```bash
/var/log/birdstep/reverser/reverser.log | jq '. | select(.level=="OTHER")'
```
