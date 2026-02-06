# NECYPAA 36 Landing Page

> A single HTML file with more engineering in it than the committee has collective impulse control.

## What Is This

A single `index.html` file that took more engineering effort than the entire convention budget. It's a mobile-first landing page for a regional young people's convention, and it has:

- A dark gradient event hero card with zombie emojis because loading an 851KB flyer image was apparently too easy
- A button that says "Pre-Register" (it links to a website that also says "Pre-Register")
- A hotel booking link (because apparently we needed a whole card for one hyperlink)
- A calendar button with platform detection logic more complex than the event it's promoting
- A Zoom link with someone's face next to it (mysterious)
- A sticky bottom bar because we looked at what every billion-dollar app does and said "yeah we need that too, for our two buttons"

## Tech Stack

- **Framework:** None. Raw HTML like God intended.
- **CSS:** 532 lines of hand-crafted artisanal stylesheet, inline, because we don't believe in separation of concerns. We believe in separation of nothing. This file is a monolith and so is this committee.
- **JavaScript:** Vanilla. We wrote a full ICS calendar file generator from scratch instead of just linking a Google Form. We regret nothing.
- **Build Tools:** Opening the file in a browser.
- **CI/CD:** Texting the file to someone who has access to the hosting.
- **Testing:** "Does it look good on my phone?" — QA department (1 person, in bed, at 2am)

## Architecture

```
necysite/
├── index.html    ← the entire application. the whole thing. that's it.
├── neb1.png      ← someone's face. for the zoom link. don't ask questions
└── README.md     ← you are here. you are trapped. there is no escape
```

> `zp1.JPG` has been honorably discharged. Its 851KB of flyer image have been replaced by ~180 lines of CSS and two zombie emojis. The information density per byte ratio improved by approximately infinity percent.

## Features Nobody Asked For But We Built Anyway

### Event Hero Card
We replaced an 851KB flyer image with a hand-crafted dark gradient card featuring zombie emojis, a "Save the Date" pill badge, date/location rows with inline SVG icons, a three-column schedule grid, and radial gradient overlays for *atmosphere*. It weighs approximately 0KB because it's just HTML and CSS. We are unreasonable people.

### Anonymity-Safe Share Menu
The share button opens a scrollable dropdown with 10 platforms: WhatsApp, iMessage/SMS, Email, Telegram, FB Messenger, Signal, Discord, Snapchat, GroupMe, and Kik. No Twitter. No Facebook. No Instagram. Because this is AA and anonymity matters more than engagement metrics. Platforms with direct URL schemes (WhatsApp, SMS, Email, Telegram, Messenger) open natively. The rest copy the message to your clipboard with a toast that says "Copied — paste in [app name]" because we respect your privacy but we can't rewrite Snapchat's API.

### Platform-Aware Calendar Integration
The "Add to Calendar" button detects whether you're on iOS, Android, or desktop, and serves you the appropriate calendar format. This function is 52 lines long. The convention is one weekend.

### Pulse Glow Animation
The main CTA button literally pulses with a glowing aura on an infinite loop. Like a heartbeat. Like it's *alive*. Like it's *begging* you to pre-register.


## The Backstory

Connecticut has never been known for anything. We are the state you drive through to get somewhere that matters. The loading screen between New York and Boston. Our biggest cultural export is insurance paperwork. The last interesting thing to happen in Hartford was the Colt revolver in 1836.

So naturally, this is where we're throwing a four-day sober convention. In a Marriott. Over New Year's.

NECYPAA 36 is the first Northeast Conference of Young People in AA hosted in Hartford, and the first one to run four days instead of three — because three days of sober people doing the Macarena at 3am in formalwear wasn't enough. We needed a fourth day. For what? Nobody agreed. Probably karaoke.

We're also throwing a Zombie Prom with the Massachusetts committee as a unity event. Friday the 13th. Church basement. Thrift store suits. Fake blood. Two states' worth of sober people pretending they know how to dance. Someone will show up in a wig they bought that morning. Someone will refuse to participate and then be the loudest person there. $15 suggested contribution to dance with people who collectively owe more than that in library fines. Free if you're broke. We've all been broke.

This website exists because a flyer wasn't enough. Flyers are what normal organizations make. We are a committee that invented its own fake government positions and once seriously debated organ donation as a fundraising model. So instead of a JPEG we built a full webpage with calendar integration, a share button, and a CTA that pulses on an infinite loop because we do not know when to stop.

A freelance developer would charge maybe $200 to build this. We had an AI do it at 2am for $0. You are being asked to pay 7.5% of what a professional would have invoiced for this work to attend a zombie dance in a church basement. That is the value proposition. The button is still pulsing.

We don't know what we're doing. We never have. We keep showing up and somehow that keeps being enough.

## How to Run

```bash
open index.html
```

That's it. That's the deployment.

## How to Contribute

