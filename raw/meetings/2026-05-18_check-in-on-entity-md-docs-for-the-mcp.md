---
title: "Check-in on Entity MD docs for the MCP"
date: 2026-05-18T15:30:34Z
duration: 0 min
participants: []
attended: true
processed: false
source: grain
grain_id: 1e7e007d-04ee-450e-889a-1cce73540324
grain_url: https://grain.com/recordings/1e7e007d-04ee-450e-889a-1cce73540324
---

**Ygor Castor:** Hello.

**Jeff Whitlock:** How are you doing.

**Jeff Whitlock:** Good.

**Ygor Castor:** I was a weekend.

**Jeff Whitlock:** It was really nice. Yeah, it was really nice and it was My mom got back from a long trip. So we hung out there had some way out to dinner It was good she was gone for like two months So it's last year again. Cool nice. One second. I noticed a little product thing I want to write it sure feed on.

**Jeff Whitlock:** What's up Shane.

**Shane Howley:** How's it going.

**Jeff Whitlock:** Good doing great you have a good weekend.

**Shane Howley:** Yeah, it was good and dublin was over in Ireland visiting family friends.

**Jeff Whitlock:** Nice.

**Shane Howley:** Sounds lovely.

**Jeff Whitlock:** We have how I imagine Ireland Irish weather would be right now. Last draw. Very cold and rainy.

**Shane Howley:** Yeah, it was like the whole weekend was just alternating between like sun and then rain Like every half an hour. Oh wow Just you know like driving around so it's just like constantly and like okay put on the wipers and the 10 minutes later

**Shane Howley:** It's funny.

**Jeff Whitlock:** Well wanted just to quickly sink Igor I think you have finished you can update please update me if I'm wrong this and you have this but you'd finished Some of the miscellaneous path we've been kind of talking about Yeah Everything's like it's merged.

**Ygor Castor:** I asked Brownie to test like the smart topic stuff. So I gave me like a guide on what to test and he like I will check. So like I want like it's Tested then we can wrap up like that vector DB.

**Jeff Whitlock:** And then you have you just shipped that bulk company or at least you have any review the bulk company look up.

**Ygor Castor:** Yeah, like that's like a merged on staging I think. No or not merged yet. Let me check. No, it's not perfect yet. Yes I think it's waiting for review.

**Jeff Whitlock:** Take a look at it spawned a conversation this morning. So We had talked we've been we've been having some conversations about how to try and connect context across entities So that the MCP doesn't have to like refigure out that context every time. When it's when people make inquiries or trying to do tasks that could be used that context be useful. And Yeah, I'd like I like to kind of align on what's a good I don't want this one of those things where I feel like you could weigh over in venced in it early But I so I'd like to align it like what's a good kind of V1 iteration we can start to dip our toe into this. And learn the utility of as well as like the compute costs and stuff.

**Ygor Castor:** You kind of look at it depends on which level do we want to have kind of like a memory right? Do we want like a global memory that learns with everything or do we want like to have something like on the project level which is like a playlist Then like it would be like updated every time like we have something new on the playlist.

**Jeff Whitlock:** I mean, I think that I think that we're still kind of in the early stages of playlist rehabilitation So I'm not I'd rather not couple. The learning here with the adoption of playlists I imagine as we have more product marketing around play what are going to become projects.

**Jeff Whitlock:** And we kind of teach people that these are ways to kind of hold curated context will get more adoption of them But I'm not sure like again, I don't I'm not sure I want to cop couple that So my mind is more like probably starting with one entity or two entities or like like people I think people and companies are the obvious and simple ones to try But that's just my bias. I'm not sure so I guess I'd say global Um, but the question is kind of like which entities do we want to try to do and then what are the how do we want to trigger the creation of those entities.

**Ygor Castor:** Because look up right now Like on the segments we already have like the extraction of entities. But like we don't use it quite a lot and like it's not like.

**Ygor Castor:** I'll kind of see like a memory wise. So like I don't inject it. It's like a by request. So let me think yeah like what we can do like as initial approach is like to have like a simple stored markdown in the database that like it keeps track of like Oh, like a nurse reading is these were like a the users you were talking about or this is where like a company. And like a like every like. Recording finishes we update like it is. Mardown. It's one option.

**Jeff Whitlock:** So keep saying it would be a single markdown or would it be like a marked on per entity? What's your goals are there?

**Ygor Castor:** So I would go like a single markdown like a we keep like a single simple markdown there that gets updated. After every meeting.

