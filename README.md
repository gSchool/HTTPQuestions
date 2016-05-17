## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
* Name the pieces of the following urls:
	* `https://www.google.com/`-->protocol, domain
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367` -->protocol, domain, path
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy` -->protocol, domain, port, path, query string, anchor tag
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error` -->protocol, domain, path, anchor tag
* Can a server use more than 1 port?
```Yes```
* Why is https different than http?
```it is the secure version of http```
* How does a server interpret the following url's query paramter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

```I think that an object is created, more specifically, perhaps, an array```

__HTTP Request/Response__

* Name at least 4 http verbs
```GET, POST, PUT, DELETE```
* What is each verb useful for in your own words
```GET is used to grab or access some resource; POST is used to upload something; PUT is used to modify some data that already exists; and DELETE is used to remove some data.```
* What does idempotent mean?
``` It describes an element or value that is unchanged over multiple requests. I think. ```
* Name the 5 http status code ranges.  What are they used for in general?
``` 5xx: an error has occurred. 4xx: No error on the server side, but what was requested is not deliverable. 3xx: what was requested exists somewhere else. 2xx: What was requested was delivered in some form. 1xx: What was requested is in the process of being delivered. ```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
``` 301 means the page has been moved, and the browser should redirect the user```
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept ```both```
	* Content-type ```both```
	* User-agent ```request```
	* Set-cookies ```response```
	* Cache-control ```both```
	* Cookie ```request```
	

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
``` ```Above is a response; listed first are response fields, and then the html of the requested doc```

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
``` ```this is a request; the request type is given (delete), the url of the target site, the file format that is accepted, etc.```

__JSON__

* Describe what JSON is.  What is it used for.
``` Javascript Object Notation; it is used for exchanging data over the web```
* Convert the following map into a javascript object then console log the age.

```
var company = JSON.parse('{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}')
console.log(company.age);

```
* Convert the following to a javascript object.  Console log each company name.

```
var companies= JSON.parse('{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}')

for (var company in companies) {
	console.log(company);
};

```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};

var myObjJSON = JSON.stringify(myObj);
console.log(myObjJSON.stringify);

```
__MISC__

* Describe what DNS is.
```stands for Domain Name Service, and it controls the translating of IP addresses to human-readable domain names"```

* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
``` I think that the -v flag returns more information on the GET request than normal. According to explainshell.com, the -X flag "Specifies  a  custom  request  method to use when communicating with the HTTP server. The specified request will be used instead of the method otherwise used (which defaults to GET)." ```

* What is TCP/IP?  How does it interact with HTTP?
``` TCP stands for 'transmission control protocol', and it ensures that data is communicated between servers quickly and reliably. From my understanding, TCP controls the transmission of data between servers (underground, in a metaphorical sense), while HTTP works on the surface to bring the data to the web application. ```
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
``` No, the TCP is responsible for breaking the data into smaller chunks ```
