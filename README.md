# CloseableHttpClient
在生成HttpClient的时候，指定相应的 SSLSocketFactory，之后，使用这个HttpClient发送的GET请求和POST请求就自动地附加上了证书信息

如果我们只需要忽略掉对服务器端证书的验证，而不需要发送客户端证书信息,在构建SSLContext的时候，只需要 loadTrustMaterial() 不需要 loadKeyMaterial()
