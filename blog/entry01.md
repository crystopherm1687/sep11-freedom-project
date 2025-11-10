# Entry 1
##### 11/9/25

### Content
<!-- Talk about progress and intro to tool -->
For my tool I have decided to go with Api's because I wanted to make a quote generator for my project. In my case this project is proving to be slightly difficult because of how much learning I need to do in order to pull off the full use of my tool. Since Api's rely on a server that means I have to call it

```
function fetchRandomQuote() {
    fetch('link')
        .then(response => response.json())
        .then(data => {
            const quote = data.content;
            document.getElementById("quote").textContent = quote;
        })
        .catch(error => {
            console.error('Error fetching quote:', error);
        });
}
```
This is some code that would help me process information from that server and input it onto my generator.
#### Sources
<!-- links, videos, websites -->
* https://forismatic.com/en/api/
* https://coda.io/@mark-davis/random-quote
* text
* text
### EDP
<!-- Straightforward what stage i am in -->
I am in the first stage of the engineering design process because my progress so far is adapting to use Api's and understand how they work so I can successfully call a server for information and put it on a website. While it is still early into my project phase I am thinking of adding a couple of quotes to my project so that it can be an array that is accessed instead of a server in case it doesn't fully work.
### Skills
<!-- Talk about the specifics, how, when, -->
* Time management
text

* Critical thinking
text


[Next](entry02.md)

[Home](../README.md)
