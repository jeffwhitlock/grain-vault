---
title: "Strategy Session (5/15/26) - Capture & Sharing"
date: 2026-05-15T20:01:39Z
duration: 71 min
participants: ["Jeff Whitlock", "Mike Adams", "Ben DeMordaunt", "Ryan Johnson", "Jake Adams"]
attended: true
processed: true
processed_at: 2026-05-18T17:42:33Z
wiki_articles_touched:
  - topics/Capture and Recording.md
  - topics/Grain Sharing Model.md
  - people/Jake Adams.md
  - people/Ryan Johnson.md
source: grain
grain_id: 3293e129-c57d-4a02-95bd-d74406419b8e
grain_url: https://grain.com/recordings/3293e129-c57d-4a02-95bd-d74406419b8e
---

**Jeff Whitlock:** Subject.

**Jake Adams:** How's it going.

**Jeff Whitlock:** How are you?

**Jake Adams:** Good. I'm just not. We're traveling.

**Jeff Whitlock:** Me. No, I'm at home right now.

**Jeff Whitlock:** But I was traveling this week. Yeah, yeah. Yeah, I went on anniversary trip to Washington, DC.

**Jake Adams:** Oh, nice.

**Jeff Whitlock:** Yeah, it was really fun. What's up, Brian? Have you been there recently, Jake?

**Jake Adams:** I've never been to Washington, DC, and I would like to go.

**Jeff Whitlock:** So highly recommend it. Like, it's super nice because you can fly out of Provo, they have a drag flights now from Provo. Which just makes it awesome. And I have to put up with Salt Lake stuff. So you can go out straight at Provo. It was like 250 dollar flights. So chat flights were cheap. And then, yeah, it's just really nice. It's like, especially if you could find a way to like have some watcher kids. Because we just, like, we took a train straight from the airport as fast, was quick, like three bucks and fast. And then we didn't rent a car and we just like road bikes and scooted everywhere. Cause they like lines everywhere. And it's, it's really nice. It's a, especially if you go on like the fall or the spring. Like beautiful city, very, very easy to get around, lots of great restaurants, tons of amazing museums. Plus all the main like national mall stuffed in capital stuff to see.

**Jake Adams:** That sounds awesome. Is it doable with kids.

**Jeff Whitlock:** Yeah. For sure. You just would have to rent a car.

**Jake Adams:** You have to do it.

**Jeff Whitlock:** And then I think parking would be tricky, but I'm sure you could figure it out. But yeah, like I was, I underestimated how cool was I was really impressed. I really, really liked it. And the museums were just so cool. There's like 21 Smiths on your museums at all three. They're really fun to go to.

**Jake Adams:** Go.

**Jeff Whitlock:** Yeah. So it was, it was a, it was a really fun trip. Micah, you and you taught two or just Steph.

**Mike Adams:** Just she's there on a girl strip. She gets home around. Six on Sunday and I leave Monday.

**Jeff Whitlock:** Talking places.

**Mike Adams:** Are the airport. That'll be nice.

**Jeff Whitlock:** Let's, uh, what's she doing out here? Anything fun?

**Mike Adams:** Girls trip. Yeah. Up in, uh, she has a recall drewmate's dad was like the CEO of blackens and Stanley. And he's just like an uber billionaire or whatever guy. And they have this home up in, uh, the colony. And so I'll go hang out of the colony.

**Jeff Whitlock:** Cool.

**Mike Adams:** Call dreams. It's been long, long time since they've done it. So it'll be fun for them.

**Jeff Whitlock:** That's fun. When I hear you say the colony, my brain goes to the terrible like dorm thing and I do.

**Mike Adams:** We're all the, we're all the bros lived. Every brother.

**Jeff Whitlock:** It's like the colonies and the King Henry are the bro places.

**Mike Adams:** I'm on the road. I'm going to go get some drive - thru and then I'll be back in my desk.

**Jeff Whitlock:** What I wanted to talk about, I think the most valuable thing to talk about in this form was just, um. Getting some feedback, Mike discussion feedback on kind of the model around sharing and recording in teams that we've been discussing. And I specifically would like with Jake here, which is kind of like his thoughts on, um, kind of how to, how to synthesize that like the model from like a product perspective with some of the work you were doing on, on like actually operationalizing it with LLMs. Bo with you out.

**Mike Adams:** You can probably drive because I was really just riffing off of the cloud design that you had. And then I sent you where my riffs ended up. Yeah.

**Jeff Whitlock:** Let me, let me do that. I'll pull your latest riffs and then, and then you can editorialize if I'm, if I'm missing something or not capturing some nuance, do you think it's important.

**Mike Adams:** Maybe I can like say it like the high level just for framing around kind of jumping to the conclusion. It's like. I think what stood out to me across that exploration was that the sensitivity stuff is a really good idea. But, and I read and Jeff had a great proposal doc that I think he shared out, but my current opinion is that it's an admin feature. And that we still need to fix like the core sharing, um, model. In a way that I think my proposal makes a lot more sense than the status quo. And I don't know. So we're either thinking about it as the sensitivity as an alternative to heuristic based. Or the sensitivity as like an admin feature for like business and enterprise plans that is like additive and supplementary and additional kind of visibility transparency control on like a core model. It's probably pretty similar to what we have today, but might be like organized and presented visually or differently from a kind of mental model perspective. But I think that's kind of like the high level framing of the convo. Does that sound right, Joe?

**Jeff Whitlock:** Yep. I'll just let me pull this. I'll pull up your diagram. That might be a good place to kind of

**Jake Adams:** for what I was worth that. I haven't seen any of that or viewed it.

**Mike Adams:** So I just, I was up very late last night and just shared it all through to Jeff. So it hasn't been shared out. I just, I just ran out of bandwidth. To do a wider share out. So he has a, he has it all though and he'll share it. Yeah.

**Jeff Whitlock:** We were just riffing. So I'm going to pull it up and we can walk through it. All right. So, and yeah. And like Jake, this is kind of like another iteration from what I shared. So, um. So. A couple of different points here. So the first one is some changes to. How we conceptualize or end present, um, auto recording rules of what gets captured. So right now it's like right now we're really focused on. Its organized by capture method. Um, which is. I think, I think it adds confusion because it's, it's sort of like, I think we want to. And as we evolve and maybe even move more and more towards like desktop video and stuff, like I think we don't want to like so strongly emphasize the method and more just about like ranking capture everything. And so this is more about flipping the access. So it's now about like the meeting types and then like how you capture each of them. There's this content.

**Mike Adams:** I'd add the other driver here is this idea of fallbacks.

**Jeff Whitlock:** Yeah.

**Mike Adams:** As opposed to the like forced binary. But just throwing one more thing in there to throw off.

