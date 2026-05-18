---
title: "Product Coordination Meeting"
date: 2026-05-18T16:29:48Z
duration: 30 min
participants: ["Browni", "Shane Howley", "Jeff Whitlock", "Chris Naismith", "Juan Ramón Fernandez", "Ygor Castor", "DEV: Andrew", "browni.wilson", "Thomas Tabi", "Diego Rojas Salvador", "Jonny Andreola", "Ryan Johnson", "Andrew Clarkson", "Jake Bagley", "taylor-old"]
attended: true
processed: true
processed_at: 2026-05-18T17:42:33Z
wiki_articles_touched:
  - people/Ygor Castor.md
source: grain
grain_id: 90e0ac44-fd8c-472d-8c4f-e94d973dea94
grain_url: https://grain.com/share/recording/90e0ac44-fd8c-472d-8c4f-e94d973dea94/OcPSPSAFbxLjS0HL2gfxmjqwOCbpJ37hFmzfycYw
---

**Browni:** Good day, go. On.

**Browni:** You. Go.

**Juan Ramón Fernandez:** Hey, wait till as well.

**Browni:** All right, so today most of our front - end engineers are out.

**Ygor Castor:** Canada something something.

**Jeff Whitlock:** What'd you say Shane.

**Shane Howley:** Was a whole front end to you in Canada?

**Jeff Whitlock:** Yeah, pretty much. Pretty much yes.

**Jeff Whitlock:** They are doing Victoria day. Freaking Queen's birthday man. What do we care about a queen? I don't know.

**Shane Howley:** Don't even have that here the Commonwealth or whatever.

**Jeff Whitlock:** Really there's no Victoria day. I mean why why did it why do they have Victoria today? What is it. Let's learn about it Toria day.

**Jeff Whitlock:** Federal Canadian public holidays in honor of our good friends up on our front - end friends. The federal Canadian public health last Monday to honor Queen Victoria who's known as the mother of Confederation. The holiday has existed in cannacense at least 1845 originally on her natural birthday all on Monday blah blah. Federal stature hall as well why though. Not even your sovereign anymore guys You know move on. Such good news I went to common ground between list and French Canadians. Okay, well it was to unite the English and the French Canadians always nice It's a holiday of unity. All right. How's everyone doing everyone? Have a good weekend.

**Jeff Whitlock:** Anyone have a highlight share.

**Shane Howley:** Got to meet my new niece.

**Jeff Whitlock:** Oh, that's awesome. How old.

**Shane Howley:** Like a month.

**Jeff Whitlock:** Oh wow cute. Lovely.

**Jeff Whitlock:** I went to the rooftop concerts. In pro. It was really fun It's like this old concert series they used to do in provo a decade ago and then it kind of died and then the new mayor brought it back. And It's fun. They closed down like the whole block and then have a big stage in the middle It's called the rooftop because they initially did it on a rooftop and then it kind of outgrew that So now they just put it in the street and it's fun A lot of people there is good community. Good band too. I want to start listening on they were really good the headliner was good anyway. Really fun.

**Jeff Whitlock:** They were called.

**Jeff Whitlock:** I have some complicated name that I couldn't remember. They were called I don't know how but they found me.

**Jeff Whitlock:** Yeah, so yeah, they're pretty good They're like. They're like rock. Yeah They're a rock band. Maybe pseudo glance like glam rock almost I don't know but it was it was cool. It was fun or Uncle rock I don't know exactly what you'd call it. Kind of like do you remember the band the strike? No. All right, let's dive in we got a smaller crew today So I think rather than Ryan I just went through all the projects rather than kind of getting we'll just skip any Projects that are front and heavy. And then I'll just sync individually with folks.

**Jeff Whitlock:** Like everything's gonna go out on the next release. So I'm gonna move this to monitoring because we still need to test it and make sure it's working well. So let's turn on when this goes out can we turn on the flag for our workspace. And then Brownie and I can test it thoroughly.

**Ygor Castor:** Sure can.

**Jeff Whitlock:** Okay great so all bang on it for the next couple days and brownie will you take a special note to set up smart topics and have and we can talk about a testing strategy brownie Let's you and I talk about that briefly after his call.

**Browni:** Okay.

**Jeff Whitlock:** Awesome good stuff really excited about that.

**Jeff Whitlock:** Some good savings there and I think it'll work better too.

**Jeff Whitlock:** Looks like Juan good great job getting in these tickets here Anything that you need help with on these tickets.

**Juan Ramón Fernandez:** No, I think we should be on the clear. Probably we will need to build a little bit of Monitoring to see how the solution works like and we still need to run a few things like. On Friday probably regarding these like a backfield. But we should leave it for the most part it is.

**Jeff Whitlock:** This one we probably want to make sure is probably the most user facing feature we want to make sure is Working once it's out right one.

**Juan Ramón Fernandez:** Yeah, they're basically like mini issues of the same thing But yeah.

**Juan Ramón Fernandez:** Basically you should see the updates like after another deploy Because we will be like.

**Juan Ramón Fernandez:** Yeah. If you went to get the technical details basically we were not like updating the display names. For meetings that were already scheduled But now we will be like running like updates like 10 minutes before a meeting stars to make sure that things are up to date.

