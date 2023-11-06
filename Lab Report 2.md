# Lab Report 2 - Servers and SSH Keys (Week 3)

## Part1
Write a web server called StringServer that supports the path and behavior described below. It should keep track of a single string that gets added to by incoming requests. The requests should look like this:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String str = "";
    static int i = 1;
    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                str += String.valueOf(i) + ". " + parameters[1] + "\n";
                i++;
            }
            return str;
        } else {
            return "404 Not Found!";
        }
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0);

        CustomServer.start(port, new Handler());
    }
}

```

**Hello**
![cd1](https://github.com/AdamMa2000/cse15l-lab-reports/blob/2e8c2dbb813af24ccaa11af896a2ef6fad9cf391/1.jpg)

**Which methods in your code are called?**
The command mainly uses the main method in StringServer, which is the entry point of the application. There is also the handle request method in Handler, which will be called when sending a request to the server. There is also the ServerStart method, which is called to start the Web server.

**What are the relevant arguments to those methods, and the values of any relevant fields of the class?**
Main in StringServer: The relevant parameter is arg, which has no relevant fields.

Handle request in Handler: URI URL, this has no related fields

There is also the ServerStart method: int port URL Handler, which also has no related fields.

**Hello
How are you**

![cd1](https://github.com/AdamMa2000/cse15l-lab-reports/blob/2e8c2dbb813af24ccaa11af896a2ef6fad9cf391/2.jpg)

**Which methods in your code are called?**
The command mainly uses the main method in StringServer, which is the entry point of the application. There is also the handle request method in Handler, which will be called when sending a request to the server. There is also the ServerStart method, which is called to start the Web server.

**What are the relevant arguments to those methods, and the values of any relevant fields of the class?**
Main in StringServer: The relevant parameter is arg, which has no relevant fields.

Handle request in Handler: URI URL, this has no related fields

There is also the ServerStart method: int port URL Handler, which also has no related fields.

---

## Part2
![cd1](https://github.com/AdamMa2000/cse15l-lab-reports/blob/9e6457ea79ab30a7c872850faab71d0d53ff37e5/111.jpg)

---

## Part3

I think what I learned in the second week and was very surprised was the startup of the server. I learned that the command '$javac Server.java NumberServer.java' helped me generate the corresponding .class file. The command ‘$ java NumberServer 4000’ helps me start the virtual machine JVM and then run the Java class named NumberServer. 4000 is the port number of the server. After these two commands were successfully executed, I received a "Server Started!" message that made me very excited. This indicated that I had successfully connected to the server and my client could communicate with the server.
