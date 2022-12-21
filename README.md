# Red-Team-Preparation

How Do I Prepare to Join a Red Team?

An overview of the skills which make you valuable.



What Exactly Does a Red Team Do?

On a Red Team, you’ll be emulating, simulating, or otherwise pretending to be a particular, set of, or your own theoretical threat actor(s). Activities are usually encapsulated into individual operations or exercises. The purpose of these are to train the Blue Team, which consists of groups or individuals who are responsible for various defense capabilities. This can be anything from application security to active defense.

There are as many kinds of Red Teams as there are organizations with Red Teams. Some are what we’d call a “half”, where a single person is only partly responsible for Red Team functions. Some do other offensive security tasks like penetration testing or vulnerability assessment. Some have numerous members with very well-defined roles, all distinct from other offensive security tasks in order to focus on detection and response.

As long as the capability of a Red Team is well matched to the capability of the organization’s Blue Team, you’re on track.
On the Attack Lifecycle

It’s important, first and foremost, to understand the attack lifecycle or cyber kill chain or just kill chain. This outline defines all the steps of how an attack might be carried out by a threat actor. Most of the Red Team operational work is executing on these steps, which are in service of a particular goal, often called “actions on the objective.”

Threat actors are usually classified by their motivations, such as making money with stolen payment data. All of the steps in an attack will eventually lead to this, and knowing this helps the Blue Team organize their defenses.

If you’d like to know more about the steps, called tactics (or tools), techniques, and procedures, review the MITRE ATT&CK Framework.
What Role Should I Choose?

There’s a spectrum of skills Red Teams can use to best organize their capabilities into roles, and no one right way to do this. It helps to logically group two different types of activities though, engineering and operations. This is a common strategy for all types of teams in technology.

Simply: Engineers build the tools, operators deploy and execute them.

Many teams create specific, often temporary, operator roles for individual operations. For example, one member can be sending out phishing emails, while the other is acting on incoming remote access as targets begin to execute the Red Team’s payloads.

How a Red Team distributes these skills across one or more team members is entirely a matter of taste, aptitude, training, and available talent. You should pick several of these to get up to speed on so you can be flexible when attempting to join small teams.
What Skills Should I Work On?

Easy! Pick relevant skills you find interesting, and that make you a better technical communicator. Try these on, and see how they fit…
A selection of Red Team skills, and their role relevance
Offensive Mindset

As a career in security grows, all of the ways the world is duct tape and bubblegum begin to reveal themselves. Most systems are designed only well enough to achieve the task for which they were designed. It will be your job to pick those systems apart, and poke at the gooey innards.

This is the skill which will get you through all of the tough problems.

Example: You have to open a lock for an operation, you use two hair pins instead of a key.

Skill Building: CTFs, wargames, or pen testing labs are a great way to exercise offensive mindset, such as PicoCTF, and Hack The Box. Look for groups doing live CTFs at local conferences. The real key here is to always question assumptions.
Penetration Testing

Under the banner of penetration testing lies a lot of what might be classified as vulnerability assessment, but for the sake of argument, let’s just describe it here as the process of hunting for known vulnerabilities on networks or hosts.

This responsibility may not lay primarily with the Red Team, but you’ll want to stay sharp on this topic. Taking opportunities to leverage a known vulnerability during an operation is good for training Blue Team incident response analysts.

Example: You scan for unauthenticated MongoDB instances for data which may be worthy of exfiltration.

Skill Building: Familiarize yourself with the existing automated vulnerability scanners available like Nessus or OpenVAS. Like offensive mindset, CTFs, wargames, or pen testing labs are also great for this.
Vulnerability Research

It’s not necessary, but often very helpful to have the ability to develop your own 0-days as a Red Team. These are unknown vulnerabilities in either third-party or in-house developed applications.

There is a lot of overlap here with penetration testing, but the key is that research time dedicated specifically for developing 0-days is expensive and may not improve your Blue Team from the perspective of detection and response enough to justify. Set your expectations accordingly.

Example: Your team finds that a particular in-house application would be very risky if exploited. Following this, you find an exploitable vulnerability, and write a proof of concept tool your team can leverage to achieve code execution.

