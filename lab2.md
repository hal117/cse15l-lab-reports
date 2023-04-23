CSE15l Lab Report 2
---
In the past two labs, students were taught how to create and implement a String Server which takes a String and prints it on a local website. We also learned how to debug programs and fix them using jUnit tests. 

---
Part 1 Creating a Web Server called `String Server`
---
I created a new file `StringServer.java` in the wavelet folder from the lab in week 2. Using the knowledge I gained from lab, I created two classes, `Handler` and `StringServer`. The code looks like this. 

![Image](StringServercode.png)

In the code, the `handleRequest` class takes a URI object as an argument and returns a string response. If there is no path, then the code will just print "Harrison's message:" because there is no string. If there is a path and there is a string after "=", then that string will be printed. The `StringServer` class checks whether or not any arguments have been added and if not, asks for a port number. Then it starts the server and handles any new information through the `Handler` method.

The next step is to launch the server using `javac StringServer.java` and `java StringServer (insert any port number)`. You should get a page that looks like this. 
![Image](Websiteserver.png)

Now that you have your webiste up and running, we can add `/add-message?s=<string>` to the end of the url or query.
For example:
`
-http://localhost:4000/add-message?s=hello
-http://localhost:4000/add-message?s=I am Harrison
`
![Image](I am Harrison.png)
![Image](Hello.png)

In both images, the handleRequest method was called and took in the URL as an argument and satisfied the requirement of including the "add-message" strinng, so it printed out the string that came after, in both cases `Hello` and `I am Harrison`.

---
## Part 2 Debugging
---

In the third lab we focused on debugging methods using JUnit tests. We debugged, reported the symptoms, and then changed the code in order to fix it. 

For example in the ArrayExamples file
