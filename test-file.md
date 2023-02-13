Code for programme
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler { 
    ArrayList<String> requests = new ArrayList<String>();

    public String handleRequest(URI url) {
        System.out.println("Path: " + url.getPath());
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                requests.add(parameters[1]);
                String listString = new String();
                for (String s : requests) {
                    listString += s + "\n";
                }
                return String.format(listString);
            }
            return "error!"; 
        }
        else {
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

**PART 1**

* Code for program 
```
import java.io.IOException;
import java.net.URI; 
import java.util.ArrayList;

class Handler implements URLHandler { 
    ArrayList<String> requests = new ArrayList<String>();

    public String handleRequest(URI url) {
        System.out.println("Path: " + url.getPath());
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                requests.add(parameters[1]);
                String listString = new String();
                for (String s : requests) {
                    listString += s + "\n";
                }
                return String.format(listString);
            }
            return "error!"; 
        }
        else {
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```
