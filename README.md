# pickembot

Pick'em is a Discord bot that creates and manages sports pick'em games.  After setup and initialization, a game runner can use a command to post games/contests from a selected sport and period.  Each game/contest will send a separate message with buttons for each team/competitor.  Users can select a winner for each game/contest by selecting the appropriate button.  The buttons will lock automatically when the game is scheduled to start.  Users can view their selections by clicking the "check" button on any game or by using the /mypicks command.  When games are completed, the game runner can use the /update command to record the winners and update the leaderboard. 

**INVITE LINK**
https://discord.com/api/oauth2/authorize?client_id=1014165020294250496&permissions=2147871808&scope=bot

**SUPPORT SERVER**
https://discord.com/invite/QazedBBhUj

**CONTRIBUTE**
If you enjoy Pick'em bot, consider supporting me through the link below.  This will allow me to continue to pay for hosting and database access as well as developing more sports and games into the bot.
https://www.buymeacoffee.com/jb082005

**FREE SPORTS**
Pick'em currently offers free contests for MLB, NFL, NBA, WNBA and NHL!

**FREE GAMES**
Pick'em bot includes capability to run a March Madness bracket contest!

**PREMIUM**
Upgrade your server to access additional sports and game modes!  NFL has two premium modes: Survivor and Locks.  Survivor is an eliminator game where users select one team each week to win. Each team can only be used once during the season and if your team loses, you're out!  Locks is a pick'em style game where you can select as many teams as you'd like each week, but you only score if every team you selected wins!

Also included in premium is a Bet module - submit and take sides on custom bets within Discord. Set a time for the bet to lock and use a command to update it with the winner.  Each server has a custom leaderboard that will track scores.

NCAAM, NCAAW, NCAAF, Soccer, ATP, WTA, MMA, and PGA are currently on the premium tier, but more sports will be added based on interest. Join the support server and let me know what you want the next sport to be!

**COMMANDS**
The bot uses slash commands to interact with users.  

**ADMIN COMMANDS**: can only be used by someone with Administrator privileges. 

**/assign_role** - assign a game-runner role whose member(s) will be able to set up, run, and restart contests for given sport
  - **This needs to be completed before any games can be run!**


**GAME-RUNNER COMMANDS**: can only be used by someone with the game-runner role (established in /assign above)

**/setup** - initialize the setup for a given sport
  - game_channel: the channel where games/contests will post
  - notification_role (optional): the role that will be tagged when a set of games/contests has finished posting

**/lock** - manually lock buttons for games that have started. 
  - A recent update has rendered this unnecessary.  Each time a button (team) is selected, the bot checks if the game has begun.
    If it has, the game buttons will lock automatically and the pick will not count.

**/post** - posts games/contest for given sport
  - date: define a date or date range for which to post games in YYYYMMDD or YYYYMMDD-YYYYMMDD format (basketball only)
  - seasontype: define if week/date given is for preseason, regular season or postseason (defaults to regular season)
  - spread: T/F option if games will be scored by spread or by winners (defaults to False: score by winner)
  - group: select which group of games to post; options are conference, Top 25, or favorites.  (college sports)
  - conference: select which conference to post games for.
  - tag: select if you want to tag the notification role after games are posted (defaults to True)

**/update** - updates all open games/contests that have completed.  Will update each embed and the leaderboard as well

**/reset** - will close ALL open contests, clear the leaderboard, erase all scores, begin a new game and post an empty leaderboard
  - confirmation: click "Yes" to confirm that you want to start a new game

**USER COMMANDS**: can be used by anyone in the server

**/help** - view a list of commands enabled by the bot

**/helpmm** - view more help with March Madness

**/mypicks** - view your selections for games in given sport that haven't been scored yet.

**/myscore** - view your score for given sport

**/addfavorite** - record your favorite team for given sport (college only)

**/removefavorite** - remove a favorite team from given sport (college only)

**/conferences** - view a list of conferences available for given sport (college only)

**/leaderboard** - view a leaderboard for your server that totals all active sports.
