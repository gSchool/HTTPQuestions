## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
* Name the pieces of the following urls:
	* `https://www.google.com/`
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
* Can a server use more than 1 port?
* Why is https different than http?
* How does a server interpret the following url's query parameter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

__HTTP Request/Response__

* Name at least 4 http verbs
	Get, Post, Update, Delete
* What is each verb useful for in your own words
	Get info from server
	Put information on the server
	Change information on the server
	Delete information on the server
* What does idempotent mean?
		denoting an element of a set that is unchanged in value when multiplied or otherwise operated on by itself.
* Name the 5 http status code ranges.  What are they used for in general?
	Accept
	Content-type
	Cookie
	User Agent
	Cache-control

* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
		It autamatically redirects into the new URL location
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept - requests
	* Content-type - both
	* User-agent - request
	* Set-cookies - both
	* Cache-control - both
	* Cookie - both
* Is the following a http request or response?  How do you know for each?

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: *
Vary: Accept
Content-Type: text/html; charset=utf-8
Content-Length: 722
ETag: W/"2d2-Wu0We9N5g35FXWY+gOATLA"
Date: Tue, 08 Mar 2016 20:37:11 GMT
Connection: keep-alive

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/style.css">
    <title>Student Roster</title>
  </head>
  <body>
    <main>
      <h1>Student Roster</h1>

        <section>
          <h3>Daenerys Targaryen</h3>
          <span>Student Id: nys8fbohl</span>
          <h4>Hobby: Motherhood</h4>
          <img src="https://i.imgur.com/KlycRG5.jpg" alt="Daenerys Targaryen" />
        </section>

        <section>
          <h3>Tyrion Lannister</h3>
          <span>Student Id: njehukbohe</span>
          <h4>Hobby: Traveling</h4>
          <img src="https://i.imgur.com/fFMusdC.png" alt="Tyrion Lannister" />
        </section>

    </main>
  </body>
</html>
```

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```

__JSON__

* Describe what JSON is.  What is it used for.
	javascript Object Notation. Used to structure data
* Convert the following map into a javascript object then console log the age.
	github = {
		 "company" : "Github",
		 "age": 7,
		 "categories" : "Services,Internet,Software"
	 }
	 console.log(github.age)
```
{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
```
* Convert the following to a javascript object.  Console log each company name.

```
{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}
```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};
```
__MISC__

* Describe what DNS is.
Domain Name System
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
-v, --verbose
						 <!-- -v Be  more  verbose/talkative  during  the  operation.  Useful for
						debugging and seeing what's going on "under the  hood".  A  line
						starting  with  '>'  means "header data" sent by curl, '<' means
						"header data" received by curl that is hidden in  normal  cases,
						and  a  line starting with '*' means additional info provided by
						curl.

						Note that if you only want  HTTP  headers  in  the  output,  -i,
						--include might be the option you're looking for.

						If  you think this option still doesn't give you enough details,
						consider using --trace or --trace-ascii instead.

						This option overrides previous uses of --trace-ascii or --trace.

						Use -s, --silent to make curl quiet.

              -x Use the specified proxy.

              The  proxy  string can be specified with a protocol:// prefix to
              specify alternative proxy protocols. Use socks4://,  socks4a://,
              socks5:// or socks5h:// to request the specific SOCKS version to
              be used. No protocol specified, http:// and all others  will  be
              treated as HTTP proxies. (The protocol support was added in curl
              7.21.7)

              If the port number is not specified in the proxy string,  it  is
              assumed to be 1080.

              This  option  overrides  existing environment variables that set
              the proxy to use. If there's an environment variable  setting  a
              proxy, you can set proxy to "" to override it.

              All operations that are performed over an HTTP proxy will trans-
              parently be converted to HTTP. It means  that  certain  protocol
              specific operations might not be available. This is not the case
              if you can tunnel through the proxy, as one with the -p, --prox-
              ytunnel option.
							 -->


* What is TCP/IP?  How does it interact with HTTP?
		TCP/IP (Transmission Control Protocol/Internet Protocol) is the basic communication language or protocol of the Internet. TCP/IP is the how things are supposed to communicate between one another, HTTP is data sent over the TCP/IP protocol to be viewed in a browser.
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
		TCP is responsible for breaking data down into IP packets before they are sent, and for assembling the packets when they arrive.
