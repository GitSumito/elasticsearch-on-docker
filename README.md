# healthCheck
``` curl -X GET "localhost:9200/_cat/health?v&pretty"```

# データ確認
``` curl -X GET "localhost:9200/library/_doc/1" -H "content-type: application/json"```

# データ投入
``` curl -X PUT "localhost:9200/library/_doc/1" -H 'Content-Type: application/json' -d '{"title": "hoge"}'```

# データ全取得
``` curl -X GET "localhost:9200/library/_search" -H "content-type: application/json" | jq .```

# クエリ検索
``` curl -X GET "localhost:9200/library/_search" -H "content-type: application/json" -d '{"query": {"match": {"title": "hoge"}}}' | jq .```


# 参考情報
https://qiita.com/kiyokiyo_kzsby/items/344fb2e9aead158a5545