**Jeff Whitlock:** Um, sounds good. I mean do you think that there would be value in a markdown per I mean obviously does it just ideas here that we're throwing around because Nobody's really tested it out yet But like there's this. Ceiling like you know go and look at mic's demo and all that sort of stuff around like oh like make this wiki page per entity. I started playing with that this weekend. I built last weekend. Yeah, that's like the we haven't proven out the value there yet necessarily but like it's there's a there's. Some work there's some I can't do the right phrase but people have done work similar to that out there in the world and so you know I think the thing that people are curious about right now is could we build something like that? And if we did with that be valuable. I also feel like that approaches more if we exposable if that's where there's

**Ygor Castor:** like a based on like on the m3 car party Something something which is kind of like a Unproved. We have a lot of like a noise in the area still and like absolutely no numbers that that's efficient or not.

**Ygor Castor:** For everyone So like it's because like that's like a kind of like a unified graph. It's pretty similar to us like we did with mileage graph stuff But more like runtime based like instead of like a break compiling everything like a generating the whole stuff We just. Like a follow like a kind of like a the graph edges and everything. But I think is an overkill.

**Jeff Whitlock:** So I guess the the question is what are we trying to accomplish right and so then that then based off of that we could decide if it's overkill or not That's probably what the most important thing that we can answer right now.

**Jeff Whitlock:** What we're trying to accomplish is a per user per person or per contact or whatever you want to call them and per company brief. I guess that there's an assumption or hope that that like a perp company per contact brief. Is going to make the MCP more Useful right. Say that again.

**Shane Howley:** What do you want to see in there.

**Jeff Whitlock:** Exactly well I think the the idea And like I said, I don't this hasn't been proven to me yet in my mind But the idea would be here's recording with Bob. And At the top simulator like rich transfer to whatever we would append the brief about Bob and the brief about his company and like that's the payload that we give to the LLM as opposed to a one

**Shane Howley:** According What are the contents of the brief.

**Jeff Whitlock:** Well the all of the information from all previous recordings.

**Shane Howley:** All the information what does it mean

**Jeff Whitlock:** Like it would be like summary of like brain is it would be like grain is they you know post series a startup You know that does X, Y, and Z You are currently working with them on this project and these are some of the main goals of the project and these are you know This is what you've accomplished so far here are some things you've yet to accomplish here the outdoing out action items from across So just like it's just like a computer.

**Shane Howley:** Combi level sounds pretty similar to what we already built for the spice stuff But like for the person briefs like what would that would you want like more than like two sentences. I don't know if the if Say for it was like a project say we're doing the brief on grain like what do you what do you say about Ryan.

**Jeff Whitlock:** S the CTO the company. He you know you've had in your previous meetings You've talked about these three topics and and you said you were going to do these two things for him. And You guys both like cheese. I'm just gonna eat the bolts I don't know that kind of you're right. I think a lot of the personal context is probably not valuable. I think kind of like role things you've talked about in the past outstanding commitments.

**Jeff Whitlock:** But again I mean maybe this conversation highlights that we just should start with companies and save companies are valuable. Because I think it's way more likely that a company is going to come across in context than a person

**Shane Howley:** Company would include information about the contacts also.

**Ygor Castor:** Yeah, exactly.

**Shane Howley:** It'd be like this you know Grain is a company blah blah blah CTO is Ryan CEOs Jeff like that will be. Contain in that like the heat these are the stakeholders this kind of thing, right?

**Ygor Castor:** Okay Yeah, like I think like we can start with companies and let's say yeah.

**Jeff Whitlock:** So I guess what if you know one off gmail dot com address or whatever. Like. What's our company there you just call the company after the full email address. Like. Bob at gmail. com. And he's a company or something like I don't know I mean because like you might still want to create a single brief for all your comedians you have with.

**Shane Howley:** Meeting with like 10 people from one company Like you don't want probably our need. A brief about like this engineers on the car.

**Ygor Castor:** This is their Yeah, you also have that right like a pretty simple you have like a several different like. Meetings in the same like a company in several different like a discussions Like let's say like you have a call like a which is like a for HR like interview discussions and then like I have a call that is completely different for sales Like it will be like the same entity wiki. Or like we will split like a by. Meeting type also I think that's like a kind of like an over engineering because like what I'm thinking is like a wary of spauntex bleeding right so like you have like a meeting that Has something and then like a wind jack some stuff from this company that makes like a no sense to the whole or for the for the thing that you are like a searching for now.

**Jeff Whitlock:** Yeah, I mean that's fair I think that's a reasonable point like I think. I Think yeah, I think the other thing just to kind of like ground us is like the way that this is valuable is that if there is a relevant brief if the brief relevant to a company or an entity that is. Instantiated in a prompt. And so. Yeah, to me the things that are most likely to be instantiated our companies and like topics Yeah, we don't we don't we don't want to just be like for more graphic information because we can get that. No, it needs to be like specific being as you've talked about commitments made right to be clear like what should be in there should be based off of the median contents So like it almost is like company times project or like company times like topic with that company or something like that right like where it's just more so than just like top level. Company green brain is a series a startup like that's not as useful because you can get that from. Anywhere right people they'll laps or whatever. And maybe we should do that right maybe that should be one of the things that we all do add is helpful content This is like a two sentence blurb at the top But then. What we're actually maintaining is the you know the project information the project threads.

