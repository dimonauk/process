
# Process Manual - Opus Novum      
---
---
#### Contents
__1 Introduction__

__2 Basic Skills__
* Text editing
* Operating system on your computer 
* Linux command-line interface
* Regular expressions 
* IRC 
* SSH 
* Git 

__3 The Commandments:__
* GENERAL 
* CODING  
* TESTING
* DESIGN 
* ESTIMATING 
* MANAGING

__4 A list of questions to elicit requirements from stakeholders__

__5 Mustard__

Roles:
* Checklist for customer role 
* Checklist for architect role
* Checklist for project manager role
* Checklist for developer role
* Approximate process flow

Data model 
* License management in projects
* The aspects of good requirements
* Verification Criteria
* Glossary

__6 Using Kanban__

* Boards
* Buckets 
* Cards
* Workflow
* Milestones
* Management

__7 Work Review__

* Simple, clean, clear review commentary
* Things to consider when reviewing code (or other things) 
* Who and when 
* References

__8 Standing up__

Performing a standup:
* Characters
* Notes 
* Keep it short 
* Phrasing 
* Raising hands during the discussion

An example standup 

__9 Project Management__

* Project Manager Role and Responsibilities
* Project Startup 
* Establishing project accounting
* Establishing the project groups on the git server
* Pushing the initial project admin wiki to the git server 
* Day-to-day PM Role 
* Risk Analysis
* Internal Project Reporting
* Customer Reporting 

__10 Laptop policies__

* Installation layout guidelines 
* Security considerations 
* Backups

---
## 1
##### Introduction

This document aims to standardise the way we do things. Some of our approach is derived from Open Source best practices, some from Automotive SPICE, some from manufacturing and some from our own experience. The aim is that Codethink’s processes should make life easier, by reducing uncertainty. We want Codethink’s processes to be lightweight and applicable either iteratively or linearly. Criticism and questions are encouraged, once you’ve taken the time to understand the reasoning for the current processes. We are aiming to establish the same default processes, rules and tools on all projects. This extends to standardising our approach for custom tools with Python + YAML + Markdown + Git. This set of documents specifies those defaults. Doing something else is only ok if the project/situation explicitly justifies a variation. Any variation needs to be documented in the location provided for in the project management template. Everyone is expected to know and understand what is in these process documents, to follow them where appropriate, and to help improve them. 

* Apply The Software Commandments
* FIXME: Sales handover process 
* Identify risks on new projects using the Risk Management Checklist 
* FIXME: Naming Standards 
* At project start, use the Project Startup Checklist 
* Capture requirements using Mustard 
* This applies even if there’s no architecture to do, and even if requirements documentation is provided by the customer. 
* Refer to the Requirements Capture Checklist. 
* Describe architecture and design in Mustard. 
* Use Kanban for day-to-day task allocation, short term milestone planning and deliveries. 
* Follow the Kanban Guidelines. 
* Keep all source files in Git, in the appropriate place on the Codethink Trove. 
* Write all documentation in markdown format, and keep it in Git too. 
* Use Baserock wherever possible 
* FIXME: Issue Tracking 
* Code Review

---
### 2
##### Basic Skills

Engineers (and perhaps managers too) need a lot of core skills and experience to be effective. The following is a shopping list.

__Text editing__

Everyone should be comfortable using plain text editors of some kind or another. *  edit with vi, vim, emacs, (or at worst nano, gedit, geany or similar) 
*  non-trivial document navigation, including jump to specific line, page up, page down, beginning or end of document 
* search for complex pattern 
* search and replace • delete n characters 
* delete n lines 
* cut and paste 
* quit without saving 
* save to current file or a different one

__Operating system on your computer__ 
* install your preferred Linux-based distro. If you have no preference, then Fedora or Debian is recommended in order that others in the company can support you. 
* understand how a desktop works 
* understand how a command line shell works

__Linux command-line interface__ 
* bash (or some other shell) – pipes – stdin and stdout, and redirecting them 
* Use command line utilities, at a minimum (with their common options): man (this should help with all the others), info, /usr/share/doc, cd, pwd, ls, cp, mv, grep, find, sort, uniq, sed, awk

__Regular expressions__
* understand regexp syntax and be able to decompose/evaluate existing regexps 
* create your own regexp, especially for pattern matching 
* understand the difference between shell globs and regular expressions

__IRC__

* be able to install your chosen client 
* use it to join Codethink network, and freenode
* join and leave channels 
* send channel messages 
* send and read private messages 
* understand common abbreviations and slang

__SSH__ 

* understand public/private keys, create your own, understand how/what to copy 
* use ssh for non-Codethink services 
* access Codethink services (eg access) via ssh (Note: 2048bit or larger RSA keys, or else 384 bit or larger ECDSA keys are the only acceptable options here. DSA keys are not acceptable any longer).

__GIT__

* initialise a new repo 
* clone an existing repo 
* make changes and commit them with appropriate commenting 
* work with local branches - create, checkout, commit, merge, delete etc. 
* switch between branches 
* work with remotes 
* push work from your local branch to a remote branch 
* work with remote branches - create, checkout, merge, delete etc. 
* work with tags 
* cherry-pick 
* reset 
* rebase 
* understand git datastore structure principles

---
### 3
##### The Commandments

Derived from version 2.1 of the ‘Software Commandments’ by Paul Sherwood.

__GENERAL__

