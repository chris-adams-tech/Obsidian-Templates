# Obsidian Habit Tracking Templates

Obsidian has really changed a lot in the way I document and track my projects and progress in not only tech, but also my personal life. Though I have never been officially diagnosed, I definitely have ADHD as I have found a lot of people in tech, especially those into Obsidian, so I hope that someone may find some use in these templates!

Here are some templates that have helped me to document and track notes. This can be adjusted to your liking, but does require some plugins for functionality. 

**List of needed plugins**:

* **Calendar** - https://github.com/liamcain/obsidian-calendar-plugin
* **Dataview** - https://github.com/blacksmithgu/obsidian-dataview
* **Periodic Notes** - https://github.com/liamcain/obsidian-periodic-notes
* **Templater** - https://github.com/SilentVoid13/Templater
* **Style Settings** (optional) - https://github.com/mgmeyers/obsidian-style-settings


> [!warning] Open-source software
> Obsidian allows *Community plugins*, ones that are built from the open-source community. Note that these are not maintained by Obsidian and are not official software. I tend to do my own research into the code in the Github repo and suggest you to verify on your own as well! *Always verify, never trust*.

To find the instructions on how to use the templates, go to the [[How to use Templates]] page.

There is an example template already generated for each of the notes, `Daily`, `Weekly`, `Monthly`, `Quarterly`, and `Yearly`. 

Everything is adjustable. Any of these can be removed to minimize frequency using the *Periodic Notes* plugin.

---
# Dataviews

A very efficient way to visualize the data in Obsidian is using *Dataviews*. This is a community built plugin that uses *javascript* to query within the vault to visualize data. It really is a game changer and is an incredible way to manage pages within your vault. 

#### 3 Use Cases

Here are 3 use cases that I am using it for in my vault.

1. **Habit Tracking** - Within the *Periodic Notes* you'll notice that there are emojis as a *key/pair* value with a habit. This is to signify whether the habit was met for that day. 
	1. 🙌 = habit was met
	2. 💩 = habit was not met
		By using *Dataview*, this data can be queried and put into a table with whichever parameters you indicate. For example, in the weekly note, include the habits from the past 7 days in a table format. The code would look a little something like this:

![[dataview.png]]

And the output would be this table. This pulls the data from the daily notes of the past 7 days and populates them into this table.

```dataview
table medicine as "🍃 Medicine", push-ups as "💪 Push-ups", write as "✍️ Write", running as "🏃 Running", apply-for-2-jobs as "📋 Apply Jobs" 
FROM "Personal/Daily Notes" 
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7 days) SORT file.day ASC
```


2. **Tracking Published Pages for Website*** - Using *Dataview*, I can review the pages I have in my `published` directory along with the associated *metadata*. I tend to track mostly by the tags and will filter based upon the date creation. This way I can also review everything that has just been published, as we reviewing and updating anything that is old and outdated, possibly needing an update. 

![[dataview1.png]]

```dataview
table file.name as "File", date as "Date", type as "Type", tags as "Tags"
from ""
sort desc
```

Now, with this vault there is only one page with a date. When using this in production with templates, it makes more sense. Right now is only the templates, and baseline configuration. From this simple query, it can be adjusted to review specific tags or any other *metadata* within the properties. 



# Other Templates


This can be adjusted to your own liking. You'll notice the `gradient-text`. This is using a *CSS* class in the `.obsidian/snippets` folder. Ensure the file is there and enabled in the settings.

Here is the code for the snippet, I named it `gradient-text.css`. When you want to use this code within an HTML block, just use this code wrapped around the text you would like the effects to apply to:

```html
<div class="gradient-text">your-text-here</div>
```



```css
@keyframes gradientShift {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}

.gradient-text {
    background: linear-gradient(90deg, #892be249, #37ff146c);
    background-size: 200% 200%;
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
    animation: gradientShift 10s ease-in-out infinite;
}```

![[footer.png]]

# Task Tracking

