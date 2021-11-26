# Rock-Paper-Scissors-Lizard-Spock
// A rock, paper, scissors game 
#include <iostream>
#include <stdlib.h>

int main() {
  /* Scissors cuts Paper.
Paper covers Rock.
Rock crushes Lizard.
Lizard poisons Spock.
Spock smashes Scissors.
Scissors decapitate Lizard.
Lizard eats Paper.
Paper disproves Spock.
Spock vaporizes Rock.
(and as it always has) Rock crushes Scissors.*/
  srand(time(NULL));

  int computer = rand() % 3 + 1;

  int user = 0;

  std::cout << "============================================\n";
  std::cout << "Rock, Paper, Scissors!\n";
  std::cout << "============================================\n";

  std::cout << "1) Rock\n";
  std::cout << "2) Paper\n";
  std::cout << "3) Scissors\n";
  std::cout << "SHOOT!\n";

  std::cin >> user;
//--------------------------------------------------------------
  if(user == 1) {
    std::cout << "You chose Rock and...\n";
  }
  else if(user == 2) {
    std::cout << "You chose Paper and...\n";
  }
  else {
    std::cout << "You chose Scissors and...\n\n";
  }
//---------------------------------------------------------------
  if (user == computer) {
    std::cout << "It's a tie!\n";
  }
  else if(user == 1) {
    if(computer == 2) {
      std::cout << "You lose\n";
    }
    if(computer == 3){
      std::cout << "You win!\n";
    }
  }
  else if(user == 2) {
    if(computer == 1) {
      std::cout << "You win!\n";
    }
    if(computer == 3) {
      std::cout << "You lose\n";
    }
    else if(user == 3) {
      if(computer == 1) {
        std::cout << "You lose\n";
      }
    }
  }
}
