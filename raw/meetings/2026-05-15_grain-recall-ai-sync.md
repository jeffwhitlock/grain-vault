---
title: "Grain <> Recall.ai Sync"
date: 2026-05-15T19:45:20Z
duration: 26 min
participants: ["Chris Naismith", "Elliot Levin", "Jeff Whitlock", "Mike Adams", "Ryan Johnson", "Amanda Zhu", "austin", "Tucker von Holten", "David Gu"]
attended: true
processed: true
processed_at: 2026-05-15T21:00:00Z
wiki_articles_touched:
  - companies/Recall.ai.md
  - companies/AssemblyAI.md
  - companies/DeepGram.md
  - people/Tucker von Holten.md
  - people/Ryan Johnson.md
  - people/Chris Naismith.md
  - people/Elliot Levin.md
  - topics/Diarization.md
  - topics/Engineering Decisions.md
source: grain
grain_id: ef76b47a-703a-433c-b05d-d1e8108ae715
grain_url: https://grain.com/recordings/ef76b47a-703a-433c-b05d-d1e8108ae715
---

**austin:** I think there is a chance, let me check here. I believe he should be. But. Then on your end, does anybody else joining?

**Chris Naismith:** Jeff probably will not be, but Ryan most likely will be. Not just, I believe it'll be a quick one. Might end up going over sort of the red around like the diarization stuff, but I also don't really think that he's had a huge amount of time to take a look at that yet. So we'll see.

**austin:** Yep, nope, that is totally fair. I know he said he was just getting to it too. And so I imagine he's probably got to spend a little bit more time there.

**Chris Naismith:** So if you don't mind me just asking, so with the diarization stuff that I believe you implemented, that is taking the provider data that both DeepGram and AssemblyAI does, and you guys just massage the data into like the payload that exactly.

**austin:** And the nice thing too is we've used kind of like our big data set of recordings to get some ideas of how we can sort of flag when you probably shouldn't trust the transcription provider labels, because you can kind of look at a lot of data from the past and see when it actually is right and when it's wrong based on like how long it's seen audio, for instance. Hi, Ryan. Awesome. I think everybody is here. So I guess we can kick things off. I guess, yeah, to start, if the general things too, that I've come up with issues or bottlenecks I'd love to hear anything that we'd be able to help with.

**Ryan Johnson:** So I know we had that thread going around 2.0.14. Where it was kind of captured asking for the screen capture permissions. So I don't know what the status is there. But then the other, I had a couple of questions around Austin some of your messages around the experiment stuff as well. So it's one of the two things that are top of mind for me.

**austin:** Yeah. That's perfect. Well, I can give you an update on the discussion about the 2.0.14 Safari screen capture issue. We looked into that and it looks like this behavior has actually been there for a while. And the reason it happens is because on Safari, it actually uses the screen capture permission to determine the active speaker. We're going to be investigating that next week though to see if we can get around that because that would be ideally nice to avoid obviously having to request that permission.

**Ryan Johnson:** Right. Yeah. Sounds good. So I guess. We probably should avoid updating because I was, I need to kind of figure out maybe on our end like why we've not ever triggered that. I think it's because we've never like gotten the signals that we were expecting from the meeting detected that would allow us to try and trigger it. And so that's the reason, but like something changed in 2014 that would make it so that we would trigger. I don't know if that was just like the addition of a URL or some extra metadata in the meeting detected that we were then starting to trigger it. And then that's the reason why we ran into this previously unseen issue.

**Chris Naismith:** The main thing is like it shouldn't be. Granted or like because of the init permissions option of the SDK where we are not requesting it. Like to me, it shouldn't just like in the middle of a thing try to ask for it. Given that this kind of opt-in flow that this is actually.

**Tucker von Holten:** Yeah, this is absolutely a bug. Like I just want to be clear from our end that like this is not the behavior. The proper thing 100 percent should be to do a screen capture. If we can't figure something out within the next week of like, how do we fix this problem permanently? Then what we'll do is just put a gate around that to just make sure that if you don't have the permission, we just don't get that metadata back.