1. Commit to deliver, to help, to learn, and to improve
2. Be honest, be reliable, and work hard 
3. When you mess up, own up! And LEARN from your mistakes 
4. Don’t stay stuck, get help! If you’re in a hole, stop digging. If in doubt, ask. Keep asking til you’re answered 
5. Communicate! Keep colleagues and customers informed - avoid surprises 
6. Write effectively, speak effectively - keep it short and make it matter to the recipients 
7. Finish your project. Know your deadlines, hit them if you can, shout if you realize you can’t
8. Solve problems, and help others to solve problems too – everyone learns faster that way 
9. Never leave a mess behind you: this applies to your project, the kitchen AND the bathroom! 
10. Think for yourself: challenge bad decisions, escalate if necessary - stay calm and polite 
11. Make sure you really understand the objectives/target of the project, from your customer’s point of view 
12. Keep a log book and use it every day
13. Always keep your own backups, and make sure you can restore

__CODING__

14. Code LESS: every line creates a work-chain 
15. Read the documentation, use existing code if possible. Don’t re-create what already exists
16. If there isn’t a spec/definition, write a short one (with constraints, goals, non-goals) and agree it 
17. If it isn’t specified as a requirement, don’t code it. If the agreed spec is wrong, challenge it 
18. Understand why code style is important, and comply with existing style
19. Get someone to review your code. Learn from the reviews, don’t take it personally 
20. Use version control, ideally Git. Commit early and often, with descriptive comments, and push your commits! 
21. Quality code WORKS! All the time 
22. The bug stops here! You are responsible for testing and fixing every line of code you write 
23. Remove uncertainty as fast as possible. Prototype, learn and iterate 
24. Set yourself doable targets every day and every week. If you’re not making daily progress, shout

__TESTING__

25. Test behaviour, not structure. Don’t be gentle, break it! 
26. Write down what you need to test before or at the same time as you write the code 
27. Look for difficult, unexpected cases too 
28. If it can’t be tested, it shouldn’t be there 
29. If there’s a test framework, use it. Aggressively replace/remove tests when things change 
30. If someone else finds a bug after you’ve said it works, kick yourself and improve your practice!

__DESIGN__

31. Establish constraints and write them down 
32. Plan to remove uncertainty fast - prototype and test against realistic scenarios ASAP 
33. Design for testability, and design defensively: garbage in DOES NOT equal garbage out! 
34. Design should be communicated clearly in writing, pictures or both 
35. The first idea isn’t necessarily best: consider alternatives, discuss
36. Great design (and leadership) is methodology-independent 
37. K I S S - simplicity is ALWAYS a design objective

__ESTIMATING__

38. Discuss the requirement with others – get perspective 
39. If you’re unsure, say so. If you need more information, ask for it 
40. Break the problem down into component tasks – get someone to challenge the breakdown 
41. Compare like-for-like: try to check against previous productivity on similar work 
42. Estimate the whole job, not just the coding. State what’s included, what’s excluded. State that it’s a GUESS 
43. Don’t be over-optimistic. It’s ALWAYS worse than you think

__MANAGING__

44. Get the best people you can find/afford, and clear the way so they can be effective 
45. Provide strong leadership – make sure your people know what they need to do, and when 
46. Allow and foster open and honest communication. Listen and learn. React effectively and fairly 
47. Encourage debate where necessary, but if things get bogged down, be a benevolent dictator 
48. Set short timescales for targets and reviews – weekly is probably best. 
49. If you’re squeezed on time and cost, reduce scope – or it’ll be late/broken/over budget 
50. Nail the risks, before they nail you!

---
### 4
##### A list of questions to elicit requirements from stakeholders

* What does the system/software need to do? 
* What external interfaces are required? 
* Who are the target users/customers? 
* When is the solution required/expected? 
* Must everything be delivered at once, or are some requirements more urgent? 
* Has this kind of thing been done before, either by the customer or elsewhere? 
* Are there constraints, lessons or other relevant information from previous attempts? 
* Are there existing tools, components, systems or code that may (or must) be used? 
* What are the requirements for performance and/or response times? 
* What are the requirements for data volumes, transaction throughput, peak load? 
* What are the requirements for reliability, robustness, SLA, uptime? 
* What are the implications in the event of downtime? 
* What are the requirements for confidentiality, data security, encryption? 
* What are the requirements for prevention of hacks, exploits, denial of service? 
* What are the implications if the system/software is hacked or compromised? 
* What requirements for maintenance and support? 
* What requirements for regular/planned updates to the live system/software? 
* What requirements for emergency updates, eg security fixes? 
* What requirements for backup and restore of data, systems? 
* What are the requirements for user/technical/support/maintenance documentation? * What are the requirements for training of users and/or support personnel? 
* How will we test and verify the requirements are met?

---
### 5
##### Mustard

Mustard is a product development process loosely based on SPICE, using a custom tool called Mustard. The goals of the process are to improve project planning and management by doing the following: 

* Track requirements. 
* Document architecture/design. 
* Track large-scale work items. All of the above are stored in text files stored in version control, and visualised using the Mustard tool. 

This forms the basis of a development process where: 
* The master branch in version control shows the state that has been agreed upon with the customer.
* Changes to requirements are made explicitly, by merging them in from another branch to master, after the customer (and other relevant parties) agree to them.

__Roles__

In this process there are several roles. In this idealised description we pretend the roles are always played by different people. 
* The customer is the source of all requirements and money. 
* The architect gathers requirements from the customer, and produces an architecture: descriptions of components and interfaces, and a list of largescale work items for implementing the system. 
* As part of the architect’s requirements analysis, verification criteria are developed for all requirements, and the architect may work with developers to plan how to verify the components of the architecture. 
* The project manager, together with the development team, breaks down the work items into smaller tasks, estimates the work to be done in collaboration with the developers, arranges work on a timeline, and assigns work to specific individuals. They also negotiate changes to the requirements or design with the architect and customer. 
* Developers produce the system by doing the work planned by the architect and project manager. They plan the work in detail, and produce estimates for the project manager.

