# Practical OpSec

(Based on a "Family OpSec Workshop" deck from Desmond (not his real name).)

# Introduction

## Objectives

Present an overview of the landscape of risks and protective practices across:

* Online Accounts & Passwords
* Browsers
* Internet / Websites / Email
* Phones / Tablets
* Computers
* Travel

...and also cover some "Advanced Paranoia".

## The Real Objectives

Okay, I was kidding; those aren't the objectives. These are the objectives:

* You all need to start using a password manager, and go rotate your old passwords on all your places
  * This is an ongoing process. You don't have to do it overnight, but it's something to start soon.
* You need to enable MFA on your key email accounts and your bank accounts
  * SMS MFA is better than nothing.

## The Real Objectives, Part II

From here on out, you'll:

* Always know your password to a site
* Only ever install software from a trusted app store
* Be aware of phishing emails
* Never give anyone your password to anything

And, best of all, you'll understand _why_.

## External References

Read this stuff to get more perspectives, ideas, and tools.

* <https://pack.resetthenet.org/>
* <https://www.privacytools.io/>
* <https://myshadow.org/increase-your-privacy>
* <https://decentsecurity.com>
* <https://www.eff.org/privacybadger>
* <https://cpj.org/safety-notes/>
* <https://www.phishing.org/what-is-phishing>

# Topics

* What's OpSec?
* Identity
* Threat Models
* General Advice
* Travel Advice
* Advanced Paranoia

## What's OpSec?

* OpSec is short for “Operational Security”
* Being secure in the things that you do
* Mostly security is about your personal identity and things tied to you
  * Not about hardcore cryptography or deep security topics
* Starts with the basics of how you do things everyday
* No one has perfect opsec

Let’s all be terrible together. All of today’s problems seem intractable at first. You’re not alone. We can work on them; I will help you; let’s make your opsec better one step at a time.

## Identity

![Diagram of "identity" linked to a bunch of things](images/what-is-identity.png)

* What _services_ am I registered on?
* What _identities_ of mine exist online?
* How are they _distributed_ across services I use?
* How are they _collected_? Or _shared_?
* How are they _stored_? How am _I_ storing them?
* How can I _protect_ them?
* How are they at _risk_?

## Threat Models

### Threat Modeling

Threat modeling is a way of organizing and prioritizing your various combinations of risks and defensive measures so you can make good decisions.

One good way to think of a threat model is "An _attacker_ with a _capability_ and an _objective".

### Threat Modeling: Examples

Examples of threats:

* A _Law Enforcement Officer_ with _backdoor access to your email_ who wants to _see if you are buying illegal drugs online_
* An _Organized Crime Group_ with _your personal information_ who wants to _open lines of credit in your name_
* A _Malicious Computer Program_ that can _hack your browser_ and wants to _show you ads to scam money from ad views_
* A _coworker_ who can _sneak into your office_ who wants to _snoop on your conversations with your boss_

#### Threat Modeling: Example: Ocean's Eleven

* A _ragtag group of eleven expert thieves, including a hacker, an acrobat, three con men, a pickpocket, three mechanics, and an explosives expert_, with _the schematics of your casino_ who want to _pull off the greatest heist of all time_

### Threat Modeling: Purpose

One purpose of threat modeling is to help you choose between different options based on which threats are either more likely or more damaging, such as in the question “Should I enable automatic updates?” where you must pick either Yes or No.
* “Automatic updates theoretically enable Apple/Google/LEOs to backdoor my phone/computer”
* “Automatic updates protect me against Organized Crime Groups who are trying to hack my browser”

(The correct answer is "Yes".)

### Threat Modeling: Make Good Trade-offs

The purpose of security measures is to mitigate threats.

The reality of security is that everything is a trade-off. To use any service or technology involves trusting someone or something, which is a risk. To not use a service or technology may incur risks as well.

Being more secure means doing some work, keeping track of secrets and thinking through your decisions. The amount and kind of trust you are willing to give, and the work you are capable of and willing to do should be inputs into your decision-making.

Being specific about which threats you are most concerned with, and how you can mitigate them, will help focus your efforts on realistic, achievable outcomes.

### Make Good Trade-offs

When deciding between “more safe” and “less safe”, a key question you need to answer is: "More safe from what?" More safe from one thing may be less safe from something else.

![Edward Snowden tweet about security trade-offs](images/snowden-tradeoffs-tweet.png)

<https://twitter.com/snowden/status/1165391070726950913?s=21>

### Threat Modeling: Good Hygiene

Securing your data and resources is about more than protecting you. Attackers may target you, your data, or your devices in order to achieve an objective that does not directly harm you, such as attack someone else, launder money or stolen credit cards, send spam emails, construct a false persona online, or send anonymous threats.

The multitude of possible threats will break down into a much shorter list of good practices you can adopt, and these good practices are like good hygiene. Good hygiene helps everyone; it doesn’t just help you.

*Lots of weird possible scams may use your identity without directly harming you.*

![Picture of a phone farming scam](images/phone-farming-scam.png)

