---
layout: resources
currentpage: football
---

# Football Module

- [Football Modules](#football-module)
    - [Configuration](#configuration)
        - [Team Table](#team-table)
        - [Instructions](#instructions)
    - [Features](#features)
    	- [Leagues and Competitions](#competitions)
    		- [Commands](#commands)
    - [Usage](#usage)
		- [Triggering Football Module](#football-module)
		- [Available Responses](#available-responses)
			- [Competitions](#competitions-usage)
			- [Teams](#teams-usage)

<hr>

<a name="football-module"></a>
# Football Module

Due to the complexity of this given module, I thought it'd be better to devote an entire page to let you know about all the features it offers. Configuration and Usage
are also available below to let you gain a solid understanding of the given module.

<hr>

<a name="configuration"></a>
## Configuration
First of all in order to use Football Module, it's strongly recommended to fill in your favorite id and name from the given table listed below to enjoy all the features
available to you by this given module.

**Note** : If you can't find your favorite team in the given table listed below, head to the features section to know 
more insight about it.

<hr>

<a name="team-table"></a>
### TEAM TABLE

| Official Name | ID | NAME |
| ------------- | --- | ----- |
| Hull City FC | 322 | hull-city |
| Leicester City FC | 338 | leicester-city |
| Southampton FC | 340 | southampton |
| Watford FC | 346 | watford |
| Middlesbrough FC | 343 | middlesbrough |
| Stoke City FC | 70 | stoke-city |
| Everton FC | 62 | everton |
| Tottenham Hotspur FC | 73 | spurs |
| Crystal Palace FC | 354 | crystal-palace |
| West Bromwich Albion FC         | 74 | west-brom-albion |
| Burnley FC | 328 | burnley |
| Swansea City FC | 72 | swansea-city |
| Manchester City FC | 65 | man-city |
| Sunderland AFC | 71 | sunderland |
| AFC Bournemouth | 1044 | bournemouth |
| Manchester United FC | 66 | man-united |
| Arsenal FC | 57 | arsenal |
| Liverpool FC | 64 | liverpool |
| Chelsea FC | 61 | chelsea |
| West Ham United FC | 563 | west-ham-united |
| FC Bayern Munchen | 5 | bayern-munich |
| Werder Bremen | 12 | werder-bremen |
| FC Augsburg | 16 | augsburg |
| VfL Wolfsburg | 11 | wolfsburg |
| Borussia Dortmund | 4 | borussia-dortmund |
| 1. FSV Mainz 05 | 15 | mainz-05 |
| Eintracht Frankfurt | 19 | eintracht-frankfurt |
| FC Schalke 04 | 6 | schalke-04 |
| Hamburger SV | 7 | hamburger-sv |
| FC Ingolstadt 04 | 31 | fc-ingolstadt-04 |
| 1. FC Koln | 1 | koln |
| SV Darmstadt 98 | 55 | sv-darmstadt |
| Bor. Monchengladbach | 18 | borussia-monchengladbach |
| Bayer Leverkusen | 3 | bayer-leverkusen |
| Hertha BSC | 9 | hertha-berlin |
| SC Freiburg | 17 | freiburg |
| TSG 1899 Hoffenheim | 2 | hoffenheim |
| Red Bull Leipzig | 721 | rb-leipzig |
| SC Bastia | 536 | bastia |
| Paris Saint-Germain | 524 | psg |
| AS Monaco FC | 548 | as-monaco |
| EA Guingamp | 538 | guingamp |
| FC Girondins de Bordeaux | 526 | bordeaux |
| AS Saint-Etienne | 527 | saint-etienne |
| SM Caen | 514 | caen |
| FC Lorient | 525 | lorient |
| Dijon FCO | 528 | dijon |
| FC Nantes | 543 | nantes |
| FC Metz | 545 | metz |
| OSC Lille | 521 | lille |
| Montpellier Hurault SC | 518 | montpellier-hsc |
| Angers SCO | 532 | angers |
| AS Nancy | 520 | nancy |
| Olympique Lyonnais | 523 | lyon |
| OGC Nice | 522 | nice |
| Stade Rennais FC | 529 | rennes |
| Olympique de Marseille | 516 | marseille |
| Toulouse FC | 511 | toulouse |
| Malaga CF | 84 | malaga |
| CA Osasuna | 79 | osasuna |
| RC Deportivo La Coruna | 560 | deportivo-la-coruna |
| SD Eibar | 278 | eibar |
| FC Barcelona | 81 | barcelona |
| Real Betis | 90 | real-betis |
| Granada CF | 83 | granada |
| Villarreal CF | 94 | villarreal |
| Sevilla FC | 559 | sevilla |
| RCD Espanyol | 80 | espanyol |
| Sporting Gijon | 96 | sporting gijon |
| Athletic Club | 77 | athletic-bilbao |
| Real Sociedad de Futbol | 92 | real-sociedad |
| Real Madrid CF | 86 | real-madrid |
| Club Atletico de Madrid | 78 | atletico-madrid |
| Deportivo Alaves | 263 | alaves |
| RC Celta de Vigo | 558 | celta-vigo |
| CD Leganes | 745 | leganes |
| Valencia CF | 95 | valencia |
| UD Las Palmas | 275 | las-palmas |
| AS Roma | 100 | roma |
| Udinese Calcio | 115 | udinese |
| Juventus Turin | 109 | juventus |
| ACF Fiorentina | 99 | fiorentina |
| AC Milan | 98 | ac-milan |
| Torino FC | 586 | torino |
| AC Chievo Verona | 106 | chievo-verona |
| FC Internazionale Milano | 108 | inter-milan |
| Empoli FC | 445 | empoli |
| UC Sampdoria | 584 | sampdoria |
| Genoa CFC | 107 | genoa |
| Cagliari Calcio | 104 | cagliari |
| Bologna FC | 103 | bologna |
| FC Crotone | 472 | crotone |
| US Citte di Palermo | 114 | palermo |
| US Sassuolo Calcio | 471 | sassuolo |
| Pescara Calcio | 585 | pescara |
| SSC Napoli | 113 | napoli |
| Atalanta BC | 102 | atalanta |
| SS Lazio | 110 | lazio |

<hr>

<a name="instructions"></a>
### Instructions

Let me show you first hand, how to go about configuring this module in case you are still kind of confused with this toy example.

- First pick your favorite team, you can use **CTRL+F** to use inbuilt search option of the browser to track your favorite team, in my case it's Real Madrid,
so find the row containing real madrid as follows:

        | Real Madrid CF | 86 | real-madrid |

- What we need out of this row are ID and NAME, so copy them and paste it in your config.ini file like so.

        favorite_football_team_id = 86
        favorite_football_team_name = real-madrid

- In order to use news section of this module, enter the various other configs as well like so. The available options are as follows:  premier-league, championship, league-one, league-two, la-liga, bundesliga, serie-a.

        favorite_football_competition_name = premier-league

**Note :** Using `favorite_football_team_name` and `favorite_football_competition_name` is used by getting information from sportsmole website, so using it entirely your decision and I don't have any warrany on it's usage, So use at your own decision.

And well to be honest, that's it. You have successfully configured the football module. Now let's head straight into the features section.

<a name="Features"></a>
# Features
In this section, we will discuss about all the features that this module offers so to get you an overview of it.

<a name="competitions"></a>
## Leagues And Competitions
Stephanie currently offers a total of 13 competitions/leagues from european football as follows:

1. Premier League (English League)
2. Championship (English Second League)
3. Bundesliga (German League)
4. Bundesliga 2nd (German Second League)
5. Ligue 1 (French League)
6. Ligue 2 (French Second League)
7. La Liga (Spanish League)
8. La Liga Segunda (Spanish Second League)
9. Primeira Liga (Portuguese League)
10. Serie A (Italian League)
11. Eredivisie (Netherlands League)
12. DFB-Pokal (German Cup)
13. Uefa Champions League (Champions League)

**Note** Take a look at the phrase listed between parantheses above, those are the keywords which trigger the given league.

### Teams

Stephanie offers team information of almost every team present in the given competitions but to shorten down the list, 
I showed the team information of top 5 leagues of european football above, so in case you can't find your favorite league in the table shown above, just contact me through any of the social media links through pm in facebook, post/comment in reddit, question in quora or whatever, and I will get you your team id and name as follows.

<a name="commands"></a>
## Commands

So with stephanie in general, this football module can do these given tasks quite efficiently, Anything written between parantheses are the examples and not the actual phrases for you to use, leave that for the usage section.

- League
	- League Specific News (top news of premier league)
	- League Specific Table (league table of premier league)
	- League Specific Next Fixtures (next matchday fixtures of premier league)
	- League Specific Previous Results (previous/current matchday results of premier league)
- Team
	- Team Specific News (top news of real madrid)
	- Team Specific Injury News (injury updates of real madrid players)
	- Team Specific Transfer Talk (Transfer rumours and headlines surrounding real madrid)
	- Team Specific Players (Squad of real madrid)
	- Team Specific Next Fixtures (next fixtures of real madrid)
	- Team Specific Previous Results (previous/current results of real madrid)
- News
	- Latest News (Get latest news from the entire world football)
- Coming Soon (don't know it should be present here or not? \('_')/)
	- Stats (beta phase)
	- Live Commentary (beta phase)
	- More competitions

<a name="usage"></a>
#Usage

Usage of football module is pretty simple to be honest, as soon as the football module is triggered, it 
acts as a new source of program which takes in your various commands and acts accordingly.

<a name="football-module"></a>
## Triggering Football Module

In order to trigger football module, all you need to do is say any command which has "Football" and "Information" attached to it, for instance, "Can I have some football information?", "Hey Stephanie give me some football information". After that stephanie will respond by asking which kind of information you seek?

<a name="available-responses"></a>
### Available Responses

Anything written inside paratheses are the keywords that your command should have inorder to trigger that 
functionality. for instance ("English", "League"), your command should be like: "How about english league?"

The reason why I used the native words like english, german, italian and so on was because of the fact that STT doesn't works too well in languages other than english, for example : La Liga, Serie A, Bundesliga, they are really hard to pick and hence native words are used since they are so effective.

- Get all competitions available ("all", "competitions")
	- Results in giving information about all the competitions available to explore with stephanie.
- Get Premier League ("english", "league")
- Get Championship ("english", "second", "league")
- Get Bundesliga ("german", "league")
- Get 2.Bundesliga ("german", "second", "league")
- Get Ligue 1 ("french", "league")
- Get Ligue 2 ("french", "second", "league")
- Get La Liga ("spanish", "league")
- Get Liga Segunda ("spanish", "second", "league")
- Get DFB-Pokal ("german", "cup")
- Get Uefa Champions League ("champions", "league")
- Get Eredivisie ("netherlands", "league")
- Get Primeira Liga ("portuguese", "league")
- Get Serie A ("italian", "league")
- Get Team Information ("team", "information")
	- Triggers a new module resulting in team information as listed in your config.ini file.
- Get news of all of the surrounding football world ("latest", "news")
	- Returns the currrent latest news in football world.

<a name="competitions-usage"></a>
#### Competitions

So after triggering one of the competition handles, like ("english", "league"), ("spanish", "league") or whatever, 
You can do lots of stuffs with it as per your command usage, and there are currently 4 commands given to you for your usage.

Stephanie will open the conversation by telling which league you selected and all kinds of commands available to you briefly. For example: "Get me the latest news."

- Get League Specific News ("get", "news")
	- Gets latest news about the selected league.
- Get League Specific Table ("get", "league", "table")
	- Gets league table (Points Table).
- Get League Specific Next Fixtures ("get", "next", "fixtures")
	- Gets next fixtures of the league (next matchday).
- Get League Specific Previous Results ("get", "previous", "fixtures")
	- Gets the results of the previous fixtures (last/current matchday)

After triggering and let's say after the completion of the latest news, stephanie will ask if you would like to know other information about this given league in which case you can use any of the commands listed above to go towards that function and if all you wanted was news, just say anything negative to get out of the module like. (No, Nevermind, Nah)

<a name="teams-usage"></a>
#### Teams

Team nested module can be triggered as using keywords like "team" and "information:", for example: "Hey stephanie, give me some team information",
You can again do lots of stuffs with it as per your command usage, and there are currently 6 commands given to you for your usage.

Stephanie will open the conversation by telling which team you selected and all kinds of commands available to you briefly. For example: "Get me the latest news."

**Note**: This section won't work unless you have configured your favorite team information configuration listed above in your config.ini file accordingly.

- Get Team News ("get", "news")
	- Get latest news revolving around your favorite club.
- Get Team Injury News ("get", "injury", "news")
	- Get injury updates about your players
- Get Team Transfer Talk ("get", "transfer", "talk")
	- Get some tasty, completely delusional transfer talks surrounding your club. (I hate rumors, Perez if only you could had fixed your fax machine.)
- Get Team Players ("get", "players")
	- Get information of your squad.
- Get Team Next Fixtures ("get", "next", "fixtures")
	- Again same shit, ain't gonna copy, paste.
- Get Team Previous Results ("get", "previous", "fixtures")
	- ... just piss off dude, you know it.

and again, (I am copy pasting) After triggering and let's say after the completion of the latest news, stephanie will ask if you would like to know other information about this given league in which case you can use any of the commands listed above to go towards that function and if all you wanted was news, just say anything negative to get out of the module like. (No, Nevermind, Nah)
