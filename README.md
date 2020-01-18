# Faire Play: The Harvest Festival

This is a live action role playing game. It’s like one of those murder mystery parties, except it doesn’t revolve around a murder, and you play as you enjoy any local [Renaissance Faire][ren-faire]!

*WARNING*: if you plan to play, do not read any of the documents in this repository! They will spoil the game for you!

# Playing

This game is designed for exactly 12 people: 11 players plus 1 game master known as The Bard.

## Players

This game is set up so that players only need to prepare minimally. In short, they need to:

* Read the character sheets (sent by The Bard) in advance
* Read the instructions (sent by The Bard) in advance
* Wear a costume befitting their character

Unfortunately, the game does not support adding or removing players without significant extra work that must be done by The Bard (or some other non-player). See [Developing and Modifying](#developing-and-modifying) for more information.


## The Bard

The Bard must spend a lot of time preparing the game, and will be present during the game to run it and ensure it goes smoothly. If you've run a murder mystery game or a tabletop RPG as a game master, the role will feel familiar.


### Preparations

In advance, The Bard must do several things.

Note: To play an unmodified game, everything is in the `published` directory. The `development` and `source` directories are only useful when modifying the game.

First and foremost, read through these instructions, the instructions document, and every character sheet and card. It's a lot, but a good sense of the game and what it has to offer is important for The Bard to have in mind.

Then, select a local Renaissance Faire to serve as your playing ground. Choose a date, and allow several hours for play.

Next, assign players to characters. There are certain restrictions if you want to use the game unmodified, and some suggestions:

* Chrysalis must be a woman
* Lux must be a woman
* Yates must be a woman
* Daniels must be a man
* Lordyn is referred to as a woman, but only superficially
* Daniels and Lordyn interact minimally

After assigning characters, send (usually via email) to each player:

* a copy of the instructions sheet
* a copy of the particular character sheet this person will player
* a copy of the cards sheet corresponding to that player

In the email, ask them to read all documents in advance, and to prepare their costume. Be sure to coordinate arrival at the Renaissance Faire you have selected.

Next, print out all the cards on cardstock and cut them out--the "cards" document has them all together and separated by character, so you will not need to print the per-player card sheets. Put each player's cards into a separate stack or bag, and keep the bonus cards separate--and labeled--for distribution by The Bard during the game. The bonus cards are not included in the player-specific documents, but you still need them to play!

Print out one instructions sheet for each player, and one copy of each character sheet (both work well double-sided).


### The day of the Faire

The Bard needs to bring:

* These instructions, for The Bard's use only
* A copy of each character sheet
* A copy of the instructions for every player
* Printed, cut, and organized cards on cardstock (this takes a while!)
* A pocket to hold bonus cards
* A working pen
* A good understanding of the game and each characters' goals
* A willingness to adapt
* A fitting costume

Players each need to bring only one thing:

* Their costume, which must include a pocket

But have them read the instructions sheet, which has more details.

One everyone has arrived in costume, distribute a copy of the instructions to everyone, then hand out each player's character sheet to that player only.

Have everyone re-read the instructions and their character sheets.

Then, get in character, for you are now The Bard. Introduce the game in your own words. Don't forget these points:

* Each person has a secret
* Each person has a clue that won't be known to most other people
* Each person has goals they want to accomplish--and this may keep you from achieving yours! Find your friends and foes.
* The game is mostly talking! Make deals, swap knowledge/favors/items, and use your abilities before the game ends!
* Players should refer to their character sheets and the Tips page whenever they need or want to!
* Pull people aside for secret conversations! Watch for other people having secret conversations!
* It's all about having fun!
* The game ends when The Bard says it ends--The Bard will announce the coming end 5-10 minutes before the game ends. Afterward, all will be revealed!

Answer any questions the players may have. Be sure to know the characters well enough that you may help them during the game.

Then begin!

During the game, be sure to have conversations in secret when necessary. It's The Bard's job to ensure people are engaged, but don't tip the balance of the game unless you truly think it will save someone's enjoyment. You may need to improvise, so just use your best judgment and don't overthink it. It's a game, but The Bard's word is law!

Keep tabs on how many goals players have left. When it seems like things are winding down (typically when all the easy goals are complete and some/many of the harder ones are done), or if it's getting late, give 5-10 minutes notice and end the game.

Meet up as soon as the game ends, possibly over drinks. Go around in a circle, and have everyone:

* Reveal your secret identity
* Reveal your Secret and your Clue
* Reveal what your goals were and whether you did them
* Share your favorite moment or event

Help fill in details when people forget to cover them, and encourage sharing fun stories and tangents along the way. Answer any questions players have, but don't steal any player's thunder!

And that's it! I sure hope you had fun!

Send me a message/GitHub issue to let me know how it went, open a GitHub issue with any suggestions or comments you might have--if I heard people played it, I'd sure feel encouraged to make more!



# Developing and modifying

The original source files are included so you may modify _Faire Play_ for your own needs!


## Getting started

The source files are written in rich text format (RTF) and should be editable in any word processor. I use macOS's TextEdit and Pages, though much of it was originally developed using [Markdown][markdown] and a text editor. You should download and install the [Fontin][fontin] typeface so your new documents use the right fonts. You will also need "Snell Roundhand" and "Zapfino" for the authentic and forged Penelope signatures, both of which are available on macOS. On other systems, replace them with comparable fonts.

The `development` directory has a few unfinished notes and ideas in Markdown format from early versions of this game.

There is also `connections.dot`, a [Graphviz][graphviz] file that shows the important connections between characters and concepts. This was the primary tool used for ensuring the game had enough interesting intrigue, content, and overlap between characters. It is somewhat difficult to edit and use. A Graphviz viewer is [available online][graphviz-online], which may be easier than installing Graphviz, and makes it easy to quickly compare different viewing modes.


## Making changes

I would recommend a development workflow similar to this: Update `connections.dot` with your changes, perhaps adding/removing characters and relationships between them. The differences between this and unmodified _Faire Play_ can act as your reference as you update everything else, typically player sheets and corresponding card sheets.

If you decide to modify the instructions on how to play, they are all in `instructions.rtf`. If you decide to modify the setting, background, or Common Knowledge, you will need to update every player sheet since this is copied on to each one.

Lastly, export your documents to PDF for printing.

If you find some other way of making changes is easier--do that instead!


## Basic structure

The game is made up of a few components:

### Characters

Each character has both a false apparent identity, and a hidden true identity. These are given at the beginning of each character sheet. This is also where players learn something of the events they will care about in the game.

Next comes Common Knowledge, which is known to all players and lightly describes the setting.

Street Knowledge is shared among players "in the know." There are two special phrases, one for acquiring black market magical goods, and one for black market documents. All characters think they know the right phrases, but those without a good reason to have accurate knowledge are instead given a mangled version of the true phrase.

All players have Goals that they will seek to accomplish, many of which preclude other characters from completing their goals. All characters must "stay out of trouble" because there are ways to be penalized after the game ends.

Each player has a Secret. Preventing this knowledge from falling into the wrong hands should help them, and letting it be revealed should impair them.

Each player has a Clue containing secret knowledge that most players will not have. This can be very valuable.

### Cards

Cards represent Abilities and Items, which are clearly specified on each kind along with reminders about how they are used. Most cards start out possessed by players, but The Bard must hold on to a few "Bonus" cards that are given out when certain goals are accomplished (e.g. for Mikael, Daniels, Chrysalis)

### Setting

The game has an explicit location and setting that is known by all players, but is very light on details. This is conveyed through the instructions read by The Bard combined with the Common Knowledge section on each player's character sheet.

The rest of the knowledge each player begins with is all given on their character sheet. Much about the slice of the world they will care about is given implicitly in the opening text that also conveys their false and true identities. Other character-specific knowledge is in the Street Knowledge, and more is in their Goals, Secret, and Clues.

There are a few events in the "recent past" that are implicit in the backstories of several different characters. Players who reconstruct what happened will have an advantage, as many of these events involve multiple playing characters.


## Suggestions

Keep a careful eye the number of connections a given character has. The more they need to accomplish, the harder that character will be to play, and the more they begin with (knowledge or items) the more leverage they will have in the game.

Try to make sure there is lots of overlap between characters--mingling is key to making the game fun.

Some goals should be easy--perhaps requiring only a single step--while others should require multiple steps. Players will have significantly more fun if they accomplish at least some of their goals. However, many goals can and do prevent other characters from achieving their goals. This competition makes the game more exciting.

Notice that every character has an apparent identity and a hidden true identity. Players are never told this, and it's fun for them to realize it as the game goes on--it's fun to disguise yourself while seeing through the deceit of others! This is probably something to preserve.

The names were originally chosen to be easy to remember by resembling the names of the corresponding players.

Don't worry about the accuracy of your "olde English." I certainly didn't, it just adds a bit of flavor.

Everybody will say "Princess Penelope" instead of "Priestess." I guess you could do something about that.

It would be cool to have standardized card sizes.

It would be nice to have an easier way to update the shared knowledge on each sheet.


# About

_Faire Play: The Harvest Festival_ was designed and written by me (Mike Solomon) for a birthday party in October 2018.

Unfortunately, I never wrote up instructions on how to run and modify the game until January 2020.

If I were to make one change to the game, it would be to have optional characters to be easier to play more or less than 11 players.


# License

_Faire Play: The Harvest Festival_ is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License][license], a copy of which can be found in the LICENSE file adjacent to this one. You may remix, adapt, and build upon Faire Play non-commercially, as long as you credit me and license your new creations under the identical terms. If you want to do something different, contact me!

[ren-faire]: https://en.wikipedia.org/wiki/Renaissance_fair
[markdown]: https://daringfireball.net/projects/markdown/
[license]: https://creativecommons.org/licenses/by-nc-sa/4.0/
[fontin]: https://www.exljbris.com/fontin.html
[graphviz]: https://www.graphviz.org/
[graphviz-online]: https://dreampuf.github.io/GraphvizOnline