Skill Building: Chew on one of the many blogs or books on application exploitation, such as Security Sift’s Introduction to Windows Exploit Development, or the Web Application Hacker’s Handbook by Dafydd Stuttard and Marcus Pinto.
Development

It cannot be stressed enough that the linchpin of a successful Red Team is in its development capabilities. The best Red Teams will be nearly indistinguishable from standard application product teams; adapting formal development methods, using version control and releases, setting roadmaps, using CI/CD techniques, writing tests. Most Red Teams do devops natively, if unknowingly.

You’ll find yourself writing code in numerous languages depending on the platforms and adversarial techniques you intend to use, and having to collaborate with others on that code.

Critical to this is understanding the minimum viable product (MVP). Get it working, get it documented. If it becomes a go-to tool in the future, spend more cycles on it later.

Example: Your operators need a way to search a host for sensitive files. To support them, you write a Python script that lists all potential private keys and spreadsheets.

Skill Building: There’s a vast array of methods for improving here, but there are also numerous books which focus on offensive use of programming languages, such as Black Hat Python: Python Programming for Hackers and Pentesters by Justin Seitz.
Infrastructure

Red Team operators can work best when the busy work of setting up and maintaining the command and control (C2) infrastructure they operate on is someone else’s problem.

This is where a reliable and repeatable infrastructure strategy shines. Using infrastructure automation and configuration management tools, you can iterate quickly and spend less time in the terminal.

Infrastructure-as-code should be an aspiration for Red Teams to limit the everyday tweaking and frustration of literally having to manage an entire infrastructure for a small team.

Example: Your reverse proxy should be configured to defend against nosy analysts, and this capability should be deployed automatically from a repository or container.

Skill Building: Try setting up a cloud-based network lab using free-tier AWS resources, and the automation tools they offer such as CloudFormation and OpsWorks. Review the Red Team Infrastructure Wiki by @bluscreenofjeff for processes optimized for Red Teams.
Networks and Systems

In the design and crafting of infrastructure, is all of the nuance required to maintain functional hosts and networks — reliably and securely. I can’t stress the securely enough.

These systems can be public or private cloud hosted, virtual machines on ESXi, physically or virtually networked. They’ll often be hacked together in weird ways to assure the attacker techniques you’re emulating work without much effort. You’ll need to be very comfortable with the command line.

Any familiarity with these topics will help you operate in the target environment as well.

Example: A typical first step once access to a target host is gained is to list running processes.

Skill Building: These skills can be augmented with the usual suspects, but practice things like setting up reverse proxies, firewalls, authentication. Try to set up a post-exploitation framework like Empire in your lab, and explore all of its features.
Reverse Engineering

Reverse engineering is process of analyzing something with the intent of figuring out how it works.

Reversing can be done to analyze in-the-wild malware (malware analysis), with the intent to emulate its functions, and the threat actors using it. You can find malware samples in various places to practice on, but be very careful in doing so.

You can also use this process understand how potentially exploitable applications function, with the intent of eventually finding an exploit for them.

Example: Say you want to execute code using unusual COM objects. You need to analyze, in bulk, Windows COM objects to find the ones which import the functions necessary to start processes.

Skill Building: You may get a kick out of learning how to use IDA Pro with The IDA Pro Book by Chris Eagle, or following @malwareunicorn’s excellent Reverse Engineering Malware 101.
Social Engineering

Since what we call initial access for threat actors so often involves schemes like phishing emails, it’s important to understand how people might be susceptible to a bamboozle.

There’s various applications of such social engineering in offensive work, like USB device drops and watering-hole attacks.

Using social engineering as part of actual Red Team operations with the intent of tricking unsuspecting users is also well within the realm of Red Team. Tricking people is optional though. You can skip the phishing part and use seeded access, or intentionally creating remote access to a specific host or hosts, to make your operations less time consuming.

This function is distinct from phishing assessments which are for end-user awareness measurement and training.

Example: You’re tasked by the intel team to create a convincing whale phish to test against your C-suite.

