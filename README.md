Quizify is an interactive command-line quiz application built with Node.js. It asks the user a series of questions, evaluates their answers, and displays their score. Additionally, it maintains a leaderboard to show top scorers.

Installation
To run Quizify, ensure you have Node.js installed on your machine. Then, install the required dependencies by running:

bash
Copy code
npm install readline-sync kuler
Usage
To start the quiz, run the following command in your terminal:

bash
Copy code
node quizify.js
How to Play
Start the Game: When you run the program, you will be prompted to enter your name.
Answer Questions: The quiz will present a series of questions with multiple-choice answers. Select an answer by typing the corresponding letter (a/b/c/d).
Score Display: After you answer all the questions, your score will be displayed.
Leaderboard: The leaderboard will show your position among the top scorers.
Code Overview
Data Structures
Database: Contains the quiz questions, options, and correct answers.
Leaderboard: Stores the names and scores of the players.
Functions
playGame(userAnswer, correctAnswer): Evaluates the user's answer and updates the score.
showQuestionAndOptions(database): Displays each question and its options, then prompts the user for an answer.
showHighScorer(leaderBoard): Updates and displays the leaderboard.
Example Questions and Answers
javascript
Copy code
const database = {
  data: [
    {
      question: `let a = {}, b = {}
console.log(a == b)
console.log(a === b)`,
      options: {
        a: "false false",
        b: "false true",
        c: "true false",
        d: "true true"
      },
      correctAnswer: "a"
    },
    {
      question: "Object.assign(target, source) creates which type of copy?",
      options: {
        a: "Deep Copy",
        b: "Shallow Copy",
        c: "Nested Copy",
        d: "Creates a new reference"
      },
      correctAnswer: "b"
    },
    {
      question: "Is method chaining possible with forEach?",
      options: {
        a: "Yes",
        b: "No"
      },
      correctAnswer: "b"
    }
  ]
}
Sample Leaderboard
javascript
Copy code
const leaderBoard = {
  data: [
    {
      name: "Ashish",
      score: 1
    },
    {
      name: "Riya",
      score: 3
    },
    {
      name: "Jay",
      score: 2
    }
  ]
}
Future Improvements
Add more questions to the database.
Include different types of questions (e.g., true/false, fill-in-the-blank).
Implement a timer for each question.
Create a web-based version of the quiz.
Contribution
Feel free to contribute to Quizify by submitting issues or pull requests on the GitHub repository.

License
This project is licensed under the MIT License. See the LICENSE file for details.