### Threat Modeling: Breaches

Realistically, the greatest threat to your personal information is also the one you have the least amount of control over: *breaches*.

A “breach” is a data compromise that exposes data stored by a third party. Data breaches can be huge, potentially affecting hundreds of millions of people at once. This data can include all your personal information, credit history, passwords, email, online dating activity; *anything* stored on a remote system.

![Article summary of a "mega breach"](images/mega-breach.png)

Breaches happen because companies are *lazy*. Breaches are not your fault. You can limit your exposure to them, though.

Read more: <https://enterprise.verizon.com/resources/executivebriefs/2019-dbir-executive-brief.pdf>

A number of account security and other practices we’ll cover help to mitigate the effect of breaches on you. (Most notably, [HIBP](https://haveibeenpwned.com/) and using a password manager.)

### Threat Modeling: Squirrels

Not every attacker is a person with intent to harm. Even a [squirrel](https://cybersquirrel1.com/) could severely affect outcomes you care about, if that squirrel is in the wrong place at the wrong time. A lightning strike could destroy your data as quickly as any online attacker.

Some of the good hygiene practices you adopt can mitigate against these risks, too.

When you’re considering the details of each threat model, you want to be able to “zoom out” to see the big picture, to see how all your decisions could benefit you in combination with each other, so you can make the best combination of decisions.

### Threat Modeling: The InfoSec Spiral of Doom

![Spiral of Doom](images/infosec-spiral-of-doom.png)

* It is *always* possible to hypothesize a way in which an attacker could attack you.
* The more you know, the easier it is to *imagine* vulnerabilities.
* “What If” scenarios play out endlessly
  * <https://en.wikipedia.org/wiki/Evil_demon>
* Nothing is perfect
* The only guarantee is that the attack vector you obsess over will not be the one that gets you
* We still need to make *practical* decisions
  * Which are good *on average* and *in aggregate*
* Don’t get let your paranoia get on top of you – stay out of the Spiral of Doom

# General Advice

## Tier 1 Advice

This is the most crucial stuff. Definitely do this.

1. Enable Automatic Updates
2. Use a Password Manager
3. Don’t Re-use a Password
4. Stay on Top of your Account Security
5. Don’t get Phished
6. Use MFA with Key Accounts
7. Never Give Anyone Your Password
8. Only Install Trusted Applications

### Enable Automatic Updates

Software becomes more insecure as it grows older.

Modern software stacks, from the Operating System to an individual app, on computers, phones, and tablets (iPads), are complex, and have large teams of the most qualified people on the planet constantly evaluating new threats and risks, and applying better testing and tools to improve their software security every day. These people are idealistic and incredibly good at their jobs.

Keeping this stuff up-to-date on your own is real hard.

There is a counter-argument that the capability to automatically update software exposes that software to exploitation by the updating authority (Apple, Google, etc.) as well as Law Enforcement. This is theoretically true, but pragmatically, the greater threat is from all other parties (such as international organized crime).

Relying on centralized, for-profit institutions to keep software secure is like relying on the government to keep roads well-maintained. Neither is a perfect model, but we can’t achieve the same outcomes as individuals that these organizations can.

Threats from Law Enforcement will be covered later under Advanced Paranoia.

#### Threat Model: Without Automatic Updates

An _automated virus_ which can _exploit your out-of-date software with known vulnerabilities_ so it can _steal your data and hold it hostage, forcing you to pay for it_.

### Use a Password Manager

Password Managers (such as 1Password, LastPass, or Bitwarden) are encrypted personal databases which help you keep track of which passwords are in use for which sites/apps/services, and to generate new secure passwords that fit a given site’s password policy (letters, numbers, etc.).

This makes it easy to follow these rules:

* Never re-use a password (use unique passwords everywhere)
* Do not use a “common” password
  * <https://en.wikipedia.org/wiki/List_of_the_most_common_passwords>

Password Managers have different availability and features on different platforms. Some have apps for phones, some for desktop computers, some support keeping your encrypted password database in a cloud storage solution such as Google Drive. Some phones or browsers have built-in password managers.

> Specifically for So You Wanna Code students: It might be good for all of us to be on the same password maanger just so everyone can help each other. Andrew uses and recommends 1Password. If you have any questions about it or need help setting it up, he'll sort you out.

### Don't Reuse a Password

Don't reuse a password. This means don't use the same password on any two accounts.

Once an attacker gains access to a password for one site (such as Netflix), the attacker will then try that name/password combination across all other sites (such as Venmo or Wells Fargo).

Using a Password Manager will eventually fix this problem. Fixing this problem without using a Password Manager is basically impossible, because in 2020 we all have way too many accounts to memorize passwords for all of them.

This does mean going around and fixing all your old accounts where you may have re-used a password. 1Password will help you do this using its "Watchtower" auditing feature, which creates a to-do list of all your reused passwords.

#### Threat Model: Password Reuse

An _Organized Crime Group_ with _access to your password from HBO_ who wants to _try this same password against all your bank accounts_.

