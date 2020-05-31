# PostBigExtractRequest
Solarium plugin for post big extract Solr query. The Solarium PHP library (v. 5.2.0) is affected by an issue: posting extract query with a lot and/or big literals may lead to HTTP 414 "Uri too long" error. So I made this plugin: when literals parameters are too long, they are removed from URI and inserted into post's multipart body.
