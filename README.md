# event-stream-processor
** EXPERIMENTAL** Event Stream Processor for Event Stream (logs, audits, errors, trace, etc)

## 1. Pre-requisites

### 1.1 Elasticsearch

Ensure that you have created the `mojatemplate` based on the following config: [template](./config/template-mojaloop.json).

#### 1.1.1 Create Template
 ```curl
 curl -X PUT "http://elasticsearch:9200/_template/mojatemplate?pretty" -H 'Content-Type: application/json' -d @config/template-mojaloop.json'
 ```

#### 1.1.2 Delete Template
_Note: only needed if you need to remove the template_
 ```curl
 curl -X DELETE "http://elasticsearch:9200/_template/mojatemplate"
 ```
 
 #### 1.1.3 Get Template
 _Note: useful for debugging template issues_
 ```curl
 curl -X GET "http://elasticsearch:9200/_template/mojatemplate"
 ```
 