**Ryan Johnson:** Yeah. That makes sense. I think we probably could do a little bit of defensive stuff on our end to avoid this particular issue so that we can just so that we can upgrade. I do want to kind of get the new versions out just to, I know you guys are doing other bug fixes in them. So I think we'll probably figure out a way to do that. Because already we haven't been popping up in the Safari. So it won't be a downgrade for us. So yeah, sounds good. I appreciate that. So yeah, just kind of keep us in the loop on the status of that bug fix. The other thing that was top of mind for me, I mentioned it was with the experimental diarization stuff. The two questions that I had, I think I posted one of them in the channel last night, Austin, but like does this do anything as far as just like changing the payloads that you folks are giving us or anything like that when it comes to like, for example, like the system audio capture where, you know, there are no accessibility based like speaker change events or anything like that. Are you now providing more speaker related information in those or is that still something that we'll have to pull out separately if we want to use the diarization for those.

**austin:** Yeah. That's a great question. So first in terms of just things that like might change as far as what you should expect, really the only change might be in the case of when you have the unknown feature enabled where some words might be labeled null if that indicates we have no confidence basically in the attribution for the speaker label. And then, but it technically according to our schemas should be nullable. Some people have not necessarily accommodated for that. But if implemented according to our types, everything should be good. And then, as far as what to expect in terms of information, you should really only expect generally speaking more information. So like, for example, in the ad hoc recordings, the speaker labels should pass through. You shouldn't really run into any situations where you're now suddenly seeing less, like only like pseudo participant IDs instead of what used to come, which might be speaker labels.

**Ryan Johnson:** Cool. That sounds great. I will, I need to still play around a little bit and so to give it a fair shake I was trying to test it here right before the meeting. And wasn't getting audio capture work on a Zoom call on it. I need to debug that a little bit more to see if I have an actual issue or something weird set up on my end. So I'll get back to you on that if there is an issue, but that sounds great. I'll take a look at those. The other question I had was, I know that there is at least some amount of shared DNA between the SDK and like the recording bots. Does this diarization fusion work, does that have also any plan into the bots, or just the SDK.

**austin:** Presently, it's all gated to just be affecting the SDK. Things just work a little bit differently on some things. And so as long as it's in sort of beta phase right now, there's not going to be any sort of leakage.

**Ryan Johnson:** Okay. Yeah. Sounds good. I mean, I think we are looking at, yeah, diarization stuff is top of mind for us right now. So I appreciate you guys pushing on this. And I'll play around with it and let you know if I have any other more kind of concrete questions about it. Cause we've been doing a little bit of implementation stuff on our end. And then I think some of the work you did probably for the best kind of made it to where maybe some of our work is no longer needed, which is great. We love being able to delete code. So going to try that out and see how it goes for us and see if it works for what our needs are.

**austin:** That sounds perfect. Just let me know if you have any questions there. I know I had sent a message regarding the unknown feature. Some people oftentimes cause you see a lot of words that aren't labeled. And that's because it turns out before the models aren't actually great. But if you always guess that the previous speaker is speaking, it looks like they're good. And so they get surprised by that. And so sometimes it requires post-processing there to say, well, we have unknown, but if we're in a sentence, let's just attribute it to the other word in the sentence.

**Ryan Johnson:** I have a feeling that like DeepGram, for example, sometimes I think does that maybe in their results actually. I don't know. Maybe I'm wrong, but like I had a hunch sometimes. But maybe they were doing that.

**Chris Naismith:** And so they might just thing when I was doing stuff, they just rolled it into the other person. Whereas Assembly had its own issues with like the turn based stuff.

**Ryan Johnson:** So it's yeah, Assembly is much more willing to return unknown than DeepGram was, it seems like.

**austin:** So yeah, interesting.

**Ryan Johnson:** Just so you guys, this is a heads up to you guys. We have been running on DeepGram because they have had the streaming diarization stuff, but AssemblyAI released their discrimination. Their first pass was not great. We're testing, they've taken a second pass on a particular with their like pro universal streaming pro model. And my quick testing was like, it seems decent enough. We're going to a much better deal with AssemblyAI than what DeepGram's. So we are actually going to be moving everything over to AssemblyAI.

**Chris Naismith:** Question. If either Austin or, is the work that you've done, does it also implement the word based speaker labels? Just cause that was something that they released recently. Before it was like speaker labels per turn and now they've done per word.

**austin:** So the speaker labels really should be essentially issued the same way that they come into us. So if we're getting from the transcription provider per word, you'll get them per word. If you get it per turn, you'll get them per turn.