**Jeff Whitlock:** Makes sense Good stuff Brownie Let's just make sure that's working. Okay test and then there's also.

**Jeff Whitlock:** Actually let me just go back to this I think we also want to close a look at that customer.

**Jeff Whitlock:** Okay, awesome.

**Jeff Whitlock:** Okay now let's go to the next one. Voice signature actually Yeah, we can go to this one. I took this one off pause one because it seemed like Everything else I think we'd paused it while you're working on the stuff in the ownership model. And I think the hub spot stuff is completed and donorship models completed So I reopened this is that right.

**Juan Ramón Fernandez:** Well next in priority is the phantom importer And after that's true.

**Jeff Whitlock:** Okay, so I did the wrong thing Let's keep this in pause and then let's do the Fathom imported Or which I think we have a project for.

**Jeff Whitlock:** Uh. Okay cool And we'll move this off pause then to do And you've got everything you need for that white one.

**Juan Ramón Fernandez:** Yep Yeah, yeah man already working on it.

**Jeff Whitlock:** Okay, awesome Good stuff.

**Jeff Whitlock:** How long do you expect us to take.

**Juan Ramón Fernandez:** Uh I imagine it will probably be done by Tomorrow or Wednesday at the most. Uh Then after the deploy we have to run the actual import for the customer.

**Jeff Whitlock:** I'll put Wednesday Thank sir.

**Jeff Whitlock:** Voice signatures. Shane You want to give an update here

**Shane Howley:** Uh I've got the new model Kind of figured out So start migrating the existing code over to use the new model.

**Shane Howley:** And the thing that's like net new is storing Dye - i'd transcript separately So that's going to be the next thing to layer on. Then once we have that we can use those two data sources to start doing the voice leaks.

**Jeff Whitlock:** Cool.

**Jeff Whitlock:** Awesome. Darry Curious to see how this develops. Um, any input needed or help needed on this one.

**Shane Howley:** Um Not right now. Um Just had a few threads going Ryan and Slack I don't think I'm weighing specifically on anything.

**Jeff Whitlock:** King me if there's on and else because I don't remember them

**Shane Howley:** I'll go back and take a look and see this Okay Thank you.

**Jeff Whitlock:** Rownie Have you moving on to this project now Have you. Tested this.

**Browni:** Yes I did it I didn't I tested this Um yesterday and I found I think I asked Ryan question about I added a question about Um.

**Browni:** The exclusion Uh description members from those who get access on hotspot And I think Grazit They can view But I think it's Badikano edit So yeah, I think Otterth yesterday. Okay.

**Jeff Whitlock:** And we aligned here one that we're not doing anything Right.

**Jeff Whitlock:** Not doing anything. We're not running any jobs. That's When we exclude a meeting.

**Juan Ramón Fernandez:** Sorry Yeah. When when I'm eating is excluded We don't run automation context or anything at all So it's easier to understand that way Great Castell manually sync it But yeah Okay Awesome.

**Jeff Whitlock:** Great stuff Alright I'm gonna move this one to monitoring then Since this is already QA verified And I assume it'll go out here soon. And uh, yeah I think this is something I will work with Ops on to. Let people know that we make sure the documentation and how it works is updated. And maybe and probably will message Um... This is going to be... And just message users to know that that's up capability if they want to configure it that way. Probably people who currently have it contact Uh connected. So great stuff And then the kind of the fire drill that started this in the first place Feel like was resolved They really appreciated how quickly we moved on it And... Don't seem to be threatening any behavior So that's good But I also think this was a good Um it was good hygiene anyway Because I think we should have done it. Um, in the first place So really appreciate the rally there. Alright lastly Uh Igor I know we just talked about this But for the sake of the rest of the group Do you want to just give a quick update on this project and kind of what the next steps are?

**Ygor Castor:** Yep We decided to Go like a to entity memory for companies right now So like we'll start like a with companies A single market down memory. And like a then like we'll see how we get vote from there So let's try not to make the same knowledge breath That we did before that was the expensive and big So those some baby steps to the usage And then we can build the bonnet.

**Jeff Whitlock:** Awesome Um, and we're getting better results on this Uh The search meetings as far as I can see I think this bulk company look up I think will be helpful and make the MCP experience much better And, uh, yeah So then the next thing is what you just mentioned Good stuff. Anything else worth syncing on anyone blocked or needing put on anything.

**Jeff Whitlock:** Is there anything to talk about with that's how I recall Um.

**Jeff Whitlock:** Now I might need to get. We can talk when Chris gets back as far as what he's working on next Like I think the desktop related projects that I think would be good to get a friend - end person Or you know Okay.

**Jeff Whitlock:** Yeah quick update just for folks here Uh is this opt - in capture notification project is basically done That's gonna go out shortly We're just before GA finishing up analytics on it. And then the project is also very close to going out. That'll be nice. Okay good stuff everyone Uh. Any anything else.

**Jeff Whitlock:** Taby Any anything from the customer side we're sharing. You're seeing.

**Jeff Whitlock:** Okay cool Alright appreciate everyone Let's have a great week. Bye.
