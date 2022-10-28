# Lab Report 3

## **Part 1**

```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {

    List<String> str = new ArrayList<>();

    public String handleRequest(URI url) {
        if(url.getPath().contains("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                str.add(parameters[1]);
                return String.format("The item %s has been added", parameters[1]);
            }
        } else if (url.getPath().equals("/")) {
            String items = "";
            for (String s : str) {
                items += s + ", ";
            } return String.format("The String contains: %s ", items);
        }  else if(url.getPath().contains("/search")) {
            String[] parameter = url.getQuery().split("=");
            if (parameter[0].equals("s")) {
                String items = "";
                for (String s : str) {
                    if (s.contains(parameter[1])) {
                        items += s + ", "; 
                    } 
                    else { return "Sorry, there is no item that matches your search"; } 
                } return String.format("The items that match your search are %s ", items);
            } 
        } return "404 Not Found!";
    }
}

class SearchEngine {
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

![Image](CSE15L_Images\LocalHost1.png)

In this screenshot, the main function was called to create a localhost website. Since the path is empty, the method that return string format was called to display the sentence "**The String contain:**". There are three possible outcomes in my program: it can add items if the url's path includes **"/add"**, it can search for some items that contain certain string of letters if the url's path includes **"/search"**, or it can display the list of item if the url's path includes **"/"**. If we use anything else for the path, it will return **404 Not Found!**. 

![Image](CSE15L_Images\LocalHost2.png)

In this screenshot, we use the method that check if there is a query. Because there is a query called "add", we use the "add" method to push the word "pineapple" onto the list of item. So now, if we use the earlier method, we should now see the screen displays **"The String contains: Pineapple, "**. This method knows what word to add by looking at the string of letters after the symbol "=", they are the string that will be added to the list. If we change the string, then the list at the end will contain a different item.

![Image](CSE15L_Images\LocalHost3.png)

![Image](CSE15L_Images\LocalHost4.png)

In this screenshot, we use the "search" method to find if the any string in the list contains the string of letter that we want to search for. Since we are looking the items that contains the three letters "app" in it and the words "pineapple" and "apple" both has the letters "app" in them, the program display the two words. In this method, the main arguement we want to look at is the string after the symbol "=". That symbol will tell the program what item to search for. If we were to change this to "hello", none of those words that we have added early will appear, instead the sentence **"Sorry, there is no items that matches your search"** will appear.

## **Part 2**

The two bugs I chose are: the **"reversed"** method in the ArrayExamples.java file and the **"filter"** method in the ListExamples.java file.

### Reverse method:

1) 

![Image](CSE15L_Images\FailureInducingInput1.png)

    The failure-inducing input is { 0, 1, 2}

2) 
![Image](CSE15L_Images\Symptom1.png)

    The symptom is { 0, 0, 0}

3) 

![Image](CSE15L_Images\Bug1.png)

    The code that needs to be fix is "arr[i] = newArray[arr.length - i - 1];" because it is replacing all of the elements in the input array with the elements in the empty array.

4) The buggy thing about the code is that it was trying to replace the elements from the input array with a new and empty array of integers.

![Image](CSE15L_Images\FixedCode1.png)

`I fixed the code by swapping arr with newArray on line 21`
 
### Filter method:

1) 

![Image](CSE15L_Images\FailureInducingInput2.png)

    The failure-inducing input is { hello, world, hi}

2) 
![Image](CSE15L_Images\Symptom2.png)

    The symptom is { hi, world, hello}

3) 

![Image](CSE15L_Images\Bug2.png)

    The line that needs to be fix is "result.add(0, s);" because it adding every new elements to the head of the list which reversed the order of input list.

4) The buggy thing about the code is that it was trying to add the elements from the input list to the head of the list which means the new list will become the input list in reversed.

![Image](CSE15L_Images\FixedCode2.png)

`I fixed the code by getting rid of the first argument from the result.add() method.`