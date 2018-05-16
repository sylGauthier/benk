# koneb1
CLI flashcard program entirely written in bash

*This program requires the color.sh script in your PATH*

https://github.com/fx-carton/bash-scripts

koneb1 is a (tentatively) suckless approach to flach card learning. It uses the
Leitner system for an optimized learning schedule.

The cards are simple text files containing the content of the front face, back
face and the date at which it was lastly seen (the date is in number of days
since 1970-01-01 for convenience).

The boxes are folders inside the deck. The boxes' name is the number of days for
the learning interval. You can add or remove boxes and change their names to
your convenience, but there should always be a box 0 for new cards. The script
will automatically select cards that need to be learn at the current date and
upgrade them to the next box if they are known, or downgrade them to the lowest
non-zero box.

All decks are stored in the CARD_DIR environnement variable which defaults at
$HOME/cards.

To create a new deck, simply run:

    koneb1 new <deck_name>

To add cards to a deck, run:

    koneb1 add <deck_name>

To train on a deck, run:

    koneb1 train <deck_name>

You can search for keywords in all your cards in a given deck by running:

    koneb1 search <deck_name> <keyword>
