---
title: "PQL playbook Follow-up w/ Ben & Jeff"
date: 2026-04-30T15:02:07Z
duration: 47 min
participants: ["Jeff Whitlock", "Ben DeMordaunt", "Jeff Hardison"]
attended: true
processed: false
source: grain
grain_id: 3b93ff1d-3d42-42d2-bb4d-2bd0199f564c
grain_url: https://grain.com/recordings/3b93ff1d-3d42-42d2-bb4d-2bd0199f564c
---

**Jeff Whitlock:** Hey, Ben, are you there. Hello.

**Ben DeMordaunt:** This is the error that we've been saying. I have recorded the HR.

**Jeff Whitlock:** Ben?

**Ben DeMordaunt:** Yeah. You hear me?

**Jeff Whitlock:** Yeah, I can hear you. I'm hearing like another voice.

**Ben DeMordaunt:** Oh, sorry. I'm watching a video. Someone shared with me.

**Jeff Whitlock:** Okay, no worries.

**Ben DeMordaunt:** I don't know. This is. The... We have these people trying to build an integration right now and they have to be the dumbest people I've ever interacted with.

**Jeff Whitlock:** That's so, yeah, we should just not spend time.

**Ben DeMordaunt:** The funny thing is, like, we told him like a year and a half ago. Oh yeah, like, you know, go ahead and build integration. Like, now they're like, okay, we're ready to build it now. And it's like. We did say back then, yeah, like you could build it. And we'd support you. But I don't know. I just kind of wanted to like turn around and be like, hey, so no,

**Jeff Whitlock:** this was a year ago, yeah.

**Ben DeMordaunt:** Yeah. But they had already like built the production and now they just can't seem how to. Test it. Like. Yes. So. Watching the video, then I'm trying to explain. What's happening. What's up.

**Jeff Whitlock:** You wanted to meet with me. Okay, what's up generally? Uh, I'm good. I actually, I published the reason why I need a few more misses. I had an auto schedule post about our MCP. And I needed to add a link to the comments. Actually, I'm going to send this to Slack. Um, so we should just go through this real fast. I need to. Me and I need to run here a little quickly for a meeting, but. All open up this document.

**Ben DeMordaunt:** Yeah. Um.

**Jeff Whitlock:** Just give me one second. I'm going to send this to. Marketing. Worship in this. Then I need to post this on. I need to post this on our main company linked into. That's actually good idea. Do you have access to the company. Out. Yeah. Um, he doesn't right.

**Ben DeMordaunt:** Uh, I can check. There's a list of users there. Which is reminds me I need to remove. Yeah, he does. He has, he has access.

**Jeff Whitlock:** Okay. Great. Okay. All right. Let's dive into your docker real fast. Pulling it up. Okay. I got to keep it high level. Yeah.

**Ben DeMordaunt:** I think, yeah, just a quick read would be good. The way it's structured is essentially like define the cohorts. And then discuss like how we're going to structure the vitally.

**Jeff Whitlock:** Yep.

**Ben DeMordaunt:** Dashboards. Okay.

**Jeff Whitlock:** Not sure this is. Sorry. I'm not. Sure. I'm just going to comment so we can talk to them.

**Ben DeMordaunt:** Interesting. Well.

**Jeff Whitlock:** I just think it's the most, I think it's, I think it just takes longer. It's the most likely for them to lose momentum and fail, not necessarily the most likely to convert at that moment. Until we fix stuff in the product. Yeah.

**Ben DeMordaunt:** I mean, based on analytics, it is the most likely, but that's just because. That's fair.

**Jeff Whitlock:** That's fair, but they probably, yeah, that's fair. I think that's fair. I think, I think what I'm thinking about is the. Expansion motion is likely to fail. We might get a two seat conversion. Right. Like this like organic expansion with our workspaces most likely to stop and get slowed down. Okay.

**Jeff Whitlock:** Like if you look at our, I looked at this very reason, like if you look at our average error art conversion, it's tiny. It's like one and a half C average or something like that.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** And I think that's because of how we've structured our trial screwings. Makes sense.

