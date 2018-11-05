In Spring 2018, I helped redesign one of my favorite classes in the [MAET program](http://edutech.educ.msu.edu/programs/masters/), which is on *[Electronic Assessment for Teaching and Learning](http://edutech.msu.edu/programs/masters/courses/cep-813/)*. One of the changes that I'm making is removing Minecraft from the module on game-based assessment and replacing it with Twine. While Minecraft was a wonderful resource, the last two semesters that I taught CEP 813 were characterized by serious technical problems that made using Minecraft a real pain in the rear. In contrast, Twine costs less, shouldn't present any compatibility issues, and actually allows us to think more deeply about designing game-based assessments than Minecraft can. 

This is a walkthrough of a sample Twine game that I put together for 813 students, both as an example for them as they prepare their own Twine games and as an outlet for me to reflect on and gush about my experience with Twine. I also wanted to provide some helpful context to people trying to understand this example: This is a game-based assessment I could actually use in a French classroom, which means that you actually need to know some French to navigate through it. By walking people through the game, I can make it clear what I'm assessing and how I'm assessing it, which won't be clear to someone who hasn't been through the hypothetical lessons I would teach before administering this assessment. I also wanted to discuss some of the technical aspects of the game, because I challenged myself to learn as much as I can about adding some more advanced features to Twine. 

This is not a perfect example for CEP 813 students, but I hope it will be useful! It took me about 30 minutes to sketch out some of the basic aspects of the game (though I've been thinking about designing a game like this for years, so that's probably a low estimate). Actually implementing the game took me somewhere between 4-6 hours, but that's largely because I insisted on adding some of those advanced features, which took some time to learn. Someone sticking to the basics would cut a lot of time off of that estimate. 

To play through the game, visit this link, and download the file by right-clicking it and clicking "Save As." Then, double-click on the file to open it in your browser and follow along with my walkthrough. You can also open the file in Twine if you want to see more of what's "under the hood." 

I'll let the game speak for itself whenever possible, so this walkthrough might not make much sense without opening it up and playing through alongside it!

## Introduction

### Instructions

I designed this game as a self-assessment for French students nearing the end of a unit on transportation, so before beginning the game proper, I started with some basic instructions. I try to give some background for how the game works, what it reviews, and what students should do with it. I'm using the SugarCube [Twine format](https://twinery.org/wiki/twine2:how_to_choose_a_story_format) because when I was looking for walkthroughs on some of the advanced features I used, they used that same format. SugarCube adds options to save and load your progress in the game, which kind of undercuts my suggestion to play through even if students make mistakes, so I would probably do things differently if I were to start from scratch. Plus, I think the default format for Twine looks nicer. :) 

From here, click on "Let's get started." 

### In front of the train station

I love the idea of including a Google Maps street view here, and it's surprisingly easy to do. I actually lived in Dijon for a few months, and adding the ability to take a quick look around a city that I love makes this so much more compelling for me (and hopefully for the students, too!). 

I originally planned to use a lot more French in the game so that students would have to be more on the ball with vocabulary. I was also planning to use some HTML/CSS code to make the English equivalent for the French words show up so that students had a help line if they needed it (something like this: <code>&lt;span title="streetcar"&gt;le tramway&lt;/span&gt;</code>. Ultimately, though, I decided against this. Dropping French into the middle of English sentences just to remind students that this was a French assessment felt a little too much like [Poirot Speak](http://tvtropes.org/pmwiki/pmwiki.php/Main/PoirotSpeak), and letting students translate words just by hovering over them felt like too easy of an out. So, I decided that it would be more authentic to only use French in those places where an American in Dijon would actually have to deal with it **but** not offering any kind of translation, so that students would have to be on the ball at key moments. 

One invisible thing that happens in this location is that I set up certain *objects*, which you can read more about [here](https://twinery.org/forum/discussion/1516). This is one of the more advanced things I do in this game, so I wouldn't recommend it to someone on their first Twine game unless they're feeling pretty confident or patient. In short, I tell the game that the player does not have a ticket, that the ticket is not stamped, and that it does not have a destination. These things will change throughout the game (spoiler alert, these are the things you need to do to win the game), but setting them up here is important. I also set the time to 12:45pm&mdash;this will also change at certain points throughout the game. 

From here, click on "Go inside!"

### Main hall

This is an actual picture of the main hall of the Dijon train station that I got from Wikimedia Commons. Being able to embed authentic media into my game is one of the things that most appeals to me as a former French teacher using Twine. 

In this location, I don't offer choices, just the names of different objects and signs (which are in French, since this meets the authenticity standard I mention above). *Les guichets* refer to the ticket counter, *les quais* refers to the platforms (i.e, where you board the train), and *la sortie* takes you out the exit back in front of the train station. I could set things up so that the language about getting off the streetcar disappears if you access the location from *la sortie*, but it's not crucial to the assessment. 

The clock and the sign are also important. The clock displays whatever time it is (based on the hidden Twine objects I've set up), and the sign will tell players what platform their train is going to arrive at. This actually isn't mentioned anywhere in the game, so it's one of the subtler, non-language things that I'm assessing here. Of course, knowing that *Départs* means *Departures* will help clue students in to why they need to view the sign at some point, but I think it's nice that there are no explicit instructions to figure out what platform to visit. Naturally, because this is part of the assessment, I would need to teach about these *Departure* signs (and not just the vocabulary word either) in class before administering the assessment. 

At this point in the game, there's nothing stopping you from going to the platforms, picking one at random, and boarding the first train that comes by. Why? Because that's just how it works in France. No one checks your ticket before boarding, but if you're caught by a *contrôleur* without a ticket, with an incorrect ticket, or with an unstamped ticket you'll get in trouble. So, the game is assessing the player in an authentic way. However, as I mentioned earlier, the game **knows** that you don't have a ticket (and that your non-existent ticket has no destination and is not stamped), and you'd better believe that if you try to get on a train without going through the right steps, you're going to get  caught (this doesn't always happen in real life, but it does happen in M. Greenhalgh's French class). 

So, let's take the proper steps. Click on "les guichets."

## Buying a ticket

### Ticket counter

This is just a small page that gives students the chance to walk back out to the main hall if this isn't where they want to be after all. 

From here, click on "Walk up to employee"

### Talking to the employee

I'm really proud of the fact that I worked an audio component into this game-based assessment. French classes tend to privilege reading comprehension and writing over listening comprehension and speaking for practical reasons, but I remember really struggling to understand the woman behind the ticket counter the first time that I tried to buy train tickets in France, so I wanted to make this more authentic (even if I did allow for play/pause controls on the audio so that students could listen several times if they needed to). 

The first thing I did here was to activate a feature on my Mac that allows users to convert any block of text into recorded speech (and, of course, make sure that the French "voice" was activated). Then, I wrote some dialogue that I wanted students to listen and respond to, converted them into iTunes tracks, converted those into mp3s, hosted them on my website, and then used &lt;audio&gt; HTML tags to embed the recorded dialogue into the game. I could have also recorded myself, but even though my voice is less robotic than a computer one, its pronunciation is (mostly) better, and I also didn't have to worry about background noise, etc. Our friend behind the counter is saying hello and asking us how we are.

Click on "Je voudrais un billet, s'il vous plaît." 

This asks for a ticket politely (that is, using formal language). The other choices include demanding a ticket rudely (that is, using commanding language instead of requesting language and using informal language instead of formal language), or asking the man how he is doing, either informally or formally. Asking the man how he's doing doesn't make a difference, but using informal or rude language starts to make him progressively more frustrated, which changes the way that he responds to you in future interactions (using the same kind of *objects* I use to govern time and tickets). I think including this is important in my assessment, since it reminds my students that successfully using French is more than just vocabulary and grammar. It's also a question of culture and social cues, and they always need to remember that sort of thing. Our friend then asks us for our destination. 

Click on "Je voudrais aller à Lyon s'il vous plaît." 

These choices again distinguish between formal and informal language, and the man behind the counter again gets offended if we use informal language with him. Either way, though, he asks a clarifying question: Is our destination the *Gare de Lyon*? Or is it *Lyon&mdash;Part-Dieu*? This is based on an anecdote I heard from people I knew when I was living in Dijon, though I can't say for sure whether it's true. The *Gare de Lyon* is the name of a train station in Paris, but because it has the name *Lyon* in it, there are people who would buy tickets for there when they were trying to get to the city of Lyon, which is in a totally different direction. The game provides you with opportunities to realize you've made a mistake and come buy the correct ticket if you choose the wrong one, but it will slow you down. Also, as much as this makes a great story, I wouldn't actually assess this knowledge without at least mentioning it in class. 

Click on "Je veux dire, Lyon&mdash;Part-Dieu. 

Here you get the ticket. The description of the man at this point depends a lot on how much you've offended him. Behind the scenes, the game is recording that you now have a ticket and what the destination is. It is also advancing the clock: Every time you order a ticket, it takes you 15 minutes. 

Click on "Leave"

## Heading to the platform

You're now back in the main hall of the train station, with all the same options that were there before. If you check the clock, you'll see that time has advanced. You can also check the sign at this point to compare the destination on your ticket (which will appear if you have a ticket) with the list of departures. That tells you that you need to go to Platform I. It also tells you the departure time for your train (if I had thought about it, I would have had the departure time listed on your ticket appear for reference, but I didn't). 

From here, click on "les quais"

## Underground passage

I was tickled to find that Google Maps also has a Street View of the underground passage of the actual Dijon train station, so I put it in here. As I mentioned before, I think it adds a lot to the assessment to be able to see authentic media like this. It's also nice that you get a view of the ticket stamping machines that students need to use to win the game. You can also see some stores down here, as well as the exit at the other end of the passage. I wrote the exit (and the park across the street) into the game, complete with making the time advance if you choose to goof around outside instead of go straight to your platform (you can still visit there and make it back in time for your train, though!). I would have liked to add the stores into the game, but ran out of time. It would have been neat to use the objects function in Twine to add a money element into the game, where students would have to provide the correct bills based on the price that the man behind the ticket counter "said" to them. Then, with any leftover money, students could go into one of these stores and place another order... as long as they had the correct amount! Maybe in the future, though. 

From here, click on "ticket stamping machines." 

## Ticket stamping machine

If you have a ticket, visiting this location will stamp it for you. If you don't have a ticket, the text will say something about you admiring the machine instead. If you already have a stamped ticket, it will tell you to stop messing around and that other people are in line. This is yet another subtle assessment built into the game. When you buy a train ticket in France, you buy it for a particular route, not (usually) for a particular time. So, you can typically hop on any train that matches the route on your ticket. This has the downside that someone could cheat, using the same ticket over and over again for the same route until it expires; so, before using a ticket, you're supposed to date-stamp it, which shows when you actually used the ticket. As above, you can hop on a train without doing this (I've accidentally done so), but if you get caught, you'll get fined. So, there are no explicit instructions for students to take this step&mdash;they need to remember from our lessons that this is something they have to do. 

From here, click "Leave machine." Then, click on "Go up the stairs to Voie I / Voie J"

## Platform I

Each of the platforms is associated with some YouTube footage from the actual Dijon train station (yay for train nerds!). All the footage is actually from the same video, so I used [this reference page](https://developers.google.com/youtube/iframe_api_reference) to make sure that the clip being played was different for each platform (when possible, I used visual clues to make sure the footage corresponded with the platform you're on, but that wasn't always possible). I also used the tips there to force autoplay, take away the controls, and take other steps to make it feel a little more authentic. 

At this point, you should have the right ticket, it should be stamped, and you should be on the platform. The *information sign* will help you confirm that you're on the right platform, and as long as you haven't dawdled too much, all you'll need to do is click "Wait for train" and "Board TER." Then, you've won! However, a few things can happen here if you've made poor choices. I don't think they're very effective right now because of the particular way they're designed, but I did want to think them through.

First, you can board the correct train without the right ticket or without a stamp. In that case, you still win, but you have to pay a fine or buy a ticket (this is where the money option would come in handy). I kind of like that you can win (by getting to your destination) but still get slapped with extra costs. Traveling in France isn't going to get you an A or an F: It's a question of what you achieved what you wanted to and whether you ran into any problems along the way, so this feels like an authentic way to assess it. 

Second, you can board the wrong train. There are a lot of trains programmed into the game, and there are two trains for most platforms (since platforms in French train stations are typically for two separate tracks). So, you could pick a totally wrong train or just get the track mixed up for your platform and board the wrong one that way (though in the case of Tracks I and J, the right train comes first, so this isn't likely to happen; I'd like to fix this so that the wrong train comes first and students really need to pay attention before getting on a train). Also, as hinted at before, you can wind up in Paris instead of Lyon because you bought the wrong ticket. This is interesting because you won't get fined, but you will still lose the game&mdash;kind of the opposite of the "win" above, and another taste of authenticity in the game. 

Third, you can miss your train. It took a lot of effort, but trains only show up on a platform if you're at the platform before the train is scheduled to come by. Plus, if you wait for a train and let it go past, the game advances the clock to after that train's departure. I'm really not using this time feature to its full potential, but it has me thinking about what else I could be doing with it. It's possible to mess around enough that the game will inform you that you've missed the train you were waiting for, which is another way to "lose." 

## Conclusion

I hope this walkthrough gives you a peek at some of the technical details of this game and of some of the assessment and design philosophy that went into it. I'm really, really impressed with this tool, and I hope to keep messing around with it in the future!
