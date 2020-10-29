# Rewarding the Roles using Bounties

* [Bounty definition](#bounty-definition)
  * [Title](#title)
  * [Scope](#scope)
  * [Deliverables](#deliverables)
  * [Bounty owner/gardener](#bounty-ownergardener)
  * [Size and Sizing](#size-and-sizing)
* [Who can create a new bounty](#who-can-create-a-new-bounty)
* [How to create a new bounty](#how-to-create-a-new-bounty)
* [Pair bounty](#pair-bounty)
* [Objecting bounties](#objecting-bounties)
* [Work on Bounty](#work-on-bounty)
  * [Gardener](#gardener)
  * [Worker](#worker)
  * [Reviewer](#reviewer)
* [Dealing with Scope Creep and/or getting stuck](#dealing-with-scope-creep-andor-getting-stuck)
* [Challenging bounties](#challenging-bounties)
* [Links](#links)


## Bounty definition

Bounty is a reward for completing a properly defined Action or Project. For simplicity, we will may call such Actions or Projects themselves a Bounties from now on.

Properly defined bounty must specify the following attributes

### Title

Succinct name for the bounty.

Example:
> Implement Basic Token Governance UI

### Scope

A list of specific things which should be done to deliver the bounty. These could be seen as requirements to verify/review the bounty against.

### Deliverables

Artifacts produced as the result of this bounty. Something that could be verified/reviewed. Some examples: updated code, deployment made, blog post published, public event conducted etc

### Bounty owner/gardener

The Person who is responsible for the bounty.

### Size and Sizing

Size of the bounty.

We use t-shirt sizes:

* size-XS: 200 DAI
* size-S: 350 DAI
* size-M: 550 DAI
* size-L: 900 DAI
* size-XL: 1400 DAI

We don't prescribe a method of sizing by time or complexity, but rather every-one should decide themselves how much they want to put in for a given t-shirt size. Workers should remain aware of **bounty value consumed**, an estimated percentage of how much of the planned effort they have put in already, so they can take emergency steps as described in section [Dealing with Scope Creep and/or getting stuck](#dealing-with-scope-creep-andor-getting-stuck).

The sizing process should involve as many knowledgeable eye-balls as possible. Use tools like [planning poker](https://en.wikipedia.org/wiki/Planning_poker) or chat-bots that support sizing.

## Who can create a new bounty


## How to create a new bounty

1. Create a Github issue with properly defined bounty description (see above) in an appropriate repository.
2. If the bounty spans across multiple repositories, consider splitting it in a smaller per-repo bounties if possible.
3. Submit proposal via the bounty form
4. Add the bounty to the [bounties board]()

## Pair bounty

If two people work on the bounty together, the payout increases by 1.5x.

## Objecting bounties

Any bounty can be objected by anyone through GitHub for 2 days after its creation. A valid objection should describe how the bounty is not helping the purpose or how the bounty is harming the Organization. The objector must ensure that their objection is clearly communicated to the bounty proposer and e.g. not misunderstood as a minor comment on the issue.

In the cases where objector and proposer are not able to come to an acceptable solution, the objection has to be solved as a tension.

If the tension was integrated successfully or if there weren’t any public objections, the bounty is considered approved.

## Expiration

All non-taken bounties older than 1 month (time of submission through bounty form), MUST be submitted to bounty form again and undergo a new round of objections (as defined in by this spec) before the work can be started on it.

## Work on Bounty

### Gardener

Gardener is the one who creates the bounty and is responsible for it's completion.

Gardener is expected to:

* find a Worker for the Bounty.
* help the Worker to understand the scope of the Bounty.
* find a Reviewer for the Bounty.
* ensure the Bounty doesn’t get stalled (see "Expiration" section).
* request the payout for the Bounty once it is done and reviewed (see "Payout" section below).

### Worker

Worker is the one who actually implements the Bounty.

Worker is expected to:

* create WIP Pull Request within 4 days from the start of the bounty (if applicable)
* actively work on the Bounty according to it's Scope, don't linger (see "Challenging bounties" section below)
* stay accountable by publishing WIP updates at least every 2 working days:
  * for coding bounties, the Worker is expected to push commits in WIP Pull Request.
  * for writeups, the Worker is expected to share a draft Hackmd document (or other meidum of his choice) he is working at.
* request a review once the work is done. Review is requested on Slack in a Circle's channel like this:
  > 🌴👀 Requesting review for **\<bounty title\>** \
  > Issue: \<link to the Bounty on Github\> \
  > Product: \<link to deliverable, e.g. PR or writeup\>

### Reviewer

Reviewer is the person who reviews the Bounty's deliverables.

Reviewer is expected to:

* do review in timely manner, don't linger (see "Challenging bounties" section below)
* ensure all the delivables are provided
* ensure all the Scope items are addressed
* for coding bounties:
  * make sure the code is compiling/building correctly
  * review the code for logical correctness, inefficiencies and style (TBD)
  * ensure unit tests are passing
  * ensure code coverage is not reduced
  * ensure integration tests are passing for the PR branch
* for public writeups
  * do fact check
  * check readability
  * correct grammar and punctuation
  * check social network preview e.g. twitter card (if applicable)
* forward all the issues found publicly to the Worker (e.g. as comments on Github)
* approve the PR once the review is complete successfuly (if applicable)

## Dealing with Scope Creep and/or getting stuck

A task can easily get out of hand in fast-moving projects:
- The worker finds that a task takes much longer than expected.
- The reviewer requests so many changes that the worker feels overloaded.
- The worker or rewiewer might find that a feature doesn't work without certain functionality, which was not sized into the bounty for the task.

To prevent frustration, dispute, and a feeling of "being exploited" the process of **bounty forking** should be used. Forking is the process of separting a part of requirements and deliverables from the task into a new task, with the objective to complete the remaining effort in short time. This has multiple advantages:
- the sprint is unblocked, and blockers can be discussed separately.
- workers are protected from self-exploitation.
- "bounty resizing" is discouraged.
- small feelings of success (bounty delivery + payout) are injected more regularly.

The worker should use the following estimates when delivering a bounty:
- start packing up and sending a first WIP pull request when 50% of bounty value consumed on task.
- asking for help or finding pair-programmer when 67% of bounty value consumed on task.
- notify the gardener and start forking when 80% of bounty value consumed on task.
- keep a buffer of at least 20% of bounty value for review efforts.


## Challenging bounties

Gardener/Worker/Reviewer roles may be taken over by other people in a certain situations (see below). Each takeover must be stated in written form in corresponding Github issue including new assignee and the reason for takeover.

### Challenging worker and reviewer

If worker or reviewer are not publishing any updates for the bounty for 2 working days, then anyone can challenge him and take over the worker role. Updates for worker role can be in any form, most notably: commits to WIP Pull Request, updates on product artifact (hackmd, presentation, diagram etc), review comments, updates in form of github comments or slack conversations.

### Challenging gardener
If gardener is not helping worker to find a reviewer or doesn't address worker's questions within 2 days, then anyone can challenge him and take over a gardener role on the bounty.

## Payout

Funds allocated for bounty are split between Gardener, Worker and Reviewer in a proportion defined by Gardener (can be negotiated).

It is Gardener's duty to request the payout once the bounty is completed and reviewed. Payout is requested on Discord like this:
  > 🌴💰 Requesting payout for **\<bounty title\>** \
  > Issue: \<link to the Bounty on Github\> \
  > Product: \<link to deliverable, e.g. PR or writeup\> \
  > gardener: \<@gardener\> \<gardener share\> \
  > worker: \<@worker\> \<worker share\> \
  > reviewer: \<@reviewer\> \<reviewer share\>

## Links

* [Bounty issue template](https://github.com/sushiswap/contribution-guidelines/blob/master/.github/ISSUE_TEMPLATE/bounty.md)
