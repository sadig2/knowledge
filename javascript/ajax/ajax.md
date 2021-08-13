onreadystatechange Specifies an event handling function to be called 

whenever the readyState property of anobject changes.

readyState An integer property that reports on the status of a request. It 

can have any of these values: 0 =Uninitialized, 1 = Loading, 2 = Loaded, 3 = Interactive, and 4 = Completed.

responseText The data returned by the server in text format.

responseXML The data returned by the server in XML format.

status The HTTP status code returned by the server.

statusText The HTTP status text returned by the server.



abort() Aborts the current request.

getAllResponseHeaders() Returns all headers as a string.

getResponseHeader(param) Returns the value of param as a string.

open('method', 'url', 'asynch') Specifies the HTTP method to use ( GET or POST ), the target URL, and
whether the request should be handled asynchronously ( true or
false ).

send(data) Sends data to the target server using the specified HTTP method.

setRequestHeader('param', 'value') Sets a header with a parameter/value pair.


