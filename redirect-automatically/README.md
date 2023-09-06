# Redirect Automatically 

When the `Redirect Automatically` option is enabled, JMeter will automatically handle HTTP redirects (status code 3xx) and follow them without any additional configuration or intervention.

### Example :

Suppose you have an HTTP Request that initially requests a URL `https://example.com/page1` and the server responds with a redirect status code, such as `302 Found`, along with a new URL `https://example.com/page2`. If `Redirect Automatically`  is enabled, JMeter will automatically send another request to `https://example.com/page2` without any manual intervention.

##### Use Case : Enabling `Redirect Automatically`  is suitable when you want JMeter to handle redirects seamlessly, without explicitly adding additional requests for each redirect in your test plan.


