---
layout: docs
currentpage: configuration
---

Configuration

- [Configuration](#configuration)
    - [Config.ini](#config-ini)
        - [USER settings](#user)
        - [SYSTEM settings](#system)
        - [STT (Speech To Text) settings](#stt)
        - [STT Keys (API TOKENS) settings](#stt_keys)
        - [TTS (Text To Speech) settings](#tts)


<hr>

<a name="configuration"></a>
### Configuration

Configuration is divided into two categories, primary configuration and secondary configuration, primary configuration sets up how
Stephanie works internally, while secondary configuration sets up functionality that Stephanie will provide, since secondary configuration
would differ module by module (Facebook, twitter, restaurant and so on), there is a whole set dedicated to that which you could refer up
anytime here at [modules](/stephanie/documentation/modules), For now let's focus at primary, since this lays the very foundation of your virtual assistant.

<hr>

<a name="config-ini"></a>
### Config.ini file

There will be a config.ini file present with every download of source code, so if you look inside the folder you'll find it named
"config.ini", this file contains all the configuration related settings, you can open it with simple notepad, text editor or any of your favorite IDEs.
Inside this file you'll find some predefined settings, where some are set by default while other needs to be filled.So let's go through each
division and it's sub-divisions one by one.

<hr>

<a name="user"></a>
#### [USER]

A sample axample showing how you fill up the configuration.

        [USER]
        name = Ujjwal Gupta
        gender = male

        age = 18
        birthday = 15/10/1998

        city = kanpur
        state = Uttar Pradesh
        country = India
        zipcode = 208001

- **name** - As the name suggests, here you fill up your name with a white space differentiating your first name from the surname.

- **gender** - Well, this is quite basic, should I continue this? I wonder.

- **age** - as long as you're age doesn't exceeds 2147483647 it's fine, just kidding python 3 doesn't has int. Oh god I am pathetic.

- **birthday** - Ah, finally something need, you'd probably need some assistance, the format of birthday is Date/Month/Year.

- **city** - The city in which your mom lives in.

- **state** - The state where that city doesn't belongs to.

- **country** - No stephanie, Australia is both a country and a continent!

- **zipcode** - anything but 42069.

<hr>

<a name="system"></a>
#### [SYSTEM]

okay enough of jokes, the next few settings will be really important ones. Example:

        [SYSTEM]
        assistant_name = Stephanie

        welcome_message = How may I help you?

        wake_up_engine = True

        wake_up_command = Stephanie wake up

        greet_engine = True

        always_on_engine = False


- **assistant_name** - This resonates to the name of your virtual assistant, The system is optimized to give best results for "Stephanie".
but you can give your own name to your assistant, and test how it goes. Just don't name anything stupid, bots have feelings.

- **welcome_message** - This is spoken by your assistant, after it's all initialized and ready to run.

- **wake_up_engine** - Can only take (True or False) Now this is a really cool part, what it basically does is that it toggles hibernation mode of stephanie, so what does that mean?
Well instead of actively responding to each of your command, it just kind of goes to sleep. When you run the application, it's already in sleeping mode, and
In order to bring it in active mode, speak "Stephanie, Wake Up.", this will bring stephanie to alive, and will now actively respond to each of your command,
and now when you're done, you could say, "Hey Stephanie, Go to sleep.", and it will again go to sleep mode, and not responding to anything you're saying unless
it's "Hey Stephanie, Wake up", or something similar to that. I personally recommend True status because it just feels quite human, when you need stephanie, you call her,
and when you're done, you just shut it off.

- **wake_up_command** - The command which enables stephanie to get in active phase, from hibernation one. remember if you have changed the assistant_name, make sure to change this one as well, in short this command is used to enable stephanie to active mode, again it's optimized to default, "Stephanie wake up" to yield best results.

- **greet_engine** - Defaults to True, basically with this feature on, whenever you say something as "Hey Stephanie what is...", "Umm, well stephanie give me...", it ignores everything written before stephanie so that you can use it in exchange with "what is..." meaning using stephanie in any command is not necessary, my advice, let it the way it is.

- **always_on_engine** - Defaults to False, basically it's equivalent to "Siri, ...", meaning just like in siri and cortana, you speak it's name and that makes the service to work, it's exactly that except, it will use assistant_name, which defaults to "Stephanie", and you can't give command, with the name, like can't do, "stephanie, what ..." instead "stephanie" and then after beep-boop, the command. **My advise? let it stay False, oh and whenever you turn it to true, make sure to wake_up_engine false since they are completely opposite to each other and wake_up_engine takes the precedence over this one.**

<hr>

<a name="stt"></a>
#### [STT]

This is most probably the backbone of the entire application alongside the searching algorithm(which I invented/assembled, idk, and yes I am bragging),
So look I neither have a PHD in computer science nor am I a genius, the way Stephanie, or any virtual assistant works is that, it takes your
audio as a input and uses some algorithm to convert it into normal text. that's why STT - speech to text. (Mostly that algorithm is a neural network,
one of the main algorithms of machine learning, and quite honestly one of the most used ones, I am learning it myself.) So there are some open source
STT engines, but they don't produce the best results, for instance - Sphinx, and it also needs additional configurations to get even a correct "hey" out of it.
So it's better to rely on 3rd party services to do the heavy lifting for us, like google, facebook, microsoft and so on.

As of now, Stephanie provides interface to link 5 services, namely,

1. [Google Cloud Speech API](https://cloud.google.com/speech/){:target="_blank"} - Created by Google, name says it all, free for first 60 mins.
2. [Bing Speech API](https://www.microsoft.com/cognitive-services/en-us/speech-api){:target="_blank"} - **Most Recommended** Don't go after name tag, Created by Microsoft their service, and free flexible quota is best of all.
3. [Wit.ai](https://wit.ai/){:target="_blank"} - Created by Facebook, again it's pretty good, can be a bit overwhelming at first but they did an amazing job especially with documentation for developers. On a side note, they have the best data quota, which is 1 request per second, that's fucking best.
4. [Houndify](https://www.houndify.com/){:target="_blank"} - Created by soundhound, pretty exciting project though free quota can be a bit underwhelming.
5. [Watson AI](https://www.ibm.com/watson/developercloud/speech-to-text.html){:target="_blank"} - Created by IBM, their demo is pretty good, though I still had to give it a try yet.

Now time for an example:

        [STT]
        initial_stt_engine = google

        master_stt_engine = bing

all the available options are as follows: "google_cloud", "bing", "wit", "houndify" and "ibm". Now there's a bonus one called,
"google" which refers to web based speech to text, it has a default API token, and hence is the default engine, though it's probably
not the best one in the market.

- **initial_stt_engine** - refers to the engine which takes care of stephanie's hibernation phase, "hey stephanie, wake up",
since it'd be constantly hearing, I thought it'll be better to use google web based engine to set it, but as always you can change it
to whichever engine you like from the above options.

- **master_stt_engine** - refers to the engine which takes care of actual functionality, like triggering the correct response to
"what is the time right now?" or "Do I have any facebook notifications?" and so on. Change it from default "google" web based to any of the above option you
like, to get good experience.

<hr>

<a name="stt_keys"></a>
#### [STT_KEYS]

Here you enter your API tokens, for your given STT service, in case you're not a programmer, an API Token is a way for those 3rd party
services to recognize you, just like username and password is used to recognize your account, and hence put up a cap at how many times you
can use their service, each service has it's own way of signing you up and providing with token. Example:

        [STT_KEYS]
        google_speech_api =

        google_cloud_speech_api =

        bing_speech_api = 724iut143dc049ed76153451230f4g6h

        wit.ai_speech_api = E56B1BD2AD3D4EF2AF5536011F9A0DD9

        houndify_client_id =
        houndify_client_key =

        ibm_username =
        ibm_password =

And of course don't try to put them, since they're not real.

For wit.ai and bing_speech_api, I will actually guide you on the process about how to get API_TOKENS if you have no experience whatsoever with it.

- Bing Speech API
    - Firstly go to their main site at [Bing Speech API](https://www.microsoft.com/cognitive-services/en-us/speech-api){:target="_blank"}, scroll bottom to the page and press on try for free.
    - Now it will take you to new page, press on create under SELECT API, of bing speech API and create your account.
    - Now you will finally get two keys, select any one of them and put it in config.ini file.

- Wit.ai
    - Again go to the main site at [Wit.ai](https://wit.ai/){:target="_blank"}, create an account, and press go down to rabbit hole.
    - Now go to the settings tab, and under API details, you'll find Server Access Token, copy that paste it in config.ini file adjacent to wit.ai

<hr>

<a name="tts"></a>
#### [TTS]

TTS refers to Text-To-Speech, it just basically converts text to speech, and hence speaks through your speaker. Example:

        [TTS]
        tts_engine = google

        tts_player = os

- **tts_engine** - refers to the service used to get audio from the text that stephanie has as it's end result, google provides it for free,
and is the best in the market, and is the only service which stephanie offers out of the box, so just don't interfere with it for now.

- **tts_player** - os refers to operating system, and it just plays that audio (.mp3) from your preferred way of audio listening
application (probably vlc media player), if it keeps speaking same thing again and again, you probably have repeat setting on your application.
Stephanie provides 'pygame' as other option, which works independently, but they have a weird bug which sometimes fails the process, so again don't mess
with these settings for now.

And this ends the primary configurations of stephanie, now it will probably work efficiently, and all you need now is set up modules,
like facebook and so on, to get your Jarvis v-999 ready. (Look you must be frustrated that so much work you need to do, but comeon
if you can get facebook notifications without you doing anything, wouldn't that mean anyone can do that, and hence they have your
account credentials. So.. I don't hate you or something, you gotta work to reap the benefits man!)

To [secondary configurations](/stephanie/documentation/modules), here we come!