**Jeff Whitlock:** I think this needs a TLDR. Really like it just goes immediately into the weeds without telling me what like it just needs like an upfront. These are the five.

**Ben DeMordaunt:** Yeah. Okay.

**Jeff Whitlock:** Like one cent, like five bullet point one, one sends each. So I can just kind of get a high level picture.

**Ben DeMordaunt:** Yeah. That makes sense.

**Jeff Whitlock:** These are high priority counts. A new user landing at high ACV paint count. Okay.

**Ben DeMordaunt:** What do you mean I think we need to filter this in some way. Meaning like based on like domain users. Yeah.

**Jeff Whitlock:** Or something. It's too much to do well. I think we want to do less better. Like we have, I mean, we have thousands of signups and not even domain users. Maybe companies that are bigger than a hundred people or, or bigger than many people, like we just need to make it more tight. Yeah.

**Ben DeMordaunt:** Yeah. It's that balancing act between like not making it so tight that you're not getting signal. Yeah.

**Jeff Whitlock:** Maybe it's like on it. Maybe it's like, maybe it's companies over 10. I don't know, but. Yeah, just something not, not anything. And I think just domains might not be quite enough of a filter because we get a lot of these like single solo consult.

**Ben DeMordaunt:** I called that out here. Tier by company size to prioritize larger companies first. So like I had thought about that.

**Jeff Whitlock:** Yeah.

**Jeff Whitlock:** I just define it tighter. And then we can always expand it. Also might remove this ownership bit for now. Oh, really? Yeah. Cause I think in the way that the way I see the doc, how it should be structured is like define the cohort's conceptually. Define how you're going to track. The progress. Like the progress, like those different courts and how they're performing. And then the playbook on like actually, how do you, uh, intervene in a successful way. And I think that ownership is in that third bucket. Right now we're just kind of conceptually defining it.

**Ben DeMordaunt:** Okay.

**Jeff Whitlock:** Let's see here. Well, I don't want existing.

**Ben DeMordaunt:** I guess I probably.

**Jeff Whitlock:** Can filter by cohorts and amplitude.

**Ben DeMordaunt:** And vitally and vitally. Yeah. Yeah. We have tons of them already.

**Jeff Whitlock:** So what is a tile mean? I'm not, I don't really follow this part. A tile showing what.

**Ben DeMordaunt:** Uh, yeah, I guess I have you seen a vitally. Dashboard before. Like how we use them.

**Jeff Whitlock:** I might not have. I have like a lower value seat.

**Ben DeMordaunt:** Okay. So like. Yeah. So like a lot of our. Notifications come from these dashboards. And so like you can create, um, you can create. Different views. And this is kind of like, I want to create a view for each of the cohorts.

**Jeff Whitlock:** Uh, so this is like dashboard will be a co each one. This will be one cohort view. Yeah.

**Ben DeMordaunt:** Exactly. And we have like turned accounts, canceling accounts, renewang accounts.

**Jeff Whitlock:** Upgrading. Even if it's not the dashboard, I would just include that a screenshot of that into the doc so you can visualize kind of what you're talking about. Yeah.

**Ben DeMordaunt:** That's, that's what I was, I have like these at risk accounts. This is like the one I was, uh. Referencing at the top of the file. Uh, or the top of that section. Um, like we built this recently and it's just kind of like. A, you know, here's, you know, current ones that turn concerning the last seven days. And like, this is kind of like the process I want to run. It's like, Hey, these are the new ones. Like let's look at all these. Like the blow up, you know, so.

**Jeff Whitlock:** Yeah.

**Ben DeMordaunt:** So we have tons of these. Um, and then for each of these, like if you go to the account. It'll have like, um. A, like a, a. You can, it has like a task. Right.

**Ben DeMordaunt:** Like, we marked this as a dressed. Once you completed that and then it removes it from that section.

**Jeff Whitlock:** Okay.

**Ben DeMordaunt:** So. Yeah, I can. I didn't want to like include too many screenshots, but I can probably include a couple to make it feel more.

**Jeff Whitlock:** Okay. Um.

