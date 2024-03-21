# pickembot

Pick'em is a Discord bot that creates and manages sports pick'em games.  After setup and initialization, a game runner can use a command to post games/contests from a selected sport and period.  Each game/contest will send a separate message with buttons for each team/competitor.  Users can select a winner for each game/contest by selecting the appropriate button.  The buttons will lock automatically when the game is scheduled to start.  Users can view their selections by clicking the "check" button on any game or by using the /(sport)picks.  When games are completed, the game runner can use the /update(sport)scores to record the winners and update the leaderboard. 

**INVITE LINK**
https://discord.com/api/oauth2/authorize?client_id=1014165020294250496&permissions=2147871808&scope=bot

**SUPPORT SERVER**
https://discord.com/invite/QazedBBhUj

**CONTRIBUTE**
If you enjoy Pick'em bot, consider supporting me through the link below.  This will allow me to continue to pay for hosting and database access as well as developing more sports and games into the bot.
https://www.buymeacoffee.com/jb082005

**GAMES**
Pick'em currently offers contests for MLB, NFL, NBA, NHL, NCAAB, NCAAF and PGA!  More sports are added based on interest so join the support server and vote on what you want the next sport to be!

**COMMANDS**
The bot uses slash commands to interact with users.  

**ADMIN COMMANDS**: can only be used by someone with Administrator privileges. 

**/assign(sport)** - assign a game-runner role whose member(s) will be able to set up, run, and restart contests for given sport
  - **This needs to be completed before any games can be run!**


**GAME-RUNNER COMMANDS**: can only be used by someone with the game-runner role (established in /assign above)

**/setup(sport)** - initialize the setup for a given sport
  - game_channel: the channel where games/contests will post
  - notification_role (optional): the role that will be tagged when a set of games/contests has finished posting

**/lock(sport)** - manually lock buttons for games that have started. 
  - A recent update has rendered this unnecessary.  Each time a button (team) is selected, the bot checks if the game has begun.
    If it has, the game buttons will lock automatically and the pick will not count.

**/post(sport)** - posts games/contest for given sport
  - week: define a week number for which to post games (football only)
  - date: define a date or date range for which to post games in YYYYMMDD or YYYYMMDD-YYYYMMDD format (basketball only)
  - seasontype: define if week/date given is for preseason, regular season or postseason (defaults to regular season)
  - spread: T/F option if games will be scored by spread or by winners (defaults to False: score by winner)
  - group: select which group of games to post; options are conference, Top 25, or favorites.  (college sports)
  - conference: select which conference to post games by conference ID. (college sports) (the conference IDs can be found in the /(sport)conferences)

**/update(sport)scores** - updates all open games/contests that have completed.  Will update each embed and the leaderboard as well

**/reset(sport)** - will close ALL open contests, clear the leaderboard, erase all scores, begin a new game and post an empty leaderboard
  - confirmation: click "Yes" to confirm that you want to start a new game

**USER COMMANDS**: can be used by anyone in the server

**/help** - view a list of commands enabled by the bot

**/(sport)picks** - view your selections for games in given sport that haven't been scored yet.

**/(sport)score** - view your score for given sport

**/add(sport)favorite** - record your favorite team for given sport (college only)

**/remove(sport)favorite** - remove a favorite team from given sport (college only)

**/(sport)conferences** - view a list of conferences available for given sport (college only)
