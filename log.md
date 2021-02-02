# 100 Days Of Code - Log

### Day 1: December 24, 2020

**Today's Progress**: Cloned the 100 Days of Code repo over to my Tyler personal profile. Set up basic projects for the IncHelpParser and BrazosNewWorldDataComparison repos. Getting the IncHelp project going on VS2019, which included the Python extension. Got the basic Hello World example for tkinter going. (https://wiki.python.org/moin/TkInter)

**Thoughts:** It's easy to want to spend time setting up project boards and such when I just really need to stop and actually code something. Also, tkinter seems convenient, but maybe not the easiest to start with as far as a GUI. I might try something else later.

**Link to work:** [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)

### Day 2: December 25

**Today's Progress**: Started connecting the GUI to the parser program. Figuring out not only how to import a module, but actually get it to run. Need to keep appending self. to functions and adding self as the first parameter of said functions.

**Thoughts**: Python classes/functions keep passing self in. I guess it doesn't want to be left out of anything. Also, these were helpful: [Digital Ocean link on modules](https://www.digitalocean.com/community/tutorials/how-to-write-modules-in-python-3) and [Type Error](https://stackoverflow.com/questions/18884782/typeerror-worker-takes-0-positional-arguments-but-1-was-given)

**Link to work:** [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)

### Day 3: December 26

**Today's Progress**: Finished debugging/testing the GUI. It now fires the parser and works as before! Also got same-directory Output to work.

**Thoughts** Actually spent the full hour, instead of less than 30 mins like I was expecting. Next, I'll see about adding a Browse button/functionality to allow for custom input paths/files.

**Link to work:** [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)

### Day 4: December 27

**Today's Progress**: Tinkered more with tkinter and getting an Entry box on the screen. Start back up on line 19, moving the other objects onto the Canvas.

**Thoughts** Tkinter is hard, but not terribly so.

**Link to work:** [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)

### Day 5: December 28

**Today's Progress**: Got the Parse button onto the Canvas, added the Browse button. Got it working as a fileDialog process. Started work on getting this to flow into the Parser. Pick back up on line 165 next.

**Thoughts** Still don't understand tkinter wizardry, but at least this is more closely resembling a decent app. Comparing it in my mind to Royce's shape file parser, which could also be a good next project update idea to keep in mind.

**Link to work:** [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)

### Day 6: December 29