**Jeff Whitlock:** Yeah. Exactly. So this, there's, there's this concept here of like a fallback of like, the various reasons why I capture on your preferred means might fail. Someone doesn't let in the bot. Someone, um, the bot crashes your desktop app crashes, whatever it is. So there's, and so right now, like we just don't capture that meeting, but we're playing around with this idea of a fallback. Uh, let me pause that and see if, just curious folks have any questions or reactions, quick reactions.

**Jeff Whitlock:** And we can keep going too, if, if it makes sense to just kind of see it all.

**Jake Adams:** I mean, my, my first reaction here is like just the cognitive load of a user to think around defaults being different across these different meaning. We're calling a meeting types. Um. Like, that's going to default to, and I don't know if this is selected or actually like what we propose is the default.

**Mike Adams:** Jeff, can you just show them my meetings page design? I think it's just easier to look at the actual design. Cause it is, in my opinion, when you actually look at the design, it is exponentially easier to think in terms of like, okay, for my meetings, my external meetings I want. To have the bot from an internal meetings I want. The desktop capture. And then you check a box that's either like use a fallback or don't use a fallback, which I think should be like checked by default versus having to think like, okay, so, so for my bot, I want external and internal for my, like it just, it doesn't make sense. Like it literally doesn't make sense because then you end up basically forcing them to think about the duplication scenario. What we're trying to do is like reduce this. So the ideal path would be on the, on the current settings where we would be like the current settings would be fine if we just managed duplication and we didn't force them to like use one auto path or the other. So that we weren't duplicating. And we were just like, cool. Like turn on or don't turn it on. Have, have both there. We don't care. Um, we'll just merge them together because they're the same meeting, but we've discussed that as the solution, you know, for a long time. And we just haven't wanted to take on the investment to do it or whatever reasons we haven't, but we're stuck in this world. We make these like, you know, really poor UX trade - offs. And I think that we can either keep it kind of the way that it is now. And handle duplication. Or I think, Jeff, can you share the design or the, at least my latest drift that I shared of the actual, just my meetings page.

**Jeff Whitlock:** Yeah. Let me, let me pull that up.

**Mike Adams:** Or you can just flip it to think in just these much simpler terms of like, um. Yeah, just, okay, these are my external meetings. This is what happens. This is my internal meetings. This is what happens. Like this is my unscheduled meetings. This is what happens. And then you got the two levels of auto capture and auto share. And then my design also has this kind of like flow through that makes sense to me around the idea of like, okay of those capture methods, like which ones do we want to consider? And I think I did a bunch of like research and amplitude and hex around just like a lot of these, the current behavior. Cause we, we just, we give people like so much room in these settings to hang themselves. You'll get like one or two percent of users that will ever make these choices will ever go outside the defaults. And it's just not worth the complexity of the model. To instead just kind of like reduce the set of possible spaces to the ones that people actually want to consider. Uh, and have like the, the, the organization model of how it works to be to best match the way they think about it. That's the ultimate question I think you're surfacing Jake is how do people actually think about it? This is how I think about it. Is like, I don't think about it as like which capture method do, you know, or, or, or starting at the capture method of like, what do I want my bot to do? And what do I want my desktop app to do? It's like, no, I just, why don't I, what, what do I want for my external meetings, you know, like I just want to understand like how they're going to be captured. Given that we don't want to like. Be redundant. If we're okay with being redundant, then this whole proposal kind of goes out the window, but I'm kind of, I'm riffing off of a position where we're not okay with being redundant. And we don't want to like handle the duplication on our end. So we're just going to like have them have a preferred one path, but then a fallback, if that doesn't work, the bot doesn't get out of the waiting room. They don't have the desktop app installed, whatever it is.

**Jeff Whitlock:** Guys. I'm going to have to leave my zoom is like crashed. Give me one second. I'll be right back. Sorry. I've been trying to share the designs for the last two minutes on Michael's talking before going on too.

**Ryan Johnson:** Yeah. So yeah, just clarify.

**Jake Adams:** Yeah. Go ahead, man. Sorry.

**Ben DeMordaunt:** When we talk about redundancy, we're talking about the duplicate capture.

**Mike Adams:** Right. Duplicate capture. Yes. Two, two capture methods, bots and desktop at the same time for the same meeting.

**Ben DeMordaunt:** Yeah. Yeah.

**Mike Adams:** I think, I think that what we've done instead is created this kind of false. Trade - off of forcing, you're basically, you're ruining people's bot recording behavior. That exists as users by getting them to try the auto capture on desktop because it turns off their bot to prevent the double capture. And so then they're on a different computer. They're on mobile. All of these workflows that have been working for them from a capture perspective are now dead. And so that's why the fallback is been the discussion in Slack. Is the best alternative to just allowing you to capture both if you want. And so you're just basically turn it all on in all times. And if, if it's bought and desktop, then cool. And then we just like, you know, handle that redundancy on our end. And so the problem with that, even if we wanted to take that engineering investment is that we literally do have double cogs because, you know, you have bought and desktop going at the same time. Same person. I think.

**Jeff Whitlock:** It's. The idea of merging or picking the best recording. And I think, I think it's a good idea. It's just one of those things to me that feels like the scope to nail it is going to be dramatic. Um, so I would, I think it's far better decision to either handle it along the lines of this proposal. Or just not worry about dupes. Just let people set it up, whatever they want and just deal with it.

**Ryan Johnson:** Hey, my one. Uh, pushback, I don't know, pushback the right word, but like, no, um, I think you could simplify this a little bit. Um, bought as a fallback to me makes sense conceptually, right? It's like, okay, default, uh, desktop capture. If I'm not there, I'm on my phone or whatever. Oh crap. I can't capture it like I want to send in the bot for me. Thank you. Uh, desktop captures fall back is a little bit hard for me to kind of wrap my head around. Cause it's like. It doesn't really work necessarily as a fallback because there's so many conditions required in order for it to work. I think desktop capture as a, Hey, we see you're at the, your machine, the bot failed to get in there. Do you want to desktop capture this instead as opposed to like codifying it as like a fallback and then oops, all the conditions weren't meant. So we weren't able to fall back. And so like we're kind of making a promise that's harder to, um, fulfill as desktop as fallback as opposed to bot S fall back. And so that, that's why I like, I feel like you could simplify it where it doesn't have to be a setting. For the, if you default to bot and the bot fails prompt them to, Hey, or bot failed. Do you want to desktop capture if they're on the desktop? I feel like you just always should prompt them there. I don't think you need setting.

**Jeff Whitlock:** But for if you have desktop, you're saying, Ryan, we could use the op, we could use the opt - in notifications.

