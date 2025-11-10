# Entry 1
##### 11/9/25

### Content
<!-- Talk about progress and intro to tool -->
For my tool I have decided to go with Api's because I wanted to make a quote generator for my project. In my case this project is proving to be slightly difficult because of how much learning I need to do in order to pull off the full use of my tool. Since Api's rely on a server that means I have to get the relevant information like Headers and URL's for the client which is my project. AS a start I first made a function that would help me down that in a simple way so the quote would be displayed without long lines of code.

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
This is some code that would help me process information from that server and input it onto my generator. Considering the knowledge I have so far it is something but not good enough to help me look through the information as I'm only calling the URL with no addition data that it would require. For now I will keep testing it out and see how the detailed Api call examples work so I don't get stuck on this part. 
#### Sources
<!-- links, videos, websites -->
* https://forismatic.com/en/api/
* https://coda.io/@mark-davis/random-quote
* https://technologyadvice.com/blog/information-technology/how-to-use-an-api/
### EDP
<!-- Straightforward what stage i am in -->
I am in the second stage of the engineering design process because my progress so far is adapting to use Api's and understand how they work so I can successfully call a server for information and put it on a website. While it is still early into my project phase I am thinking of adding a couple of quotes to my project so that it can be an array that is accessed instead of a server to see how the data goes through the API process.
### Skills
<!-- Talk about the specifics, how, when, -->
* Time management
In order to manage my time in a smart way I will focus at least an hour of my time on the project when possible every day so that I can keep up with Api prodecures and implement them as soon as possible. Right now I have a bit of tasks going on so I will have to make do with some time like working Monday, Thursday and Friday since those are those days I won't have much going on. On top of that I feel like having breaks in those work hours could help me break down the steps of my project to be simpler.

* Critical thinking
While it still isn't clear for me if my tool will work, what I can do right now is focus on the overall goal of my project and keep discovering new details that would aid me in completing work for Api's. That said Api's for me are challenging at the moment but once I get used to their functions then I could start designing a cool front page that would attract attention from the viewers. It's important for me to understand that some things don't just do themselves overnight and they could essentially put me into a focused mode that allows me to put one and one together like if I was working with someone but it was just me doing all the work as I need to think positively for a successful project.


[Next](entry02.md)

[Home](../README.md)
