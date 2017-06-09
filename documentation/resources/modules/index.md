---
layout: resources
currentpage: More Modules
---

# 3rd Party Modules


- [Introduction](#introduction)
- [Demo](#demo)
- [Joke](#joke)

<a name="introduction">

# Introduction

This section is dedicated for all of the modules built by the community in one place so that anyone can search it quickly and effectively.

**Note :** Make sure to double check any 3rd party module before installing in order to make sure you're privacy stays intact.

<hr>

<a name="demo">
### Test Module

write a short discription.

#### Setting Up

- Details on how to install it with stephanie.

#### Usage

- Some basic usage.

#### Github\Bitbucket\File Link

Link to your given module.

<hr>

<a name="joke">
### Joke Module

This is a joke module which fetches some jokes from  www.goodbadjokes.com and speaks it out through Stephanie.

#### Setting Up

- Download this repository and then copy joke_module.py and paste it to the modules subfolder present in Stephanie Package
- Open modules.json file, and add this at the very end before the last ending bracket :

		["JokeModule@TellJoke", ["tell", "joke"]]

- Somewhat like this (Notice there's no comma in the end if it's the last):
		
		[
			[...]
			[...]
			["SomeOtherModule@DoSomeShit", ['just', 'a', 'sample']],
			["SomeOtherModule@DoSomeShit", ['just', 'a', 'sample']],
			["JokeModule@TellJoke", ["tell", "joke"]]
		]

- And that's it.

#### Features

- Tells a random joke.
	- tell
	- joke

#### Usage

**You**: Hey Stephanie, tell me a joke.

**Stephanie**: What did one snowman say to the other snowman?It smells like carrots out here!

#### Github/Download Link

[Joke Module](github.com/slapbot/JokeModule) By [Ujjwal Gupta](github.com/slapbot)
