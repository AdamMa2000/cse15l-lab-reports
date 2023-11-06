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

1. Hello
1.jpg

