var seconds = 0;
var lives = 3;
var score = 0;
var background;
var highscore = 0;
var random;
//These variables on lines 1-6 were made by both my collaborative partner and me

var secondOne;
var secondTwo;
var secondThree;
var scoreAddition = 0;
var check = 0; 
//These variables on lines 8-12 were made by my collaborative partner

var colorPicker;
var wordArray = ["red", "orange", "yellow", "green", "blue", "purple"];

onEvent("beginButton", "click", function() {
  setScreen("gameScreen");
  refresh();
});

onEvent("yesButton", "click", function() {
  screenColorChange();
  scoreFreeze();
  checkMatch(); 
  refresh();
});
//This onEvent function contains the function scoreFreeze that was made by my collaborative partner 

onEvent("noButton", "click", function() {
  screenColorChange();
  scoreFreeze();
  checkNotMatch();
  refresh();
});
//This onEvent function contains the function scoreFreeze that was made by my collaborative partner 

onEvent("playAgainButton", "click", function() {
  clear();
  lives = 3;
  score = 0;
  setText("livesCountLabel", lives);
  setText("scoreCountLabel", score);
  setScreen("startScreen");
});

function refresh() {
  screenColorChange();
  random = randomNumber(0,5);
  check = 0;
  setText("scoreCountLabel", score);
  setText("timeCountNumberLabel", "3");
  setText("gameArea", wordArray[random]);
  colorPick();
  secondOne = setTimeout(function() {
    seconds++;
    setText("timeCountNumberLabel", "2");
  }, 1000);
  secondTwo = setTimeout(function() {
    seconds++;
    setText("timeCountNumberLabel", "1");
  }, 2000);
  secondThree = setTimeout(function() {
    seconds++;
    zeroEffect();
    screenColorChange();
    setText("timeCountNumberLabel", "3");
  }, 3000);
}
//This function refresh was written by my collaborative partner with the exception of line 56
//and the function colorPick

function scoreFreeze() {
  scoreAddition = getNumber("timeCountNumberLabel");
  clear();
  return scoreAddition;
}
//This function scoreFreeze was written by my collaborative partner

function clear () {
  clearTimeout(secondOne);
  clearTimeout(secondTwo);
  clearTimeout(secondThree);
}
//This function was written by my collaborative partner

function zeroEffect() {
  updateLives();
  refresh();
}
//This function zeroEffect was written by my collaborative partner

function updateLives() {
  lives = lives - 1;
  setText("livesCountLabel", lives);
  if (lives === 0) {
    setScreen("scoreScreen");
    if (score > highscore) {
      highscore = score;
    }
    setText("yourScoreCountLabel", score);
    setText("highScoreCountLabel", highscore);
  }
}
//This function updateLives was written by my collaborative partner 

function colorPick() {
  colorPicker = randomNumber(0, 5);
  if (colorPicker === 0) {
    setProperty("gameArea", "text-color", "red");
  } else if (colorPicker == 1) {
    setProperty("gameArea", "text-color", "orange");
  } else if (colorPicker == 2) {
    setProperty("gameArea", "text-color", "yellow");
  } else if (colorPicker == 3) {
    setProperty("gameArea", "text-color", "green");
  } else if (colorPicker == 4) {
    setProperty("gameArea", "text-color", "blue");
  } else if (colorPicker == 5) {
    setProperty("gameArea", "text-color", "purple");
  }
}

function checkMatch() {
  if (getProperty("gameArea", "text-color") == "red" && random === 0 ) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "orange" && random == 1) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "yellow" && random == 2) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "green" && random == 3) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "blue" && random == 4) {
  check = 1; 
} else if (getProperty("gameArea", "text-color") == "purple" && random == 5) {
  check = 1; 
} else {
  updateLives();
}
if (check === 1) {
    score = score + scoreAddition;
    setText("scoreCountLabel", score); 
  }
}
//This function was created by me with the exception of the function updateLives which was made
//by my collaborative partner 

function checkNotMatch() {
  if (getProperty("gameArea", "text-color") == "red" && random !== 0 ) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "orange" && random != 1) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "yellow" && random != 2) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "green" && random != 3) {
  check = 1;
} else if (getProperty("gameArea", "text-color") == "blue" && random != 4) {
  check = 1; 
} else if (getProperty("gameArea", "text-color") == "purple" && random != 5) {
  check = 1; 
} else {
  updateLives();
}
if (check === 1) {
    score = score + scoreAddition;
    setText("scoreCountLabel", score);
  }
}
//This function checkNotMatch was modified by my collaborative partner but created by me

function screenColorChange() {
  background = randomNumber(0,5);
  if (background === 0) {
    setProperty("backgroundArea", "background-color", "red");
  } else if ((background == 1)) {
    setProperty("backgroundArea", "background-color", "orange");
  } else if ((background == 2)) {
    setProperty("backgroundArea", "background-color", "yellow");
  } else if ((background == 3)) {
    setProperty("backgroundArea", "background-color", "green");
  } else if ((background == 4)) {
    setProperty("backgroundArea", "background-color", "blue");
  } else if ((background == 5)) {
    setProperty("backgroundArea", "background-color", "purple");
  }
}
//My collaborative partner and I wrote screenColorChange together

//The background image we used is from http://wallpapercave.com/wp/3A3nSax.gif



