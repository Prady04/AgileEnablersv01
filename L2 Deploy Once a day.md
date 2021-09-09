**Moving to Deploy once a day** 

## Keys to success 
## -----------------
* 
* Accelerate metrics; frequency, lead time, change failure rate and MTTR.
*  A fully automated CI/CD pipeline that can reliably deploy changes to
 multiple environments and the ability to quickly revert.
* Observability and alerting capabilities that allows detection when changes have caused negative impact.
* Culture that provides the team with the ability to
self-serve their deploys, the confidence to understand what to do if
things go wrong and, for non-technical team members, how to know
what’s changing.
* A strong buy-in from the whole team around working in small batch
sizes and deployimg features in a continuous fashion.


**Moving to Deploy once a day**
### Measurements 
# -----------------------------------
* Change failure, broken down by different code bases and flags 
* Quick access to outliers related to your failure rate and deploys
* The ability to quickly drill into the original source of measure (e.g.,
  Datadog)
* Teams/Slack-based notifications at the team and individual level on failure
* Deployment locking
* An automated system that allows smoke tests to stop production
promotions
**Moving to Deploy once a day**
## Development Practices for One Deploy a Week

** repeatable deployment process that doesn’t take longer than X (X<6) hours for an individual to perform. **

## Practices:
### Source control
*  developer branches for new changes

*  “release” branch that is always in a deployable state.

* Developer branches are merged into this branch

* Code reviews
* mechanism for accepting or rejecting changes into release branch

* using pull requests to review new changes, and

* well-defined process for merging these changes

### Testing

* at least 50% unit test coverage

* unit tests are at most 20% flakey
* unit tests run on every code commit

### Deployments
*  mostly automated continuous delivery pipeline in place that can build a “release” from our “release” branch

* we have a well-defined production environment and a strong understanding of how changes affect this environment

### Observability
* we have basic observability in place, such that we can judge the
success of our changes to production.

## Communications for One Deploy a Week


### Developer communication
* well-defined day / time for when changes need to be integrated into  release branch such that they will ship with the weekly deploy.

*  well-defined window of when the changes will be live in
production.
* well-defined understanding of who is responsible for determining if a deploy is successful. 

* This can be a build engineer,
automated alerts, or the developers who made the changes. Theimportant thing is to know who makes the call to rollback or keep
our changes live.

### Intra-team communication
* way for Product Owners, Engineering Managers, and
developers to know when a deploy has completed and what was
included.

### Issue tracking
* issue tracker
* Real-time chat
* mechanism for developers and those who own the
deploy to have real-time communication; e.g., via Slack/teams.
### Visibility
* a way to know, even if it’s cumbersome, what code and
high-level tasks have been deployed.
### Knowledge sharing
* we have some form of documentation that describes how our
deployment process works, who owns it and who is a point of
contact to find out more. 

## Culture 
### Developers
* Developers need to understand and buy into the team's dev loop.

* They need to be trying to make smaller changes and target their
changes to deploy windows.

* They need to agree that a break in the
release branch trumps other concerns and will be fixed immediately.

### Mechanisms to achieve:
* Weekly or bi-weekly sprint planning can help set the size of tasks
and create a team agreement on how tasks will fit into this window.

* Automated CI against the release branch and team-wide visibility
into those results to help the team keep the release buildable.

* Maintaining a “disturbed” role on a team where it’s clear whose job it
is to keep the release branch buildable.

### Engineering Managers
* Engineering Managers need to shift from putting in processes that
help the team play defense (e.g., “How can we add processes to slow
down and make sure our 3-month release has no bugs and is “safe” to
ship?), to 

* putting in processes that help the team play offense (e.g.,
“How do we keep the code flowing? What can we do to ship smaller
changes and quick fixes if we make a mistake?”).

### Mechanisms to achieve:
* Put in place processes that facilitate communication such as
recurring planning meetings, code review and weekly demos.

* Commit to dedicating engineering time to keep the release branch
builds passing. 
* Keeping the code flowing also means paying into this new system. 

* When the team identifies a bottleneck, the
Manager should be able to allow the team to remove it (e.g., fix CI tests that have a flakeyness higher than 20%).

### Upper Management
Before frequent deploys, upper management could evaluate the team
on the release boundaries.


### Mechanisms to achieve:
* Surface the Accelerate metrics for our projects and make them
available, with context, to our management.

* Surface our uptime or equivalent for our applications.

* Make sure to provide our management team with the same high-level information about large chunks of functionality that are shipping.

* If you are an upper management person, understand that change takes time and be firm
about holding your teams accountable for high-level goals but flexible about how they achieve them. ** Trust, but verify. **