**Ygor Castor:** Underneath the company.

**Ygor Castor:** Yeah, because like we can we can start like a simple and have it like in a single market opera entity and see how it will behave and then like Maybe in the future if you like a this is like a bleeding a lot of context everything We can like add relationships. But let's not do this thing knowledge graph stuff which is really

**Jeff Whitlock:** I really don't want to do that way too complicated and way too slow and way too expensive So that's why like the hope is like a much simpler knowledge bait knowledge grab You know we're not doing ourselves to face something. Yeah. We're not trying to build a graph database here. We're just trying to brief say that again.

**Shane Howley:** The idea be similar in that we would you know we generate.

**Shane Howley:** Booster up the thing first and then like let's say after each call. We kind of fold new information into that.

**Ygor Castor:** Yeah, I think that's the idea, right? We use like an all into

**Shane Howley:** So we want to use the full transcript for that or just take the already commenced outputs

**Ygor Castor:** like muscle was going to be my next question because the full transcript it would be expensive

**Jeff Whitlock:** I would just do the condense do the notes or the notes on items.

**Jeff Whitlock:** Yeah. You could. Allow for a multi - turn agent to get an exposed a transcript search tool to it if we want, I suppose But I guess depends on how limited you want to be if we think it'd be too expensive to allow it to Do any sort of. Probing of the actual transcript.

**Ygor Castor:** Oh this may be useful because like right now on the segments like I already add like entities there What we can do is like at the search on the on the on the segments for Like a segment that already has that like a data entity So then it gets like an easier to filter. So like this slash data.

**Ygor Castor:** Because already have it there, but yeah, I would start like a simple as possible Like let's start like a with a single markdown based on a on action items and nodes. And that's it for now.

**Jeff Whitlock:** Yeah. Okay.

**Jeff Whitlock:** Just at the kind of like mechanics level I think it would be useful to store dips. Of these things and you know I think that's useful information for both internal and potential external I don't know but ideally we'd be storing these as like kind of a diffs on top of a markdown file.

**Jeff Whitlock:** And.

**Jeff Whitlock:** Yeah, I don't think about if I have anything else. But.

**Ygor Castor:** Yeah, the deeps look are also good like a kind of like a paper 3 of the changes But like do we want like a limit on dips because like a disc can grow absurdly. Right?

**Shane Howley:** Man I can't see us needing like a hundred versions of each entity, right?

**Jeff Whitlock:** I wouldn't yeah, I mean different amount of version I said, but yeah Maybe sure

**Shane Howley:** it is kind of a version if you like this is the new truth. Yeah.

**Jeff Whitlock:** What's the point of the diffs. To the history of how it changes over time for us to know proditing and also I mean, I don't know.

**Shane Howley:** What's that. What do you want to expose it.

**Jeff Whitlock:** Potentially right I don't know I'm I'm still forming a an opinion there right now I mean I'm just. Obviously like like I said a lot of this is like the experimentation that's going on out there and so hard to say like what this actually valuable This actually works or not but you know one of the memes is that like oh yeah store your agent memory as like markdown files tracked and git and they get history itself is valuable. Right. Is that true or not? I don't know maybe it's true But people are saying claiming it is. So, you know

**Jeff Whitlock:** this could be a potential useful tool yes or no I don't know.

**Jeff Whitlock:** Let me just post a thread of this of this guy I don't know obviously this is kind of like a Yeah, a bit of a codex Advertisement because this dude works for codex But like, you know. Just what he's doing right now It's like yeah, you know like maybe that's that would be useful. I don't know.

**Jeff Whitlock:** I Don't have conviction about around like but I think that's the point I think the point is we don't really know a lot of this stuff So we just need to do simple things and well whatever simple thing. I mean I like the disc idea. I just wouldn't want to like over engineer a complex. I mean we're going by Jake Adam like vision It's it's like all this is like a SQLite database that is accessible to end users. Basically right and they each end user has their own SQLite database that they can add this information and in their client can. Turn through it as need to be or whatever, right. I mean it's interesting idea because it's like I like that it's the idea But it's that would be I'll add some non - true real complexity on top of this project in order to build that sort of thing So yeah, but I mean I wouldn't start with that.

**Ygor Castor:** No, no, I think that's too much for start like I think like yeah Let's start like a bit of a simple memory. Without relationships and then like we see the users see if people use it and then like we can go to a more Smart

