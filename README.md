# Guessing-game-with-rust
How i implemented and buiilt a guessing game with the Rust Programming Language

---

# Guess the Number Game

This is a simple command-line game where the player tries to guess a randomly generated number.

## How to Play

1. Run the program.
2. The program will generate a random number between 1 and 100.
3. You'll be prompted to input your guess.
4. Input your guess and press Enter.
5. The program will tell you if your guess is too small, too large, or correct.
6. Keep guessing until you guess the correct number.

## Code Breakdown

- The `rand` crate is used to generate random numbers.
- The `std::io` module is used for input/output operations.
- A secret number is generated using `rand::thread_rng().gen_range(1..=100)`.
- The player's guess is read from the standard input using `io::stdin().read_line(&mut guess)`.
- The guessed number is converted to an unsigned 32-bit integer using `parse()` and `match` statement handles errors.
- The player is informed if their guess is too small, too large, or correct using `match guess.cmp(&secret_number)`.

---
## How to Run

Make sure you have Rust installed. You can run the code by executing `cargo run` in your terminal while inside the project directory.