**Ben DeMordaunt:** Potential AR is like. For accounts that haven't been converted in trial. We can do a formula to say like, this is the number of seats. This is potential. ARR. Just so that we like can prioritize the higher seat counts.

**Jeff Whitlock:** Yeah.

**Ben DeMordaunt:** I probably should have said that ACV. But yeah. PC makes more sense.

**Jeff Whitlock:** Yeah. I think this is pretty good. Um, what I would do. Is I would take this dashboard. Just what you've written, you might've already done this. But I would take what you've written here for the dashboards. I'd put it into AI. To like, like. 5. 5047. And, uh. Then take mics forensic report. And say, you know, what like I'm trying to create a dashboard to give like an at view, like an at Glance view of some of this forensic report. What am I missing. Like, would like give me feedback. Cause I'd be, I'd just be curious. I think it does it, but I would just be curious for another. Check. Yeah.

**Ben DeMordaunt:** Okay. So like. Yeah. Okay.

**Jeff Whitlock:** I think the one thing is like,

**Ben DeMordaunt:** but directly it's the direction, right? Like so.

**Jeff Whitlock:** Yeah. I think so. Right. I think the one thing that's maybe not here is like, is it the same dashboard for every cohort? Like I'm not, does that make sense? I'm not sure. I think you might want to customize it a little bit. I might also, um, like I think you probably want the same few things for everybody, but you might want like a special section for like, like, um, yeah. So that's one thing that I push maybe a little bit on. The other thing I push on a little bit is I'm not sure like you probably want users that have fallen off. Like users that were active, but of stop being active. Um. But I'm not sure. But I think this direction right. I think instruction right. Yeah.

**Ben DeMordaunt:** That makes sense. Um. Yeah, I get. On the dashboard side. I kind of called it out. That like, I want each. E to the filters I'm talking about in the cohorts. Like will be included in the dashboard. Yeah.

**Ben DeMordaunt:** But I probably could get more specific about like how. But I also don't want to spend like too much time like. Pre - drafting the dashboard rather like, I think making them will make it. You know, that's, yeah, but I get your point. Yeah.

**Jeff Whitlock:** Okay.

**Ben DeMordaunt:** Um. Cool. Well, good. I'm glad I was in the right direction. Cause like, I guess I was just a little. I feel like you and my cat something in your head and it just wasn't quite clear to me. Like I wasn't sure exactly. How.

**Jeff Whitlock:** I think the other thing that I push. Yeah. No, it's the right direction. The other thing that I push on is like, do you like, how does the dashboard tell you what to do? That's not clear. Right. You don't want to drown in numbers. You want to be able to say like. Um, and that's the next part about pushing to the playbook, right? It's like. Um, you want to be able to like for each, and this is what I was saying, like the difference between the cohorts and the dashboard is like, okay, let's say, for example. The cohort is the people who. Were active during trial and trial ended, right?

**Jeff Whitlock:** What's going to be helpful to those people. It's going to be. Extending their trial. So that can keep, you know, see if they're, you know, like if they need more time to, to test features. So it's like, it's kind of be like. They just started these two features that are. Going, they're going to lose access to at the end of trial. And so probably the most valuable thing I can do is say, Hey, I just started, I just saw you were, uh, you know, you just started using X feature. You hit a trial. Like happy to extend the trial 15 days if you get on a quick call for me and I can show you how to get more value out of these features or whatever.

**Ben DeMordaunt:** Right. Right.

**Jeff Whitlock:** So like the dashboard isn't just to swim in like, like, okay, there's two views. The outward view is to just like which accounts matter, like which accounts do I need to look at. That's the, the, the, you know, the overview. And then inside the view, it should just be like a quick way to like guide. The CSM on like what action to take.

**Ben DeMordaunt:** Like, yeah, exactly. Yeah. Yeah.

**Jeff Whitlock:** So I might even step back a little bit here. Um, and say, uh, what are the principles for each. Cohort? Just like thinking about it, like thinking about it logically, like what are the principles that would guide, could guide some kind of an interaction. Um, that would be likely to be valuable or helpful. And then, then just make sure that the dashboard sort of like follows those principles or make. Does that make sense? Yeah.

