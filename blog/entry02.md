# Entry 2
##### 12/X/25

### Content<!--Evidence of learning from the logs for our tool. Keep in mind that our work looks slighty different from the first blog amd so it has to be explained and broken down in detail.-->

During my time learning more about my tool and doing my project I found that in order for my tool to completely work I had to work around the constraints of JSON and and use JSONP since I was putting my time into the forismatic website which was a good server to test my JSON tool. When I was doing more research on the JSONP part of my tool I could use it because this site was like an older version of modern servers so I had to change some things with calling the site for quotes. At this point I found it was useful to obtain the quotes JSON couldn't


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

### Sources<!---use [text](link.com/net/org/gov)->
* [Jsonp video](https://www.youtube.com/watch?v=EKaic2TjMAM&t=562s)
* [learning about JsonP](https://beeceptor.com/docs/concepts/jsonp-introduction/)
### EDP<!--What step of engineer design process are you at-->
The step of the Engineering design process I am at now is the fourth stage because I wanted to have my ideas out there first so I came out with the best amount
### Skills<!--Specific things to do or need to do-->

* Problem Solving

* Attention to detail



[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
