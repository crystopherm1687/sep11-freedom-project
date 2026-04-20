# Entry 5
##### 4/19/26

### Content

Throughout this project there has been a bunch of challenges and one of them was a time crunch where we had to design an mvp as soon as possible to be ready to present something cool or interesting that we made using avaible javascript concepts. Even with that said I was still able to make something out of it and feel like my tool JSON api's has helped bring my idea to life. Now then let's get into what I have done so far with my project. Since it has taken time for me to develop something like this I am going to also show more details about what I put.

For example this part here with the date is something that I wanted users to see so that they could get today's date and feel more interactive with my project.
```
    function todayKey() {
      const d = new Date();
      return `qotd_${d.getFullYear()}_${d.getMonth()}_${d.getDate()}_${categorySelect.value}`;
    }
    function formatDate() {
      return new Date().toLocaleDateString("en-US", {
        weekday: "long", month: "long", day: "numeric"
      });
    }
```
Since this function has been added I made sure to put it in a spot where the user could easily see it and made it blend in with the colors of gold and black so everything would work well together. Another idea i had in mind was to add specific categories for each user to want to see in my project so I added this feature to get users more adjusted to using my project and seeing some good quotes that they would feel inspired by. If you don't what this does it basically filters through a categories tab then puts quotes it finds through the api into local storage as a way to access specific quotes tied to that category so that the user can see their favorite quotes but in a certain topic.
```
    {
      const filtered = getFilteredQuotes();
      const q = filtered[Math.floor(Math.random() * filtered.length)] || quotes[0];
      const qotd = { text: q.text, author: q.author };
      localStorage.setItem(key, JSON.stringify(qotd));
      renderQotd(qotd);
    }
```
My finished project is accesible here [Random quote generator](https://crystopherm1687.github.io/sep11-freedom-project/) and now i feel basically done and confident to show this to other students.

### Sources

The sources I used to help bring the extra details to life was [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) which helped build upon my date settings for the page and automatically change dates when I needed it. Also this page[W3schools](https://www.w3schools.com/js/js_date_methods.asp) helped clarify a couple of details when it came to building the actual time system inside my project which seems pretty useful if the user is unable to remember the date. I also used this site [coding artist web](https://codingartistweb.com/2023/09/random-quote-generator-with-local-storage/) to find a way to build the categories that a user would want and bring quotes with those ideas.
### EDP
For the Engineering Design Process I can for sure say that I am on the 7th stage which is improving as needed because in just a couple of weeks this project will be presented so by making changes or including beyond mvp details it makes it so that my project looks even better than the original framework and more reliable to use when users decide to come look at it. Also now that the mvp has been done it makes more much easier to adjust intro present mode which would probably happen by the next blog or in a few weeks depending on the schedule.
### Skills

* Project management: For this skill I found myself wondering if i could actually finish on time before the deadline for the mvp was due which made me feel a little bad about myself for not wanting to do it but i set dates by which i had finish certain parts/sections by and that gave me some influence to want to complete small things here and there with all my busy schedules that have something to conflict with so by completing it now i give myself more time to do other things.


* Work ethic: Being able to complete my project took a lot of motivation and resources to be able to pull something together because at first it felt almost diffcult and looked like something that i would not able to do but then i remembered that there are so many coding sites, videos and files that deal with javascript and JSON api's which helped me a lot and that was what i needed to be able to want to explain the entire project and build something cool.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