**Ben DeMordaunt:** The dashboard surfaces those.

**Jeff Whitlock:** Surfaces information that would inform how to apply the principles basically is how to say it.

**Ben DeMordaunt:** Yeah. Exactly. Yeah. Okay.

**Jeff Whitlock:** And like, cause I, I, I look at this and I'm a little worried. It's just going to be like a sea of data and not useful. What's more useful for the dashboard give the quick signal that helps a CSM like know how to write the right message. Yeah. Yeah. Do the right thing. Paul send the right message, whatever it is.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** Um, in product message. I don't know. Um, and who, and who to do that with. It's like what to do and who to do it with. That should be the main goal of the dashboard. And then like, if you need more details, that's where you can use like AI to do like this forensic report or whatever like Mike is talking.

**Ben DeMordaunt:** So in like, let's take this cohort active engaged catch before expiry. Like in the motion I say like, it's a daily review of new account personal outrage to the workspace creator and most active user lead with what they're doing well and often help them get more out of it before the trial wraps up. All for trial extension. So like, I guess I'm just one. So. Is there principles on top of this that we need to like.

**Jeff Whitlock:** Kind of like what I see missing here is this idea of what we were talking about in text messages. When it's like a narrative and like, I think this is fine. Like the principle here is, uh, what's the cohort? Can you ground me in the cohorting?

**Ben DeMordaunt:** Active engaged catch before or like acting gay child catch before expiry.

**Jeff Whitlock:** So the principles are this one might be help them see like help them see what features they're not utilizing with a bias towards the MCP and the connectors. Yeah.

**Jeff Whitlock:** And like bulk export to AI. And then, and then. And also the other thing that's missing is like the narrative. Like I think the overall narrative is really important with in line with the new strategy. Like that's just not popping in this document at all. Yeah.

**Jeff Whitlock:** And if you go back to the text messages with me and Mike, it'll just, the idea and like we, we should even, and maybe this is on me and not on you. And maybe you just have to have a placeholder. Like we should have some idea on like, this is like a, you know, some framework or hierarchy of like how well you've adopted. Grain and AI. Right. So like step one is actually I'll take a pass at this, but like, but you, but you can at least reference it, but like step one is, you know, you're reading, you're sending AI notes. Step two is on a meeting by meeting basis. A meeting by media basis you're pulling transcripts and using into AI and using it on a meeting by meeting basis. So that you're to like do next steps. Right. Um, step three is you have connected the MCP and you're moving and you're using analysis to do work across multiple meetings. Step four is you have automated agents doing the work. You know, uh, as scheduled tasks or on trigger - based work so that like, there's independent autonomous agents leveraging your meeting deity to get word done. Right.

**Jeff Whitlock:** We want to, like we should have like an onboarding flow that automatically teaches them that framework helps them understand like this is how you become like, you know, an AI masters that with meeting data or whatever, I don't know. We need to have better like marketing language, but it's like, you know, and then like this email sequence is going to teach you how to do this and you can start off, you know, we start, we're going to start off with level one or what, I don't know, but, um, but then so that this is just kind of in the background. Maybe they read the emails and rate it or not. But then when you're, but then when you're like doing these like personal touch is you're sort of helping them in.

**Ben DeMordaunt:** You should know what level they're at.

**Jeff Whitlock:** Like how communicate that you're not actually like, let's I would love to teach how to get to level three and level four. With our AI experts. Interesting.

**Ben DeMordaunt:** That makes sense. Yeah.

**Jeff Whitlock:** That's probably like and so this like, this is fine, but it's like, and I like the cohorts. I think the cohorting is the best part of this. I think once we're kind of getting the dashboard in the playbook, it's kind of missing that overarching viewpoint. And so I would probably like take a chart sharing with Mike.

**Ben DeMordaunt:** Yeah. That's the viewpoint that I'm like most lost on. I feel like you and Mike have had a lot of conversations without me around that. And so that to me just feels like I kind of vaguely understand what you're saying, but then I've been able to read or it's just like picking up bits and pieces in like different meetings that I've been a part of. Yeah.