**Today's Progress**: Got the file path field to properly pass the path on to the parser. With some more tweaks, we now have a fully working, albeit primitive version of the parser. There's still a lot of room for polish and updates, but at least someone could download this project and run it (provided they're on the latest version of Python). I also created a Release (v0.1.0) on GitHub.

**Thoughts** Even an MVP (Minimum Viable Product) takes a bit of work. At last now I feel I can move over to the New World Data Comparison project. Also, creating an actual Release feels pretty official.

**Link to work:**

* [Inc Help Parser](https://github.com/bertbronaugh/IncHelpParser)  
* [IncHelp Parser v0.1.0 Release](https://github.com/bertbronaugh/IncHelpParser/releases/tag/v.0.1.0)

### Day 7: December 30

**Today's Progress**: Made some good progress on the NWData project. Started laying the groundwork for the Processor and TestAide classes.

**Thoughts** It's been a while since I used Typescript/Angular, so it's been a bit like remembering how to ride a bike again. Trying to remember to atomize functions and KISS where I can.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 8: December 31

**Today's Progress**: Tinkered a bit with the Testing sections, mainly getting the newline/tab splits to work properly. Currently working on the initial parsing steps now, using JSON formatting for easy visual debugging.

**Thoughts** Looking back at the PrintjobConverter and bzParser projects helped. The tab files I'm using for testing have some quirks in that some rows use have SetId and EntryId separated by tabs (as they should be) and others just have a space-hyphen-space, which naturally doesn't parse correctly. I'll have to come up with a way to identify/handle those instances without affecting the rest of the data on that row.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 9: January 1

**Today's Progress**: Started laying the groundwork on the Library. Still tinkering with showing/manipulating the Sections.

**Thoughts** Actually spent a couple of hours on this today, mostly because I just got so caught up in it (and it was during naptime). After some thought, creating a Library to house the different sections just seemed like a great way to organize everything. This way, each section can be processed and organized as needed without interfering with other sections. Each Section can be a standalone item, but still contained within the overall Library.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 10: January 2

**Today's Progress**: Yay, settings are borked!

**Thoughts** So....whoops. My tinkering around with .NET Core (and the supplied IIS Express install) from the NWData project ended up breaking my current IIS settings. Tried to debug another (previously working) app earlier today and got some new errors. Spent time trying to get NWData to play nice on IIS. Ultimately decided to start trying to get NWData Dockerized, because I'd really rather not have to plead/cajole IIS into working every time I want to switch to/from my other apps.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 11: January 4

**Today's Progress**: Read up some on Terraform.

**Thoughts** Skipped yesterday because time got away from me. Almost missed today, but decided to read up on Terraform a bit. I've been considering restarting my Tyler server and getting it going as a CI/CD target, both for existing and new projects.

**Link to work:** [Terraform](https://www.terraform.io/)

### Day 12: January 5

**Today's Progress**: Added container orchestration support to the project (I think). Didn't work, so started a new project from scratch to try and get Docker going.

**Thoughts** I just want to be able to run this without breaking other stuff. It spins up a container image via Docker Compose on the Docker Desktop status window, so that's something I guess? Of course, it still doesn't run when I start Debugging. "An unhandled exception occurred while processing the request." Yaaaaay. I started a fresh project and added Docker Support right away, which made it start up a container. Wasn't accessible via the browser, though. Tried doing a build. If I can at least get the boilerplate project to run in Docker, I'll copy over my previous NWData page work and go from there. Build works, but can't debug. "SocketException: No connection could be made because the target machine actively refused it." I think I need to check the "Expose daemon on tcp://localhost:2375 without TLS" box in Docker Desktop.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 13: January 6

**Today's Progress**: More Docker tinkering, project restarts.

**Thoughts** I think I'm at the spaghetti stage now, where I'm just throwing stuff at the wall and hoping something sticks enough to get my project running again. Spent a good amount of time tonight trying to get a boilerplate project going, but no luck. Maybe I should indeed go back to IIS Express for the time being, or maybe find a way to get it to play nice with IIS. Either way, I feel like I've been spinning my wheels on this for long enough.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 14: January 7

**Today's Progress**: Restart and reconsider.

**Thoughts** So, I had a realization tonight. I think I started down the wrong path with my push to get Docker up and going. My other apps seemed to actually run normally today, so maybe IIS Express wasn't the issue after all (or at least most of the issue). Second, I think I've been focusing too much on the NW Data parsing step and not on the actual comparison/mapping step. My thought was: "Why can't I just get a database connection going and work from there on getting the mapping figured out?" Breaking out and uploading the relevant sections of the NW Data is indeed relevant and can (hopefully) be addressed in the future, but the crux of the problem lies with the mapping. That's where I should be focusing my efforts. Tonight, I cleared out the project folder and started fresh. It builds/debugs happily now. I tried starting an Azure SQL Server Serverless instance, but I apparently don't have any credits on Azure yet. Still working on that, and I may need to work out a separate testing database to use for the time being, but we'll see.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 15: January 8

**Today's Progress**: Server shinanigans

**Thoughts** Tinkering around with the Azure SQL Server. Created a Serverless instance so it wouldn't be running when I didn't need it. Kept having trouble creating the database/table I needed to start with, so ultimately ended up using what appears to be the locally created db within Visual Studio. Also started looking at tutorials for reference on creating a SQL connection from the Angular/.NET Core project.

**Link to work:** [Brazos New World Data Comparison](https://github.com/bertbronaugh/BrazosNewWorldDataComparison)

### Day 16: January 10

**Today's Progress**: Maybe an API?

**Thoughts** Accidentally skipped yesterday. Didn't even realize it until today. Realized the SQL Connection tutorial from earlier wasn't the right direction, so searched for some more pages to help. Found a good idea to try: an API with an Angular front-end added on. That actually makes sense, since the API will handle the CRUD heavy lifting and Angular just displays it. I intend to first follow along with this tutorial somewhat, substituting the blog posts for the "data maps" as I've come to call them.

**Link to work:** [CRUD app API with Angular](https://dev.to/dileno/build-a-simple-crud-app-with-angular-8-and-asp-net-core-2-2-part-1-back-end-39e1)

### Day 17: January 11

**Today's Progress**: I have a working API!

**Thoughts** I'm surprised. I didn't think it would be this straightfoward to get a working API, and yet so difficult. The guide was written in 2019, using .NET Core 2.2, whereas I started out using 3.0. Yes, there's a difference and it's a very crucial one. Apparently, around the time 3.0 came to pass, there was a change from using MVC Routing to using Endpoint Routing. Fascinating, I know, but this threw me for a 30-45 minute loop of trying things, getting errors, Googling StackOverflow, and so on. I almost didn't realize the initial 404 Error didn't mean the API wasn't working, but that I just didn't have a GUI to use for my initial tests. I've now approached the end of the first page, and I have a working API that allows GET/POST requests. I still need to keep in mind the DataMap model should probably reflect my destination table and its columns, but that's not yet a breaking issue just yet.

Oh, and I've now created a new and separate project as well. I call it DataMap, which I think is a much better and more developer-y sounding name. I'll start on Page 2 of the tutorial tomorrow.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 1](https://dev.to/dileno/build-a-simple-crud-app-with-angular-8-and-asp-net-core-2-2-part-1-back-end-39e1)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 17: January 12

**Today's Progress**: Starting on the front end with Angular

**Thoughts** Page 2 of the tutorial. Created the Angular front-end. Tested it. Added the components and service. Next will be updating app.module.ts.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 18: January 13

**Today's Progress**: The first wheel now turns the second. (.NET Core now starts the Angular server.)

**Thoughts** Picked back up on the tutorial, learning how to get Startup.cs to start the Angular server when the API backend is started. Stumbled upon some red squigglies along the way. Evidently, 3.0 was a breaking change from 2.2, enough so that I had to pick through StackOverflow to find out what NuGet packages I needed to install. Finally banished the squigglies for the time being. Picking back up tomorrow on "Create blog post model and service methods".

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 19: January 14

**Today's Progress**: Adding Model. Updating Service. Fleshing out the components to show the data maps.

**Thoughts** Added the rest of the fields for the current table that's the target of this build. Migrated the database. Took a break, then came back and made some more progres. Stopped at 'blog-post-add-edit.component.ts' for now. Just need to finish going through data-map-add-edit-components and modifying all of the blogPost-related references for dataMap.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 20: January 15

**Today's Progress**: Finishing updates to add-edit component.

**Thoughts** Finished going through this section and cleaning everything up. I'm learning more (bit by bit) of how this all connects together, and I'm also realizing how much my idea is straying from the tutorial. Not a ton, but I'm having to take care not to skip stuff that's referencing the old BlogPost code in any way. Stopped on the section where we're editing blog-post-add-edit.component.ts.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 21: January 16

**Today's Progress**: Finished the tutorial. Hunting errors.

**Thoughts** Finished the updates to the data-map-add-edit-component. Had some issues with the Angular CLI server not talking to .NET Core again. Learned how to increase the timeout so Core would be a little more forgiving to Angular. Unfortunately, having an issue when I hit the Add DataMap button. Errors in the Core-side output. Still investigating that.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)  
[CRUD app API with Angular - Page 2](https://dev.to/dileno/build-an-angular-8-app-with-rest-api-and-asp-net-core-2-2-part-2-46ap)

### Day 22: January 17

**Today's Progress**: IIS Express issues

**Thoughts** 'Unable to connect to IIS web server. Class not registered'. Well, that's new. Restarted Visual Studio, same thing. IIS Express is running, through. Attached to the w3wp process and it worked. Or at least, it seemed to work. The Add Data Map button stil takes me to a blank screen, and I don't see any output in VS. Rebuild, debug, and same 'Unable to connect' error. I'm seeing stuff online about trying a different port, so I'll try that next time. It's pretty late and I need to call it for tonight.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)

### Day 23: January 18

**Today's Progress**: Internal server updates / Reading up on Tyler Deploy

**Thoughts** Didn't feel up to troubleshooting the IIS Express issues. Logged back into my server, kicked off Windows updates. Can't access it via the URL, so maybe something's up with IIS. Read up on Tyler deploy. Considering setting it up to deploy my IncHelpParser to start with.

**Link to work:** (No links tonight.)

### Day 24: January 19

**Today's Progress**: Connection Refused

**Thoughts** Spent a bit of time puzzing about the error. I think it's due to the API url that Angular's trying to use. I'll need to come back to this and see if I can follow the trail more. My current hypothesis is that the API URL that Angular is using may not be the one set up by .NET Core.

**Link to work:** [Stack Overflow - Connection Refused question](https://stackoverflow.com/questions/52067788/failed-to-load-resource-neterr-connection-refused-nodejs)

### Day 25: January 21

**Today's Progress**: Light reading about MVC

**Thoughts** Skipped last night. Nearly skipped tonight. Decided to spend a bit of time reading over how MVC works. Still don't fully understand it, but it was helpful to read some about how the process works. It seems like Core could be a really powerful tool for some of the services we run. Maybe some of them could be converted and become more standalone in the future.

**Link to work:**  
[Overview of ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview?view=aspnetcore-5.0)
[DataMapper](https://github.com/bertbronaugh/DataMapper)

### Day 26: January 22

**Today's Progress**: Dr. Frankenstein's monster awakes.

**Thoughts** AAAAAAAAAAAAAAAAAAAAAAAAAAAA The main page works now! I spent maybe 15-20 minutes tinkering with the API settings and trying Postman, before I figured I'd try and search for a guide using .NET Core 3.1 and Angular. Honestly I think the addMVC stuff was the monkey wrench. I was at that stage where everything API-related just seemed dumb, why am I fiddling with this, why am I not seeing progress. That whole deal. Sure, the Add portion still doesn't work, but at least the home page is displaying the one row I currently have entered. That's certainly a start. Chasing Validator errors on the Add page now.

**Link to work:** [.NET Core 3.1 / Angular tutorial](https://www.c-sharpcorner.com/article/build-crud-operation-using-angular-9-and-dot-net-core-3-1-webapi-and-deploy-to-a/)

### Day 27: January 24

**Today's Progress**: A New Idea Appears!

**Thoughts** Skipped last night. My personal laptop died and I wasn't able to resurrect it. Wasn't really in the mood to code after that. Really late tonight when I got free, so instead of going to the trouble of spinning up DataMapper again, I decided to break ground on another project idea I had recently: Fixed Length Export Checker, or F.L.E.C. The idea is that you'll define a list of fixed length fields used by your interface on one screen/tab/etc, then switch to the "data" view and paste in a sample you want to check. It'll use that template to show you what data is in which field, along with (hopefully at some point) being able to identify/diagnose root cause(s) of a bad sample.  
  
Also, I have soooo much to learn about Git. I tried to be smart and ng new locally and push/create on Github, but ended up tying myself up in a digital knot. Git is some sort of magic that you have to be very careful about getting it right the first time, or you'll spend a lot of time trying to clean up the mess.

**Link to work:** [F.L.E.C.](https://github.com/bertbronaugh/FixedLengthExportChecker)

### Day 28: January 25

**Today's Progress**: Under construction

**Thoughts** Moved the files up one level so I could actually build it like normal without having to cd down every time. Cleared the template HTML and started fresh. Only a few divs right now, but at least it's something.

**Link to work:** [F.L.E.C.](https://github.com/bertbronaugh/FixedLengthExportChecker)

### Day 29: January 26

**Today's Progress**: Groundwork

**Thoughts** Basic groundwork for the sample/template components, using a past project for reference.

**Link to work:** [F.L.E.C.](https://github.com/bertbronaugh/FixedLengthExportChecker)

### Day 30: January 27

**Today's Progress**: Light Reading

**Thoughts** More study about MVC and Core. Actually feel like I'm starting to get parts of it, albeit still mostly conceptually.

**Link to work:** [Overview of ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview?view=aspnetcore-5.0)

### Day 31: January 29

**Today's Progress**: CI/CD ideas

**Thoughts** Skipped last night, mainly due to energy. Happened to read a StackOverflow article about CI/CD and it gave me some great ideas for my current projects. The issue is that while it's great to have my server running and available as a CD target, it's on the VPN that you need to deploy to and browse to.

**Link to work:** [Fulfilling the promise of CI/CD](https://stackoverflow.blog/2021/01/19/fulfilling-the-promise-of-ci-cd)

### Day 31: January 31

**Today's Progress**: Validator hokey pokey

**Thoughts** Skipped last night as well. Returning to my Mapper project. I think I've had a long enough hiatus, and I'd like to put the CI/CD ideas into practice. First thing to do is to get rid of these Validator errors. Made a bit of progress, I think. Still having issues with what I think is Reactive Forms not playing nice with my form references. Looking at everything, I still feel like it's all a bit of the "Hokey Pokey" song. Maybe I should ask for a bit of outside help on this to get unstuck.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)

### Day 31: February 1

**Today's Progress**: ProgressGoesHere

**Thoughts** I. Finally. Got it. Not the entire thing of course, just the Edit page. Turns out, I was using a naming convention/process when looking for the form controls by name that it couldn't find them. I didn't think this guide was this out of date, but apparently it needed more than just the MVC/Routing updates from before. I got a lot farther on this than I expected tonight. I'm able to Add new data map entries and I'm currently investigating why I can't Edit existing ones.

**Link to work:**  
[DataMapper](https://github.com/bertbronaugh/DataMapper)
[SO Article](https://stackoverflow.com/questions/60929346/cannot-read-property-value-of-null-angular-reactive-form-get-value)

### Day X: Month Day (Template)

**Today's Progress**: ProgressGoesHere

**Thoughts** ThoughtsAboutLifeTheUniverseAndEverything

**Link to work:** [Links to stuff](http://example.com)
