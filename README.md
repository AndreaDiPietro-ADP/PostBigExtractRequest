# PostBigExtractRequest
Solarium plugin for post big extract Solr query. The Solarium PHP library (v. 5.2.0) is affected by an issue: posting extract query with a lot and/or big literals may lead to HTTP 414 "Uri too long" error. So I made this plugin: when literals parameters are too long, they are removed from URI and inserted into post's multipart body.

es:
```PHP
$plugin_PostBigExtractRequest = new PostBigExtractRequest();
$plugin_PostBigExtractRequest->setCharset( 'UTF-8' );
$client->registerPlugin('postbigextractrequest', $plugin_PostBigExtractRequest);
```

Submitted to Solarium organization
([follow the issue](https://github.com/solariumphp/solarium/issues/794)) to be included or solved into future release.
