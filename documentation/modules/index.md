---
layout: docs
currentpage: modules
---

# Modules

- [Modules](#modules)
    - [Config.ini](#config-ini)
    - [Search](#search_engine)
    - [News](#news)
    - [Weather](#weather)
    - [Note Something](#note)
    - [Emails](#emails)
    - [Twitter](#twitter)
    - [Facebook](#facebook)
    - [Football](#football)
    - [Calendar](#calendar)
    - [Restaurants](#restaurants)
    - [Wikipedia](#wikipedia)
    - [Movies](#movies)
    - [System](#system)


<hr>

<a name="modules"></a>
# Modules

In this section, we will dive into the modules, or in simple terms, adding functionality to your virtual assistant, like hooking
your facebook, twitter, google, favorite football team, etc with Stephanie. Again each module has a separated sub-section dealing how to configure it,
and what kind of features it will bring into play.

<hr>

<a name="config-ini"></a>
### Config.ini file

All the configurations will go in the config.ini file under the tab [MODULES] present in it. Again configuring modules isn't compulsory,
so for instance if you're not a football fan, (what the hell man!) then there is no need to hook that in, but that will mean that you won't be able
to use certain commands related to football (that given module) which stephanie offers. There are also certain modules which doesn't require any
prior configuration to use them, like Wikipedia (Thank you Jimmy Wales!), IMDB and few others.

<hr>

<a name="search_engine"></a>
### Search Engine

The search engine, works just like how it sounds, you ask it some kind of question, and it responds with an answer, Stephanie uses
[Wolfaramalpha Search Engine](https://www.wolframalpha.com/){:target="_blank"} since it provides a public API, which anyone can use since it has a
free quota, of 2000 requests per month, which is quite sufficient to be honest.

##### Setting up

- Go to the [Developer Console](https://developer.wolframalpha.com/portal/signup.html){:target="_blank"}, and sign up for an account by
filling a simple form.

- After that there will be a button stating, "Sign up to get your first app ID", click that, after that it will redirect you to
same page, with a "get app id" button, press that, give your application some stupid name, with a description, just fill in anything there,
and press get app id, that will give you APPID: XXXXX-XXXXXXXXXXX just copy that, and paste into config.ini file like so:

        [MODULES]
        wolframalpha_search_engine_key = JH67HS-UGA621HJS6A

##### Test

**You** : Hey Stephanie, Do an alpha search, Which is the largest continent in the world?

**Stephanie** : The answer is Donald Trump.

<hr>

<a name="news"></a>
### NEWS

There is a news module present in Stephanie, which can be use to retrieve all kind of news such as latest, popular, etc, from
various sources all around the internet, to be specific around 73 sources provided here at [newsapi.org](https://newsapi.org/sources){:target="_blank"}.

##### Setting up

- Go to [Newsapi Signup Form](https://newsapi.org/register){:target="_blank"}, and sign up for an API key.

- This will show you a tab showing your API key just copy that and paste in the config.ini file like so.

        newsapi.org_key = 8f2918c0653kjahsd37y4ah95c8b1

##### Test

**You** : Hey Stephanie, Get me some news.

**Stephanie** : Would you prefer any specific category? If yes then what would it be?

**You** : Technology

**Stephanie** : Any preference you would like to have about source of your news?

**You** : Nah.

**Stephanie** : //Gives you top news from google news as default source.

<hr>

<a name="weather"></a>
### Weather

Weather module helps you to get weather updates and forecasts for the upcoming week and so from one of the awesome public API
named [OpenWeatherMap](https://openweathermap.org/){:target="_blank"}

##### Setting up

- Make sure you have filled in the city where you're located at in config.ini file under [USER] section, don't fill it with
your address or something, don't be stupid, just fill it with your city name.

- Go to (Sign up Form)[https://home.openweathermap.org/users/sign_up] to sign up for an account.

- After it, just write your company name : "lady_lowercase" (just kidding write whatever the thing you want.), and purpose, Save.

- Now go to the API keys [tab](https://home.openweathermap.org/api_keys){:target="_blank"}, copy that key, and paste it in config.ini file like so.

        open_weather_map_api_key = 7b9b999c28jkhg4jg2yj2l4jil2hce

##### Test

**You** : Hey Stephanie, How is the weather today?

**Stephanie** : Weather today at kanpur is sunny, There is a chance of rain. Now the temperature is 23 degree celsius, with .... blah blah.

<hr>

<a name="note"></a>
### Note something

You can use stephanie to note something for you using this module, it will sync with your [Evernote](https://evernote.com/) account, and help you to
note things on a fly.

##### Setting up

- Go to the [Developer Console](https://www.evernote.com/api/DeveloperToken.action){:target="_blank"} to get your developer token for production use,
(production use, so that it syncs with your actual existing Evernote account), click on "Create a developer token".

- That will give you your developer token, copy that and paste it in config.ini file like so :

        evernote_auth_token = S=s300:U=2f643c3:E=1625efe2085:C=15b0kjahsd7a58:P=1cd:A=en-devtoken:V=2:H=85122627d1fdkhad7adihgaid

##### Test

**You** : Hey Stephanie, Can you note something for me?

**Stephanie** : What would you like me to write down?

**You** : I HATE WRITING DOCUMENTATIONS, I like to program not write these documentations! Most boring job ever, but one of the most important ones so yeah. :/

<hr>

<a name="emails"></a>
### Emails

You can read the unread emails sent to you by syncing your [Gmail](https://mail.google.com/mail/){:target="_blank"} account with Stephanie in as little as couple of steps.

##### Setting up

- (Look I am really busy with assignments and books and whatnot, so I couldn't implement oauth verification, so bare with me on this one.)

- You need to provide your gmail address and password in the config.ini file to enable this feature, again config.ini file should never be shared and must stay with you all the time.

        gmail_address = my_password_turns_into_stars@gmail.com
        gmail_password = hunter123

##### Test

**You** : Hey Stephanie, do I have any unread emails?

**Stephanie** : You have 1 unread email, they are as follows : user verifiedson from reddit has broken his arms and is requesting for your help, by interestingfamily@gmail.com

<hr>

<a name="twitter"></a>
### Twitter

Sync your [Twitter](https://twitter.com/){:target="_blank"} account to post tweets, get notifications and much more by simply hooking it up with your API tokens using
the steps listed below.

##### Setting up

- Go to [Application Management](https://apps.twitter.com/){:target="_blank"}, and create a new app, it will ask for some details like name, description
and so on, just fill it up with some random stuff, for website again, just put anything there, while leaving the callback url section empty.

- Now this will redirect you to a section, showing bunch of details, click on Access level's modify app permissions and select
read, write and access direct messages to get full hold of your account, update settings.

- Now go to keys and access tokens tab, there you'll find consumer key and consumer secret, but we need two more stuffs, for that
scroll down to Your access token section, and create access token.

- After that just copy consumer key, consumer secret, access token and access token secret, and fill it accordingly in config.ini file, like so ;

        twitter_consumer_key = x0thyGfcT2v3k08jgEJmI128e
        twitter_consumer_secret = oN0qv3WNG5T6MQHSHD7AD7AKDH8fpZQB2kXrg1rOpTc6aUzR
        twitter_access_token = 396469661-eeT6lAiTJHADAJH72vst2kPmsPybRhSgL3x2q
        twitter_access_token_secret = weQFSwKLAJDIAJ87ADxkqXUTvC74wK4dkOlrAXVprFt

#### Test

**You** : Hey Stephanie, I wanna tweet something on twitter.

**Stephanie** : What would you like to tweet?

**You** : I just found out this virtual assistant called stephanie, and I have already fallen in love.

**Stephanie** : (blushes) "What you tweeted" has been tweeted.

<hr>

<a name="facebook"></a>
### Facebook

Well if we're talking about social medias then who can forget the heavy influence of facebook around it, you can easily sync your
[Facebook](https://www.facebook.com/){:target="_blank"} account to get facebook related information, though the entire process is probably the hardest among all of the other modules. Don't look at me, it's the facebook's way to validate user. But fear not, I've written it's exact way and it will take not more than 1 minute to set it all up.

##### Setting up

- First thing first, you'd need an account in [Developers Facebook](https://developers.facebook.com/){:target="_blank"}, it's easy as pie.
- Now click on my apps present in the top bar towards right hand corner, and then add a new app.
- Now give your app a name, How about, "Stephanie Virtual Assistant", and then create the app, This will now lead you to your app's main page, look for dashboard section in the sidebar, over there you'll see App ID and App Secret.
- Copy both of them and paste it in config.ini file like so:

        facebook_app_id = 1927910726401696
        facebook_app_secret = e00ce143d4352c36100775kajhd869ad5e9

- Now first part finished, leaving behind another step, after that stephanie will take care of anything by requesting for a long term access token.
- Now, Go to [Graph API Explorer](https://developers.facebook.com/tools/explorer/){:target="_blank"}, in the right hand side there will be a Graph API Explorer written with a popup menu, click it and select your given app that you just created.
- Now you can select Get Token > Get User Access Token, this will open up a modal asking which permissions you wanna allocate to your app. Now since this app is entirely yours, selecting everything wouldn't cost a dime but for now stephanie only offers two services, birthday reminders and status update, so you can choose them or all, I recommend all honestly for future updates on stephanie and since it's entirely open source. But you can just select all of user permissions.
- Now click on get access token, to get your access token, which will be filled in access token form, copy that and paste it in like so:

        facebook_access_token = EAACEdEose0cBABuCsc1GdSUemdHby6C1w2xZCA7MQhKBgedtQFq716vCNftKiO8JvrVu2NlD360aXPs63LpZC5wwrVjBMKTWi03khRtqWeqLkiwzGabOzBgXbUZAUISwWrs4mdD3w7rxrAUgiTdIZASbEWrcmqdEAeJUHUHcW3IT1kpN8kgxbZBIZBKODlwetgN3RDVxtpi1hzGAPDbnw4pqqAlrC9ZBtgZD

- And that's it congrats, facebook module will work properly now, and you can enjoy all of it's functionality as stephanie will handle the rest. (facebook_oauth_token is recieved by sending a request to graph api with app id, secret and this token to get a more permanent one which wouldnt expire in 30 mins like this one does.)

##### Test

**You** : Hey Stephanie, Do I have any facebook notifications?

**Stephanie** : Yes you have 1 notification. HufflyPuffy has commented in your profile picture, why do you never smile UG?

<hr>

<a name="football"></a>
### Football

FINALLY! YES! you can get all the football updates, like latest news, fixtures, team information, league tables and much more with
Stephanie using this amazing public API [football-data.org](http://www.football-data.org/index){:target="_blank"} and also some minimal information from
[Sportsmole](http://www.sportsmole.co.uk/){:target="_blank"}.

- Go to [register form](http://www.football-data.org/client/register){:target="_blank"} and register for an API key, but do it only if you are interested
in football, the guy who made that website is awesome and is delivering this entire API for completely free.

- Click on get free api key, and check your email, you will get a mail with API token, copy that and paste it in config.ini file like so :

        api.football.org.key = 05d52d8812a548c6a9f6f29ed60e8e00

- Football module is huge and requires a configuration on your favorite team, league and so on, in order to make use all of that,  head to [Resources](/stephanie/documentation/resources/football).

##### Test

**You** : Hey Stephanie, I need some football information.

**Stephanie** : What would you like to know about?

**You** : Spanish League

**Stephanie** : What would you like to know about of La Liga? latest news? league table? blah blah..

**You** : Get me the league table

**Stephanie** : The league table of la liga is as follows : Real Madrid at 1st position, ..., Barcelona at 20th position. (suck it barca fans) Would you like to know anything more information?

**You** : Nah.

<hr>

<a name="calendar"></a>
### Calendar

You can set up dates, and get reminders accordingly by syncing your google calendar with stephanie using these steps.

##### Setting up

- Go to [Google Developer Console](https://console.developers.google.com/apis/api/calendar-json.googleapis.com/overview){:target="_blank"} over there
click on to create a project, give it some name and create it.

- now press on Enable button to enable calendar API, after that click on create credentials. select web based application for
where you'll be calling the API from, and user data for what data you will be accessing.

- Now copy your client ID and client secret to paste it in config file accordingly.

        google_calendar_client_id = 633640441985-h70ljc5cks51ufcc6i0fin9jb7kv09ou.apps.googleusercontent.com
        google_calendar_client_secret = 92xll41lWUqCd0TYEImRFeGr

##### Test

**You** : Hey Stephanie, Add a calendar event.

**Stephanie** : What would you like to add?

**You** : Movie with HufflyPuffy Friday at 6 pm.

**Stephanie** : Movie with HufflyPuffy on May 17 at 6:00 pm, is this what you mean?

**You** : yeah.

**Stephanie** : Okay the event is added to your calendar.

<hr>

<a name="restaurants"></a>
### Restaurants

You can let Stephanie find restaurants for you with this given module and sparing you from the endless trouble of picking the correct place to eat food.

##### Setting Up

- Go to [Zomato API](https://developers.zomato.com/api){:target="_blank"}, scroll down the page and click on Generate API Key, Sign up for an account.

- Get the API key, copy it and paste it in your config.ini file as follows:

        zomato_api_key = e74778cd3728858df3578092ecea0jahd7y7232cf

- Make sure you have correctly filled in your city information in the [USER] section as well, like so:

        city = kanpur
        state = Uttar Pradesh
        country = India
        zipcode = 208001

##### Test

**You** : Hey Stephanie, I am feeling quite hungry.

**Stephanie** : Starbucks situated nearby Rest Fruit Street is found, it offers cuisine like coffee, ice-cream, snacks, and many more with an average
price range of around 10-15$ and over 560 people have rated this place with average ratings of 4.5. So would you like to order this place?

**You** : Yes.

**Stephanie** : // opens the browser with the webpage of that location, with contact number, directions and  many other information present in it.

<hr>

<a name="wikipedia"></a>
### Wikipedia

[Wikipedia](http://www.wikipedia.org/){:target="_blank"} doesn't requires any kind of configuration, thanks to my man, Jimmy Wales, since they provide a completely
free public API without any API token required for light uses.

<hr>

<a name="movies"></a>
### Movies

Similarly Stephanie also comes up with a movies module to take care of retrieving any kind of information about movies without
any prior setup required.

<a name="system"></a>
### System

Stephanie offers a basic system module, which tackles some of the basic systematic options. Again no prior setup is needed for this module to work out of the box.

**Now let's movie to the [usage](/stephanie/documentation/usage){:target="_blank"} section to get a look at all the functionality provided by
various modules of stephanie, and How to use them.
