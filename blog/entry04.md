# Entry 4
##### 3/15/26

### Content  <!--Progress towards MVP, explain it, what else have you learned/evidence -->
For my tool I focused on building small things that would make it feel a bit more noticeable but I kept the same functions in play so everything would run together smoothly. Right now the MVP includes all the basic stuff like obtaining quotes and some organization but i still need to work om adding the best color scheme for me and putting on the rest of the good elements after I have decided where to put them.

Despite this I have made good progress and am expected to finsih on time just as my MVP schedule says. Below I have made something that would allow the user to copy the quote they liked and input where ever they wanted to so that they didn't have to manually do it. It uses event listeners through a button the user presses and intergrates details from a site I researched that could help me with this specific function.

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
It also became relevant that another idea I had was to make the quotes much more accesible through key presses and so that the user could cycle through them much quicker and not spend as much time clicking for a good quote. I used FCC as a basis and knowledge from in class lesson/notes to create a function that would help my project feel more intergrated with JS while adding different elements that would fix errors and create a good way for users to see that they could do more with my tool.
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
For my sources I looked at sites that would help develop my site even more so i used small details that would help me improve the functions further and that was done through [clipboard site](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API) which helped me build a copy function and [FCC](freecodecamp.org) which helped me decide what elements I wanted to have so the user could move to a new quote using their keys through event listeners,
### EDP
The current of the engineering design process that I am in right now is the 7th stage or improving the prototype because I feel that I am closer to being finished with my tool and adding small details to it will the user feel much more comfortable using it. For my project I am using a different shade of colors so the users can blend themselves into my tool and overall feel very experiencied at getting quotes.

### Skills

* Time management: For this skill I realized that I need to work on setting times for when I want to do my work because at the moment I always seem to find myself working on project late at night so my solution is to put the work in right after I get home and eat around 6pm to have more than enough time to be able to complete the work before I sleep close to 11pm.

* Adaptability: Since my tool is a bit different than regular projects I have to add small details that would make it slightly better but not drift away too much from my MVP as I still need to work on it but adding small changes wouldn't hurt as I understand the amount of time put onto my project and the complex code that sometimes comes with errors but is managable with my problem-solving



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
