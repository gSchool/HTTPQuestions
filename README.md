## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
The URL is composed by:

1. protocol: it declares how the web browser should communicate with the web server when sending a web page or document. The most common one is "HTTP".

2. Subdomain: is a subdivision of the main domain name.

3. Domain name: is a unique reference that identifies a website on the internet.

4. Port: is a end point of communication in an operating system. It allows to complete the destination or origination address of a communication session.

5. Path: is the file or directory on the web server. Specifies a unique location in a file system.


6. Query: is found in the URL represented by a question mark followed by one or more parameters.

7. Fragment: is an internal page reference, sometimes called a named anchor. It usually appears at the end of the URL and begins with a hash (#) and it referes to a section within the page.

8. Top Level Domain (TLD): is the last segment of the domain name. The TLD is the letters immediately following the final dot in an Internet address and identifies something about the website associated with it, such as its purpose, the organization that owns it or the geographical area where it originates.

9. Second Level Domain (SLD): A second-level domain (SLD) is the portion of the domain name that is located immediately to the left of the dot and domain name extension.



* Name the pieces of the following urls:
	* `https://www.google.com/`

	1. https: is the protocol.
	2. google.com: is the hostname; as well as the domain name;
	3. google.com: is the Second level Domain name.
	4. .com is the top level domain;

	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`

	1. https: is the protocol.
	2. workbook.galvanize.com: is the hostname;
	3. workbook: is the Subdomain;
	4. galvanize.com is the domain name;
	5. /cohorts/41/learning_experiences/367 is the path of where the file can be found.


	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
	1. http: is the protocol;
	2. locahost: is the host;
	3. /animals...: is the path;
	4. ?onlycute=1&size=medium#firstpuppy: are two parameters; separated by the (&);
	5. #firstpuppy: is the fragment or the named anchor;


	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
	1. http: is the protocol;
	2. en.wikipedia.org: is the hostname;
	3. en: is the subdomain;
	4. wikipedia.org: is the domain name;
	5. /wiki/List...: is the path;
	6. #4xx_Client_Error: is the fragment or the named anchor;



* Can a server use more than 1 port?
no,
* Why is https different than http?
Because the https uses an extra security layer called Secure Socket Layer (SSL), to transport data safely.


* How does a server interpret the following url's query parameter.  What data structure does it create on the server?

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```
q=url

__HTTP Request/Response__

* Name at least 4 http verbs
1. Post
2. Get
3. Put
4. Delete


* What is each verb useful for in your own words

1. Post: Creates; is used to request that the server accept the data as a new subordinate of the resource.

2. Get: Read; is used to read or retrieve the representation of a resource and data and no change it.

3. Put: Update/Replace; updates capabilities, putting to a known resource URI with the request body containing the newly updated representation of the original resource.


5. Delete: is used to delete a resource identified by the request URI.

* What does idempotent mean?
 An idempotent operation is one that has no additional effect if it is called more than once with the same input parameters.

* Name the 5 http status code ranges.  What are they used for in general?

1. Informational 1xx: indicates a provisional response, consisting only of the Status-Line and optional headers, and is terminated by an empty line. There are no required headers for this class of status code.

2. Successful 2xx: this class of status code indicates that the client's request was Successfully received, understood and accepted.

3. Redirection 3xx: this class of status code indicates that further action needs to be taken by the user agent in order to fulfill the request.

4. Client error 4xx: The 4xx class of status code is intended for cases in which the client seems to have erred. Except when the responding to a head request, the server should include an entity containing an explanation of the error situation, and whether it is a temporary or permanent condition.

5. Server Error 5xx: Response status codes beginning with the digit "5" indicate cases in which the server is aware that it has erred or is incapable of performing the request. Except when responding to a HEAD request, the server SHOULD include an entity containing an explanation of the error situation, and whether it is a temporary or permanent condition. User agents SHOULD display any included entity to the user. These response codes are applicable to any request method.

* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?

The browser should automatically redirect to the new location of the requested URI, if given. The new permanent URI SHOULD be given by the Location field in the response.

* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept: Response;

	* Content-type:both;

	* User-agent: Request;

	* Set-cookies: Response;

	* Cache-control: both;

	* Cookie: request

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

This is a response that was Successful, Because in the first line of the code above of the html code there is a "200 OK" code that indicates that the request has succeeded and that's why we received as an answer the html with the information requested.

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```
this is a response with the "Delete" code that indicates that The requested resource is no longer available at the server and no forwarding address is known. This condition is expected to be considered permanent.

__JSON__

* Describe what JSON is.  What is it used for.
JSON is a javascript Object Notation and is use as a data interchange format.

* Convert the following map into a javascript object then console log the age.

```
{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}


var myArray= JSON.parse('{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}');


	console.log(myArray.age);



```
* Convert the following to a javascript object.  Console log each company name.

```
{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}

//////answer/////

var myArray= JSON.stringify({"Companies":[
			{ "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]});

var myObj= JSON.parse(myArray);

var comp= myObj.Companies

for(var i=0; i < comp.length; i++){
	console.log(comp[i].company);
}
/////////////


```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};


//////answer////

var myObj = JSON.stringify({
  company: "Galvanize",
  age: 3,
  categories: "Education"
});

console.log(myObj)
/////////////



```
__MISC__

* Describe what DNS is.
Domain Name Servers (DNS) are the Internet's equivalent of a phone book. They maintain a directory of domain names and translate them to Internet Protocol (IP) addresses. This is necessary because, although domain names are easy for people to remember, computers or machines, access websites based on IP addresses.

* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).

-v: Useful for debugging and seeing what's going on "under the  hood".

-X: request <command>  (HTTP) Specifies a custom request method to use when communicating  with the HTTP server.  The specified request method will be used instead of the method otherwise  used  (which  defaults  to GET).  

* What is TCP/IP?  How does it interact with HTTP?
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
