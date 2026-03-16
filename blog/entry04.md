# Entry 4
##### 3/15/26

### Content  <!--Progress towards MVP, explain it, what else have you learned/evidence -->
For my tool I focused on building small things that would make it feel a bit more noticeable but I kept the same functions in play so everything would run together smoothly. Right now the MVP includes all the basic stuff like obtaining quotes and some organization but i still need to work om adding the best color scheme for me and putting on the rest of the good elements after I have deicded where to put them. Despite this I have made good progress and am expected to finsih on time just as my schedule says. Below I have made something that would allow the user to copy the quote they liked and input where ever they wanted to so that they didn't have to manually do it.

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
Another idea I had was to make the quotes much more accesible through key presses and so that the user could cycle through them much quicker and not spend as much time clicking for a good quote.
```
document.addEventListener("keydown", (e) => {
    const btn = document.getElementById("newQuoteBtn");
    if ((e.code === "Space" || e.code === "ArrowRight") && !btn.disabled) {
        e.preventDefault();
        fetchdata();
    }
});
```
### Sources
For my sources I looked at sites that would help develop my site even more so i used small details that would help me improve the functions further and that was done through [clipboard site](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API) which helped me build a copy function and [FCC](freecodecamp.org) which helped me decide what elements I wanted to have so the user could move to a new quote using their keys.
### EDP
The current of the engineering design process that I am in right now is the 7th stage or improving the prototype because I feel that I am closer to being finished with my tool and adding small details to it will the user feel much more comfortable using it. For my project I am using a different shade of colors so the users can blend themselves into my tool and overall feel very experiencied at getting quotes.

### Skills

* text

* text



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
