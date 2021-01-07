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

### Day X: Month Day (Template)

**Today's Progress**: I did stuff.

**Thoughts** I thought about stuff.

**Link to work:** [Links to stuff](http://example.com)
