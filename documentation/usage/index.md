---
layout: docs
currentpage: usage
---

# Usage

- [Usage](#usage)
    - [Introduction](#introduction)
    - [Key Concepts](#concepts)
        - [Intent Recognition](#intent)
        - [Keywords](#keywords)
        - [Framework](#framework)
        - [Convention](#convention)
    - [Modules](#modules)
        - [Search](#search)
        - [News](#news)
        - [Weather](#weather)
        - [Note](#note)
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

<a name="usage"></a>
# Usage

This section will help you understand how to use Stephanie effectively and make the most out of it, We will start with some
basic rules to help you see how stephanie works, and some tips which will come handy in the future, and then we will head
straight into each module, explaining all of it's features and how to interact with them in general.

<hr>

<a name="introduction"></a>
### Introduction

Stephanie isn't an actual AI that can understand your emotions, or sarcasms (working on this part, let's see what happens ), It's
like jarvis not Ultron (we are safe.). This section will help you get somewhat an idea about how stephanie interprets your voice commands.

<hr>

<a name="concepts"></a>
### Key Concepts

Given below, we'll deal with some of the key concepts on which Stephanie works so that you can make the most use out of it.

<hr>

<a name="intent"></a>
#### Intent Recognition

Whenever you give any kind of command to stephanie, it goes to some of the amazing 3rd party services for STT, and translates it to
text form, now it separates all the somewhat unimportant words (articles, tenses) out of it, leaving behind only keywords (nouns, adjectives and so on) which
then it sends to an algorithm (I have recently published a paper kind of thing of it, have a look at it here at ->  , it contains lot more about internals about stephanie.)
which outputs the module which it should trigger in the end, and then it gets triggered and various kind of data is sent to it as well to do stuffs like
"Hey Stephanie, do an alpha search, 'What is the meaning of life?'".

<hr>

<a name="keywords"></a>
#### Keywords.

So how stephanie decides that which module to trigger is that each module has a certain set of keywords attached to it. The algorithm searches through
all of the modules keywords and calculate the probability of the text (your command) associated to a given module using the algorithm described above and
finally chooses the best one. So each module has some keywords which help it find the given module. For example: TwitterModule
has keywords as "Twitter" and "Notifications". So whenever you say any sentence which has twitter and notifications in it, this
gives a high probability to that module and it gets selected.

**Note** : In order to make it efficient you could also try saying
twitter and no notifications and it will still pick that module, because of the way that algorithm is built. It uses some concepts like metaphones, munnkres algorithm and levenshtein principle. I highly recommend all the people who are interested to see how algorithm works to take a look here :->
And I have set it up as a package hosted in github so you can use it out of the box for your own application. It's use isn't limited to
this stephanie only, since it's used at various places in the module logic too to just do basic searching.

<hr>

<a name="framework"></a>
#### Framework

Stephanie can be used as a framework for developers to create their own versions of virtual assistant by adding their own modules since
each module provides all the functionalities of the actual application such as speaking, listening, deciphering, understanding intent,
making submodules inside module, Football module works exactly that way because of huge complexity. For more information you can always look at
Developer API section.

<hr>

<a name="convention"></a>
#### Convention

Each module in the section will have four sections, a basic introduction, features, keywords and how to use them.

<hr>

<a name="modules"></a>
### Modules

<hr>

<a name="search"></a>
### Search

Using Wolfaramalpha Search Engine, it is used to fetch quick answers of factual and to the point questions.


#### Features

- Fetches an answer to your given question.
    - Alpha
    - Search

#### Use Case

**You**: Hey Stephanie, Do an alpha search, Which is the biggest ocean in the world?

**Stephanie**: The answer is pacific ocean.

Remark: As you can notice, anything after alpha search, is taken into account as a requesting question and is sent to wolfaramalpha to get the correct answer to it.

<hr>

<a name="news"></a>
### News

Newsapi.org

#### Features

- Fetches news from your favorite sources all around the internet.
    - Get
    - News
    - Detailed
- Fetches news really quickly from your favorite resource. (recommended)
    - read
    - latest
    - news

**Note :** In order to configure this latter feature, head to [Resources](/documentation/news){:target="_blank"} to configure it a bit more.

#### Use Case

**You**: Hey Stephanie, read me some latest news.

**Stephanie**: Reads the latest news from your favorite source.

<hr>

<a name="weather"></a>
### Weather

OpenWeatherMap

#### Features

- Get today's weather information/forecast.
    - weather
    - today

- Get tomorrow's weather forecast.
    - weather
    - forecast
    - tomorrow

- Get week's weather forecast.
    - weather
    - forecast
    - week

#### Use Case

**You**: Hey Stephanie, what is the weather today?

**Stephanie**: Weather today at {your location} is sunny, there is a chance of rain, the temperature right now is ... blah blah.

Remark: Similarly you can substitute the question as follows, "what will be the weather forecast for tomorrow?" and "what will be the weather forecast for this week?"

<hr>

<a name="note"></a>
### Note

Evernote

#### Features

- Note something down to your evernote account.
    - Note
    - Something

#### Use Case

**You**: Hey Stephanie, can you note something down for me?

**Stephanie**: What would you like to note me down for you?

**You**: I hate writing repeated instructions in documentation, I've spent more time writing documentation than the actual goddamn code.

**Stephanie**: {above sentence} has been noted down successfully for you.

Remark: After triggering this module, stephanie will ask you what to note down, anything you say after that will be noted down without any kind of check or supervision
of intent you're trying to make.

<hr>

<a name="emails"></a>
### Emails

Gmail

#### Features

- Fetches unread emails from your gmail account.
    - unread
    - emails

#### Use Case

**You**: Hey Stephanie, Do I have any unread emails?

**Stephanie**: Yes you have two unread emails as follows : Single ladies present around your area, click this link to get laid by scamartist@gmail69.com and Read this 10 amazing insert douchebaggery that you never know here at clickbaitisgood.com by someguy@whyyousignedthatform.com

Remark: Stephanie is programmed to fetch you unread emails, but if due to any case there are more than 5 unread emails, stephanie instead just notifies you the number instead of going through all those emails worth more than 2 min of speaking.

<hr>

<a name="twitter"></a>
### Twitter

Twitter

#### Features

- Fetches the trending hashtags in twitter.
    - trending
    - twitter

- Tweets a status on twitter.
    - tweet
    - something
    - twitter

- Get notifications of your twitter account.
    - twitter
    - notifications


#### Use Case

**You**: Hey Stephanie, Can you do a status update on twitter?

**Stephanie**: What would you like to tweet?

**You**: Wenger Out.

**Stephanie**: Wenger Out was tweeted.

<hr>

**You**: Hey Stephanie, what's trending on twitter?

**Stephanie**: The hashtags that are currently trending on twitter are, #showerthoughts, #indianpeoplequora, #soccer, #india, #AMADisasters.

Remark: Similarly you can ask for notifications, just make sure your command has twitter and notifications in it, and frame the sentence in whatever way you want, to
get your twitter notifications. Make sure you have configured your twitter API accurately from modules sub-section to get personal message as notifications.

<hr>

<a name="facebook"></a>
### Facebook

Facebook

#### Features

- Fetches birthday reminders of your friends in facebook.
    - birthday
    - reminders

- Status update in your facebook.
    - facebook
    - status
    - update


#### Use Case

**You**: Hey Stephanie, are there any birthday reminders?

**Stephanie**: No, you have no birthday remainders for today. (Oh god I am so lonely, someone give me attention to validate my ever growing insecurity.)

<hr>

**You**: Hey Stephanie, Do a status update.

**Stephanie**: What's in your mind?

**You**: Stephanie, Cook me a sandwich, that's right.

**Stephanie**: "Stephanie, cook me a sandwich, that's right" has been posted in your behalf. Bots have no genders.

<hr>

<a name="football"></a>
### Football

football-data.org

#### Features

- Fetches information about football from football-data.org
    - Football
    - Information

**Note :** Complete information, since it's huge is present at [Resources](/documentation/resources/football){:target="_blank"}

<hr>

<a name="calendar"></a>
### Calendar

Google calendar

#### Features

- Add an event to your google calendar.
    - add
    - calendar
    - event

- Receive remainders of today's calendar events.
    - calendar
    - events
    - today

- Receive remainders of tomorrow's calendar events.
    - calendar
    - events
    - tomorrow

#### Use Case

**You**: Hey Stephanie, add an event to my calendar.

**Stephanie**: What event would you like me to add to your calendar?

**You**: Dinner with Family at 8pm.

**Stephanie**: Dinner with family on May 1st at 8:00 pm, is this what you mean?

**You**: Yep.

**Stephanie**: Okay the given event is added to your calendar.

<hr>

**You**: Hey Stephanie, Do I have any calendar events today?

**Stephanie**: Yes, you have dinner with family at 8:00 pm today.

Remark: Similarly it can be used to fetch events for tomorrow that is saved in your google calendar.
When stephanie asks you a question for assuring event, a negative answer would lead to loop back the module and asking you the event again.

<hr>

<a name="restaurants"></a>
### Restaurants

Zomato API

#### Features

- Find a good place to eat neraby.
    - feeling
    - hungry
    - restaurant

#### Use Case

**You** : Hey Stephanie, I am feeling quite hungry.

**Stephanie** : Starbucks situated nearby Rest Fruit Street is found, it offers cuisine like coffee, ice-cream, snacks, and many more with an average
price range of around 10-15$ and over 560 people have rated this place with average ratings of 4.5. So would you like to order this place?

**You** : Yes.

**Stephanie** : // opens the browser with the webpage of that location, with contact number, directions and  many other information present in it.

Remark: Similarly you can give negative instead of affirmative response, and stephanie will find some other location for you.

<hr>

<a name="wikipedia"></a>
### Wikipedia

Wikipedia

#### Features

- Fetches information about specific thing from wikipedia
    - information
    - wikipedia

#### Use Case

**You**: Hey Stephanie, I need some wikipedia information.

**Stephanie**: What would you like to know about?

**You**: Harambe

Stephanie : {Gives summary about harambe}

<hr>

<a name="movies"></a>
### Movies

IMDB

#### Features

- Fetches information about movies from IMDB.
    - movie
    - information

#### Use Case

**You**: Hey I need some movie information.

**Stephanie**: Which movie would you like to know about?

**You**: The Lord Of the Rings.

**Stephanie**: is the movie you're talking about is LOTR fellowship of the ring released in 2001?

**You**: No.

**Stephanie**: Okay how about LOTR the two towers released in 2002.

**You**: Yes.

**Stephanie**: The Lord Of The Rings : The Two towers was released in 2002 directed by Peter Jackson, of genre fantasy, epic had a plot of .... stars ... blah blah.

<hr>

<a name="system"></a>
### System

System

#### Features

- Get meaning of life.
    - meaning
    - life

- Get current time.
    - time
    - right
    - now

- Get current date.
    - date
    - today

- Wake up stephanie from sleep mode.
    - wake
    - up

- Send stephanie back to sleep mode.
    - go
    - sleep

- Close stephanie application.
    - you're
    - fired

- Get your system status.
    - system
    - status

#### Use Case

**You**: Hey Stephanie, what is the time right now?

**Stephanie**: It's 3:26 am right now.

<hr>

**You**: Hey Stephanie, wake up!

**Stephanie**: How may I help you today?

(Stephanie is ready to take all sort of commands now.)

<hr>

**You**: Hey Stephanie, Go to sleep.

**Stephanie**: Sleep for the weak.

(Stephanie goes to sleeping mode, and won't take any commands, except wake up.)

<hr>

**You**: Hey Stephanie, You are going to be fired. / You're fired.

**Stephanie**: (check for yourself.)

(Stephanie exits and the application quits.)
