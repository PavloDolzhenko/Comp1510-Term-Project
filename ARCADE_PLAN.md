# My arcade plan

## Games I chose

- Game 1: Higher or Lower — difficulty: (copy from the list)
- Game 2: Rare Find (my own design, based on Krillion) — difficulty: assigned by instructor

## Game 1: Higher or Lower

- Rules, in a few sentences: The game uses a normal 52-card deck that is
  shuffled at the start. One card is shown face up. The player guesses whether
  the next card will be higher or lower than the shown card. Aces are low
  (Ace = 1) and Kings are high (King = 13). Suits do not matter. If the next
  card has the same rank, the guess counts as wrong.

- What one turn looks like: The game shows the current card, for example
  "7 of Hearts". The player types "h" for higher or "l" for lower. Any other
  input gets a friendly message and the question again. The game shows the
  next card and says if the guess was right. If it was right, the new card
  becomes the current card.

- How it ends (win, lose, or out of turns): The game ends when the player makes
  a wrong guess, or when the deck runs out of cards.

- How a score is earned (the formula or rule, and why higher is better): The
  player gets 10 points for each correct guess in a row. Score = correct
  guesses × 10. More correct guesses means a higher score, so higher is better.

- Game settings: one 52-card deck, Ace = 1 and King = 13, a tie counts as
  wrong, 10 points per correct guess, up to 51 guesses.

## Game 2: Rare Find

- Rules, in a few sentences: The game asks 7 questions. Each question has many
  correct answers. For example: "Name a planet in our solar system." Each
  correct answer is worth a different number of points. Common answers that
  most people think of are worth fewer points. Rare answers are worth more
  points. A wrong answer is worth 0 points. The player picks a smart answer
  that is correct but not too obvious.

- What one turn looks like: The game shows the question number and the
  question. The player types one answer. The answer is checked without caring
  about capital letters or extra spaces. The game says if the answer was
  correct, how many points it was worth, and shows the rarest answer the
  player could have given. Then the next question starts.

- How it ends (win, lose, or out of turns): The game ends after all 7
  questions are answered. There is no losing early.

- How a score is earned (the formula or rule, and why higher is better): Every
  correct answer has a point value from 1 (very common) to 10 (very rare). The
  score is the total points from all 7 questions. The highest possible score
  is 70. Rarer correct answers give more points, so higher is better.

- Game settings: 7 questions per game, picked at random from a bank of at
  least 15 questions. Each question has at least 5 correct answers. Points per
  answer go from 1 to 10, and a wrong answer is 0. One try per question.

## Scoreboard fields

I am keeping the default layout. Every finished game stores the player's name
and their score. The game's module name is the key, so it identifies which
game the record belongs to.

    {
      "higher_or_lower": [
        {"player": "Pavlo", "score": 60}
      ],
      "rare_find": [
        {"player": "Pavlo", "score": 42}
      ]
    }

## My own game (optional)

Name: Rare Find. It fills the Game 2 slot. It is based on the trivia game
Krillion (https://krillion.io/). It fits the contract because play(player_name) runs one full game
of 7 questions and returns the total points as a nonnegative int (0 to 70).
Higher is always better. It never touches the scoreboard file and never calls
exit(). It ends only by returning the score.