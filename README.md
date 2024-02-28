# dnd-action-cards

A set of [nanDECK](https://www.nandeck.com/) scripts to generate various cards
for [Dungeons and Dragons](https://www.dndbeyond.com).

# Table of contents

* [Intro](#intro)
* [Current status](#current-status)
* [Future plans](#future-plans)
* [Credits](#credits)

## Intro

[D&D](https://www.dndbeyond.com) can easily be complicated for
a new player, especially when it comes to creating characters and figuring out
all the attack and damage bonues from weapons and spells.

Of course, there are many tools to automate that, including ones which track HP
(hit points) of characters and enemies and automatically throw dices. However,
use of those tools inevitable leads to players being distracted merely by
presence of an electronic device such as a smartphone, tablet, or a laptop. This
happens even if players are located on the same table in the very same room.

I recently had an experience of running a D&D game as a DM for new players and
I decided to make a small reference cards which would help them with actions
available to their characters in combat encounters (at least).

What I currently have is some cards made in Pages macOS app, which are simple
rounded rectangles with text in them (aligned using empty lines of different
line height, yay!). The look like this: ![image](https://github.com/AlexeySachkov/dnd-action-cards/assets/6417047/e99078ff-8c46-4598-b7cc-6560b160a1f4)

They are not really big (56 x 89 millimiters), because I was aiming for
[Wingspan](https://boardgamegeek.com/boardgame/266192/wingspan) cards size which
I have [sleeves](https://www.rykergames.com/products/wingspan-card-sleeve-kit)
for.

So, I just made a bunch of those cards for each party member, printed them, cut
them out and sleeved. The result is quite good and they turned out to be pretty
useful during the game.

![IMG_6490 Large](https://github.com/AlexeySachkov/dnd-action-cards/assets/6417047/52ced16d-4242-4c62-b530-ebce52067b34)

_Left to right: original cards I did (scale was screwed up during printing),
a version using a better printer (and the correct scale),
a version produced by this script (not the latest one of course)_

Going forward, we have decided to continue playing with that party for at least
a few more sessions and characters are going to level up and change slightly.
They were originally pre-made by me, but now I'm allowing players to make
changes according to their preferences, including class changes (which wouldn't
be necessary at all if not for mistranslation/miscommunication).

Anyway, I decided that doing those cards in a text editor is a pain and I would
like to automate it somehow. Spent some time googling various editors, but ended
up with [nanDECK](https://www.nandeck.com/) (who even cares about the result,
when you can **code** your cards?!).

This repo is intended to contain all the code and inputs I have for the deck I
will create with this tool. As you may have guessed, the deck may never be
complete, but at least for now it is fun digging into the docs and writing
some code. [Automation](https://xkcd.com/1319/).

## Current status

The project features two decks at the moment:
- [weapons deck](decks/weapons-deck.txt) which is capable of generating cards
  for all non-magical weapons available in [SRD][srd] and custom magic weapons.
- [armor deck](decks/armor-deck.txt) which is capable of generating cards for
  all non-magical armor available in [SRD][srd].

Both decks use a character data as an input and tailor generated cards to that
character. This includes automaticaly calculating all attack and damage bonuses,
automatically calculating armor class and filtering cards to only generate cards
for those items, which are present in a character's inventory.

See example of a ["character sheet"](data/Orianna.csv) and of a
[character inventory](data/Orianna-inventory.csv).

[srd]: https://dnd.wizards.com/resources/systems-reference-document

## Future plans

In no particular order:

* See all `TODO`s there are in the scripts
* Instructions on how to use those scripts
* Instructions on how to customize them for your needs
* Documentation on `.csv` files format
* Customization options for cards (like no dice icons, different card size)
* Support for feats (racial, class, etc.)
* Support for magic items
* Support for spells

## License

Documentation and source code for `nanDECK` scripts is licensed under
[MIT License](LICENSE).

However, the repo contains some 3rd-party assets which may be licensed
differently. Their license and credits are noted in
[`assets/README.md`](assets/README.md).

This work includes material taken from the System Reference Document 5.1
(“SRD 5.1”) by Wizards of the Coast LLC and available at
https://dnd.wizards.com/resources/systems-reference-document. The SRD 5.1 is
licensed under the Creative Commons Attribution 4.0 International License
available at https://creativecommons.org/licenses/by/4.0/legalcode.

The statement above is related to [`data/`](data/) folder that includes
information from the SRD 5.1 (like weapons and armor stats). That folder also
contains user-created content (like custom magic items) and that content is
licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/legalcode).