**Ryan Johnson:** Right. Yeah, exactly. And then, but if you have desktop as default, then there probably should be a setting saying like, if desktop, if you were, didn't start the upside caption, should we automatically send in the bot? Um. So like, I think like there's an asymmetry there, but I think the asymmetry actually is easier to understand the, because it is asymmetrical. Uh, the ability to fall back. And so that's why I think it's important to kind of be clear there. But that's my one thought on. It.

**Mike Adams:** Yeah. My assumption was that they were like of equal fallback ability. Um, so help you understand why. Um, the asymmetry exists.

**Ryan Johnson:** So like the reason why you want to fall back for desktop, right? It's because you're not at your machine. You don't have the desktop app open. Whatever. Right. Like it's, there's, the scenarios where it doesn't work, um, automatically.

**Jeff Whitlock:** Do you join from mobile exactly right.

**Ryan Johnson:** And so. But if, if you are a desktop in

**Mike Adams:** what default direction we're talking about, your default is bot and bot doesn't work.

**Ryan Johnson:** Then, then, then if, if you're able to fall back, that's only because you have the desktop open already. So like, okay, you have the desktop open.

**Mike Adams:** We just say, Hey, and you're saying the issue is the scenario where we basically say, well, there's just a lack of clarity. And you're basically promising that we're going to try to fall back when we might not actually be able to fall back. Cause you might not have the desktop app installed or it might not be signed in or whatever else.

**Ryan Johnson:** Right.

**Jeff Whitlock:** That, Ryan, and you're also, you're also saying that you don't even need to conceptualize it as a setting because we should just always try to capture using the bot failed.

**Ryan Johnson:** We're going to start auto capturing the.

**Mike Adams:** Yeah. We should leverage our notification.

**Jeff Whitlock:** Yeah, exactly.

**Mike Adams:** Infrastructure and presence and awareness. And I actually, I really relate to that. So then the other direction where local capture is your default. And it's three minutes in the meeting. We don't see anything registered. We never fired. An event because it's a difference between like they're not recording because they said not to. And we just literally never were able to fire a notification. And so you never fire notification. Then we can have the bot join instead.

**Ryan Johnson:** Exactly. But like, I think the, and maybe I'm misapplying customer empathy here or not, but like bots are a bit more visible than, uh, then desktop capture, obviously, uh, and so like we might want to be careful about just like throwing it in there. Like we want to allow you to like, okay, I want to opt into that behavior.

**Mike Adams:** Yeah. I see that. And that's truly symmetry.

**Ryan Johnson:** Right.

**Mike Adams:** Yeah. I mean, if you scroll down a little bit, Jeff, um, into the sharing stuff, it's interesting. Oh, sorry. Go up to where it's, yeah. Like grain bot includes explicit meaning consent disclosure desktop captures don't choose how each method should flow through your auto share rules below. Like that's the same premise we're talking about here in terms of like showing up as, you know, a disruption. And that one side of it is disruptive in terms of the presence of the recorder. And one side isn't at all. But then there's, you know, kind of almost the opposite implications, like what's in that text on the share side of it. But it would change the model though. And it would just change the design a lot if you just like relied on notifications. And then you basically make it a setting. Where it's like, should we try to fall back with bots if your desktop capture fails?

**Jeff Whitlock:** I think it just wouldn't be making this not try to do the vice versa thing, which is complex until just being like, call it like, just call it bot fallback or something like that. I think it'd be a lot simpler to grow.

**Ryan Johnson:** I really need to show that if they are defaulting to desktop capture.

**Jeff Whitlock:** Yeah. Exactly.

**Ben DeMordaunt:** So I feel like as I've been helping users set up their accounts, one of the things I've noticed is that it tends to be that they want. The same capture on every type of meeting.

**Jeff Whitlock:** You're saying they're fall into one bucket.

**Ben DeMordaunt:** They don't have. They always just fall into one bucket. It's either grain, bot or it's grand desktop capture. I have not really seen anyone kind of select the example you're showing, which is like, yeah, external meetings desktop capture. Inter means Grain Bot. So I understand that, but I wonder if there's like a simplification here, which is like just how do you want to capture meetings? And it's, you choose the default as desktop capture or grain bot. Like a customize for someone.

**Jeff Whitlock:** There's like old school like advanced settings.

**Mike Adams:** You actually had a prompt design that last night. And then I just, I ran out of just cloud codes nine credits.

**Jake Adams:** Yeah. Uh, that, that's kind of what I was alluding to is like, it's just like, seems like cognitive load that maybe not, might not be necessary. And then we could have progressive disclosure to, to manage.

**Mike Adams:** I like three settings that I had was kind of like, I just scroll down a little bit, Jeff. Using that pattern, which is like, so you'd have capture everything. Um, customize don't capture. Like that one, two, three is pretty simple to just think about. And then if you are in, so, but the question is, is like capture everything. Okay. But like by what method. That's still a secondary kind of choice that needs to be made. Right. Like by, by what default method. Or is it, we just say that the default method is one, you know, we just have these kind of like defaults on capture everything where we just try to like be as redundant as we can. And it's just a super simple setting. And we. Leave as best for the user. S unless you click on and then you're making a choice between bot and not bot. But like, but the like capture everything is capture all types of meetings, capture it on every platform possible all the time.

**Mike Adams:** That's why I would simple.

**Jeff Whitlock:** Yeah. That's how like if we were to go into direction like this, that's how I would conceptualize it, which like you would just basically select what meetings get captured. And then you would have, what's your preferred capture method. And then there would be a setting for fallback.

**Mike Adams:** Yeah. I think that, that's, that's great. Yeah. When I get back to my computer, I can, I can refine that direction. Thank you.

**Jeff Whitlock:** And then you can just, you can have like an advanced settings like carrot or something that expands to something that's more, you know, people want to mix and match, but we could also not even add that.

**Ryan Johnson:** We're going to open that Pandora box. I feel like we should be much more willing to. Build out the capacity of the power users really want. Like based off of email domain based off of email, all this sort of stuff they want all these rules that they can set up. And so like this rule based engine that we could expose. But the default is just simple. Single selector or whatever. Yeah.

**Jake Adams:** Where do we actually, where do we manage users interfacing with this like in their journey. Like do you imagine it being a FTX tech experience or do

**Jeff Whitlock:** we currently it is people, people currently in their F talk set up their auto capture settings. We have defaults.

**Jake Adams:** Do they, do they know, do they even understand like, like I wonder how strong the opinion is. Like around like if you're new to Grain, like do they like really have strong opinions that they want a bot or they don't want to bought.

**Jeff Whitlock:** Um, so, okay. So, Oh, I get, I get your question, Jake. So. Right now in the FDAX, they just select which meetings, but we default, they don't select weather bot or not bought. We just default to desktop capture. That's the current experiment being run. So it's like, it's primarily set around. It's from a letter to set around desktop capture. And then on the homepage, if people change a method, like if, if, um. Let me show my screen. So for example, like on this page, if people change something from, from desktop capture to the bot, then we prompt them to set up their settings. That's how it currently works.

