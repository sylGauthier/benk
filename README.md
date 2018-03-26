# koneb1
CLI flashcard program entirely written in bash

koneb1 is a (tentatively) suckless approach to flach card learning. It uses the Leitner system for an optimized learning schedule.

The cards are simple text files containing the content of the front face, back face and the date at which it was lastly seen (the date is in number of days since 1970-01-01 for convenience.

The boxes are simply folders inside the deck. All decks are stored in the CARD_DIR environnement variable which defaults at $HOME/cards.

To create a new deck, simply run:

    koneb1 new <deck_name>

To add cards to a deck, run:

    koneb1 add <deck_name>

To train on a deck, run:

    koneb1 train <deck_name>
