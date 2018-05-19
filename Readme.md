# SugarCRM on Docker

SugarCRM の動作環境を Dokcer で構築します。

- Apache 2.4
- PHP 7.1
- MySQL 5.7
- ElasticSearch 1.7

## 使い方

```
git clone https://github.com/rythgs/sugar-docker-example.git
cd sugar-docker-example
docker-compose up -d
```

`./src` が DocumentRoot になります。  
Sugar のソースはここに起きましょう。