Checklist for customer role The customer is expected to: 
* Explain the problems they want solved or the product they want built. 
* Answer questions 
* Test deliveries for acceptance. 
* Pay their bills.

Checklist for architect role The project architect has the responsibility to: 
* Understand what the customer wants and needs from the project. 
* Encode this understanding in a Mustard document, as a set of well-defined requirements. – The customer may provide a non-functional requirement, which the architect keeps as a top-level requirement, and splits into mechanically verifiable requirements. 
* Write up verification criteria for all requirements, explaining how to determine if the requirement has been met. 
* Design a way to achieve that, and encode that in Mustard as well: high-level architecture, major components, their interactions, and the internal architectures of the major components, and downwards through the abstraction stack down to components that can be implemented without further design. 
* Do any research and experimentation needed to make sure the design is a good one. 
* Plan a series of implementation steps for implementing the design.
* Understand the current state of the implementation, and all of its known problems, and any change requests from users, customers, and Codethink, and adjust the design and work items accordingly. 
* Monitor and measure project progress, together with the project manager, and guide the project to meet milestone deadlines. 
* Choose components that have acceptable licenses to fulfil the license requirements set by the customer, without violating any of the relevant licenses. The project architect need not do everything alone: delegation is allowed and encouraged. It is the project architect’s responsibility to ensure the delegated parts are done and done well.

Checklist for project manager role The project manager has the responsibility to: 
* Support the sales process. – Ensure the project is well understood, well-defined, and clearly scoped. – Ensure the project is well understood by the architect and engineers from the client’s or sponsor’s perspective. – Manage changes in the project purpose and communicate them clearly to engineering. 
* Discuss priorities with the customer to understand what should be delivered and when. – Document decisions, make sure all stakeholders understand them and agree to them. 
* Work with the architect to ensure that the captured project requirements meet the customer’s priorities and goals. 
* With the architecture team, plan what needs to be done for the milestones, and estimate the needed work for doing that. 
* With the engineering team, refine those estimates and ensure that everything necessary has been planned to a level of details which can be supported. – Some of this can be had from the work items produced by the architect in the Mustard document. 
* Make sure we have what we need to achieve the milestones (people, machines, time, knowledge), and negotiate with relevant parties if not. 
* Analyse risks and discuss them with customer and Codethink management to prepare strategies for handling them. 
* Keep track of what everyone is doing, and make sure they are making progress at a good pace, don’t get blocked on anything, and are doing the right thing.
* Keep track of overall progress towards milestones, and watch out for the schedule slipping, and deal with problems when they happen. 
* Ensure a smooth, complete (tested and documented) and timely delivery during the project, and/or at the end of the project. 
* Look after project infrastructure. – Management reports. – Project documentation. – Project monitoring. – Project facilities. 
* Ensure the the appropriate engineering process is used, is well defined, and understood by everyone. – Ensure the client is also informed about or involved in the engineering process, and understands it. 
* Ensure the client is understands the risks of the project, its progress, and any current issues. 
* Maintain the quality of, and improve, the project infrastructure. 
* Improve the quality of the engineering.

Checklist for developer role The developers have the responsibility to: 
* Review the architect’s output for sanity, implementability, and other aspects. 
* Estimate the time needed to implement the parts of the project they will work on. 
* Implement the project. 
* Raise any problems they see with the project, the architecture design, or other parts of the project.

__Approximate process flow__ 

1. Customer wants a system to be developed. 
2. Architect gathers requirements by interviewing customer. 
   * architect writes up requirements in Mustard, and documents the verification criteria for each requirement 
   * architect reviews the requirements with the customer
architect plans an architecture to fulfil known requirements, also in Mustard, refining it in as much detail as necessary to know whether everything is clear, will work, and is implementable; this includes components, interfaces, verification criteria, and anything else necessary 
   * this usually leads to additional questions, leading to new requirements or changes to existing ones 
3. Customer signs off on the requirements as being correct and complete. 
   * this is tagged in the git repository
4. Architect refines the architecture, if needed, to produce a work plan. 
5. Architect produces the work items needed to implement the architecture. 
6. Architect, project manager, and developers estimate work to be done, by breaking work items into smaller parts, when needed, etc. 
7. If necessary, project manager and sales negotiate with customer to agree on the price, scope, and timeline for the project. 
8. Developers do the work. 
   * To facilitate this, developers break down the work items into ‘doable’ cards in the Kanban. The architect may need to help here. 
9. When (not if) there is a need to change requirements or architecture, the architect discusses the changes with the customer or developers, and prepares a change in Mustard in a new branch. 
   * the architect updates the requirements, architecture, components, interfaces, and work items as necessary 
10. The architect and project manager discuss the proposed branch, making estimates (perhaps with the developers) on the impact on the amount of work to be done, and the project manager prepares the corresponding changes to work schedule and project cost. 
11. Project manager discusses the changes with the customer, who either accepts or rejects them, or wants to have the plan for the changes amended. 
12. Once the customer accepts the changes, the architect merges the new branch to master, and creates a tag for the new state of the agreement with the customer. 
13. Repeat until done.

In rough graphical form:








The above graph is not authoritative.

Data model A project is represented in Mustard as a set of nodes, which are linked to each other in various ways. Each node has a kind: 
* project: Core information about the project as a whole. 
* requirement: Customer requirement on project. 
* component: A part of the system. 
* interface: An interface of a component. 
* integration-strategy: A way to describe how to combine sub-components into a coherent supercomponent. 
* verification-criterion: How do we know a requirement is met, or a component works? 
* work-item: Lumps of work needed to implement the project.
* tag: Arbitrary tags on other nodes. The following UML diagram shows the relationship between different kinds of nodes.

