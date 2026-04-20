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
Since this function has been added I made sure to put it in a spot where the user could easily see it and made it blend in with the colors of gold and black so everything would work well together. My finished project is accesible here [Random quote generator](https://crystopherm1687.github.io/sep11-freedom-project/) and now i feel basically done and confident to show this to other students.

### Sources

The sources I used to help bring the extra details to life was [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) which helped build upon my date settings for the page and automatically change dates when I needed it. Also this page[W3schools](https://www.w3schools.com/js/js_date_methods.asp) helped clarify a couple of details when it came to buidling the actual time system inside my project which seems pretty useful if the user is unable to remember the date.
### EDP
For the Engineering Design Process I can for sure say that I am on the 7th stage which is improving as needed because in just a couple of weeks this project will be presented so by making changes or including beyond mvp details it makes it so that my project looks even better than the original framework and more reliable to use when users decide to come look at it.
### Skills

* Skill1

* skill2

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
