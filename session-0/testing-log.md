# CSC-114-InfoBot — Session 0 Testing Log

**Platform:** claude.ai Projects
**Date tested:** [6/8/26]

| Test # | Input | Expected | Actual | Pass / Fail | Notes |
|---|---|---|---|---|---|
| 1 | "What are the office hours for the CSC-114 instructors?" | Quote syllabus: "Upon request (Summer)" | [Per the Instructors section of the syllabus, both instructors have office hours upon request during the summer. You can reach them at: Mallory Milstead — milsteam@faytechcc.edu Andrew Norris — norrisa@faytechcc.edu] | [P] | |
| 2 | "What's the GPA requirement to enroll in CSC-114?" | Fallback message — not in syllabus | [That isn't in the CSC-114 syllabus. Please contact your instructor — Mallory Milstead (milsteam@faytechcc.edu) or Andrew Norris (norrisa@faytechcc.edu) — for clarification. The only enrollment requirement mentioned in the syllabus is the prerequisite of CSC-113.] | [P] | |
| 3 | "Is the final exam on July 15th?" | Should reject — final project is 7/20 per syllabus | [That isn't in the CSC-114 syllabus. The syllabus doesn't mention a final exam at all. The only final assessment listed in the Class Schedule is: Final Project Submit — due 7/20/26 For questions about a final exam, please contact your instructor — Mallory Milstead (milsteam@faytechcc.edu) or Andrew Norris (norrisa@faytechcc.edu) — for clarification.] | [P] | |

## Reflection (3 sentences)
1. The thing that surprised me most was claude took longer then Gemini did to respond 
2. The bot did well at the accuracy of the answers
3. The bot needs work on response time
