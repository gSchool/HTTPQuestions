## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
```
Protocol: the connection in which you access the webpage?
The port: typically 80. dont remember much else
The path: the file path that of the website.
the domain: the URL which represents an IP address
the query: What is being searched for
anchor tag: link to specific part of page

```
* Name the pieces of the following urls:
	* `https://www.google.com/`
	```
	Protocol - domain -port
	```
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
	```
protocol - domain - port - path
	```
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	```
protocol - domain - port - path - query - anchor?
	```
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
	```
	protocol - domain - port - path - anchor?
	```
* Can a server use more than 1 port?
```
no
```
* Why is https different than http?
```
https is more secure
```
* How does a server interpret the following url's query parameter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```
```
3 separate searches for a puppy named fido, max, and moxie
```

__HTTP Request/Response__

* Name at least 4 http verbs
```
get, post, delete, put
```
* What is each verb useful for in your own words
```
getting information from the server, adding information to the server, removing information from the server, updating information on a server
```
* What does idempotent mean?
* Name the 5 http status code ranges.  What are they used for in general?
```
1XX Wait
2XX Things went mostly right
3XX In the wrong place
4XX Something went wrong, but it wasn't our fault
5XX Some type of error
```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept  ```requests```
	* Content-type ```both```
	* User-agent ```requests```
	* Set-cookies ```both```
	* Cache-control ```both```
	* Cookie ```response```
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
response, because it is giving me information
```
```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```
```
request. I am asking to delete it
```

__JSON__

* Describe what JSON is.  What is it used for.
```
javascript Object Notation. used to make objects usable in other applications?
```
* Convert the following map into a javascript object then console log the age.

```
var Obj = { "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
console.log(Obj.age);
```
* Convert the following to a javascript object.  Console log each company name.

```
var Obj2 = { "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}
for(var i = 0; i<Obj2.Companies.length; i++){
	console.log(Obj2.Companies[i].company);
}
```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};
console.log(JSON.stringify(myObj));
```
__MISC__

* Describe what DNS is.
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
* What is TCP/IP?  How does it interact with HTTP?
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