**Jeff Whitlock:** I can do a better job. I'll codify it a little bit. Um, but also we can use this. I mean, like what questions do you have? Like let's use this time just to talk through it. Yeah.

**Ben DeMordaunt:** I mean, I think for me, it's just. It's, it's. It's not understanding. I don't understand necessarily why the people coming to grain will expect that to be there or not expect, but just like that that's the experience they're hoping to get.

**Jeff Whitlock:** You know, not expecting that they're expecting AI note taking, we are doing the work to teach them, Oh, wow. There's another, the horizon that's way better than just note taking. Yeah.

**Ben DeMordaunt:** I guess my fear with that is like. Is it just going to be noise to them? Like, okay, cool. You guys have this super opinionated.

**Jeff Whitlock:** You know, I don't know, man. I don't maybe, but I don't think so. I think people are hungry to get ideas on how to use AI and people who present themselves as leaders to help, help you. Are like, this is so valuable. Yeah.

**Ben DeMordaunt:** I, I think the other concern is like, is it. Going to. Help you. Like understand how you use the product? You know, like. If you're so focused on like teaching them how to. Engage with the AI, engage with like the MCP, like are they going to be like, well, like I still. The number one thing I hear from customers is like recording sharing settings, security security security security. Like they are like, that is the number one thing when they start using a note taker is like, Hey, where's this meeting going to go?

**Jeff Whitlock:** That's fine. We should totally have that as part of the supplemental information. Right. Like there's all in lots of things in life. There's like a primary like sexy angle. And then the defensive angle. It's like think of this is like a bad example. Cause I hate these things, but like think of it as like a drug, like a new drug. Like this drug. What are the things GLP one is going to make your like, make your, you make you sexy, you know, stop, you know, finally help you control your diet dramatically put your life at the end. Disclaimer, you know, you may also experience like a loss of sexual appetite or whatever. Like we can lead with, this is a thing, but we can also still have like, if you have questions about security, here you go. Like we should do that. We should do, the difference between like objection handling, which is I think security versus point of view leading narrative. And so I like, I like your, I like your like hard one perspective on sales of like, these are the objections we need to handle. So let's do that as a framework. Like let's lead with a point of view. And let's objection handle every onboarding email.

**Ben DeMordaunt:** Interesting.

**Jeff Whitlock:** And to your point, the thing that the other thing that I think is a very strong signal that's missing from this is people waiting in, in, uh, waiting to be added.

**Ben DeMordaunt:** People waiting. Yeah. The pending users is this one pending users.

**Jeff Whitlock:** Okay. Yeah. Okay.

**Ben DeMordaunt:** I specify, they said it for high priority account, but you know, if it works, I think we should try and get this. To, yeah. Um. But I definitely agree. That's a huge miss opportunity for us. Um. Yeah, I. I see division. I am. Still trying to understand a little bit like. That they're. Just not to me like I'm like, yeah, if I try to put my always like put myself in the shoe of like, if I sign up for a new product, is this what I want. And that's to me where I'm like, man, I don't know if I want to just be like six emails about how, you know, become an AI master. Like I think. I want just.

**Jeff Whitlock:** To be like, well, it's not an AI match master generally. It's, it's how, how do you build, how do you build a culture where your meetings leverage AI? How do you like, set up and build a culture where your meetings don't become just like wasted, you know, breath, but actually AI leverages them into.

**Ben DeMordaunt:** Well, it's kind of like a combination of like become a master of our product, but also like an AI master. I don't think it's AI generally.

**Jeff Whitlock:** I know, no, no. It's not like, how do you do all these things, but people are going to feel like they're learning AI because we're teaching them also to how to use these things that can have other domains, but it's still central to, this is how you leverage AI with your meetings.

**Ben DeMordaunt:** Got it. Got it. Got it. Got it. Okay. That's a little bit more people using grain.