The data is expressed using YAML. Each node is an “object” consisting of some key/value pairs. Some constraints: 
* Every project SHOULD have a “project” node. 
* Every requirement SHOULD be verifiable, and must have one or more verification criteria to express how that happens. Verification criteria SHOULD be designed so that verification can be made automatic with sufficient effort. 
* By the time the architecture is finished, every requirement MUST be fully mapped. 
* Every project SHOULD have exactly one top-level component.
* Every component with sub-components SHOULD have an integration strategy. 
* Every integration strategy SHOULD have exactly one architecture parent. 
* Every large component SHOULD have one or more components that implement it. 
* Every component SHOULD have exactly one component parent. (excluding the top level component) 
* Every component SHOULD have either more components, or else a work item as a child. 
* Every component SHOULD have one or more verification criteria.

License management in projects Every project must manage the licenses in the components it includes to achieve several goals: 
* Follow licenses of all components. 
* Avoid including code under unwanted licenses in the end result. For more information, see the Codethink admin wiki. The list of licenses for each component, or each file in each component, known as the “bill of materials”, is stored with project documentation in a manner suitable for the project. Capturing the choice of licenses is done in the Mustard document using tags.

The aspects of good requirements Requirements are very hard to write well. Customers frequently get them very very wrong. It is the role of the architect (and project manager to some extent) to analyse the requirements captured from the customer and encode them in a way which makes them ‘good’. Good requirements have a few simple characteristics: 

1. Unitary (Cohesive): The requirement address one and only one thing.
2. Complete: The requirement is fully stated in one place with no missing information. 
3. Consistent: The requirement does not contradict any other requirement and is fully consistent with all authoritative external documentation

__VERIFICATION CRITERIA__