**Jake Adams:** I've noticed that button, but I didn't ever really pay attention. Like, like interrogate it. Um. Cause I just get back to like, well, I started doing some research around like local, uh, local capture versus bot capture today. And overwhelmingly still like, like bop capture, you know, rules, rules the day. Um, but I'm like, it's like the point of view of like, you know, should that be so going forward. Um, I think that is this like tension around it. Right. There's just like benefits of each. And disadvantages to each. Yeah.

**Jeff Whitlock:** I, I mean, this is a perennial challenge. I think. Not to get too far off. I don't want to get too far off course into this like bot this esoteric kind of bot. Or not question, but I will share some context with that. I'm sure it'll come up more Jake so you can be thinking about it and share your perspective because I'd love to hear it. Is like, if you look at the macro direction of the world, I think bots are continually becoming harder and most of the platforms are putting more and more restrictions on them and, and, you know, it's ebbed and flowed, but the secular trend is like making it really hard for these things to work. And I think, you know, five years from now. I'm not sure they're going to be permit, like it's basically like a constant tip between recall and the platforms. I'd like recall tries to find ways to get around their restrictions. Um, and, uh, so that's like, that's like something to keep in mind. There's been multiple times where we've had to like kind of stop normal production work of our product and what we're doing. And then like have to like conform to these stupid new requirements put on us by Zoom. And Google. Me. So that's one strain of, of the bot that is a consistent problem and why I wouldn't bet on it in the long run. The second is that, um, while it is true that current numbers are way in favor of bot is because the five years of legacy on it. Whereas if you look at like this new experiment, for example, um, the early data suggests that activation rates are quite a lot higher on local capture. Um, and there's also a kind of like ancillary perspectives to support that like with granola success. And even, even when I had to sit down with Richard in, you know, recently, and we talked strategy, he was like very, you know, they just recently launched their sort of local cap that he was very convinced, like the friction of bots is still, um, problematic. Um, so anyway, I think, I think like over, I think, I've been other perspective a long time that we need to push eventually towards like a local capture only or local capture almost exclusive, uh, but I think it's going to take a while to really get there. Because you, because to be local cap, you have to have a mobile app. And I think you also have to have a video. And the things you need to have that are like a lot of, a lot of product investments that I don't think are the critical path to us getting relevant again in the market, like the critical path in the market is, um, is the MCP capabilities and working those into our main flow and then preventing and then dealing with a lot of our core model complexity and problems that make it hard for people to get the value out of it. That's what I see as the critical path, not necessarily capture. We just have to solve capture enough to be good.

**Mike Adams:** I think that bots only die if the platforms force them to die, but I agree with you that they become a minority. Use case. And I think that the general shift is like without a doubt local capture is better for Ftux for new users, new signup. Um, it's easier to get to that aha capture. You know, forcing a desktop app, popping up the notes afterwards. There's just, you know, everything about the local component is, is better from an FTEX perspective, but like, um, as an entrenched user, it's like, I value like I, I, I can't stand local capture. Overbots. And it's not even the video. It's the, just the reliability of bots is so much better. And I don't care about the video thing. It's annoying. But like the value of it just being there and showing up versus the unreliability of like the local capture for me is meaningful. And I might need to be a minority. But I think it's just worth calling out that like that's the, it re - enterizes, it reemphasizes the importance of like getting a coherent model where.

**Jeff Whitlock:** Yeah. We're going to be stuck with a while.

**Mike Adams:** Choice. We're going to be stuck with it for a while.

**Mike Adams:** And even I think the only reason it would ever go to like zero is because, um, the platforms have killed it.

**Jeff Whitlock:** Yeah. I agree with that. I think that's just the reality we're in.

**Jake Adams:** Yeah. Yeah. And so I think it's have a point of view around how we want the new users to experience grain. Then allow them to easily trade off to the benefits of the bot where they, like when they need it and when it's necessary.

**Jeff Whitlock:** Yep.

**Jake Adams:** Um, uh, bot usage is increased a hundred percent since the beginning of the year. So it's two X. And I did see that like MCP, people that use the MCP are twice as likely to use the local capture.

**Jeff Whitlock:** Oh, interesting. That's really interesting.

**Mike Adams:** But the other problem is that the MCP is much more valuable with bots because of the speaker levels.

**Jeff Whitlock:** That is true. But actively investing on making that less true with voice signatures and new diretization work.

**Jeff Whitlock:** That in a few days.

**Jake Adams:** Yeah. I just don't know if the user, users are like getting to that like cognitive understanding that like that it would be better versus I, I would imagine the first users is like, they're just going to have a strong opinion around whether they want that bot in there or not.

**Mike Adams:** That's going to be the strongest early opinion.

**Jake Adams:** Yeah.

**Mike Adams:** Until eventually you reach a point of realization of the value. That it's like, okay, I'm running into these downsides of local capture. Oh my gosh. There's this alternative. This is better for me, which is going to be a meaningful section of real business, you know, grade customers. And so that was the thing I wanted to bring up next, which is like we could think about, um, removing bots from even like the free tier, um, of users to where it's just like the free version of grain is granola. And if you want this customization kind of era and that's what bots have kind of moved into to where our existing user base, they're already there. But like a net new user didn't even really even think about bots unless it's in this kind of like upgrade path to solve a specific problem, but you've removed that like decision of even having to think about, you know, what capture method from that new user experience if we believe that the vast, vast majority of people that are signing up that are net new prefer the local capture. To get started.

**Jeff Whitlock:** I mean, I mean, one riffing on that is like as a. As Jake was saying, like I didn't even notice this button to try the video. And I mean, if we pull back from a reverse trial, you could use like trying bots as a trigger into trial or if someone opts into a trial, you could then onboard onto bots as an option. Just riffing on that. Instead of trying to like, I just think, I just think it's like, you know, like I still think our product is. I think the markets moved a lot, but it's, it is still a newer product. It's cognitively complex. I think like. Pushing too many things that are going to. Okay. I was going to feed back and just asking these are to grow up too many things early, early in the journey before they've ever even had an aha. I'm wary of. And so like trying to find a way to layer the bots kind of at a natural point subsequent attorney makes sense to me. That's probably a little, that probably needs to be a little bit stronger than where how we're doing it now is what I'm hearing from Jake. I agree with its resonating, as you mentioned, like I didn't even notice that button. Should we go to sharing. Should we move to Cherry Mike.

