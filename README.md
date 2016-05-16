## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
* Name the pieces of the following urls:
	* `https://www.google.com/`
	```
		protocol and domain
	```
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
	```
		protocol, domain, path
	```
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	```
		protocol, domain, port, path, queries
	```
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
	```
		protocol, domain, path
	```
* Can a server use more than 1 port?
```
		sure, why not (I actually am not sure)
```
* Why is https different than http?
```
		https is http over a secure socket
```
* How does a server interpret the following url's query parameter.  What data structure does it create on the server?
```
		JSON, creates a JSON object
```


```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

__HTTP Request/Response__

* Name at least 4 http verbs
```
		get, post, push, delete,
```
* What is each verb useful for in your own words
```
		get is basically requesting the url you pass it; post pushes JSON changes to the url; push ... not sure; delete allows you to delete JSON values from the url you pass it
```
* What does idempotent mean?
```
		complicated algebraic term meaning roughly that the value remains the same if operated on itself
```
* Name the 5 http status code ranges.  What are they used for in general?
```
		Information (1xx), success(2xx), redirection(3xx), client error(4xx), server error(5xx); information for the user and/or browser
```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
```
		301 is a redirect, so the browser should follow it
```
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept ```requests```
	* Content-type ```both```
	* User-agent ```requests```
	* Set-cookies ```responses```
	* Cache-control ```both```
	* Cookie ```both```
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
* Convert the following map into a javascript object then console log the age.

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
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
* What is TCP/IP?  How does it interact with HTTP?
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