1.  Non-conjugated (Atomic): The requirement is atomic, i.e., it does not contain conjunctions. E.g., “The postal code field must validate American and Canadian postal codes” should be written as two separate requirements: (1) “The postal code field must validate American postal codes” and (2) “The postal code field must validate Canadian postal codes”.
2.  Traceable: The requirement meets all or part of a business need as stated by stakeholders and authoritatively documented.
3.  Current: The requirement has not been made obsolete by the passage of time.
4.  Unambiguous: The requirement is concisely stated without recourse to technical jargon, acronyms (unless defined elsewhere in the Requirements document), or other esoteric verbiage. It expresses objective facts, not subjective opinions. It is subject to one and only one interpretation. Vague subjects, adjectives, prepositions, verbs and subjective phrases are avoided. Negative statements and compound statements are avoided.
5.  Prioritised: Many requirements represent a stakeholder-defined characteristic the absence of which will result in a major or even fatal deficiency. Others represent features that may be implemented if time and budget permits. The requirement must specify a level of importance.
6.  Verifiable: The validity of the implementation of the requirement can be determined through basic possible methods. (The above was ‘borrowed’ from Wikipedia’s Requirement article: http://en. wikipedia.org/wiki/Requirement)

Every requirement and component in a Mustard SHOULD have verification criteria detailing how to tell if the requirement is met or the component is working. Interfaces can also have verification criteria to detail how to test that the interface is implemented correctly. While there are a multiplicity of ways to verify the behaviour of components; requirements can be verified (in general) in one of four common ways:
1. Analysis: Look at the Mustard – you can tell if the requirement is met. i.e. for parent requirements, do the child requirements cover all aspects of the parent requirement and are they themselves marked up with verification criteria? 
2. Inspection: Simply look at what has been done and decide if it meets the requirement. For example, a requirement that a project be implemented in Python can be verified by inspection at delivery time. 
3. Automation: Does the project pass tests defined to verify this requirement? These might be unit tests, black box tests, integration tests, scenario tests, system tests, etc. The tests must be defined elsewhere.

Observation: Think of this as human-based testing. The result of the project is simply observed (used, deployed, whatever) and then its external behaviour is observed to see if it meets the requirement.

Obviously the above is not 100% exhaustive. In each case the verification criterion should explain how and when verification should be done.

Glossary 
* component: a physical or software part of the system being developed – large component: a component with sub components. The sub components break down the functionality of the large component and as such, shows how they work and interact together in order to fill some or all of the requirements of the project 
* interface: a part of a component via which other components, or users, may interact with it 
* work item: a set of tasks to implement some part of the project 
* requirement: something the customer wants or needs the project to do for them

---
### 6
##### Kanban

Kanban is a way of working, not a specific tool. We call our tool “the kanban” in Codethink but its real name is ‘hobokan’. The Kanban approach originated in engineering manufacturing, not software development. We are using custom Codethink software to help us apply the Kanban approach, and have refined the software and our workflow over tens of projects. There is still lots of room for improvement. The broad principles of Kanban are 
1. letting work-in-progress build up is inefficient and wasteful
2. so work is broken down into ‘cards’ in ‘lanes’ denoting state, eg ‘to do’, ‘doing’, ‘done’.
3. limit the number of cards in each lane to increase throughput & efficiency Why this is important: the more things we are juggling at once, the less effective we are at doing any of them. Engineers understand the concept of ‘context switching’ in code - a key effect of Kanban is to reduce context switching for each member of the team, and for the team as a whole. So an engineer should not have too many cards to think about at any time, and nor should the project as a whole. An implication of this is that an untidy/overfull kanban board probably means the team/manager is struggling A further implication is that for a large team, it’s probably best to have separate kanban boards for sub-teams, limiting the active team on each so the view does not get too cluttered. Conversely it’s not ideal for an engineer to work solo for long periods of time, so it’s probably best to track solo work as part of a bigger team project if possible. Our current usage guidelines are as follows: 


__Boards__ 
* we create new boards on our internal hobokan instance kanban.codethink.co.uk by default 
* if we expect the customer’s staff to access the board directly, it’s probably best to create a separate hobokan instance. 
* it’s ok to create a new board for an existing project, to make a fresh start we’ve done this several times 
* do not delete lanes - this can crash the current system

__Buckets__ 
* buckets are collections of cards, for filtering and traceability 
* each Mustard work item should be created as a bucket 
* sometimes, buckets may be created for other aspects of task management, such as ‘Could-You-Just’.

__Cards__ 
* a card should normally contain a short summary of a task, verb first, eg ‘build rome in a day’ 
* the summary plus the card description should be enough information to allow the engineer to understand and begin the task 
* the result should be completed when the work is done, to assist with review of the task and of the project as a whole 
* where appropriate the description and/or result field should include link(s) to mustard, git commits etc. 
* summary+description+result should be enough to allow someone external to the project to understand the task and if appropriate trace through and examine the work 
* each card SHOULD be in a bucket where possible, to group cards up according to the justification for having them.

__Workflow__
* the default lane titles can be varied depending on the project 
* cards normally move from left to right, but can move back, eg if we find that something else needs to happen first

__MILESTONES__
* we define a ‘doable’ card as something which is expected to take a day or less 
* the aim is for cards that land in the ‘doing’ lane to be ‘doable’
* so normally we ‘break down’ or ‘card out’ a big task into smaller ones 
* when a card is finished it should move from ‘doing’ to ‘review’ and then to ‘done’ 
* some informal projects (eg sales demo) may choose not to have a ‘review’ step in which case cards can go straight to ‘done’
* A milestone is normally a short term target date for achieving a set of things 
* Cards can be associated with a milestone by engineers or by the manager 
* milestones stay visible until all associated tasks are ‘done’ and the date has passed 
* the further in future a milestone is, the less accurate its planning will be

__Management__ 
* broadly we should expect to see each engineer getting through at least one (doable) card each day 
* if an engineer is stuck on the same task for more than a day, the project manager should be checking why 
* if (remaining cards for a milestone) + (manager’s guess at unexpected cards) \>= (engineers \* working days) we need to re-plan, cut scope or do something else to fix the situation 
* the manager should review progress at least once per week, and re-plan to ensure that the milestones are realistic 
* the manager should also ensure that the board overall is tidy: – reduce clutter - limit number of cards per lane, per engineer etc – choose sensible colours – short clear names for buckets, milestones etc – archive dead cards FIXME: get Alex and Mike to review and comment on the above.

__Work Review__

Work review (particularly code review) should always happen on completion of a kanban card (or feature) that produced any reviewable content. Every component in a project should have at least 2 engineers assigned to review that module. Patches are always sent to the project mailing list, unless there is a need to have a reviewspecific mailing list. The aim should always be that reviews should happen within a day of the patch being sent to the mailing list. Note that review is not just for code (although it is primarily for code, and the majority of this chapter is directly related to reviewing for code in particular) and it also applies to documentation and indeed architecture. FIXME: The Kanban flow integration is very new, being used by Baserock to some extent, but needs review by Paul, Rob Taylor, Lars etc. The flow is as follows: 
1. The patch should be squashed into a set of sensible orthogonal patches on a feature branch like /. This may be 1 or more. Orthogonal in this case means that no two patches should touch the same area of the code. 
   * Update the commit message to explain your reasoning for the changes (e.g. if you had to try a few different things before your final version, note that in the commit) 
   * Your aim when tidying your patchset for review should be: – it should be to make it easy to review the changes. This can, for example, affect ordering of patches in a series. – when you git blame in the future to find out why a line is the way it is, you should be able to understand why from the commit message 
   * Patches should be rebased to be on top of master (or the relevant working branch) 
   * the branch with the patchset should be pushed to the server 
2. Send this patchset to the mailing list with a suitable covering latter, referencing the kanban card. The cover letter must contain 
   * The repository the branch is hosted at. 
   * The name of the branch the work was done in 
   * The sha1 sum of the head of the branch. This should be a commit, don’t tag feature branches.
   * The kanban card number, if applicable 
   * The branch that the patch is to land on (if not the master for the project) To use git send-email to send your patches through the Codethink SMTP server, edit ∼/.gitconfig to specify your account settings:

[sendemail] smtpencryption = tls smtpserver = mail.codethink.co.uk smtpuser = yourldapusername smtpserverport = 587 Prerequisites for Ubuntu/Mint:

sudo apt-get install git-email libauthen-sasl-perl sudo -H cpan Net::SMTP::SSL Once your commits are ready to be sent to the mailing list, run the following commands:

git format-patch --cover-letter -M origin/master -o outgoing/ edit outgoing/0000-* git send-email outgoing/* 
3. Move your Kanban card to the review lane, add ‘Author: Your name’ to the results field and deassign the card. 
4. The reviewer who picks up your card assigns it to themselves (but leaves the card in the review lane) and then will do the review. This should likely happen by replying inline to the mails and commenting. The reviewer should delete sections that are ok (and note this) and only reply to the sections that need comment. This is simply standard email etiquette. 
5. When the reviewer is finished, they should submit their verdict to both the mailing list (as a response to the patch series root email) and record it on the Kanban card, removing themselves from the assignee list. Then, depending on the project policy, either the patch is refused, approved, or needs further review. In the last case, the card is left for another reviewer to pick up, the other two cases are detailed below. 
6. If any changes need to be made, the reviewer will reassign the card to the original worker and put the card back to backlog. The author should then pick the card up, put it in doing, make the changes, update the patchset and push –force the patch branch. Repeat from step 3), adding ‘V2’, ‘V3’, etc as appropriate

__SIMPLE, CLEAN, CLEAR REVIEW COMMENTARY__

1. If approved, merge your feature branch to master (or the relevant working branch), then delete your feature branch, and move the relevant kanban kard from Review to Done. It is essential that when the card is in the Done lane, the assignees are the authors of the work and not the reviewers. This can be done by the reviewer or the original author, depending on the policy of the project in question
 * When merging a feature branch, use

git merge --no-ff --no-commit Then take the time to review the merge, and check that any test suites you have still run successfully, then finish off with a simple git commit 
* You can delete a branch on the server by:

git push --delete <remote name> <branch name>

Simple, clean, clear review commentary When you are reviewing anything, but particularly code, you should attempt to ensure that your commentary is clear, that your review is clean (does not inadvertently quote unneccessary content) and that you make it easy for the author to take your comments on board and work with you to improve the patches. There is a very simple way to finish a review. The system proposed involves responding to patch series with an overall +1, -1 type value. +1 means “I think you should merge”, -1 means “I veto this being merged”, +0 means “I have no reason to object to a merge but am not comfortable saying you should merge” and -0" means “I have reason to not want to allow the merge, but am not comfortable vetoing the merge entirely”. Some projects may require a +1 from one architect and at least one other engineer, others may be satisfied with a single +1 from any engineer, others may be satisfied with no -1 after a period of time. The policy will vary from project to project and there is no correct answer. Also, some projects may have engineers who are not comfortable with the four simple values above. Any value is acceptable (for example +0.25 for someone who is just starting out on a project to indicate a +1 but without confidence) and projects will find their way as time passes.

Things to consider when reviewing code (or other things) While the following is not exhaustive, this is a list of useful things to consider when performing a review. This is code-focussed but a lot of it applies to documentation or architecture review as well.
* Is the cover letter clear and understood? – Does it make sense – Does it need to happen – Is all the required data present. 
* Does the changed code pass tests? – Particularly on the reviewer’s system – If appropriate, on multiple architectures – If available for the project, evidence of passing CI would be good – Always test the result of merging, not the thing you are reviewing – Does it break any forward-building constraints on the project. For example, Baserock version X must be buildable with version X-1 
* Are the patches logically separated (did the author perform step 1 of the process above well). * Review the change for clarity 
* Review the change for correctness 
* Non-code needs to be reviewed just as much as code does 
* Is there a better way of implementing the change? 
* Are the tests good – are there enough and are they the right ones. – Give special attention to test code. Test suite failures can be either code errors or test suite errors. Test code MUST be clean, clear, simple, obviously correct. 
* Are the commit messages good. The commit messages form the primary part of tracing how/why change was written. If they’re poor it makes tracing through history that much harder. 
* Ensure documentation and implementation agree. It’s worth noting that documentation includes the project’s Mustard. 
* Do the patches introduce or enhance a smell? A smell is a hard-to-define “issue” with a codebase or document. Something which while it’s not necessarily obviously wrong, somehow doesn’t sit right with you. For example while a document might not be bad, it might have a bad smell in that the formalism doesn’t seem to be consistent, or perhaps the voice it is written in abruptly shifts causing confusion.

__WHO AND WHEN__

Everyone on a project can be involved in reviewing work. However typically a given component will have preferred reviewers. When a project is small, or tightly coupled then every engineer may be able to review any given piece of work. No engineer, no matter how new to a project, should consider themselves unable to review work. Engineers new to a project may not be comfortable giving a +1 but that does not prevent them from performing a review – they may learn something new. Reviewing work does not have to happen at fixed times, however experience shows us that engineers prefer to do work rather than review someone else’s work. As such it can benefit a project to have fixed points at which engineers’ priorities shift from generating work to reviewing work. For example, it might be considered suitable to review work directly after a standup, or perhaps directly after lunch. Both are points in the day when the engineer is already context-switching and as such there is little to no cost to switch into review mode rather than engineering mode.

---
### 8
__Standing up__

We do standups to keep the team aware of what everyone is doing, and to identify roadblocks. Doing them on IRC means we can 
* log the minutes 
* have remote participants 
* be in more than one standup at once (eg Project Manager) Standups should be short - approx 10 minutes. To make this happen attendees should have their minutes typed in advance, ready to cut and paste. Normally standups should be organised and run by the engineers, not the project manager. This is not to say that the project manager should not be present; indeed they should be there. Even projects involving one engineer working solo should create daily standup minutes. Obviously this is not ideal and we should normally aim to ensure that engineers are not working solo for long periods. In this case, engineers may be encouraged to simply email their standup notes to the internal project mailing list instead. To avoid wasting time, it is important for all participants to be prepared ahead of time, and to not wait long for people who’re present but not alert on IRC. Wake them up with whatever means, or start the standup without them. Otherwise a 10-minute standup may easily be preceded by a 15-minute wait for everyone to be be awake on IRC. Standups should be recorded in the project’s log. A good name for a standup file would be standup-YYYYMMDD.mdwn in the log directory. Don’t forget to give the standup a title and a date entry so that the log is kept in order. All engineers and managers associated with any given project should be capable of running a standup, logging the activity and pushing standup minutes to the project management wiki. 

__Performing a standup: Characters__
* The Host 
* The Engineers (Engineer 1, Engineer 2, Engineer 3) 
* The Absent Engineers (Engineer 4)

Notes This script shows an example IRC standup,  The format of the engineers’ minutes may vary but the minutes posted by everyone usually include the same things: done, doing, today/next, issues/points. The host drives the meeting, as follows: 
* the host pings on IRC a short while in advance, eg ‘standup in 17 minutes’ 
* engineers prepare their standup comments 
* at the start time, the host asks engineers to indicate their presence 
* the engineers participating in the meeting respond 
* the host reports the order in which the engineers have responded as the order for posting their minutes 
* engineers participating in the meeting post their minutes in the given order 
* the first engineer posts their name first, then their minutes, then the name of the next engineer (typically the first engineer’s report will be that of the host themselves), 
* everyone else posts their sentences, ending with the name of the next engineer, 
* the last person ends by indicating that they is finished and that the discussion may begin 
* the host drives the discussion by discussing the points raised in the minutes and anything that comes up during the discussion itself CRITICALLY the engineers should wait for the host to ask them to discuss any given point. There should never be more than one point being discussed simultaneously. Engineers may indicate a need to raise another discussion point by simply posting \_o/ to the channel (raising ones hand).

Keep it short Standups are supposed to be short. Avoid deep and long technical discussions. Instead, decide to discuss them after the standup and quickly agree a time, place and participants.

__AN EXAMPLE STANDUP__

Phrasing None of the phrases used in this script are set in stone. Some people use “meeting time, sounds off” to ask people to indicate their presence. Others prefer to phrase things in a different way.

Raising hands during the discussion A few emoticons that are commonly used to indicate someone has a point or issue to raise in the discussion phase of standups:

*o* = nothing to say *o/ = I have something to discuss / = Here! Here! Here! I have something urgent! It’s generally recommended to treat / like a regular *o/

<Host> It’s standup time everybody, please indicate your presence ... Host waits for people to say something ... 

<Engineer 3> hi 

<Engineer 1> here 

<Engineer 2> hello ... Host waits some more, Engineer 4 is not responding ... 

<Host> Is Engineer 4 working today? 

<Engineer 1> No, he’s off ill 

<Host> Ok. Order: Host, Engineer 3, Engineer 1, Engineer 2 

<Host> \#\# Lesley Engineeryface 

<Host> \* Done - S6712: Get some cake made \* Today - S6713: Eat some cake \#\# Jon Smith 

<Engineer 3> \* Done - S1234: Do this and that - S4321: Do that other thing that needed to be done \* Today - S5235: Debug this problem we’re having - S1235: Fix that bug in software X \* Points - Hardware is dysfunctional, might need replacing \#\# Flavia MacGrizzlie 

<Engineer 1> \* Done - S5444: Build a system to deploy to the hardware  S3311: Write some documentation for the customer  A couple of meetings to discuss the next steps Today - S4123: Write meeting report  S1111: Document API for software X 

<Engineer 2> \#\# Stewart Rod Done Nothing, had yesterday off Today: S5930: Test functionality Y in software X  Points:   I’m a bit short on tasks, can we do some planning? \# Discussion 

<Host> Ok, we’ll first discuss the points you’ve raised Engineer 3, what are the problems with the board? 

<Engineer 3> It randomly crashes, I’m suspecting damaged memory 

<Host> Can you email me a summary of the problem so that I can forward it to the customer to ask for a replacement? 

<Engineer 3> Sure! 

<Host> Engineer 2, unfortunately we have a tight schedule, so we cannot do planning today. Please check with the others about what you can do to help and we’ll do some planning tomorrow 

<Engineer 2> Ok, no problem 

<Host> Are there any other points to discuss?

<Engineer 2> o/ 

<Engineer 3> o/ 

<Host> Engineer 2, go ahead 

<Engineer 2> I’m getting a haircut around lunchtime, so I might be unavailable for about 1 1/2 hours 

<Host> Ok, that shouldn’t be a problem, just make sure nobody is waiting for you on something 

<Engineer 2> Will do

<Host> Engineer 3, your turn 

<Engineer 3> This only just came to my mind: if we send my hardware off to get a replacement, we only have a single board to work with. That will impact our productivity. Can we get some spares with the replacement perhaps to not have this bottleneck again in the future? 

<Host> I’ll create a card for the Portia McManager to ask for that. 

<Host> Anything else? ... Host waits 20-30 seconds ... 

<Host> If not, I suggest we end the standup in 5 ... Host waits 2 seconds ... 

<Host> 4 ... Host waits 2 seconds ... 

<Host> 3 ... Host waits 2 seconds ... 

<Host> 2 ... Host waits 2 seconds ... 

<Host> 1... Host waits 2 seconds ... 

<Host> Meeting ends ... A few moments/minutes later ...

<Host> Meeting minutes uploaded: http://url/to/the/minutes
 
---
### 9
__Project Management__

Project Manager Role and Responsibilities Codethink’s Project Manager aims to ensure the success of the project(s) he/she is managing. Success usually means 
* customer is satisfied 
* delivered results are acceptable vs budget, time and quality constraints 
* staff are not stressed/burned out 

The above usually requires ensuring that everyone knows what is happening, who is doing what, when things are required etc. Because people have faulty memories, the PM should ensure everything is written down. NB that does not mean PMs need to do all of the writing. Normally it is best for engineers to do the writing, and PM to review. The PM has both responsibility and authority for decisions taken on the project. On a day-to-day basis, this means asking questions of the architects/engineers/customers, and taking decisions based on the available information. Decisions should be clearly communicated, in writing. IRC or a short email to the list will usually be enough for internal decisions. Decisions directly impacting the customer should be documented via email, or within progress reports. Hard decisions or problems can and should be escalated to any of the Directors Paul, Stephen, Rob.

Project Startup Project startup involves the following major steps: 

FIXME: Incomplete, also a lot of this is just paraphrasing https://admin.codethink.co.uk/wiki/index.php/Proj at the moment. 
* Internal mailing list: ctxxx-something-memorable-internal@lists.codethink.co.uk 
* Customer facing mailing list: customer-project@lists.codethink.co.uk 
* Internal kanban at kanban.codethink.co.uk, or a new kanban instance if the customer will use it. 
* Mustard instance 
* Internal irc channel ctxxx 
* Customer-facing irc channel on freenode if required

Establishing project accounting

Establishing the project groups on the git server Using the ct-new-project tool available from the git server, run ct-new-project XXX pmname where XXX is the project code allocated by Stephen or Maria and pmname is the username of the project manager who will be running the project. Once that completes, you can add more people to the appropriate groups by use of ctgit group adduser ctXXX-role person where role is one of readers, writers or admins as appropriate and person is the user name on the git server of the engineer or additional PM.

Pushing the initial project admin wiki to the git server In your git workspace for ctXXX:

\$ git clone ssh://git@git.codethink.co.uk/ct014/ct-pm-wiki-template.git pm-wiki \$ cd pm-wiki ... do any edits you want before the initial push and commit them ... \$ git remote set-url origin ssh://git@git.codethink.co.uk/ctXXX/pm-wiki \$ ctgit create ctXXX/pm-wiki \$ git push -u origin master You can view the newly rendered project at: https://ctXXX.pm.codethink.co.uk/

Day-to-day PM Role FIXME: Incomplete In and among everything else, update the pm wiki for the project by editing markdown documents in the ctXXX/pm-wiki clone you have and then commit and push them to the server. The website will automatically be rendered from the content you push.

Risk Analysis FIXME: Incomplete When doing a risk analysis, you should start your first by copying the risk analysis template from the samples directory into your risks tree of your project management wiki. Give the analysis a name based on the milestone, or date, or some other identifying mark and then begin to work your way through it. For later risk analyses, you may copy the previous analysis in the risks tree if you do not believe that the details will have changed significantly. For each listed risk, determine the likelihood of it occurring and the likely impact should it occur. Then combine those and record an overall risk level along with notes of your assessment. Consider methods to mitigate against the risk causing problems to the project and record those also. Possible mitigation factors are noted as examples in the sample risk analysis document. Engineers can be a valuable source of input on risk analysis. Everyone on a project should act together to determine the level of risk and the ways to mitigate against them. In general risk analysis should be done at the start of any major portion of the project. If you have milestones, a risk analysis might be done at the start of each milestone. If your staffing on the project alters drastically, or the customer piles on many change requests, then another analysis might be called for.

Internal Project Reporting FIXME

Customer Reporting FIXME

---
### 10
__Laptop policies__

Installation layout guidelines 
1. Operating system choices You should probably be using Debian or Fedora. Ubuntu has become significantly more of a headache of recent. Try to avoid fashion statement or single-policy distributions like Mint or Arch. If anything, there are far fewer people inside Codethink who you can ask about problems you have. 
2. If your laptop has Windows installed, do not delete it. Windows can occationally be useful, especially for BIOS and firmware updates. Often Linux installers can shrink existing Windows partitions to make space. If it refuses, try to boot Windows fully first and cleanly shut it down. If it still refuses, you’ll have no option but to delete Windows, but at least retain the restore partition if you have one (normally a smaller partition of around 3GB or less.) 
3. Use LVM. It’s amazing how useful LVM is, even if you don’t think you have a need for it now. It has next to no performance penalty, so you might as well. 
4. Use device-mapper disc encryption on all partitions but /boot. This includes your swap partition. Choose a strong password which is not your usual one, and provide a copy to Stephen Jones for safe keeping (we may need to access something on your machine while you’re ill or away). Don’t bother wiping the disc unless there was something sensitive on it before. It’ll take an age. If you wish to use your usual password in addition, then simply use cryptsetup luksAddKey /path/to/device to add another passphrase to your disk. 
5. Don’t btrfs. Btrfs is not ready yet. Ext4 has been reported to have issues for some people in the case of power failures, but remains an acceptable filesystem. Otherwise, ext3 and XFS are good choices. XFS, ext3, and ext4 all allow making a filesystem larger while it is being used. XFS allows online defragmentation.

Suggested layout with Windows and recovery partition (order of Windows partitions may vary):

sda1 sda2 sda3 sda4 sda5

Windows boot Windows recovery Windows /boot, 2GB, ext3 device-mapper crypto partition (rest of space)

Inside the crypto partition, create an LVM logical group. In the group, create the following logical volumes:

lv0 lv1

swap (RAM size \* 1.5 is traditional, same as RAM size is OK) / ext4, ext3 or XFS. As large as you like, at least 64GB.

If you are going to be using virtual machines via KVM or similar on your laptop, it may be worth not allocating the whole logical volume group to your root partition. This way, you can create virtual discs for your VMs that have better performance than if they were stored on the file system. It also gives some future flexibility with other projects, and you can always grow your root file system if you need to. Some people favour a smaller root partition (maybe 20G) and then a large /home partition to allow for OS reinstallation without wiping /home. Other people find it more convenient to keep all the free space in as few filesystems as possible, to avoid wasting it.

Security considerations 
1. Do not set a root password. There is no need for a root password. Install sudo instead. Setting a root password means an attacker already has half the information they need to log in. In the Debian installer, if you leave root password empty, it sets up sudo for the user account it creates and disables the root password. 
2. Do set a screensaver and lock. 10 minutes is a good timeout. 
3. If you’re likely to be working outside the office frequently, set up the VPN. Email support for a VPN key set, and see the wiki for set up instructions.

Backups We have a file server for laptop backups.
* Backup your laptop (or other work computers) to a subdirectory of your home directory on fs1.ducie.codethink.co.uk. See the admin wiki for instructions. 
* Backup in cleartext. Your home directory is normally accessible only by yourself, so this is safe, but allows the company access to your work files if you’re not available. 
* We have no suggested backup program at this time. You can use a cronjob using rsync, for example.
