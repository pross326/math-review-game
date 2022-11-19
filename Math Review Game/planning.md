## Thoughts Prior To Starting
- Prioritize tablet and smaller device responsive design
- Aim for soft, inviting and intuitive UI
- Include streaks and point system to gamify learning
- Research 2nd grade curriculum to determine max numbers to include 

## 1 - Create UI
- Choose color scheme based on renci brand/grade level
- intuitive interface - one text box/submit button; not many directions needed
- score counter

## 2 - Incorporate API

## 3 - Error handling and Positive Reinforcement
- Positive message/checkmark when answer is correct
- When user gives incorrect answer, error message is displayed
- *Future update - hints/provide second guess*

## 4 - Score/Streak 
- 10 points per correct answer
- Score resets to zero after 1 wrong answer
- *Future update - Bonus +5 points for streaks of 3 in a row*
- *Future update - increased score for longer streaks*
- *Future update - x amount of points unlocks new level/operation*

## 5 - End Game
- For now, 100 points will end game - winning message

## 6 - Justifications/Thought Processes/Future Plans 
- Create directory for each operation (+ - / *) to account for future scalability
- operation icons in the top right corner will serve as navigation to different operation practice sets
- Add whiteboard feature so students can show work
- All images are free/open source
- Usually I would include a header/nav, but since this is a single page app, I chose card styling to bring all attention to the center
- I chose numbers <= 20 based on common core second grade standards https://www.education.com/common-core/second-grade/math/
- I did not include form validation, however that is something that should be implemented before the other mentioned features

## How This Works:
- Two numbers are randomly generated and displayed as an addition problem. User has a focused input box to enter their answer.
- The evaluated function, which is triggered by clicking the 'check answer' button or by clicking enter on the input, accesses the user's answer.
- The encodeURIComponent takes in both random numbers and is used to make the expression URL encoded. The math.js.org API returns the solution.
- The evaluated function adds the solution to an empty array (to provide access to the solution globally). The function then compares that solution to the users solution.
- If the answer is correct, the user's score is increased by 10 points. A checkmark and a positive message appears, and a new question is generated. 
- If the answer is incorrect, the user's score is set back to zero, and a message alerting the user that they were incorrect and they have to start over, appears.
- After the user scores 100 points, a message is displayed informing the user they won the game, and they are presented with the option to start a new game.