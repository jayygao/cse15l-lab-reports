# Lab Report 2

## Part 1

Below I have attached photos of my code.
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {
    List<String> words = new ArrayList<>();
    String ret = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            ret = "";
            for(String s : words){
                ret += s;
                ret += "\n";
            }
            return ret;
        }
        else if(url.getPath().contains("/add")){
            System.out.println("Path: " + url.getPath());
            String[] parameters = url.getQuery().split("=");
            if(parameters[0].equals("s")){
                ret = "";
                words.add(parameters[1]);
                for(String s : words){
                    ret += s;
                    ret += "\n";
                }
    
                return ret;
            }
            else{
                return "404 Not Found";
            }
        }
        else if(url.getPath().equals("/clear")){
            ret = "";
            words.removeAll(words);
            return "Words cleared.";
        }
        else{
            return "404 Not Found";
        }
    }
}

class StringServer{
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
---
For the screenshots attached below, it shows the method handleRequest being called, with the argument of /add-messages

It is called multiple times as I add new messages, which is saved through the "words" arraylist, and the String "ret"

displays each message in a new line, using '\n' for line breaks.

![Image](https://i.gyazo.com/2e3a807d97e9d06f99b35bac98b3f38c.png)
![Image](https://i.gyazo.com/3929a640fd96f18019e21053887b25e7.png)
![Image](https://i.gyazo.com/d63a661074f4d8b1270f87f55538a63a.png)
![Image](https://i.gyazo.com/55872223af2ea0d150f122dbf36b1c1f.png)
![Image](https://i.gyazo.com/9b90100ad8b41994103f03475030e04a.png)

The Arraylist "words" is updated with new messages being added, which inputs the messages into String "ret"

adding '\n' each time a new message is added to create new lines. If an Integer or Double is added it'll still 

register as a String. Which means the values of Strings will remain as Strings, while others will be converted

to a String.

---
If an empty argument is presented, no values get changed as the messages saved in the Arraylist "words" get displayed
through the String "ret".

![Image](https://i.gyazo.com/ac89e06efca19a37436f86331d07db5b.png)

---
I also added my own argument "/clear" which removes every element from the Arraylist "words", and sets the String "ret" to empty.

![Image](https://i.gyazo.com/b50fc50977d8f2d40ada555ea228a9e1.png)
![Image](https://i.gyazo.com/b05fa3ed3bd4fcc6bf770b64d3963b4a.png)
![Image](https://i.gyazo.com/597ceeb86744c0002f1b4c8c12dc9897.png)

## Part 2


Below I have attached the code block of the failure inducing input.

```
@Test 
	public void testReverseInPlace() {
    int[] input3 = {3,2,1};
    ArrayExamples.reverseInPlace(input3);
    assertArrayEquals(new int[]{1,2,3}, input3);

    // len = 3, 3 - 0 - 1 = 2 @ 0, 3 - 1 - 1 = 1 @ 1, 3 - 2 - 1 = 0 @ 2.
    // 3 2 1 = 1, 2, 1
	}
```

---
Below I have attached the code block of a non-failure inducing input.

```
@Test 
	public void testReverseInPlace2() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```

---
Below I have attached an image of the output of the running tests.

![Image](https://i.gyazo.com/fca0e60f47711e57e0ac10a914ec9fa2.png)
![Image](https://i.gyazo.com/ee51fada62624370d070d17267e27116.png)

---
Below I have attached the code before the bug was fixed.

```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

---
Below I have attached the code after the bug was fixed.

```
  static void reverseInPlace(int[] arr) {
    if(arr.length > 1){
      int val = arr[0];
      int val2 = arr[arr.length - 1]; 

      for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];  
      } 

      arr[0] = val2;
      arr[arr.length - 1] = val;
    }
    else{
      arr = arr;
    }
  }
```

---
### But what's the issue? 

The issue is that the method before it was fixed would make the array go in reverseOrder

however the last value in the array would remain the same, instead of changing with the first value because

it updates itself with the first value AFTER the first value was replaced. Which means nothing changed.

For example, in an array {0, 1, 2}, it'll change the first value with 2, then middle value with 1, and the 

last value remains 2 because in the first value became 2, it didn't remain as 0. Giving us {2, 1, 2}

### My Fix

In my code, before the loop runs to reverse the order, I first created two new Integer variables. With the first variable

containing the first value of the array, and the second variable containing the last value of the array.

After the loop runs its course, the bug remains, so at the end of the loop I replace the first value of the array

with our second variable, and the last value with our first variable. 

However if the length is shorter than 2, it'll just return the array itself because there is nothing to return.

## Part 3

In week 2 I learned to create my own server through java and have it run a program I create. I learned that others can connect

to my server if I host it on a remote computer, and have it run continiously while my main computer can be offline.

I never knew how to host my own webpage server, just how to access remote computers like ones from Google Cloud or AWS.

