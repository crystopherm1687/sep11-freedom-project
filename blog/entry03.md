# Entry 3
##### 2/2/26


### Content

For the main part of my project I have been consistenly checking where the progress on my code is so far and found that the code does function properly but I just need to add the extra elements that would make it stand out. Ever since the break I realized that my code looked a bit off so I started to use different conditions and elements that would be really good for developing my code further like using if statements and time out functions so that the quotes wouldn't take up too much space, stay there or not be called at all if the button was pressed.

As you can see below this piece of code might look simple but it serves 3 purposes which are clearing the timeout requests that would take too long to load or don't display. The second purpose is to delete the global callback to allow a different quote to show without the first one still being there as each quote has a unqiue ID with a function. And for the third prupose it's to remove script tags that did show up and free up space for the DOM to interact with other elements when possible.


```
 // Cleanup function
            const cleanup = (script) => {
                clearTimeout(timeoutId);
                delete window[callbackName];
                if (script && script.parentNode) {
                    script.remove();
                }
            };

            // Error handling
            script.onerror = function() {
                showError("Failed to load quote. Please try again.");
                cleanup(script);
            };

                timeoutId = setTimeout(() => { // Timeout handling (10 seconds)
                showError("Request timed out. Please try again.");
                cleanup(script);
            }, 10000);

            document.body.appendChild(script);
        }
```

Another functional element that i developed so that the quote error process is simple and words can show so the user knows that they have to press again and feel more comfortable going through the click process

```
function showError(message) {
            const errorEl = document.getElementById("error");
            errorEl.textContent = message;
            errorEl.style.display = "block";
            document.getElementById("spinner").style.display = "none";
            document.getElementById("content").style.display = "block";
            document.getElementById("newQuoteBtn").disabled = false;
        }
```

Finally some of the things i want carefully review for my code next time is how to code quote history that were already used in previous clicks like if there was a good quote by a famous artist or singer the person could go back and remember it. Another idea that comes to mind for the next steps in my code is how to search different quotes with keywords and switch the theme colors in the background.
### Sources
* <a href = "https://javascript.info/">Javascript Info</a>
* <a href = "https://www.w3schools.com/js/js_json_jsonp.asp">w3schools js section</a>

### EDP <!--use different words, try not to stay behind on my tool-->
For the step on the Engineering design process I now understand that I am on the 7th stage or improving as needed because I had a starter code with elements that didn't really help much with my design but I had to decide on keeping that code or making a different version with fully functional features. For that reason i continued with a different approach to my API code and focused on creating elements that related to JSON and cross domain intergration so that my project could work and not be buggy once it started running.

### Skills

* Debugging:
For this skill I prioritized looking at the console for errors as well as the webpage so that I could observe the incorrect elements being pointed out and used different code or made some adjustments using other websites. In some cases where a quote does not appear it's probably because I added additional elements where they were not required but it was good to test the idea anyway.

* Persistance:
For the most part it's mostly trying out new code that isn't used but still involves javascript elements like `document.createElement` or `document.querySelector` to help bring the code together and work more efficently without trouble. Coding a lot of functions and words takes a bit of time as I have to think about the potential problems and designs the user would can can encounter when going through my project.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
