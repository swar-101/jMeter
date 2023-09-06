# HTTP Request 

![[jmeter-http-request-sampler.png]]


The JMeter HTTP Request is a sampler that lets you send an HTTP/HTTPS request to a web server for load testing. 

#### Web Server :

1. Protocol \[http]\  : This field allows you to specify the protocol to be used for the request either "http://" or "https://".

2. Server Name or IP : Enter the hostname or IP address of the target web server where the request will be sent.

3. Port Number : Set the port number that the web server is listening on. The default port for HTTP is 80, while the default port for HTTPS is 443. You can specify a different port number if required. For e.g. your app may have a dedicated port number 8080, in this case the port number of the web server will be 8080.


#### HTTP Request :

1. HTTP request method : Choose the HTTP method for the request, such as GET, POST, PUT, DELETE, HEAD, OPTIONS, etc.

2. Path : Specify the path of the resources on the server that you want to request. It includes the URI path and any query parameters.

3. Content Encoding : This fields allows you to specify the encoding format for the request content. Common options are "gzip" or "deflate" for compression. Leave it bank for no content encoding. 

>	*What is content encoding?*
>	*Content encoding is the process of compressing or encoding the content of a web page or HTTP response before transmitting it over the network. It involves reducing the size of the content by applying compression algorithms which can significantly improve the performance and efficiency of data transfer. [read more](content-encoding/README)*

4. Redirect Automatically : If enabled, JMeter will automatically follow HTTP redirects (*status codes 3xx*) and retrieve the content from the redirected URL.

> *If the above option is enabled JMeter will automatically handle HTTP redirects (status code 3xx) and follow them without any additional configuration or intervention.
> [Example](redirect-automatically/README)*

5. Follow Redirects : If enabled, JMeter will track and redirect subsequent requests to the new URLs provided in the redirect responses.

> *The `Follow Redirects` option allows JMeter to track and follow HTTP redirects (status codes 3xx) by automatically creating additional requests for each redirect.                                               
>  [Example](follow-redirects/README)*

6. Use KeepAlive : If enabled, the HTTP connection will be kept alive after the request, allowing subsequent requests to reuse the same connection if possible.

7. Use multipart/form-data : If enabled, JMeter will send POST requests using the `multipart/form-data` content type. This is typically used for file uploads.

8. Browser-compatible headers : If enabled, JMeter will include additional headers to make the request more compatible with various web browsers.

9. Parameters : This section allows you to add parameters (query string or form data) to the request.
	- Name : Specify the parameter name.
	- Value : Enter the value for the parameter.
	- URL Encode? : If enabled the will be URL-encoded.
	- Content-type : Specify the content type for the parameter value.
	- Include Equals? : If enabled, an equals sign (=) will be appended to the parameter name.

These fields provide flexibility and configurability for sending HTTP requests in JMeter. By appropriately setting these values, you can simulate various scenarios and interactions with the web server during performance or load testing.


