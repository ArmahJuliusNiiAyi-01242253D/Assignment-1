#include <iostream>

int main() {
    // 1. Setup
    const int secretTarget = 42; 
    int guess = 0; // Initialized to 0 so it doesn't match secretTarget immediately
    int attempts = 0;

    std::cout << "Welcome to the Guessing Game!" << std::endl;

    // 2. The Loop
    while (guess != secretTarget) {
        
        // 3. The Logic
        std::cout << "Enter your guess: ";
        std::cin >> guess;
        attempts++;

        if (guess > secretTarget) {
            std::cout << "Too High!" << std::endl;
        } 
        else if (guess < secretTarget) {
            std::cout << "Too Low!" << std::endl;
        } 
        else {
            std::cout << "Correct!" << std::endl;
        }
    }

    // 4. Game Over
    std::cout << "You won in " << attempts << " attempts." << std::endl;

    return 0;
}
