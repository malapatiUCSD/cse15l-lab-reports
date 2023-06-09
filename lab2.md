<h1>LAB REPORT 2</h1>
<h2>Part 1: StringServer</h2>
<h3>StringServer Code</h3>

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    StringBuilder sbuild = new StringBuilder();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return sbuild.toString();
        } 
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    sbuild.append(parameters[1]).append("\n");
                    return sbuild.toString();
                }
            }
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

<h3>Step 1 Screenshot</h3>


![Image](lab2image1.png)

In the screenshot above (Step 1), there is a server request which calls the method `handleRequest` from the `Handler` class. When you use the arguments and field values of `localhost:4001` and `/add-message?s=Hello` together, it's like sending a special request to the server. This request asks the server to add the word "Hello" to a specific place. The `localhost:4001` part tells the server where to send the request. And the `/add-message` part is the server's way of knowing that it should handle the request to add a message. Lastly, the `?s=Hello` part carries the important information, which is the word "Hello" that you want to be added by the server. In the handler class implementation, the `StringBuilder` field called `sbuild` is the only field that affects the server output. When the `Handler` class is called, it adds the string given to `sbuild`  ("Hello") with a `\n` after and this is how it modifies the server output.

<h3>Step 2 Screenshot</h3>


![Image](lab2image2.png)

In the screenshot above (Step 2), there is another server request which calls the method `handleRequest` from the `Handler` class. When you use the arguments and field values of `localhost:4001` and `/add-message?s=How%20are%20you` together, it requests the server to add the phrase "How are you" to the output. The `%20` is used to bridge the spaces between the "How are you" and inform the server that there should be a space. Again, the `localhost:4001` part tells the server where to send the request. And the `/add-message` part is the server's way of knowing that it should handle the request to add a message. Lastly, the `?s=How%20are%20you` part carries the output information, which is the phrase "How are you". In the handler class implementation, the `StringBuilder` field called `sbuild` affects the server output. When the `Handler` class is called, it adds the string given to `sbuild` ("How are you") with a `\n` after.



<h2>Part 2: Lab 3 Bug</h2>
<h3>Failure Inducing Input</h3>


```
@Test
public void failureTestReversed() {
  int[] input1 = {1,11,111};
  assertArrayEquals(new int[]{111,11,1}, ArrayExamples.reversed(input1));
}
```

A failure inducing input for the Reversed method from ArrayExamples.java in the JUnit Test above would be `int[] input1 = {1,11,111};` as it returns `{0,0,0}` instead of `{111,11,1}`.
<h4>Failure Symptom</h4>
![Image](lab2image3.png)


<h3>Non-Failure Inducing Input</h3>


```
@Test
public void nonFailureTestReversed() {
  int[] input1 = {0,0,0};
  assertArrayEquals(new int[]{0,0,0}, ArrayExamples.reversed(input1));
}
```

A non-failure inducing input for the Reversed method from ArrayExamples.java in the JUnit Test above would be `int[] input1 = {0,0,0};` as it returns `{0,0,0}` as it precisely should.
<h4>Non-Failure Symptom</h4>
![Image](lab2image4.png)


<h3>The Bug</h3>

<h4>Before</h4>
```
// Incorrectly returns a *new* array with all the elements of the input array in reversed order
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```
<h4>After</h4>
```
// Correctly returns a *new* array with all the elements of the input array in reversed order
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    newArray[i] = arr[arr.length - i - 1];
  }
  return newArray;
}
```
<h4>Explanation</h4>
The problem with the orginal Reversed method from ArrayExamples.java is that it creates a new array "newArray" of the same length as "arr" but then it iterates through the "newArray" which is instantiated by 0's and then copies them back to "arr", making the "arr" array all 0's and then return the "arr" array of 0's. That is why the input `{0,0,0}` works as it leads right back to 0's `{0,0,0}`, but the input `{1,11,111}` doesn't work as it returns `{0,0,0}` instead of `{111,11,1}`. In order to fix this issue we must iterate through the "arr" array instead and copy over the values in reverse order to the "newArray" array and then return the "newArray" with the actual reversed values of "arr". I fixed this by swapping the `arr[i] = newArray[arr.length - i - 1];` to `newArray[i] = arr[arr.length - i - 1];`, essentially swapping the "newArray" and "arr"'s places. Lastly, I changed the `return arr;` to `return newArray;` in order to return the new reversed array instead of the old one. That is the bug and how I fixed it. 

<h4>Fixed Bug Symptom: Passed Tests</h4>

![Image](lab2image5.png)


After the bug fix, both JUnit tests now pass and the Reversed method now runs correctly.

<h2>Part 3: What I Learned</h2>

During the second week of CSE15L lab, I learned something interesting relating to port access. It was not allowed for multiple users on the same computer to uuse the same port simultaneously. When connected to a server, ports serve as channels through which computers transmit internet and network messages. Thus, if multiple students were using an ieng6-201 computer, they would need to select different port numbers of their respective web servers for things to operate properly. This also happened to me when trying to call the same port in `java StringServer 4000` multiple times for example.