**Ben DeMordaunt:** Just one comment. The only thing I, I'm hesitant. To like say for certain is that new users don't want bot capture. I think the challenges like what at least I've seen is that like. The large portion of new users that want video captured meetings. And that's where they usually find the bot captures is when they realize that they're meetings have not been captured with video and that they want it that.

**Mike Adams:** Well, I don't disagree with you.

**Ben DeMordaunt:** Yeah.

**Mike Adams:** My question is what is who are those people? What is this? What are the attributes of that audience that really values that. Do you know.

**Ben DeMordaunt:** I mean, it's been kind of. It almost comes down to, to be honest, it almost comes down to more of their, uh, their age. If I had to give a tendency, it's like the older generation want the video, but it just feels like that's what I know this is I'm not, a little of ageism in here, but that's genuinely what I've seen is like the older individuals feel like they want video. And I don't know if they're just like that form of content better

**Mike Adams:** than realize the dividing sector you're saying is video, not method.

**Ben DeMordaunt:** Yes. Video.

**Jake Adams:** Yeah. They want the form factor video.

**Ben DeMordaunt:** They want the form factor of the video where like. It seems like it's skewed younger where people are like, yeah, I want, I just want the transcript. That's all I want. You know, like I just want to a record where, you know, I could don't need to go back and watch it. Just need that transcript for like AI workflows pretty much. Whereas old generations like, I want to watch that. I want to, I want to, you know, re - engage with that meeting.

**Jeff Whitlock:** I mean, I would say though, I would say though, Ben, two thoughts. And I think I'm actually curious what Mike said to is like, we should try to understand better patterns of the who. Yeah. I just had a meeting with, with a customer who said like, Oh, I just, I've been showing people grain. And the people I'm showing grain are using Otter and, uh, firefly is consistently. And, um. And, uh, sorry, Otter and Granola consistently. And then I always, I showed them Grain. They're like, Oh, this is so amazing because it has the video. And so they've been swapping over for that. Um, so I, I still see it a lot in the market that the video is a reason why people choose us over some other options. Um, but, but I'm not entirely sure if the obvious correlation with like persona or sorry with role or company type.

**Ben DeMordaunt:** Yeah. That's what I was going to say too. Like I haven't seen that. Like I haven't seen a trend to be honest. I'm just, if anything just feels like age, which is an odd characteristic, but that's really all I could find a through line on.

**Jeff Whitlock:** But to that point, sorry to, two, two thoughts. One is we could still put it like if, you know, again, we're just riffing here, but you could just put it if you put it in the trial.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** People still try it. Right. And get it. And I don't know if like you need to be as generous with the premium. It's also it's more expensive. And then the other thing that was, you know, at some point in call it two quarters, maybe like two quarters or so, we will have video on desktop capture. And it will just be about the method and not the medium.

**Ben DeMordaunt:** At which point. I think this problem comes a lot easier.

**Jeff Whitlock:** Well, I think, I think this idea of like leading with the perspective on desktop capture with a bot fallback becomes like makes a lot of sense in the law in like the, you know, the mid run when we have desktop video.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** C'è quality thoughts about that.

**Jake Adams:** I think. That. Or I wonder if just the bigger opportunity is actually. Showing people what can be done as opposed to like us being an alternative because certain people want to video. Right.

**Jeff Whitlock:** Yeah.

**Jake Adams:** Is that, does that make sense? Yeah.

**Jeff Whitlock:** For sure. I agree.

**Jake Adams:** Yeah. Right. Like, like, cause we are that. I think like, like, and that's good.

**Jeff Whitlock:** But I do wonder what's going to get us to the next level for sure.

**Jake Adams:** Exactly. It's like if we do the 10x framing, right, it's going to be that we are the by far the best experience to get the right meeting to, to get the might right meaning data to your agents.

**Jeff Whitlock:** Yeah. I agree with that.

**Jeff Whitlock:** And which is it, which goes back to what I was saying earlier about how I honestly, I think there's some things we need to tighten up here, but like this whole threat is not the critical path of my perspective. To turn the corner. Like it's like, we need to fix some of the problems because there are some big problems, but

**Jake Adams:** like, well, I do actually think it is. I wrote this down. I, I think there are three tenants that really matter in this business right now. Yep. And number one is reliable capture. Right. That like, I know how and when my meetings are going to share it or like in other ways, what should Grain record automatically for my team and do I trust that it will work?

**Jeff Whitlock:** Yep. That's our strategic universal capture pillar.

**Jeff Whitlock:** So fully line when I say it's not the critical path. I'm not saying that capture is not the critical path. I'm saying pushing to having, uh, like video local.

**Jake Adams:** Oh yeah. No, I don't think with your local map. Like that's, I think we need more information to understand that. Yeah. And I do, I do think there might be a competitive advantage in the future too. Right. Where it's like, we're able to process that information. You know, more progress. Like more like, you know, like

**Jeff Whitlock:** where it helped, it helps, it helps.

**Jake Adams:** Or like, like it's more useful. Yeah. Yeah. Yeah. Like it actually produces some value. Yeah.

**Jeff Whitlock:** Um, but anyway, what's tenant tune

**Jake Adams:** three, I had four, but I removed one. And I'll talk about that. Ten to two is just correct access control. Like that it's sensible and reliable.

**Jeff Whitlock:** Yep.

**Jake Adams:** Um, and then tenant number three, I don't have a good way of saying this, but like no, no fuss agent consumption, right? Like where the, it is the ideal format for you to consume that agentic, that information agentically. And I removed contextualization from that. Like it is, that is an, I think, actually a nice to have in those three pillars. And so like in other words, I didn't finish three, but I said, what should, yeah, so what should Grain record automatically for my team? Do I trust it? And do I address that O - work? Are the right people going to have access to my company meeting data? And I actually framed this with a voice of the CEO, actually, I think. And then, yeah, and then can my team like leverage this meeting data to like the fullest extent.

**Mike Adams:** That's literally the exact same framework that I came up with earlier in the week. I don't know that I even shared. Out.

**Jake Adams:** So literally all week I have to do is if we can, they feel confident that it's going to capture the right way and the way they want it to be done and reliably. It's get access to the right people. And it's in that format for them to use it. And like, I don't think really anything else matters.