**Jeff Whitlock:** I mean, like that is the whole thing. The whole thing is, I mean, think about it. It's like, you know, gong, it's like watch a bunch of videos, but now it's like, you don't even need to do that. You can just, you can just build a recurring task in cowork that says like flag, the biggest coaching moment. You know what I mean? Some people will still do that. But like, the workflows. And so that's what we're trying to get people to do is like, how do you like, you know, call recording one dot, I was like watching the videos, which is still valuable to have as the reference occasionally. Poly reporting two dot O is like a bunch of bespoke and analytics on top of the video. Right.

**Ben DeMordaunt:** Like, yeah score cards. Yeah.

**Jeff Whitlock:** And then, you know, call recorder. And then within that too, I think as notes, right? Yeah.

**Jeff Whitlock:** It's just like, who knows basic, basic meeting by meeting analysis and no one reads. It doesn't matter. It doesn't have all the contacts. It misses information. Sometimes it gets wrong. But call recording three dot O is a library of raw meaning data, the AI can, can get work done straight from your meetings. And also be like a system of intelligence for your whole company. Interesting.

**Ben DeMordaunt:** Um, on that note, I did get a customer yesterday who said that. Whenever they tried to do full meeting or full like library analysis that it's only like showing it has like a recency bias to it. Because of our, um. Search only returning the last, uh, the top 50 results.

**Jeff Whitlock:** Interesting.

**Ben DeMordaunt:** So when they want.

**Jeff Whitlock:** Yeah. Send me that email. We're always trying to tweak these things and make them better. Yeah. Also you should check out the, if you're interested, check out the draft I sent in NJI.

**Ben DeMordaunt:** Okay.

**Jeff Whitlock:** About not basically creating knowledge graphs, which would be cool.

**Ben DeMordaunt:** Yeah. Okay. Um, well, I will take another pass at this, but I appreciate it. Like, like I said, like I think it's just been a little bit. It's just, it's obviously becoming more clear, but like it's just been a little bit hazy on like this shift in being a. Like a to the meeting system record for AI. Like I think it's just. Helpful to understand how you see that. How you're like communicating that to customers is, um, kind of our new messaging. Standards almost, I guess, or like kind of practice.

**Jeff Whitlock:** Yeah. And I need to do more work to like get that messaging more codified in, into various places, but I think at the same time, I think just like having a lot of conversations like this is going to be the best way to do like once you understand it. Then. So, but I, but that's what this all, uh, tomorrow's all hands will be about is like really trying to explain that this new paradigm.

**Ben DeMordaunt:** Okay. Sounds good. Well, thanks for taking the time. I'll, uh, take a pass with this.

**Jeff Whitlock:** Okay. Thanks, Ben.

**Jeff Whitlock:** And I would just update, I would just update micro fast and just be like, Hey, I took a pass, got a little bit of feedback from Jeff. I'm going to do one more, uh, or maybe if you join you say that, but just say like, I'll send you a doc shortly in the unit. I can jump on a call and go through it. Yeah.

**Ben DeMordaunt:** I booked a call this afternoon.

**Jeff Whitlock:** Yes. Uh, two other things that I, that I just want to kind of keep kind of, um. Update you on. So the first is. One of the things that one of the things I, I had a conversation with, uh, Mike about is just asking him to, to be more like be more of a DRI involve. Person. Rather than see if that's something that he had capacity for rather than just, um. Cause like, I think the, the, the engagement model historically has been like Mike would give me feedback. And then it was just up to me to sort of try and implement it. And sometimes that was hard because my focus was somewhere else. Right. And it's like, if I'm the CEO, I can't like, I want to give mics feedback treatments, but it's like, I'm at the same time, he's not my manager. And I mean, in a governance perspective, he's my manager, but not in like an operational perspective.

