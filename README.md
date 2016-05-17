## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
```
Protocol - that is the http or https beginning of the url. It is the starting part of talking to the DNS to get the address for the website.
Domain - It is the website or html address of what you want to display on your screen.
Port - It is the location on your computer that will decipher the file code.
Path - It is the file path where the content is located that your are wanting to access.
Query String - It is the part of the files that you want to display.
Anchor Tag - It is the part in the html file that you are starting at.
```
* Name the pieces of the following urls:
	* `https://www.google.com/`
	```Protocol and Domain```
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
	```Protocol, Domain, and Path```
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	```Protocol, Domain, Port, Path, Query String, and Anchor Tag```
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
	```Protocol, Domain, Path, and Anchor Tag```
* Can a server use more than 1 port?
	```yes```
* Why is https different than http?
	```More secure```
* How does a server interpret the following url's query paramter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```
```all puppies that have a value of fido,max, and moxie```

__HTTP Request/Response__

* Name at least 4 http verbs
```Get, Post, Put, Delete```
* What is each verb useful for in your own words
```
* What does idempotent mean?
* Name the 5 http status code ranges.  What are they used for in general?
```1xx - everything is going well, just not done yet```
```2xx - everything went well```
```3xx - it knows what you wanted but it wants to send you to a different location to get it```
```4xx - something went wrong, but it doesn't know what```
```5xx - you can not access the information```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
```redirects you to https://www.google.com/```
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept
	* Content-type
	* User-agent
	* Set-cookies
	* Cache-control
	* Cookie
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
```var Companies = {
	 company: "GitHub",
	 age: 7,
	 categories: Services, Internet, Software
 };```

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
```
__MISC__

* Describe what DNS is.
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
* What is TCP/IP?  How does it interact with HTTP?
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
