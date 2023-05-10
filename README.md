# Hosting-a-web-server-using-GO
First, create a Handler which receives all incomming HTTP connections from browsers, HTTP clients or API requests. A handler in Go is a function with this signature :
func handler(w http.ResponseWriter, r *http.Request)
The function receives two parameters:
An http.ResponseWriter which is where you write your text/html response to.
An http.Request which contains all information about this HTTP request including things like the URL or header fields.
Registering a request handler to the default HTTP Server is as simple as this: http.HandleFunc("/", handler)
	http.ListenAndServe(":8080", nil)
  Listen for HTTP Connections
  http.ListenAndServe(":8080", nil)
