Start
---
`elasticsearch -f -D es.config=/usr/local/opt/elasticsearch/config/elasticsearch.yml`

Insert fra .json fil
--
`curl -XPOST 'http://localhost:9200/twitter/tweet' -d @file.json`


lag en mapping
---
`curl -XDELETE 'http://localhost:9200/ansatte'`

`curl -XPOST 'http://localhost:9200/ansatte/ansatt/_mapping' -d @mapper.json`

`curl -XPOST 'http://localhost:9200/ansatte'`

`curl -XPOST 'http://localhost:9200/ansatte/ansatt/_search?pretty=true' -d @ansatt-geo-soek-gjennomsnitt-trh.json`
