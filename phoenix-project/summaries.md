# The Phoenix Project (Kim, Behr, Spafford)

## Prologue

Setup of the people, their roles and the starting situation of the company

## Chapter 1

- main character setup
  - Bill Palmer
  - middle aged with two sons
  - former marine
  - Getting a promotion he doesn't want
- MC primary concerns
  - outdated company
  - messy relationships with upper management
  - IT as "computer janitors"
  - blame environment
- Intro to the titular Project Phoenix
  - Online buying of parts
- First big problem
  - Payroll system not working

## Chapter 2

- Finance is REALLY ANGRY about payroll failing
  - Bill focuses on talking to people who can help and drills down
  - Manual process to fix issues with payroll 😱
  - Auditors are knocking on the doors so the problem has urgent timeline
- Further introduction of the team Bill is now responsible for
  - Patty is responsible for the level 1 & 2 support
  - Wes is responsible for DB, networking and servers
- SAN firmware upgrade failed at the same time payroll did
  - Rolling back bricked the SAN
  - Fixing this delayed Phoenix work
  - Delayed Phoenix work will have impact on management!

## Chapter 3

- Better picture on the SAN upgrade and how long and complex the upgrade path was
- Database corruption happened in one specific field (SSN numbers)
  - SAN failure seems to not have been the killer
- CISO forced a developer to push through a quick update before going on vacation
  - "The best way to make sure something doesn't get done is to have them in the room"
  - Because of the audit, a product was quickly deployed to anonymize the SSN field for compliance with EU regulations
  - CISO forced this through to avoid issues with the audit, breaking deployment process
  - Claims he had to break the change process otherwise the next deployment window would be in 4 months
- Change management and ticketing systems go unused
  - "Everyone thinks that the real way to get work done is to just do it. That makes my job nearly impossible"
- Newspaper report on the payroll failure hits the news

## Chapter 4

- Lots of emails from vendors trying to get something
- Email from board worried about Project Phoenix being delayed again and it being Bill's responsibility
  - Caused by Brent debugging the SAN issue instead of doing work for Phoenix
  - Dev silo has a two-week cycle with the Ops people
- Really messy planning meeting
  - Arbitrary deadlines being set
  - Heading towards a buggy deployment because no tests can be done in the remaining time, and lots of corners will have to be cut
- Constant firefighting is keeping the Ops guys from being able to help solve problems at the source
- Nobody shows up to the change management process
  - ITIL training has happened, and tooling exists, but nobody seems to care
  - There was previous conflict between the teams when trying to implement change management
- Security patch caused lots of laptop failures, including Bill's

## Chapter 5

- Internal audit detcted potentially catastrophic issues
  - Response required in six working days, to a document with almost 200 pages
  - Audit caught multiple of the holes we saw in the previous chapters
    - e.g. untested changes to production
- Hiring has been a problem for Ops
  - Budget cuts
  - Hiring senior engineers instead of younger ones ended up with half of them quitting and the remaining half underperforming
- IT's work list is flooded with tasks without ordering or prioritizing
  - Official business project list (owned by Kirsten)
  - IT Operations projects (not centralized)
  - Service Desk (calls + random requests)
- A plan is made to fix this: one-line summaries for all the committment

## Chapter 6

- Findings point to a gigantic backlog
  - 105 projects for 150 people mean 1.5 people per project
  - Compliance with the audit would stop the rest of the work for a whole year
  - 75% of the time is fire-fighting
  - A clear plan is established to hire 7 new people
- Big change management meeting finally happens
  - Old process is scrapped, despite Patty's objections and the amount of time+money invested in it
  - Team decides to start writing things down in paper cards
  - Almost 400 change requests submitted for next week

## Chapter 7

- Potential new board member in town
  - Bill mistakes him for the delivery company...
  - Erik is a really weird guy, who can't seem to remember anyone's name and lacks social graces
- Scientifically-grounded management is introduced
  - Theory of Constraints
  - Toyota Production System / Lean production
  - Total Quality Management
  - Common objective: control work in progress
- Three Ways
  - First Way: fast flow of work
  - Second Way: shorten and amplify feedback loops
  - Third Way: culture
- Four types of work
  - #1: business project work
  - #2-4: Erik tells Bill to find them out
- The "new" laptop stops working too!

## Chapter 8

- Marketing is selling project Phoenix to analysts even though it's far from ready
  - Might be a key factor in the pressure causing features to be released prematurely
- Meeting with the CEO  
  - Thirty minute meeting reduced to 20 minutes because the previous Phoenix meeting went over time - it ended up being just 17 because the next Phoenix meeting ALSO cut in at the end
  - Lack of will to understand just how understaffed IT Operations is
    - "Go to your peers and make your case to them"
