# Tool Learning Log

## Tool: **Json API's**

## Project: **Random Quote generator**

---

### 10/3/25:
* This tool has requests and responses to a server and a client.
* (https://www.youtube.com/watch?v=cj3h3Fb10QY)
* How to start using api's (https://restfulapi.net/introduction-to-json/)

### 11/2/25:
* Created a function named `fetchRandomQuote` and took some code to see how i would first obtain information from a server and have it show on a website that displayed this quote.
* I'm planning to get a server website that gives information because some sites are not working.
* So far i have a test website that should display a quote currently in progress.
* `https://forismatic.com/en/api/` is a site to see how an api works and using some examples for my testing.

### 11/16/25

* Watched a youtube video and saw this code I could test out. Basically the guy used his own Api to pull information about a character but i applied it to my case to see what would happen.
```
const URL = "http://api.forismatic.com/api/1.0/";

async function fetchdata() {
  const response = await fetch(URL)
  const data = await response.json();
  console.log(data);
}
```
* Another detail that I found is that if I were to connect a button to the Api call then it would be in this form.
`document.getElementById('fetchButton').addEventListener('click', getApiData);`
* I'm still trying to figure out what the Api will do and how i can access the quote information so I need to focus on adjusting the code so that I can do it.

### 11/23/25

* Woah now this is cool, I finally got the Api to send data to my server as it was being called. I'm confident this project is good and now all I need is extra details and decor. It turns out that the Api itself is old which is nomral so I had to improvise and get other parts that allowed me to access the information inside the forismatic Api.
* Here is what that extra code looks like.
```
const url = "https://api.allorigins.win/raw?url=" +
      encodeURIComponent("http://api.forismatic.com/api/1.0/?method=getQuote&format=json&lang=en");
```
* The site isn't perfect yet but it will be fixed soon as i configure more about the call function for different quotes.

### 12/1/25

* The code that I currently have right now is quite complicated so I had to look for fixes and adjustments and realized that forismatic works more with jsonp which is similar to json but in it's special way. Here is what some of the code looks like. `const callbackName = "forismaticCallback_" + Math.random().toString(36).substring(2);`.

* In order to use it properly I had to make functions and different elements for this API's purpose otherwise i couldn't make it work well and i could get more results at last.

* For now i will try to intergrate more of my API tool with the purpose i want it to do like revealing a quote.
### 12/7/25

* For now the research I have done made me discover about the element `window` which is especially made for this API and am starting to get some work into it.

* here is how I could plan to use it for getting those quotes out.
```
 window[callbackName] = function(data) {
        document.getElementById("quote").textContent = "“" + data.quoteText.trim() + "”";
        document.getElementById("author").textContent = data.quoteAuthor || "Unknown";
```
* Next I have see how i would use this with a button once i fully understand the concepts so that the quotes can show in an orderly way without much interruption from other sources like an error.

### 12/14/25
* More functions have to be made so the Api works or else nothing else would show. For that i decided to make sure that the API would call it's server for that info.
```
const callbackName = "forismaticCallback_" + Math.random().toString(36).substring(2);
otherFunctions... code here

const script = document.createElement("script");
    script.src = `https://api.forismatic.com/api/1.0/?method=getQuote&format=jsonp&lang=en&jsonp=${callbackName}`;
    document.body.appendChild(script);
```
* With this process ready I can move on to make sure the quotes show with the proper stuff but i will start simple first.
* I also made sure to include the button that would make the quote appear on your screen. Here is how that looks `fetchdata();
document.getElementById("newQuoteBtn").addEventListener("click", fetchdata);`.

### 1/16/26
* For now since the loading feels off i decided to make a function for that purpose and make it seem more professional.
```
function showLoading() {
    document.getElementById("spinner").style.display = "block";
    document.getElementById("content").style.display = "none";
}
```
*  Also I made sure to add other effect for the loading so that it is looks better when it loads.
```
function hideLoading() {
    setTimeout(() => {
        document.getElementById("spinner").style.display = "none";
        document.getElementById("content").style.display = "block";

```
* For the next time there needs to be progress on showing those quotes appear one at a time unlesss the button is pressed on the middle of the screen.

### 3/8/26
* Even still I can find small details I can add to make the page feel a bit more relevant so I made a copy function so users could copy an interesting quote without doing it manually and is much more efficent.
```
//html
<button id="copyBtn" aria-label="Copy quote" title="Copy to clipboard">Copy</button>
//js
document.getElementById("copyBtn").addEventListener("click", () => {
    const quote = document.getElementById("quote").textContent;
    const author = document.getElementById("author").textContent;
    navigator.clipboard.writeText(`"${quote}" ${author}`).then(() => {
        const btn = document.getElementById("copyBtn");
        btn.textContent = "Copied!";
        setTimeout(() => btn.textContent = "Copy", 2000);
    });
});
```
* Also decided to add an element to move forward to a new quote like `.addEventListener` so users could go through quotes faster. In this case only the space and right arrow move forward.
```
document.addEventListener("keydown", (e) => {
    const btn = document.getElementById("newQuoteBtn");
    if ((e.code === "Space" || e.code === "ArrowRight") && !btn.disabled) {
        e.preventDefault();
        fetchdata();
    }
});
```

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