**Mike Adams:** So the framework that I came up with is called the account stack framework. I've shared it with Ben and a little bit with Jeff, but, um. I was thinking about it, Jake, from this perspective of like, I'm trying to sell RAM. They have a bunch of people. They're in this, they're in their own state. I don't have any visibility into their settings around their like auto capture, not auto capture desktop install. You know, consumption patterns and then getting the information out of grain. So here I'll share my screen on this. Framework. So it's like a whole framework and they ended up applying that framework with the specifics of, um, like our data model and the difference between kind of state - based visibility that's off of, that's sitting in Postgres of like, what is their setting now. Versus amplitude, like activity or engagement around that activity? Because I think one of the challenges for us is getting in a world where like we're completely elitely reliant on the event - based stream. And it's like, it's very difficult to get that actual picture, you know, of, of what an account looks like. So. Applied that to. RAM here. And I think this is the one. Yeah. Um. Actually I pushed this quite a bit further, but this stage zero is just like, what's true of the account. Right? What are there's the facts where are they out on the trial. You know, when does their trial expire? What's the value of this thing? Stuff you'd put in like HubSpot. And then stage one is capture. Um, and then there's this kind of workspace level look at capture. And then the individual configuration of capture. So like this is a much clearer view into this account. Of the ability for me to see, okay, I can actually see the pattern. That it's really been driven by JSON. And so then Jason is this key part of the sale or this understanding of how this account is working.

**Jake Adams:** And because what does A, I mean.

**Mike Adams:** Auto record, internal external. So like, it makes sense that at this higher level of like the workspace config, their auto record internal external is off. And then that's when I discovered that in Grain, you literally because of what we did with teams, you can't even auto set people's internal external to on at a workspace level anymore. Like instead, because that got moved to teams and we don't have a default team and there's no way to do it outside of like adding everybody to a team. So anyway, that's capture. We'll go back to the other doc. Um, that's the application of it to RAM. But like, um, no, this isn't it. It's this guy. There you go. So I've been finding the creation of infographics is a double - edged sword. In some ways, it's great. In other ways, it takes a lot of massaging. But this idea of it, does this map with what you're saying, Jake, that it's all about having real visibility at an account level and then at an individual user, because they interplay with each other. Hapture, consumption, at least what I'm calling it. Like the human side of it and the agentic side of it. And then AI recalled this third level three artifacts. I was calling it create. Maybe artifact is better, but it's this. For what? Like, okay, cool. It's getting consumed by the agent, but consuming it by the agent doesn't actually produce any value. Until it gets included into something of substance and value. Same thing. There is a little bit more value on the human side of consumption, but even that contributes towards this like four what? Why am I reviewing this meaning? Why do I have this transcript? Why is this an ingestion? And I don't think this is the perfect framework, but this two by two is the recognition that it's like some combination of kind of a user is creating these things or an agent is creating things. And things are either being created on grain or they can be created off - brain. And so the, the better, my point is that the better visibility we have onto this at an account by account basis and then aggregating that across our account shows us patterns of usage profiles. Et cetera. Um, I think it's essential for us to make any good decisions. And it is also the driver of our focus and our priorities. Cause that's really what ultimately was the foundation of your comment, right, Jake? Was like, what matters? And you're saying what matters is making sure we crush it here. And we crush it here. And we crush it here. Well, there's so much we can control here, but really

**Jake Adams:** it's what we're trying to do there, Mike, is that we're trying to empower that artifact and wherever they want to do it. And we don't. Actually give a shit around what they create. Right. Like it's just like, we just want it that we want to enable it.

**Mike Adams:** And right now at the right amount of token consumption.

**Jake Adams:** Yeah, that's what I'm saying. It's like the form of that creation, it doesn't matter to us. It's that the data is available and ideally structured in the, so it's, it's that it's, it's available in the right format, which they have like an idea here, right? It's going to like, uh, maybe. And then that it's, um. Yeah, and then it's in the right, the best format to do that. And then what would be great is that it's also, you know, has the right connections to other like data that we have. Right. But that is like an ancillary. Right. But if it's, if it's available. And yeah, really, honestly, yeah, is it, is it, if it's available? And then the question will be is like, does there need to be this extra work that has to happen for us for any lay user to leverage it that needs to like some level of bucketing. Around some context, right? Or like, can we just throw everything at them? Um, but yeah, so you're, and I would say the, the difference in what I'm saying is like the consumption part is like, yeah, you're saying comes consumption is like, it's like, that's access control. Is that right? It's not that I've actually like using like. Cause I'm like, for me, I'm like,

**Mike Adams:** maybe better than consumption is access. Consumer. Like consumability. Cause there's two dimensions of that. There's the configuration side of consumable. That's the setup. Right? That's what's been called policy in this framework. And then there's the activity. Around that. Right. Like, okay. It's possible for me to view this recording. Do I actually review this recording? Those are two different measures, which are kind of both accounted for in this framework. Cause you want to understand at like the Postgres level, what is the configuration right now. For this group of people and at an individual level? What is the actual behavior of these people over time. Um, around this consumability. Is it consumable? Is it being, is it actually, is consumption happening. By agents, by people. And so it's, it's a lot of dimensions to cut it on. And I don't know, I don't know that this framework is perfect. But it's like a starting point for us to at least kind of like have a shared mental model of how it should work. And that we're designing and building around and we're selling around and we're, um, driving visibility and analytics around to, to push on support and configuration and setup, because if you are like, if you're cruising in each of these dimensions, like. That's great for our business.

**Jeff Whitlock:** The one thing I would say just about the L3 in response to saying like, we don't care about what they do is that our, one of our explicit objectives is this quarter is to try and create more user education content to inspire. And help people know what they should be doing all three. So while it's not necessarily like a product, I agree with you on the product perspective from a product marketing and a content perspective. I think it's very important.

**Mike Adams:** It's something that I think what Jake is saying is that this doesn't really matter. This isn't a big thing. This is the big thing. I don't know why AI called with the strategic warning stack bypass. Cause I don't think I really agree with that.

**Jeff Whitlock:** I actually think I even saying there. I don't really.

**Jake Adams:** Yeah. All that matters is the quadrants actually like yeah, it's yeah off grade, aging created. Yeah. Like whatever the hell.

**Mike Adams:** And so this is being like, don't let that happen, which is what I think a lot of MCPs I'm seeing like hacks and platoon in particular. They like, they don't want you to have access to the raw data. They want you to like have the MCP go and use their report creator in it seeds the prompts that generates the thing, but you still brings you back to hex. And so they're, they would be viewing that as like a strategic warning.

**Jake Adams:** Okay.

**Mike Adams:** I don't think that we view it that way.

**Jeff Whitlock:** I think we're.

**Jake Adams:** Yeah. So are you guys ready for my provocation. Let's go.

**Jake Adams:** So the mace, so I brought up this. So the company called Mesa dot dev. Like he's, they're trying to build like the next GitHub. It's like really interesting. Like, um, you should, we should look at it right in together. But they've gotten a lot of heat recently around just basically a potential format to create this

**Mike Adams:** like meaning like market momentum or heat meaning hate a market momentum.