- Change management whiteboard is overwhelming
  - 437 changes for the week!
  - Prioritization rules established
    - top 10 "most fragile" services/apps/infra must be approved by the CAB
      - Reports on the success rates and downtime important, for business to evaluate
    - low-risk, frequent changes (ITIL: 'standard changes') are approved automatically
    - middle-risk "messy middle changes" are the change submitter's responsibility - they should contact people potentially affected
  - Lack of automation in the process makes it very labour intensive

## Chapter 9

- Severity 1 outage! Credit card processing systems stopped working.
- Blame throwing immediately starts
  - Brent quickly fixes the problem... which may mean it was his responsibility in the first place
  - 0 respect for change management process
  - Bill wants people to start disclosing any changes they make during incidents, and trial runs to be done regularly
  - Patty is also responsible for every time there is a severity 1 outage, establishing a clear timeline of the issue at the start of meetings so everyone is on the same page
- First change management is very successful
  - Patty is congratulated for her work leading the project
- Bill figures out categories of work #1-3 are business projects, internal IT projects, and changes.

## Chapter 10

- Brent is acting as a bottleneck for Phoenix, as he is getting over-scheduled with tasks.
  - Everyone calls him when they need something, and these calls are not registered anywhere in the system.
  - Bill tells him to autoreply to everyone telling them to go through Wes instead of replying
- Wes, Bill and Patty meet to find a way to avoid the bottleneck
  - Level 3 engineers handle incident response, and only they can escalate to Brent, and they must document everything.
  - Other "hard measures" are taken such as collecting the names of everyone who calls him.

## Chapter 11

- Patty is disappointed with the change management process
  - Three people full-time are necessary to manage it
  - Only 40% of the changes got implemented since last week!
  - Lots of different reasons for the failed changes, but many are because Brent was not available
- We go back to the analogy between IT and the plant floor
  - If Brent is the bottleneck, we need exactly what changes need him, and if they can be done with the level 3 engineers
- If Erik was right about WIP in IT Operations, what else was he right about?

## Chapter 12

- Phoenix has turned into a _death march_
  - "It's not a good sign when they're still attaching parts to the space shuttle at liftoff time"
  - "works on my machine" syndrome, Ops vs Dev
- Deploying Phoenix in production doesn't seem viable
  - They can't even get the dev environment up and running
  - Feedback loop is very long (30 minutes setup, 3 hours smoke tests), and by the time it's done there are multiple more releases ready to test
  - Version control gets really messy