You don't. This is a dictatorship with a pulse-glowing button. But if you really want to help, join the group chat and survive 48 hours without someone trying to sell your organs or put you in an animal onesie.

## Performance

- **Lighthouse Score:** We've never checked and we're not going to start now
- **Load Time:** Instant, because it's one HTML file and one image
- **Bundle Size:** What bundle
- **Time to Interactive:** The page is interactive the moment it exists. There is no hydration. There is no virtual DOM. There is only `index.html`.

## Known Issues (Resolved Graveyard)

- ~~The calendar event was hardcoded to April 15, 2025.~~ Fixed. We finally read our own flyer.
- ~~The ICS file was missing `UID` and `DTSTAMP` fields~~ — technically a violation of RFC 5545 which means Outlook would've rejected it. We now generate both at runtime like professionals who definitely knew about RFC 5545 the whole time.
- ~~The schedule in the calendar said "Hype 6:30-7:30" which overlaps with "Meeting 7:00-8:00."~~ Fixed. It's 6:30-7:00. We can read a flyer now, apparently.
- ~~No meta description or Open Graph tags~~ — sharing this link on iMessage would've shown a blank preview with zero context. Now it shows the event title and description like a real website made by real adults.
- ~~No favicon~~ — Added a 🧟 emoji favicon via inline SVG data URI because we refuse to add unnecessary files to this project.
- ~~The Zoom avatar alt text just said "Join Meeting"~~ — screen readers deserve better than that.
- ~~851KB flyer image as the entire hero section~~ — Replaced with a CSS gradient card. The flyer has been relieved of duty. It served with honor.
- ~~Aggressive double-tap prevention~~ — Was calling `preventDefault()` on all rapid taps globally, potentially blocking legitimate interactions. Removed. You can double-tap freely now. Go wild.
- ~~Lightbox for a flyer that no longer exists~~ — Removed 60+ lines of lightbox CSS, HTML, and JS. Gone. Reduced to atoms.
- ~~Sticky bar had a useless "Flyer" button~~ — Replaced with a Hotel booking link because that's actually useful.
- ~~Page scrolled on smaller phones~~ — Rebuilt the entire layout with `100dvh` flex containers so everything fits on one screen. iPhone SE, tiny Androids, everything. No scrolling. You see everything the moment you open it.
- ~~Share button used Web Share API~~ — Replaced with a custom share menu restricted to anonymity-safe platforms only. 10 options, zero social media feeds. Because we're sober, not stupid.
- ~~CSS `100dvh` fallback was backwards~~ — `height: 100dvh` was declared *before* the `100vh` fallback, which means the fallback always won because CSS cascades. Swapped the order. This is the kind of bug you ship at 2am.
- ~~Hero card `overflow: hidden` clipped the share menu~~ — The share menu dropdown lives inside the hero card which had `overflow: hidden`. On smaller screens the menu got cut off at the card edge. Changed to `overflow: visible`. The pseudo-element gradients stay contained because they use `inset: 0`.
- ~~Signal icon was Telegram's icon~~ — Copy-pasted the wrong SVG path. Signal had a paper plane. Signal is not Telegram. Fixed.
- ~~Clipboard share links weren't keyboard-accessible~~ — The `<a>` tags for Signal, Discord, Snapchat, GroupMe, and Kik had no `href`, making them invisible to keyboard navigation. Added `href="#"` with `preventDefault()` in JS.
- ~~Dead CSS variables~~ — `--teal-hover` and `--indigo-hover` were declared but never used. Removed.

### Still Standing
- The Zoom meeting ID is just... right there in the HTML. In the open. Anyone can see it. Is that fine? Probably fine.
- On desktop the sticky bar disappears, which means desktop users only get *one* way to pre-register instead of *three*. Tragic.
- The hotel reservation link is a Marriott deep link that could expire at any moment. We live on the edge.
- `neb1.png` is 492KB for a 42×42px avatar now. Still absurd. We'll deal with it when we feel like it.
- The share menu has 10 platforms in it. For a landing page with two buttons. We have a 10-item share menu.

## FAQ

**Q: Why is this a single HTML file?**
A: Because we replaced hard drugs with overengineering and this is what recovery looks like.

**Q: Is the committee chat really that active?**
A: Someone left their phone for two hours and came back to a debate about whether meth counts as pre-workout, a fascism election, and a sober haunted house pitch where someone dresses as a resentment and screams "I'M YOUR NUMBER ONE OFFENDER" at you in the dark. So yes.

**Q: Why is the README like this?**
A: This place is a prison.

**Q: Should I pre-register?**
A: The button is pulsing. It will not stop pulsing. You know what you have to do.

## License

No license. This code is free like the coffee at the convention. Take it. We don't care. We're too busy arguing about whether shipping containers are just jungle rooms that haven't been born yet.

---

*Built with love, sleep deprivation, energy drinks, and the kind of chaotic devotion that only exists between people who got sober together and refuse act like my actual fucking family.*
