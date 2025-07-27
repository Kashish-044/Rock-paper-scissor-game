let userScore = 0;
let computerScore = 0;

const choices = ['rock', 'paper', 'scissors'];
const emojis = {
  rock: '🪨',
  paper: '📄',
  scissors: '✂️'
};

function startGame() {
  document.getElementById('intro-screen').style.display = 'none';
  document.getElementById('game-container').style.display = 'block';
}

function playGame(userChoice) {
  const computerChoice = choices[Math.floor(Math.random() * choices.length)];
  const resultText = document.getElementById('result-text');
  const computerMoveDisplay = document.getElementById('computer-choice');

  // Show computer's move
  computerMoveDisplay.textContent = emojis[computerChoice];

  let result = '';

  if (userChoice === computerChoice) {
    result = "It's a tie! 🤝";
  } else if (
    (userChoice === 'rock' && computerChoice === 'scissors') ||
    (userChoice === 'paper' && computerChoice === 'rock') ||
    (userChoice === 'scissors' && computerChoice === 'paper')
  ) {
    userScore++;
    result = `You win! 🎉 ${emojis[userChoice]} beats ${emojis[computerChoice]}`;
  } else {
    computerScore++;
    result = `You lose! 😢 ${emojis[computerChoice]} beats ${emojis[userChoice]}`;
  }

  resultText.textContent = result;
  document.getElementById('score').textContent = `You: ${userScore} | Computer: ${computerScore}`;
}
