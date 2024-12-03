---
type: weekly
week: <% tp.date.now("YYYY-[W]WW") %>
year: <% tp.date.now("YYYY") %>
week_start: <% moment().startOf("isoWeek").format("YYYY-MM-DD") %>
week_end: <% moment().endOf("isoWeek").format("YYYY-MM-DD") %>
tags:
  - weekly
---

# 🗓 Weekly Plan: <% tp.date.now("YYYY-[W]WW", 0, tp.file.title, "YYYY-[W]WW") %>

## 🏆 Goals for the Week
- [ ] Goal 1
- [ ] Goal 2
- [ ] Goal 3

## 📋 Focus Areas
- Area 1
- Area 2
- Area 3

## 📅 Weekly Overview
| Day       | Tasks / Events                |
|-----------|-------------------------------|
| Monday    |                               |
| Tuesday   |                               |
| Wednesday |                               |
| Thursday  |                               |
| Friday    |                               |
| Saturday  |                               |
| Sunday    |                               |

## 📈 Habits Tracking
| Habit              | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday | Sunday | Total |
|--------------------|--------|---------|-----------|----------|--------|----------|--------|-------|
| Medicine           | 🙌      | 🙌       | 🙌         | 🙌        | 🙌      | 🙌        | 🙌      |       |
| Push-ups           | 💩      | 💩       | 💩         | 💩        | 💩      | 💩        | 💩      |       |
| Running            | 💩      | 💩       | 💩         | 💩        | 💩      | 💩        | 💩      |       |
| Reading            | 💩      | 💩       | 💩         | 💩        | 💩      | 💩        | 💩      |       |
| Meditation         | 💩      | 💩       | 💩         | 💩        | 💩      | 💩        | 💩      |       |

## 🚂 Notes & History
- Notes:
  - 🚂 Item 1
  - 🚂 Item 2
- History:
  - Event 1
  - Event 2

## 📊 Reflection
- Wins:
  - Example 1
  - Example 2
- Challenges:
  - Example 1
  - Example 2
- Next Steps:
  - Example 1
  - Example 2

```dataview
TABLE
  medicine as "🍃 Medicine", 
  push-ups as "💪 Push-ups", 
  write as "✍️ Write", 
  call-mum as "📞 Call Mum", 
  running as "🏃 Running", 
  apply-for-2-jobs as "📋 Apply Jobs" 
FROM "Personal/Daily Notes" 
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7 days) SORT file.day ASC
```
