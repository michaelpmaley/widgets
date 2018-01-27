# HTML Widgets

A collection of HTML widgets.

## MLBScoreboard-MLBXML.html

* Simple :baseball: scoreboard with team logos, team records, runs per innings, runs, hits, errors
* Handles postponed games, extra innings, doubleheaders, and no game
* Adding the SVG logos is an excercise left to the reader

![MLBScoreboard MLB with XML](https://github.com/michaelpmaley/widgets/MLBScoreboard-mlbxml.png)

### Action Items

* [ ] Retest with live data when the new season starts
* [ ] Finalize game status, e.g. "Yesterday" and warmup states
* [ ] Maybe use "?EXT=" + today.getTime() at the end of url to disable caching

### Issues

* Widget can't be directly embedded into Start.me homepage because of HTTP url
* Widget can't be hosted on Github, Dropbox, or GDrive due to mixed HTTPS/HTTP content

## MLBScoreboard-SportsFeedsJson.html

* Simple :baseball: scoreboard with team logos, runs per innings, runs
* Handles extra innings, doubleheaders, and no game
* Line 4 requires your generated SportsFeeds authorization token
* Adding the SVG logos is an excercise left to the reader

### Action Items

* [ ] Redo with pending v2 API to get team record, hits, errors
* [ ] Retest with live data when the new season starts
* [ ] Finalize game status, e.g. postponed and warmp

### Issues

* Postponed games are absent from results instead of being marked postponed
* Accept-Encoding: gzip with Javascript XMLHTTPRequest shows an error in the Firefox debugger
* v1.1 API scoreboard endpoint team= parameter is not working
* v1.1 API scoreboard endpoint response does not contain Hits, Errors, nor cumulative team record
* v1.1 API game_boxscore endpoint can't be called on its own because with gameId=YYYYMMDD-away-home the caller has to know which two teams are playing and which is away and home
* v1.1 API game_boxscore endpoint response Wins and Losses does not appear to be cumulative team record up to/including the game in question
