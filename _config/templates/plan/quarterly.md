---
type: quarterly
quarter: <% "Q" + moment().quarter() + "-" + tp.date.now("YYYY") %>
year: <% tp.date.now("YYYY") %>
quarter_start: <% moment().startOf("quarter").format("YYYY-MM-DD") %>
quarter_end: <% moment().endOf("quarter").format("YYYY-MM-DD") %>
tags:
  - quarterly
  - habit_tracker
---
# 🗓 Quarterly Plan: <% tp.date.now("YYYY-[Q]Q", 0, tp.file.title, "YYYY-[Q]Q") %>

## 🏆 Quarterly Goals
- [ ] Goal 1
- [ ] Goal 2
- [ ] Goal 3

## 📋 Focus Areas
- Area 1
- Area 2
- Area 3

## 📈 Projects and Milestones
| Project            | Milestone 1 | Milestone 2 | Milestone 3 | Progress |
|--------------------|-------------|-------------|-------------|----------|
| Project A          |             |             |             |          |
| Project B          |             |             |             |          |

## 📈 Habits Tracking Summary
| Habit              | Month 1 | Month 2 | Month 3 | Total |
|--------------------|---------|---------|---------|-------|
| Medicine           | 🙌       | 🙌       | 🙌       |       |
| Push-ups           | 💩       | 💩       | 💩       |       |
| Running            | 💩       | 💩       | 💩       |       |
| Reading            | 💩       | 💩       | 💩       |       |
| Meditation         | 💩       | 💩       | 💩       |       |

## 📊 Reflection
- Wins:
- Challenges:
- Adjustments for Next Quarter:
