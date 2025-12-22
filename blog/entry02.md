# Entry 2
##### 12/21/25

### Content<!--Evidence of learning from the logs for our tool. Keep in mind that our work looks slighty different from the first blog amd so it has to be explained and broken down in detail.-->

During my time learning more about my tool and doing my project I found that in order for my tool to completely work I had to work around the constraints of JSON and and use JSONP since I was putting my time into the forismatic website which was a good server to test my JSON tool. When I was doing more research on the JSONP part of my tool I could use it because this site was like an older version of modern servers so I had to change some things with calling the site for quotes. At this point I found that it was more useful to obtain the quotes JSON couldn't because of inconsisties. The current code that I made so far utilizes a callback function with different elements associated with helping it to retrieve quotes by being general and specific about what to ask for. The function goes to the server and says, hey here is the format that I want my quote to be in and the site provides the quote based on what the function needs quickly and so the function displays that same quote which works well


```
function fetchdata() {

    const callbackName = "forismaticCallback_" + Math.random().toString(36).substring(2);

    window[callbackName] = function(data) {
        document.getElementById("quote").textContent = "“" + data.quoteText.trim() + "”";
        document.getElementById("author").textContent = data.quoteAuthor || "Unknown";

        delete window[callbackName];
        script.remove();
    };

    const script = document.createElement("script");
    script.src = `https://api.forismatic.com/api/1.0/?method=getQuote&format=jsonp&lang=en&jsonp=${callbackName}`;
    document.body.appendChild(script);
}

```
Now here is what that looks like so far.
* <img src= "../tool/json.jpg"> <p>First quote</p>
* <img src="../tool/json2.jpg"> <p>Second quote</p>
While I finally breath a sign of relief I can most definitely say that I did a lot testing and research in order to have my tool work because it just seemed like a difficult obstacle but I endured it and just wanted to see an end product but for now I have to continue working on improving it and inputting certain elements to make it look nicer.

### Sources
* [Jsonp video](https://www.youtube.com/watch?v=EKaic2TjMAM&t=562s)
* [learning about JsonP](https://beeceptor.com/docs/concepts/jsonp-introduction/)

### EDP<!--What step of engineer design process are you at-->
The step of the Engineering design process I am at now is the fifth stage because I wanted to test the idea of using a similar form of JSON now that I discovered it was going to be used but with some aspects of JSON still in it since that is what tool is. On top of that since I'm still testing the product I will have to add some more elements that would make the loading and quote production more smoother.
### Skills<!--Specific things to do or need to do-->

* Problem Solving
As I was learning my tool I came up with ways to get to the end which involved JSONP to intergrate my tool into my project as it produced quotes. First what I had noticed is that forismatic was a bit behind the latest APIs used today so I had be innovative with how I used it and found the that callback function which helped solve to obtain all the quotes in the server.

* Attention to detail
Since the API I was using required a more sophisticated version of JSON I used knowledge from online videos and websites to attempt to fix my issues with the code and so I got to work making something useful and simple to use that the user accessing my project would be able to use with ease. That's how I was able to get the current code in my content so far and adjusting the way I used JSON gave me a new understanding of how to work with APIs that might need more complicated code.


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