**Jeff Whitlock:** And so it's like, it was odd to be like, you know, that's not my priority. I don't have time for that. But then he wanted it done. So I was just like, Hey, I don't, I don't think this is really working very well. But like, if you have a perspective that's aligned with my strategic, like the company strategic direction, like get in and help us, like, I think that's way better than like kind of piling a bunch of stuff on me that I can't really, I don't have capacity to operationalize. So, uh, so this like, this sort of, this like PQL thing is one of the, as one of the objectives for the quarter. He said he wants to be directly helpful with, um, so what I would, and I think it's, I actually think in some ways, it'll be. Hard. But I also, but I also think that if you kind of are able to just roll with some of the, some of the, some of the hardness that I, that it'll be good opportunity for you to do really good work and to learn from Mike. He really, he really does, uh, I think have this founder level, uh, capability of like, of like starting something from scratch and figuring out something from scratch that I think I've seen like hints of you being able to do, but hasn't really been like something that I think has really flourished or like really, you know, you really completely developed yet. And so, um, so that would be my encouragement to you is like really leverage him, like hold him accountable to this commitment that he's made to me of like being, being a, uh, like a direct, like basically like a, like a partner for you on this project. And. Yeah, learn as much as you can. And, you know, obviously push back if you disagree with things. It's not like, but, uh, like, but I do think that. I do think that there's an opportunity here for it to be really beneficial to grain and to you. So, um, any thoughts or questions about that.

**Ben DeMordaunt:** Just kind of curious like what level of involvement.

**Jeff Whitlock:** That's a, you, you should work that out with him like, like I'm going to tell him like, Hey, I talked to I talked to, I gave Ben a heads up about you getting more involved on this. And, um, and I, and I encourage him to kind of talk with you about like a, what he can expect as far as a working cadence.

**Ben DeMordaunt:** Yeah.

**Jeff Whitlock:** Or process.

**Ben DeMordaunt:** Yeah. I think that's sometimes the challenge is like. Which I always appreciate about Mike is his sense of urgency, but sometimes it's, uh. And I have the same, like a similar sense of urgency with the business. I'm not saying it's like, but it sometimes feels like he doesn't quite see all the workings. And so for him, it's like, well, why are you not like a hundred percent focused on this one thing that is my focus at Grain, you know. And I think that's sometimes a challenge is. Uh, and it's just, it's hard to. So that's like, that's why, yeah, and I can have that conversation with them is like, you know, these. You know, I have a lot of balls up in the air, like, you know, onboarding a, you know, large customer and, you know, sales and things like that where it's like. I don't, I can't necessarily step away from those, you know, to like focus. I'm not like an engineer that can just drop a project and come back to later, you know. Um, and sometimes that's how I feel like my axe is like, Oh, well, just step away from all those other things and focus a hundred percent on this. One already in motion, you know, like I have sales deals. I have, you know, customer onboardings. I have like customer renewals and things like that that are already in motion. That like. Have to be continued. Or we will, you know, lose accounts, whatever, et cetera. And so I think that's sometimes the challenge is. I don't feel that that is always when Mike steps in as this. You know, as, as potentially stepping in here is more of like a DRI, like I would love to spend a hundred percent of time on like getting it up. But that, you know, it's not possible.

**Jeff Whitlock:** So that's, that's the exact kind of conversation that I'd like to have with them as just sort of starting to work on this together. So I think, I think the nice bit of alignment is this is the, you know, Q2 strategic offensive focus for, obviously you're going to still have defensive things, but like off, it is the, the priority. Uh, operation in operations. So I think there's alignment there. This isn't something where like I've asked you to do NPS or something or something else. And then Mike's coming in with, so like, the alignment there. Then I think. To your point, like the defensive stuff is he needs, you know, I think that's a good conversation to have about like, um, about, uh, how to prioritize and for him to have reasonable expectations. Um, and so I would just, I think what you just told me you should tell him and like saying like how, uh, like let's come up with like some engagement norms or whatever so that, uh, so that I'm able to do what you need me to do to be successful. But then you all, but you're also, uh, supporting me, um, the things I had on my must do's I have to do it.

**Ben DeMordaunt:** Yeah. Yeah. Okay. Will do.

**Jeff Whitlock:** Okay. Awesome. Sounds good. Uh, all right. Cool, dude. Let me just don't, just ping me if you have any questions on, on the next, on the next, uh, pass.

**Ben DeMordaunt:** Oh, well, but yeah, there's a meeting this afternoon to go over with Mike and you. Okay.

**Jeff Whitlock:** Sounds good. Talk to you later. See ya.