- Bill contacts Steve to try to get a delay
  - References a [Toys-R-Us trainwreck](https://nytimes.com/1999/12/23/business/toys-r-us-falls-behind-on-shipping.html) in an attempt to explain the level of catastrophe we coudl be facing
  - Steve passes the ball to Sarah, and she says no
- "Point of no return" is hit and things still aren't working
  - Database migration will take much longer than expected
  - Performance is terrible
  - Lots of manual hacks required
- Deployment completely fails
  - Stores have to open in complete manual mode, as all POS systems are down
  - Phoenix website is incredibly slow, double/triple charging credit cards or losing transactions
  - Website leaks credit card numbers!

## Chapter 13

- Steve gets angry at everyone, as he's been forced into interviews with journalists to justify/explain what happened.
- Sarah pressures for improved usability
  - Development & Operations both reject this, and implement a twice a day code rollout strategy, with only performance-related changes
  - "the time for usability testing and validation was months ago"
- Finance people have set up a war room with 16 people just to take care of the faxes to fix duplicate payments or missing orders
  - Five thousand issues so far, twenty five thousand still to investigate!
- CISO John detects a major security breach - manual orders are storing the CVV code of credit cards
  - If auditors catch this, it would raise the transaction fees on every credit card usage, as well as huge fines
  - Auditors are in the office today, but John tries to distract them while Bill fixes things
- Operations is at capacity and cannot help fix the credit card issue
  - John volunteers two Security engineers to help with some of the work (SOX-404 audit response letter)

## Chapter 14

- Situation is finally stabilized on Monday night
- Steve suggests it's IT's fault
  - “I need the business to tell me it’s no longer being held hostage by you IT guys."
  - Proposes outsourcing all of IT if they can't pull off a miracle within 90 days
- Bill and Chris have a meeting over lunch to discuss this
  - "Technology keeps changing faster and faster, and it’s nearly impossible to keep up anymore"
  - They decide to meet once a week to try and stop the outsourcing idea
- Dev guys throw a party and invite the Ops folks, but Wes isn't very happy with this due to the Ops team still fixing the transactions.

## Chapter 15

- Bill has breakfest with his wife in which he reviews his life situation
  - He stresses that his purpose is now to stop the oursourcing
- Change board succeeded at avoiding a collision!
- Unfortunately, the change board is super messy now, because of Phoenix disrupting all planned work
  - This means we just found the fourth category of work - **unplanned** work!
- Bill calls Erik and updates him on what has been happening
  - Next mission: figure out how to set the tempo of work according to Brent, as he is the constraint.
  - "outcomes are what matter—not the process, not controls, or, for that matter, what work you complete.”

## Chapter 16

- Company invoicing hasn't been working for 3 days!
- Primary guideline for fixing the fialure is to avoid losing transactions
  - Patty's team looks into all possible failure causes and drills down to 8
  - 8 people are responsible for looking further into each
- As the team is working on it, Bill gets a call from Steve
  - Steve is panicking, so he forces everyone to get out of bed and go to work trying to fix this
  - Bill tries to defuse the situation and continue working on things with a structured plan but Steve refuses and forces the escalation
  - In response, Bill tells him to call the shots himself, and announces he will resign the next day.

## Chapter 17

- Patty and Wes call Bill four days later
  - Everything is on fire - the inventory management systems are now down too.
- Steve talked to Bill's wife, and she gets him to call Steve back
- Steve's proposal is for Bill to assume his job again, for at least 90 days. At the end of those days, if he still wants to leave, he can do so with a 1 year severance package.
  - This proposal was brought on by Erik and the audit committee "kicking [Steve's] ass"
- After a 45 minute discussion, he eventually accepts.

## Chapter 18

- Chapter opens with an "off-site" IT leadership meeting
  - Steve admits to his mistakes managing IT and tells his personal life story
  - “Are you guys willing to do what it takes to help create a team where we can all trust one another?”

## Chapter 19

- Everyone else shares their personal stories
- Discussion on why IT always misses every commitment/schedule
  - Chris states that they hit the date for Phoenix, but how can that be when the deployment failed?
  - Dev did not factor in the work Operations needed to do!
  - "When deployments don’t go as planned, whether the plan was written by your group or mine, it affects everybody else."
- They forgot the security guy! He doesn't get to share a personal story.
- "Left unchecked, technical debt will ensure that the only work that gets done is unplanned work!”
- The managers come up with a hail mary - freeeze all work except for Phoenix work.
  - Development can still continue working on non-Phoenix projects, but just won't deploy them
  - Operations freezes all work for two weeks

## Chapter 20

- After a week of the freeze, the focus on Phoenix has been enough to start fixing things
  - Multiple people are angry about their projects, particularly Sarah
  - "the project freeze has reduced the priority conflicts and bad multitasking"
- A vendor made a change to the phone system causing downtime
  - To prevent this from happening again, the team starts a monitoring project
- Decision for what to work on at any given time doesn't have a heuristic
  - "Priority 1 is whoever is yelling the loudest"
- Erik and Bill discuss the priority issues
  - *Standardizing* work was what allowed Brent to not be as big of a constraint
  - The monitoring project will be very important, because it prevents outages, thus freeing up more of Brent's time (reducing the load on the constraint)
  - Properly elevating preventive work is important (Total Productive Maintenance)
  - Work for the CISO isn't a good use of time, as it won't do anything for the constraints

## Chapter 21

- Meeting with external audit goes well, despite John's worries
  - Erik being friends with the external auditor probably didn't hurt
- John is really angry at how the audit ignored the IT Security risks he warned about
  - Erik calls him out for this
  - "you win when you protect the organization without putting meaningless work into the IT system. And you win even more when you can take meaningless work out of the IT system."
  - He ends up leaving the room and threatening to quit his job

## Chapter 22

- John hasn't showed up for owrk
- Patty, Bill and Wes meet to try to determine which projects can start being worked on
  - They try to map the projects to physical resources (inputs, outputs, machines, etc.)
  - They decide to start the monitoring project ASAP and test some of these concepts with smaller service requests (password resets, laptop replacements, etc.)
- Patty sets up kanban boards with three columns: "Ready", "Doing" and "Done"
  - The board also has rows to subdivide the index cards
  - Cards are also colored depending on how critical the projects they support are, and if they are blocked
  - All work must go through kanban boards
- Bill now has a date for his laptop replacement!
  - Applying these techniques to laptop replacements drove down error rates, on top of having a queue with times
- Patty proposes creating a Kanban just for Brent, since he is the constraint
- They come up with a strategy for the project un-freeze
  - When determining the projects, they separate them between business and internal projects
  - The top five business projects will be unfrozen immediately
  - For the internal project, they decide to establish three lists: requires Brent, increases Brent's throughput, and everything else
  
## Chapter 23

- Scheduling estimates have failed, causing almost a week of delays
- Biggest cause is the lack of slack time - since everyone is at high capacity, WIP spends a lot of time in the queue.
- Tasks are being assigned to a single person when in reality they depend on multiple people and imply having handoffs
- "if we can standardize all our recurring deployment work, we’ll finally be able to enforce uniformity of our production configurations"
  - Brent became the constraint because he was allowed to build infrastructure only he could understand

## Chapter 24

- John has a complete meltdown
  - He asks Bill how he has helped him over the years, and Bill replies he was mostly independent
  - John's epiphany: "if I haven’t done anything useful for you, who I should have the most in common with, then it stands to reason that I haven’t been useful to almost everyone else, who I have nothing in common with."