**Chris Naismith:** Awesome.

**Ryan Johnson:** Sounds good. Give it, we'll give it a go and let you know if we have any questions or concerns.

**austin:** Yeah. Awesome. Thanks so much everyone. I appreciate it.

**Ryan Johnson:** Sorry. One last thing.

**Chris Naismith:** One last thing that I just wanted to ask. You had mentioned regarding the types, which is kind of wondering with the SDK right now, the real time events are typed as like the data property is just of type any given that obviously it's based on the different types that you pass in when you do the temp token and yada yada, but just wondering, especially on events like the transcript data event that is obviously very controlled by you guys, was just wondering if that could be typed. I know the provider data would obviously be a little bit harder because it's based off of external providers, yada, yada, yada. But just wondering if you had any like recommendations there for having it as typed as possible, especially as you change your types over time.

**austin:** That makes totally sense. Let me think here. Tucker, you might even have better input on this one as far as seeing the different forms. I've talked a lot at how things have performed, but in general.

**Tucker von Holten:** The transcripts that we have that are coming from the normalized versions should have a similar typing system. We have not implemented TypeScript types for them. Really at all. And that like part of the reason for that is because our documentation shows the schema for the resulting piece of that for the bots. And that should be the same like the actual transcript as it comes back should not differ from the bots. It's one dot 11. That said, there's no reason why we shouldn't have a typing system that works for that. I think this would just be a question of priority. I imagine right now our internal priority is probably much more closely aligned with trying to get the stability fixes out in the diarization fixes out. But the moment that we start branching out into actual forward facing features, then I think that that would be a very good time to implement that. A lot of the question about when that would be would probably be best addressed by Elliot because right now I think he's probably focusing more on just the stability. Like that's our number one priority for the SDK. But within diarization and in the life cycle and like media sources.

**Chris Naismith:** The other thing that I was wondering is this has been a topic of discussion is just around like, you guys having obviously much more data than we do given the analytics through like Datadog and stuff like that. What I was wondering, and this is just my own thing, Ryan, maybe this isn't as relevant for you. But I know that in the past, you know, we'll give you like a grouping of meeting IDs. Oh, we can fix it. We can't fix it, whatever it is. But I feel like frequently you'll come out with like a new SDK version and you'll say the fixes for that, fix this for that. And I think just like knowing if we had recordings that were impacted by some of those fixes, I think would be like a good thing to close the loop on, especially with some of our customers and let them know like, Hey, like this has been fixed for when we release a new electron version.

**Tucker von Holten:** I think actually to that exact end, we've been talking more internally about like revealing more for the customer logging just because in general, like we wanted to do one, we want to get more information to users anyway. But like just that would be a little bit of an overhaul because we would have to basically go through the entire logging system and figure out what should be and should not be considered a customer log. And I would like to err very much on the side of give more information. But one of the big reasons and pushes that we've wanted to do for this as well is like we started implementing an MCP server. And if we can implement that MCP server with the logging and associated with like customer logs, it would be much easier for everyone in the debugging process. Instead of you guys having to be like, here's a recording ID. You could be like, here's the problem.

**Chris Naismith:** You say like customer logging, are you referring to like in the Recall dashboard, you would be able to. So we wouldn't have to.

**Tucker von Holten:** Log to models with the SDK, not just for the bots. I mean, that's the big thing that we're trying to push forward again. I mean, the biggest thing here, but that is absolutely something on our list of things we'd like to do. Follow up with Elliot. And a big reason for that as not to drop a bomb, but like I am also heading out of Recall. So it's good to follow for these sort of things. Yes. All positives, you know, but I just wanted to show you guys as well. I've been working with you guys for about a year and it's been interesting to, you know, say goodbye.

**Ryan Johnson:** Well, it's been a pleasure. Appreciate it. Thanks for the heads up.

**Tucker von Holten:** I'm here. But if you have any questions, you know, team's great.

**Ryan Johnson:** For sure. Makes sense. Sounds good. Cool. Anything else from you, Chris?

**Chris Naismith:** Nope. Nothing here.

**Ryan Johnson:** Appreciate it. Thanks guys.

**austin:** Awesome. Great. Thank you so much everyone.

**Ryan Johnson:** Good one.
