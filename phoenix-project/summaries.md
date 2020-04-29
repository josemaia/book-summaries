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
  - Prioritization rules establishsed
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
- First change management is very successful
- Bill figures out categories of work #1-3 are business projects, internal IT projects, and changes.

## Chapter 10

- Brent is acting as a bottleneck for Phoenix, as he is getting over-scheduled with tasks.
  - Everyone calls him when they need something, and these calls are not registered anywhere in the system.
  - Bill tells him to autoreply to everyone telling them to go through Wes instead of replying
- Wes, Bill and Patty meet to find a way to avoid the bottleneck
  - Level 3 engineers handle incident response, and only they can escalate to Brent, and they must document everything.
  - Other "hard measures" are taken such as collecting the names of everyone who calls him.
