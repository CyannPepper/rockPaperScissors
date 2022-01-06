# rockPaperScissors
A simple game of Rock, Paper, Scissors made in Javascript to practice functions!

const getUserChoice = (userInput) => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock') {
    return userInput;
  } else if (userInput === 'paper') {
    return userInput;
  } else if (userInput === 'scissors') {
    return userInput;
  } else if (userInput === 'bomb') {
    return userInput;
  } else {
    console.log("You have entered an invalid input. Please enter rock, paper, or scissors.");
  }
}

const getComputerChoice = () => {
  let randomNum = (Math.floor(Math.random() * 3));
  if (randomNum === 0) {
    return 'rock';
  } else if (randomNum === 1) {
    return 'paper';
  } else {
    return 'scissors';
  }
} 

const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return console.log('The game was a tie!');
    } if (userChoice === 'bomb') {
      return 'The user won!'
    } if (userChoice === 'rock') {
      if (computerChoice === 'paper') {
        return 'The computer won!';
      } else {
        return 'The user won!'; {
    }
   }
  }
  if (userChoice === 'paper') {
      if (computerChoice === 'scissors') {
        return 'The computer won!';
      } else {
        return 'The user won!';
  }
  } 
 if (userChoice === 'scissors') {
   if (computerChoice === 'rock') {
    return 'The computer won!';
  } else {
    return 'The user won!';
  }
 }
}

const playGame = () => {
  const userChoice = getUserChoice('bomb');
  const computerChoice = getComputerChoice();
  console.log('You threw: ' + userChoice);
  console.log('The computer threw: ' + computerChoice);

  console.log(determineWinner(userChoice, computerChoice));
}

playGame();
