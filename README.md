  # {myapi} template

Here's a worksheet you can use to think about your own API.

**How to use this**: As you walk through the sections, write down your own answers to each of the CLI or API calls. 

## {1} have a pitch

How do you describe what you do? If you have a unique title, how to you explain it to people? Here is your opportunity to refine a simple and repeatable pitch you will use all the time. Mine is:

```
$ myctl job list

Matt is a Developer Advocate.

Developer Advocates are technical community contributors key to accelerating project adoption through internal coordination & targeted external contribution.
```

Tips for you:
* **Put your best foot forward.** No one is asking what your employer wrote down as your job description. They're asking how you describe what you do. Be positive about the work you do best and be quick about explaining it. Your pitch should be crisp and to the point. You can always follow up after.

## {2} assess your skill

Now it’s time to share what I’m good at. Some interesting options for such an endpoint include what type of work is it, by org chart definition (Sales, Marketing, Engineering, Support, HR, Finance). What’s nice about org charts as a categorization is that it leads directly to what kind of job I should pursue. That’s an API that gives me more than information, it gives me direction.

Mine is (where `-p` is preference and `-l` is level of expertise):

```
$ myctl skill list --type=ENG  -p

SKILL                     TYPE   PREFERENCE
Build Automation          ENG    3
Product Mgmt              ENG    2
Dev Mgmt                  ENG    4
Traditional Operations    ENG    4
Cloud Native Ops          ENG    3
Ruby Developer            ENG    2
Go Developer              ENG    1

$ myctl skill list --type=ENG  -l

SKILL                     TYPE   SKILL LEVEL
Build Automation          ENG    5
Product Mgmt              ENG    7
Dev Mgmt                  ENG    7
Traditional Operations    ENG    6
Cloud Native Ops          ENG    4
Ruby Developer            ENG    5
Go Developer              ENG    4

$ myctl skill list --type=MKT  -l

SKILL              TYPE    SKILL LEVEL
PowerPointing      MKT      8
Podcasting         MKT      10
Blogging           MKT      10
Public Speaking    MKT      6
Community Mgmt     MKT      10
Product Mkting     MKT      7
Social Media       MKT      8
```

## {3} manage your work

Think about where people get in touch with you, how you prioritize work and how you manage expectations of that work.

### 3.1 get in touch

When I’m honest with myself and my coworkers, my reply times and preference direct users toward Twitter. I own that – I ask people to tweet me instead of email all the time and it’s changed the way I monitor communication.

```
$ myctl contact list --all

TYPE    PREFERENCE    REPLY TIME
email   2             3d
text    3             1m
tweet   1             30s
call    4             5d
```

### 3.2 show your work

Next we turn to talking about what work I do – I want to provide an API by which anyone can see what I’m working on. What I do by showing you and others this output is I give you the context to understand what interrupting my current work will do to other work. I love that democratization of context.

```
$ myctl work list -wip

REQUEST              ORDER    DELIVERY DATE
Create PPT           1        4/18
Define OSS Release   2        4/21
Test Automation      3        5/15
Write Blog Post      4        5/20
Re to Sales          5        5/21
Schedule Meeting     6        5/21
Create other PPT     7        5/29
```

Let’s say you do have work to ask of me. How do you ask it?

![PUT request](https://cloud.githubusercontent.com/assets/1744971/25110818/c4733144-239b-11e7-9479-1edc79607489.png)

You’ll see here that if you’re going to assign me work, I expect a lot of optional information before I consider it a valid request. I need context about the work, and I now require the urgency of that request to be explicitly stated. When I assume anything said “not urgent” is lower priority, I find myself having issues. So it’s now a requirement.
