# ES部署及插件（5.5.1版本）
## 1. 安装依赖
### JDK
略
### nodejs
> 运行elasticsearch-head需要nodejs环境

CentOS下使用yum命令安装： `yum install -y nodejs`

为nodejs安装国内包管理器： `npm install -g cnpm --registry=https://registry.npm.taobao.org`
## 2. 安装Elasticsearch
* 下载Elasticsearch
使用wget下载： `https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.5.2.tar.gz`
* 解压： `tar -xvf elasticsearch-5.5.2.tar.gz`
* 修改配置文件： `config/elasticsearch.yml`

   ```yml
   ###Cluster###
   cluster.name: elasticsearch_iciyun
   ###Node###   node.name: node_2   ###Path###
   ####索引数据存储目录####   path.data: /home/user_es/data   ####日志文件目录####
   path.logs: /home/user_es/logs
   ###NetWork###   network.host: 192.168.0.19
   ####允许跨域访问--主要为elasticsearch-head使用####   http.cors.enabled: true
   http.cors.allow-origin: "*"
   ###Discovery###
   discovery.zen.ping.unicast.hosts: ["192.168.0.87","192.168.0.43"]
   bootstrap.memory_lock: true
   ###Script--查询时使用groovy script 修改score###
   script.engine.groovy.inline.search: on
   ```
## 3.安装Elasticsearch插件
* 安装文件搜索插件： `./bin/elasticsearch-plugin install ingest-attachment`
* 安装ansj中文分词插件： `./bin/elasticsearch-plugin install https://github.com/NLPchina/elasticsearch-analysis-ansj/releases/download/v5.5.1/elasticsearch-analysis-ansj-5.5.1.0-release.zip`
* 