**Jeff Whitlock:** and also see our own we're also we will also see our own usage of it usage and see how if it gives us better results and how often that you know, I just think I just would like to just get some qualitative Feedback and understanding and yeah, and I think the soonest we can get a first version of this and that's I would just start with something simple and then we can iterate. Makes sense to me Yeah said the ideas out there, but yeah

**Ygor Castor:** look at the memory like is a kind of like unsolved problem right now There are like a several different approaches from several different people from graphs like at a simple embeds to a lot of stuff.

**Jeff Whitlock:** So I think it's worth saying that like.

**Jeff Whitlock:** And you know Jeff Fried regretta me if you think I'm not saying the right thing, but like I think that this project is our attempt. To Like. Figure out what is grain beyond just like a raw storage of transcripts exactly we need to move It's just we don't know the exact way and so we want to try where do we fit in like system of record But beyond just being raw transcript sword that like it would be simpler to just store like markdown files or Wherever and like why does a company care about having grain in the middle layer. Well, it's because we can do enrichment. And what it enrichment mean probably doesn't mean doesn't mean like pulling in data from HubSpot necessarily because You know you just have your MTP client pull from grain and pull from HubSpot, right? Like why would we do that arrangement at our level unless we have some sort of unique data set that HubSpot doesn't have and the unique data that we have is the history. And so our hope belief. Wish is that the value that we are providing is by that LLMs are still not good enough at fully utilizing a large corpus of history and searching across it. And so therefore our efforts can be to enrich the data that people have and they're late at meetings with a condensed form of the history. The true or not, we'll see, but that's kind of like the underlying like strategic value of this project. And also just, it's like the sort of like, is it true or not? And if it is true, what is the way that that's going to happen? And so like starting to march down that path and learn. And experiment is important. I mean, the, I'm sure there are already power users out there. And Mike's even showing, right? Like the power user already who are just using grain as like a pull out the data and then build my own version of the knowledge graph. And the people that already said that up. Our hope is that we can act as a value at the layer for the people that are not necessarily power users or whatever. Right. And, you know, add enough value there that companies are going to. But even, even then like. Even power users, I mean, we'll see how this all goes, but like, it's all, everyone's doing it locally. Using NGROC. And it's just like, it's just like, it's super brittle because your laptop is down doesn't work. It's like people like I have 500 gigabytes on my computer and I'm about to hit like the amount of like local space I'm using, even though all these files are small. It's like, it just adds up when you're doing everything locally now. Yes, both. So yeah. So I mean, who knows what the future looks like. But. While we're in this window, uh, we hope to be able to. And it's relevant. You know, I want to be able to talk about us doing stuff here. So. All right, cool. Uh, ER, do you think you feel like you got reasonable alignment from this conversation to be able to move forward?

**Ygor Castor:** Yeah. Yeah. Yeah. Like, uh, I will create some tasks, but yeah, let's start like a simple. It's not an over engineer yet because this can go all like quite a lot. So.

**Jeff Whitlock:** Doing company based, company based markdown files, uh, that are based on the meetings we have with maybe a little bit of firmographic data from people data labs. And we are going, I don't, you can make a recommendation on diffs. I think diffs could be cool. Um, and then, uh, yeah, I think any other, any other like scope questions where aligning on. Here before we wrap.

**Ygor Castor:** No, I think like a, it's enough.

**Shane Howley:** We didn't respond how we would bootstrap. The entities.

**Jeff Whitlock:** Yeah. I mean. You could start with moving forward with kind of the assumption that like a new meeting means that they're still active. Value. And so therefore, and then once you've have a new media and that could be a trigger to be like, okay, go back and look, uh, for the past and days or whatever for anything with this

**Shane Howley:** one, something similar to how we were bootstrapping the spiced. Although I think that was very extreme. I think in that case, we did all the meetings.

**Jeff Whitlock:** Which probably too much.

**Shane Howley:** We could be like first meeting plus last end.

**Jeff Whitlock:** Yeah.

**Ygor Castor:** Yeah. Uh, maybe we can get like the last like a month of meetings usually, you know.

**Jeff Whitlock:** Yeah, well, I mean, month, maybe I didn't even just do end meetings. Yeah. Dates may not be the right last three meetings or four minutes. I don't want to do too much.

**Shane Howley:** First meeting is usually has a lot of context in it as well. It's true.

**Jeff Whitlock:** True. That's actually a good point. You could go find the first meeting you had with the entity and then do that. Yeah. That's good. I mean, and then you only do that if someone has had a meeting with that person. You don't, you don't retract your own thing on the backfill, right? No meeting is a trigger. Sounds good. Do it. Okay.

**Ygor Castor:** Cool. Thanks guys.

**Jeff Whitlock:** Good stuff. Thank you.
