## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.

```Protocol - either http or https. Just establishes which protocol is being used.
```
```Domain - a name that directs to the correct server address.
```
```Port - a specific program reference.
```
```Path - the specific folder location being directed to.
```
```Query - (optional) if there is some input on the page that needs to be duplicated. Such as a search.
```
```Link - a specific link on the HTML to direct to.
```

* Name the pieces of the following urls:
	* `https://www.google.com/` ```protocol/domain```
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367` ```protocol/domain/path```
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy` ```protocol/domain/port/path/query/link```
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error` ```protocol/domain/path/link```
* Can a server use more than 1 port?
```I don't believe so
```
* Why is https different than http?
```Https uses a secured connection
```
* How does a server interpret the following url's query parameter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

```It will only pull up the puppies, Fido, Max, and Moxie.
```

__HTTP Request/Response__

* Name at least 4 http verbs
```GET, POST, PUT, DELETE
```
* What is each verb useful for in your own words
```GET pulls down the requested information, usually the html to be rendered.
```POST allows new data to be uploaded.
```PUT allows for existing data to be modified.
```and DELETE removes data.
```
* What does idempotent mean?
```Looking at a resource without changing it.
```
* Name the 5 http status code ranges.  What are they used for in general?
```500: an error
```400: a resource that doesn't exist, no error server side.
```300: a redirection
```200: success
```100: provisional, okay for now.
```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
``Redirects to Google.
```
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept ``Both``
	* Content-type ``Both``
	* User-agent ``Request``
	* Set-cookies ``Response``
	* Cache-control ``Response``
	* Cookie ``Request``
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

```This is a response, because it has an HTTP status code
```

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```

```This is a request, because it uses the DELETE keyword
```

__JSON__

* Describe what JSON is.  What is it used for.

```JSON uses javascript objects as a standard structure for data.
```

* Convert the following map into a javascript object then console log the age.

```
var gitHub = { "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
console.log(gitHub.age);

```
* Convert the following to a javascript object.  Console log each company name.

```
var companies = { "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}

for(var i=0; i<companies.Companies.length; i++) {
  console.log(companies.Companies[i].company);
}

```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};

var object = JSON.stringify(myObj);
console.log(object);

```
__MISC__

* Describe what DNS is.

```It assigns a site's IP address a name that's easier to remember than a bunch of numbers
```

* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).

```-v provides more "verbose" information
	 -X lets you use a different keyword besides the default (GET) when sending an HTTP request.
```

* What is TCP/IP?  How does it interact with HTTP?

```TCP/IP makes sure packets get sent, to the right place, in one piece. TCP/IP is the foundation that HTTP moves across.
```

* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?

```I believe TCP is responsible for making network packets of the data.
```
