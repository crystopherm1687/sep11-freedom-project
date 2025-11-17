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
`
* I'm still trying to figure out what the Api will do and how i can access the quote information so I need to focus on adjusting the code so that I can do it.



<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
