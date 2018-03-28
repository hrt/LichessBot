# Lichess Bot
The game : http://lichess.org.

Using Javascript you can utilise the open source chess engine stockfish https://github.com/nmrugg/stockfish.js/blob/master/stockfishjs alongside websockets to have a fully automated bot that does not even need to be viewable on your screen (no mouse clicks etc) in around 40 lines of code.
Although I hope no one will actually use this against real players since it does ruin the game for everyone and you gain nothing from it.   
The only reason I started writing this was as procrastination for the advanced architecture exam I have in an hour today as well as because all the attempts that I saw on the internet achieve a lot less than this whilst using hundreds of more lines of code and silly dependencies! (You only need pure javascript).

[![demo](https://img.youtube.com/vi/6XTYFbyaXzE/0.jpg)](https://www.youtube.com/watch?v=6XTYFbyaXzE)

After the latest update it is fully automated (if you have tampermonkey).   Just give it a starting game and it will automatically start playing and find opponents after game end. 


# How to use
1. Get into a Lichess game
2. Open console (usually F12)
3. Copy paste ```lichess.js``` into the console.   NOTE: this part might take a few seconds to copy paste since the chess engine is in the code.
Optional : install tampermonkey and use this script directly to automatically inject instead of manual copy pasting into console

# Extra
You can easily customise the stockfish engine in my code to perform however you want it to (e.g. set mindepth or skill level parameters to increase/decrease elo.

# Todo
- [ ] Intercept Websocket receive events to capture FEN instead of using XML HTTP requests to stop refreshing of page to allow for consistent ultra bullet play.   Also update to have larger random (not so often) spikes of delays if this update is applied.

- [X] Bypasses anti-bot.   If you look at the source of Lichess you will notice that if you account for "inconsistent move times", "low accuracy", "no fast moves" and "don't always have advantage" you can evade all automated bot checks as long as you are not ban evading which is checked by IP, user agent and fingerprint

- [ ] ~~Add opening book to engine~~

- [ ] Use findings to update lichess anti cheat on Git?
