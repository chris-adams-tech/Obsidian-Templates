Templates are an extremely powerful way to automate the structure of your pages. I tend to use them for my daily notes and habit tracking. With this set up for the daily, weekly, monthly, quarterly, and yearly, it allows the notes to connect in a seamless way. 

One way to use them is for **habit tracking**. Here is how I use it.

There are 5 templates under the `_config/templates` folder; `daily`, `weekly`, `monthly`, `quarterly`, and `yearly`. Each of these uses a plugin called *Templater* that allow inline *Javascript* queries in the metadata (Properties). 

For each day, I have it set so the *Daily Note* opens up when opening the application. This will then auto generate the metadata as according to the `daily.md` template that I use.

###### Here is the daily.md template
```
---
uid: <% tp.date.now("YYYYMMDDHHmm") %>
date: <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
weekday: <% tp.date.now("dddd") %>
week: <% tp.date.now("YYYY-[W]WW", 0, tp.file.title, "YYYY-MM-DD") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
tags:
  - daily_note
  - habit_tracker
medicine: 🙌
push-ups: 💩
running: 💩
apply-for-2-jobs: 💩
do 1 lab: 💩
sleep: 0
exercise: 0
reading: 0
meditation: 0
writing: 0
---
#### Work
- [ ] 💪

#### Articles
- [ ] 

#### Meetings
- 🎙

#### Outcomes
1. 🦄

#### Journal
```

By creating a template, it allows for this to be deployed dynamically each day, reducing the time having to create the fields each time. 

To show for example, now when I open a new page, it will look like this:

![[daily-habit.png]]
A random `uid` is generated for uniqueness, the `date` of the note is populated and set as the title, the `weekday` is set according to the current date, `week` is set according to the week within the year, and `year` is set within that time frame. 

I've also set two tags `daily_note` and `habit_tracker` so these notes can be easily queried via the *Dataview* plugin. That plugin makes managing pages at scale much more efficient. That's a discussion for another page though. 

Now each of these `daily` notes and each of the daily habits can be reviewed at the end of the week in the `weekly` note. Then, this `weekly` note can be used to plan for the upcoming week as well. This ensures continuous improvement and planning for your next goals. 

This micro to macro goal setting can continue from `weekly` -> `monthly` -> `quarterly` -> `yearly` and can easily be adjusted to remove any for less optimization. If the system is not built to support doing this level of tracking, it can be more daunting to even approach such a task. But with small bits and adding little by little (*the 1% compounding factor rate*), you can find a system that works for you.

Additionally to this, any of the fields can be adjusted, removed, added, to tailor to your liking. 

### Managing your notes with hotkeys

I have been finding the best way to be able to manage these notes is by both using *Dataview* and the use of *hotkeys*. *Hotkeys* are customized key bindings that optimize frequently executed tasks, such as templates. 

For the note-taking, I use a plugin called *Periodic Notes*, which allows the creation of the multitude of notes. Here are the hotkeys I have set:

| Template      | Hotkey     |
| ------------- | ---------- |
| **Daily**     | `CTRL + D` |
| **Weekly**    | `CTRL + W` |
| **Monthly**   | `CTRL + M` |
| **Quarterly** | `CTRL + Q` |
| **Yearly**    | `CTRL + Y` |

This is set for basic use and can further be customized with going to previous/next note, etc. but this is a great starting point.

---

For further technical documentation on syntax and how to use *Templater*, check out their docs https://silentvoid13.github.io/Templater/introduction.html