Skill Building: Check your spam folder for phishing samples, and try out @HackingDave’s Social Engineer Toolkit for the nuts and bolts.
Physical Security

Some Red Teams include physical within their scope of operations. This can be as simple as hiding a drop box somewhere on site, to a full on covert entry scenario. Don’t expect every organization to be excited about this. It’s a fun topic, but often not a risk organizations are interested in mitigating.

Example: Network jacks in the headquarters lobby are on the internal LAN, and you need to demonstrate an attack against them.

Skill Building: Lockpicking, security system bypassing, badge hacking, and confidence games are all fair game here.
Threat Intelligence

Red Teaming requires multiple sources of threat actor tactical intelligence. This feeds the threat actor emulation portion of your tactical bucket. You can add new capability to your tools and documentation, with a reference, like a blog post, to that threat actor.

Threat intelligence also ascertains the motives of threat actors, and the patterns of their behavior in a process known as threat actor tracking. Red Teams use this information to design the story or narrative behind their operations.

Threat intelligence can also come from more benign sources, like security researchers. Their work can not only be predictive of threat actor tactics, it can even influence them.

Example: You know a particular threat actor sends malicious macro-enabled Office documents which leverage WMI subscriptions while setting persistence, so you design a proof-of-concept to replicate that behavior.

Skill Building: Review lots of blog posts and reports about malware analysis and actor tracking.
Detection and Response

The Blue Team will be your primary customer and opponent. They are the experts in detection of events, and execution of incident response. Your Red Team will need to be able to predict the capabilities the Blue Team, and use that knowledge to operate in the environment.

Learning about defending an organization will make you more valuable to a Red Team than other offensive security practitioners.

Example: You know your Blue Team monitors Powershell-related logs, so when you design tools leveraging Poweshell, you have them invoke version 2 instead of the most recent version.

Skill Building: Set up Security Onion on your lab network, and host based monitoring tools like sysmon or auditd. Keep an eye on them while operating in your lab. You’ll start to see like a Blue Team. Review blogs about threat actor tactics that describe methods which are effective in prevention and detection.
Technical Writing

Communicating highly technical issues clearly and with a broad audience in mind is challenging, but the importance cannot be overstated.

Technical writing can be vital to delivering valuable reports to clients as a consultant.

Equally important is documenting the tools and processes your Red Team uses to operate. There’s so much information with regards to capabilities and the various functions, the only way to maintain situational awareness is to have complete and consistently updated documentation.

In planning, most teams will want to develop operation proposals, written to detail the risks and rewards of a particular Red Team operation for approval of management.

Be able to know who your customers are, put yourself in their position, and write so that audience can understand the story your team wants to tell. Avoid being verbose for the purpose of being verbose — save your team and your customer’s time with concise writing.

Example: For your operation proposals, you need to reassure stakeholders that you can operate safely and responsibly while executing, and describing what the outcomes should be.

Skill Building: This is a tricky muscle to exercise. You may want to consider a formal course on technical writing, like the one offered by Coursera. Write a blog post on a topic you’re familiar with, and ask some experienced acquaintances to review it for you.
Training and Debriefing

All of the above skills build upon your ability to deliver on the educational goals of the Red Team.

You should be able to use a Red Team operational report to deliver a short presentation (the debrief) on the narrative (description of the chain of events) to the primary Blue Team stakeholders. Doing this clearly, consistently, and without harsh judgment is how the Red Team shows its value to the larger organization, and maintains a positive relationship with the Blue Team.

You should also be able to encapsulate Red Team knowledge, and deliver it in an individual or group training environment. You share what you know about the subject, and people can ask questions in real-time instead of trying to learn through inference in your operations.

Example: Your Blue Team is having trouble analyzing tactics leveraging alternate data streams in Windows. You’d want to look at what you know about ADS, collect some threat actor tactics, and build that into a short deck you can use to present to a group of analysts.

Skill Building: Practice explaining a topic you’re familiar with, like in a blog post or to friends with an interest in security. If your public speaking needs tweaking, everyone recommends Toastmasters, or you can submit a talk to a small local conference.