**Jake Adams:** Right. I just talked to him on Tuesday. Actually, and they're great users. And so the couple of different threads here, but, uh, they, um, and that he raved. He's like, we've tried everything and Grain has the best, most reliable capture. So, and like, so their smart kids, um, building this like GitHub alternative, but it's like, so it's file base to be consumed by agents. And it's those versions. And, but it's, so it's like this interesting like GitHub meets like file system. And I looked at it as like, maybe that's like, and other people are looking at is, is this, that's it. It may be an interesting substrate. To leverage knowledge graph on top of, like a company context layer. And so that's where he's getting more momentum. The tool's not ready for that yet. Like I just played around with it like no normie could ever use it. Um, but what I get to, so it's like, that's anchoring. Is grain users, but like. In this space, thinking about this space. And then I, when I did all this research with the like and playing around with the like, uh, the radioactive stuff is I just pulled the last 50 days, 50 recordings into a SQLite database. And so like. I think, and what he said is that, and this is why I brought it up and then particularly right now. And see, he doesn't like granola pezzi. It feels like a wild garden. Right. And I think he, the future beholds that that's not going to work. Right. Like people want the access to their raw data. They don't, and they don't care about the notes. You know, I was just talking to Hank Taylor about this last night. Like they just need the transcripts. And so like, what if we could just give them a hosted version of what like that SQLite experience could be. Like could we just give them a view of the database. Right? Where they can pull like the most easily interfaceable, like, like mechanism to like pull that transcript data. Right. Does that make sense?

**Mike Adams:** And then pair with a CLI. So that. Interface with it, which is why like super base is killing it. That combo. It's the like, this is your freaking data. And this is a UI. This is nice. You can go in here. You can do whatever you need. There's a safety component of the complexity. We're abstracting.

**Mike Adams:** But like it's fully available to agents to do whatever they want.

**Mike Adams:** As if they're you.

**Jake Adams:** Yeah. It's the schema and the data you as the user have access to.

**Mike Adams:** That's the winning posture for sure. Uh, I think that like this came out of AI's assumption of the strategic warning because it is, it seems like it's, you know, you're kind of screwed, but I, the question, what it comes down to is, is there enough of a business at L1 and L2 if you really nail that. And that you enable this kind of off platform creation where. It's, it's this, it's this almost marketing position of independence of, of autonomy, uh, yeah, like, uh, what's the word I'm looking for. But like, you know, freedom from the model companies and platform independence.

**Jake Adams:** So this would be bucket three of like eight, like no fuss agent consumption, like the best form factor to be consumed. And that's not defensible. Like that's just like, if it works and we figure it out, like people are going to copy it. Right. The, the defensibility is like to what like this conversation with mesa was. It's like. You're the most reliable to capture. And like, I like, I trust that this is going to work. Like that I trust the access control engine. Right. And then over time, like, can you get better at giving me more like making that like leveraging that data with like proper with context over time? Like, you know, tools and buckets and all that shit. But like, that's where the cool, what's cool. If you expose the database, it's just like, you can expose all the people too. And whatever freaking edges that you might have with that recording.

**Jeff Whitlock:** Yeah. It's an interesting provocation. Definitely, definitely they're, it's interesting. Like I look at that webinar. And I mean, this is just totally swagging based on, based on my read of the room and the chat.

**Jake Adams:** Well, webinar.

**Jeff Whitlock:** We did a webinar. Yes. Yesterday about awesome.

**Mike Adams:** 500 people crazy energy. Yeah.

**Jeff Whitlock:** And I would say. I don't know, maybe a bit more, but we're like super into what Mike was showing that was like, you know, this is amazing. Like I want to build this is what I want, which I would say like what you're proposing really would be like, just catnip for them amazing. And maybe that, but that's a, it's a turn feels like a market segment. And then there's like another segment that was like. I don't know what an M.

**Mike Adams:** Way too complicated for that.

**Jeff Whitlock:** Exactly. So it's like anyway, and it's just interesting, like where to like, and I invest in which order to kind of build and maintain momentum.

**Mike Adams:** I think it's the catnip. One.

**Jeff Whitlock:** I mean, cause we already have a product

**Mike Adams:** for the ones that are like, Oh, it was simple. Like I just want the notes. It's like, all right, cool. Like choose cream.

**Jake Adams:** Skate to the future and let that agent harness and that, that context layer that we are agnostic across both of those criteria. Or buckets of like, you know, how are you, you know, from the harness perspective to the model perspective, like let that help us grow.

**Jeff Whitlock:** Yeah.

**Jake Adams:** Right. So like mesa. dev ends up like totally pivoting into building like that is like their product. As opposed to like this like agentic infrastructure. Like we're there. Right. And like those are the users. And if people are able to progressively, you know, improve that. Like user model and like, like experience to make it intuitive than we benefit from that by being the infrastructure.

**Jeff Whitlock:** Right.

**Mike Adams:** Do we go to the share piece. I can share my screen now and I'm sitting down and driving. Kind of out of time though.

**Jeff Whitlock:** Let's introduce it. And then we can, uh, I like to ask that everyone share thoughts. Just to kind of riff.

**Mike Adams:** Well, Jake was going, I added this. I think that's a pretty simple model of just like always capture. And then it's using desktop. It's your default. And then fall back to grain bot and local captures and available. And then there's an implication there that we're just going to be better at detecting when the bot can't get into a meeting and then letting you know that it can't get in a huge amount of that value is just letting you know that your bot isn't in. That is that safety. A lot of this like we're best to capture doesn't even actually have to be that we are the best at actually capturing. It can be that we're the best at letting them know if it's capturing or not and giving you a psychological safety. So anyway. And then this would be like the customized world and then just don't auto capture. It's pretty simple. Um.

**Ben DeMordaunt:** Is that you shouldn't ever have a don't auto capture. You can either always capture and customize.

**Jake Adams:** Do these things change below? Can you flip between these dialog.

**Mike Adams:** Sir?

**Jake Adams:** So can you do the do the external internal things change as you switch between always capture and customize? Like what like, I guess what goes customized do. Yeah. Yeah.

**Mike Adams:** Customize gives you the ability to break it out between meeting type.

**Jake Adams:** Who would. Okay. And then yeah, gotcha.

**Mike Adams:** So I don't want to capture my external, but I want bots to capture my internal. It does help capture to capture my unscatch.

**Jake Adams:** I agree with Ben. They're like, that's intuitive enough that you just dropped that down and don't auto capture.

**Mike Adams:** You're saying just get rid of this.

**Jake Adams:** Yeah.

**Mike Adams:** And then they think you need it. I think that's one of the reasons that people value grain is that we are like user friendly and that otter and fireflies and others are always just like, there's no way to turn it off. Like it's just this virus. Like Michael from Vistify walked in the other room the other day and said that to Jeff and I can't, I can't, I don't know how to get these little fuckers out of here. Like I can't imagine a world where we like completely remove that ability. It's just feels like at counter to our ethos.

**Jake Adams:** Um, no, it's not you just would like you would encoustomizing murk auto capture.

**Mike Adams:** Oh, I see. Okay.

**Jake Adams:** It's just, it's as much.

**Mike Adams:** I don't know. I like the simplicity of this model. It's like it gives me a sense of like comfort and peace to be like, Oh, okay, cool. Like. Yeah, just don't. And then grain, I don't know. I think that. Um. Otherwise I have to come in here and go down and go to don't, don't, don't.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** Well, um, let's do this. Uh, we're over time, but Mike, you're in the office next week. So we can get into sharing until then.

**Mike Adams:** I think that's probably the short version of it is that you can say like share both types of captures, only share bots because it wouldn't make sense to only share local captures, in my opinion. Um, because local captures are just like more private by nature. Um. And so what that would do is basically give you the ability to say, yeah, when it's bought, it's being disclosed kind of this sentence. And then just don't auto share. So like this is like an account set up for failure. But then that goes back to the county count stack is that we should be like fully aware of when an accounts in this situation and learn from it. That's another argument for this don't auto capture is like maybe eventually we get rid of it, but we use that as like a really strong signal that someone is, you know, set up in a place where they are not going to be successful. We reach out. We learn. Um. So then if you have bot only, you know, labels as such, but same kind of organization here, but the premise being like participants only. Participants in select teams and the teams are just simply a sharing destination. And then the admin side of this too that we can kind of get into, um, but like, uh, anyway, we can, we can share more about the, the model, but like surfacing the fact that there are these integrations that are kind of like above and separate from these rules that are like kind of talked to your admin if you don't like it. And then your admins can basically kind of like force you to follow these rules. And then at an admin level, they force which teams follow which rules. So it gets moved to one place to manage the enforcing of the rules and the settings, which is just massively missing cause it's buried across each of the teams and teams ultimately just become a group of people with a checkbox that like can be associated together around, you know, sharing. Groups.

**Mike Adams:** I mean, that's my written, my opinion, the way it's always should have been.

**Mike Adams:** So I don't know how Octanes became what it is, but, um, this to me seems like exponentially more simple. The one other thing I'd say is. This whole idea of participants only. This is something to chew on. Limit auto sharing to internal participants only external attendees won't be auto shared with. I don't know. It's just what AI named it. But that premise was deliberate of. I think most of our competitors, especially on a free plan. Will send out the notes to non external participants. I think a huge amount of our lack of growth relative to our competitors. Is this one setting where we refuse. We don't even give it as an option really. If you look in actual grain to send, uh, the, the recordings out. So this also has an implication in it. And this is for Ryan. I find it very annoying when I'm a grain user and I'm cross call and it's somebody else's recording. And I'm like, okay, cool. Like, you know, especially consulting. And I don't get the call in my meeting. Like, I feel like I should. Um, I should, I should see the call and grain. I'm, I'm participant, but we don't even really like consider that world. And it's bad for our growth. And you should be able to turn it off. But to me, that makes sense. And then the same thing here with email recap, like on a per type basis. And this, I did a bunch of research on this and only me was like without a doubt the biggest request across all of the, uh, email recap. But to me, this makes sense to be like, okay, this is generally the sharing of these types of meetings, you know, and I only want these types of captures to come in to the sharing world. And I either want it to only be, you know, to be all the participants are just my, my team participants. Um, or the select teams. I'm going to kind of going from like the most restrictive to increase in the mort restrictive until it's just like, okay, everybody in the workspace gets access. And then the email recaps are either like the same audience or it's just me or I just don't want email recaps for these types of meetings. Um, and this to me, this email recap piece and this organization, it feels like a huge improvement over the status quo. Especially more coherent when you then have the admin version of these settings that then kind of trickle down in our fourth inheritance. But some to chew on. I know we're out of time. Okay.

**Jeff Whitlock:** More, uh, more to riff on next week. Thanks to y'all.

**Mike Adams:** We share all the stuff I shared with Jeff out in the exec channel.

**Jake Adams:** Um, I. Should we plan on not having their Monday meeting and just jamming on Tuesday. Yeah.

**Jeff Whitlock:** I think that's where you're going to plan on coming the office, Jake. Yeah.

**Jake Adams:** Yeah. I can come. I, I walked off that one day. So yeah.

**Jeff Whitlock:** Yeah. I think yeah, whenever you just come in, we'll just, that'll be in lieu of it.

**Jake Adams:** Okay. Sounds good.

**Mike Adams:** Is it memorial day on Monday?

**Jake Adams:** That's the next Monday next Monday.

**Jeff Whitlock:** Yeah.

**Mike Adams:** Good. I'm glad I'm not traveling there during the closed office day.

**Jake Adams:** The one thing I'd say is to sit and ruminate with is like, and I think everybody's doing this, but like one thing that feels like it's still not concrete is like. Who the, like what the buyers lenses to all of this. Right. Like it's like, is the buyer. The CEO. Right? Like, and I think if we have that and like what that, how that cascades, um, or do we believe that actually people will come in as individual users. Um, self serve. Right. Um, and like, I guess there's two is the buyer and then like, how do people really like how. Where does it start at, at the organization?

**Mike Adams:** That's what I was telling Jeff yesterday is the biggest thing in the business is the model. I felt like the product stuff is, if you're to narrow it down to product thing, I think this, what we've been talking about is pretty much the top, but the actual model itself is from, from a selfishly as a business, it just feels like pulis our buyer, how much are we selling it for? What is our motion. Like that is all up in the air right now. Um, and then the messaging and positioning on top of that, which changes depending on the virus. So I put together a ton of stuff on that that's worth reviewing. Here, let me. Share out. So like years ago, we, we did this exercise of the guy named Garrett, who's a nice dude, but ultimately, I don't think we really ended up using his stuff, right, Jeff. Um, I already found his frameworks for fantastic. The actual work we did have was fine. But like with this whole knowledge graph thing that I've done, um, put all of this together that's worth reviewing. Um, it was off of his frameworks. And then all powered by like the wiki. I need to do another version of this because I think it's evolved a little bit. But just, just calling out and I'll show the link to this folder. But it's worth. Putting some eyes on and seeing if we can get to a point where if we had documents like that around ICP messaging, positioning, um, narrative and story and pitch that we're all aligned were like, this is it. That would be huge. Cause we've never really had that level of alignment across that whole spectrum. I think we've had like alignment on one piece or the other given times. And it, you know, morphs, but I think that'd be a valuable investment to get everybody on the same page there. Yeah. And this is just a starting point. Uh, cool.

**Jeff Whitlock:** Hey. Yeah.

**Jake Adams:** Okay. Catch you.
