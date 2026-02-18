# NECYPAA 36 Landing Page

> A single HTML file that took more engineering than the four-day convention it's advertising.

## What Is This

A single `index.html` file that took more engineering effort than the entire convention budget. Nobody asked for this. Not the committee. Not the advisory. Not the guy who runs the website we're linking to (Update: I have since been elected Website Chair, a title with comedic potential I certainly won't abuse in future READMEs). I opened a text editor at 2am because I couldn't sleep and now we have a full web application with platform-aware calendar integration and a share menu that respects the Eleventh Tradition. The committee found out about this project when I dropped it in the Business chat with a 3-paragraph justification nobody requested, because I don't believe in half measures and I definitely don't believe in asking permission.

It's a mobile-first landing page for a regional young people's convention, and it has:

- A cosmic neon hero card with zero images because even CSS gradients were too much commitment for us
- A button that says "Pre-Register" (it links to a website that also says "Pre-Register")
- A hotel booking link (because apparently we needed a whole card for one hyperlink)
- A calendar button with platform detection logic more complex than the 4-day convention schedule
- A sticky bottom bar because we looked at what every billion-dollar app does and said "yeah we need that too, for our two buttons"
- A share button that opens a bottom sheet with 10 platforms because we couldn't decide which ones to cut and now it's a feature

## Tech Stack

- **Framework:** None. Raw HTML like God intended.
- **CSS:** 580+ lines of hand-crafted artisanal stylesheet, inline, because we don't believe in separation of concerns. We believe in separation of nothing. This file is a monolith and so is this committee.
- **JavaScript:** Vanilla. We wrote a full ICS calendar file generator from scratch instead of just linking a Google Form. We regret nothing.
- **Images:** Zero. The entire visual experience is CSS gradients and one emoji. We have reached peak abstraction.
- **Build Tools:** Opening the file in a browser.
- **CI/CD:** Texting the file to someone who has access to the hosting.
- **Testing:** "Does it look good on my phone?" — QA department (1 person, in bed, at 2am)

## Architecture

```
necysite/
├── index.html    ← the entire application. 895 lines. one file. no regrets.
└── README.md     ← you are here. you are trapped. there is no escape.
```

> We deleted every image. We deleted the election link. We deleted the NEB section. The hero card is now five CSS gradients pretending to be a neon nightclub. The `neb1.png` avatar? Gone. The `zp1.JPG` flyer? Cremated. The `isa2-15.JPG` convention flyer? We looked at it once for color inspiration and then pretended it doesn't exist. Information density per byte is now technically infinite because there are zero bytes of image data being served. We are ascended.

## Features Nobody Asked For But We Built Anyway

### Cosmic Neon Hero Card
We replaced an 851KB flyer with approximately 847 lines of CSS featuring a five-stop deep space gradient (`#0d0221 → #150734 → #261447 → #1a0a3e → #0a1628`), four radial gradient light bursts in magenta and cyan, a neon magenta border with inset glow, text shadows that pulse with the power of a thousand suns, and a fireworks emoji that took 12 seconds to pick. It weighs 0KB. We are completely unhinged.

### Anonymity-Safe Share Menu
The share button lives in the actions grid now because it was floating in the hero card like a haunted artifact and breaking the visual flow. When you tap it, a bottom sheet slides up from the bottom of the screen with 10 platform options displayed as pill-shaped buttons: WhatsApp, iMessage/SMS, Email, Telegram, FB Messenger, Signal, Discord, Snapchat, GroupMe, and Kik. No Twitter. No Facebook. No Instagram. Because this is AA and anonymity matters more than engagement metrics. The bottom sheet has a deep purple gradient background with a neon magenta border and outer glow shadow — because even the share menu needs to match the vibe. Platforms with direct URL schemes open natively. The rest copy to clipboard with a toast. We wrote 50 lines of JavaScript to avoid using the native Web Share API because it includes Twitter and we have principles (that we discovered at 1:45am).

### Platform-Aware Calendar Integration
The "Add to Calendar" button detects whether you're on iOS, Android, or desktop, and serves you the appropriate calendar format. This function is 52 lines long. The convention is one weekend. The code-to-event ratio is approaching unity.

### Pulse Glow Animation
The main CTA button literally pulses with a glowing magenta aura on an infinite loop. Like a heartbeat. Like it's *alive*. Like it's *begging* you to pre-register. The button has not stopped pulsing since 2024. It will outlive us all.

## The Backstory

Connecticut has never been known for anything. We are the state you drive through to get somewhere that matters. The loading screen between New York and Boston. Our biggest cultural export is insurance paperwork. The last interesting thing to happen in Hartford was the Colt revolver in 1836.

So naturally, this is where we're throwing a **four-day** sober convention. In a Marriott. Over New Year's.

NECYPAA 36 is the first Northeast Conference of Young People in AA hosted in Hartford, and the first one to run four days instead of three — because three days of sober people doing the Macarena at 3am in formalwear wasn't enough. We needed a fourth day. For what? Nobody agreed. Probably karaoke. Or a spontaneous intervention. Or someone will suggest we all go to the Wadsworth Atheneum and look at paintings while hungover on adrenaline and fellowship.

The convention starts New Year's Eve because apparently we looked at a calendar and said "yes, the night when everyone else is drinking, that's when we want 500 sober people in a hotel ballroom." There will be a countdown. There will be noise makers. Someone will suggest we sing the Serenity Prayer at midnight and someone else will suggest we sing Mr. Brightside and somehow both will happen simultaneously.

$40 pre-registration. $50 at the door. Hotel rooms available now, pay later, because we understand that sober people are still broke people and credit cards are just future-you's problem.

This website exists because a flyer wasn't enough. Flyers are what normal organizations make. We are a committee that invented its own fake government positions and once seriously debated whether we could raffle off a kidney. So instead of a JPEG we built a full webpage with calendar integration, a share button with 10 anonymity-safe platforms, and a CTA that pulses on an infinite loop because we do not know when to stop.

A freelance developer would charge maybe $300 to build this. We had an AI do it at 2am for $0. You are being asked to pay $40 to attend a four-day convention in Hartford, Connecticut, over New Year's Eve, in a Marriott, with 500 people who are all in recovery and somehow think this is a good idea. That is the value proposition. The button is still pulsing.

We don't know what we're doing. We never have. We keep showing up and somehow that keeps being enough.

## Current Build Notes

- **Event:** NECYPAA 36 NYE Convention (not Zombie Prom — we killed the zombie, long live the fireworks)
- **Theme:** Cosmic neon purple/magenta/cyan because we looked at a New Year's flyer and said "yes, gradients"
- **Hero card:** Zero images. Pure CSS. Five gradients. Four radial bursts. One emoji. Infinite vibes.
- **Accent color:** `#e040fb` (neon magenta) — previously red-orange, now we are cosmically ascended
- **Share button:** Moved from floating hero overlay to actions grid. Now opens a bottom sheet instead of a dropdown. Two-column grid: Add to Calendar | Share Event. Hotel lives in the sticky bar now because it's always visible and we don't need two hotel buttons like some kind of hotel-obsessed maniac.
- **Action cards:** Color-coded gradient buttons. Indigo for calendar (organization energy). Magenta for share (matches the pulsing CTA because color theory is real and we finally learned it at 3am).
- **Calendar:** Exports 1 event now. Just the convention. The Zombie Prom is dead. The elections are over. We are streamlined.

## How to Run

```bash
open index.html
```

That's it. That's the deployment.

## How to Contribute

You don't. This is a dictatorship with a pulse-glowing button. But if you really want to help, join the group chat and survive 48 hours without someone trying to sell you ketamine on a Tuesday or suggesting we host the convention in an abandoned mall.

## Performance

- **Lighthouse Score:** We've never checked and we're not going to start now
- **Load Time:** Instant, because it's one HTML file and zero images
- **Bundle Size:** What bundle. There is no bundle. There is only `index.html` and the void.
- **Time to Interactive:** The page is interactive the moment it exists. There is no hydration. There is no virtual DOM. There is only `index.html` and 580 lines of CSS that somehow make a neon nightclub.
- **Image Weight:** 0 bytes. We deleted them all. We are image-pure. We are CSS-only. We have reached the singularity.

## Known Issues (Resolved Graveyard)

- ~~The calendar event was hardcoded to April 15, 2025.~~ Fixed. We finally read our own flyer.
- ~~The ICS file was missing `UID` and `DTSTAMP` fields~~ — technically a violation of RFC 5545 which means Outlook would've rejected it. We now generate both at runtime like professionals who definitely knew about RFC 5545 the whole time.
- ~~The schedule in the calendar said "Hype 6:30-7:30" which overlaps with "Meeting 7:00-8:00."~~ Fixed. It's 6:30-7:00. We can read a flyer now, apparently.
- ~~No meta description or Open Graph tags~~ — sharing this link on iMessage would've shown a blank preview with zero context. Now it shows the event title and description like a real website made by real adults.
- ~~No favicon~~ — Added a 🧟 emoji favicon via inline SVG data URI because we refuse to add unnecessary files to this project. Then we changed it to 🎆 because the vibe shifted.
- ~~The Zoom avatar alt text just said "Join Meeting"~~ — screen readers deserve better than that.
- ~~851KB flyer image as the entire hero section~~ — Replaced with a CSS gradient card. The flyer has been relieved of duty. It served with honor. Then we removed the replacement flyer too. Now there are no images. Only gradients.
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
- ~~Zombie Prom still mentioned in calendar data~~ — Removed. The event is over. It's done. We have moved on. The calendar now exports 1 event: the convention. We are no longer time capsules.
- ~~Host Committee Elections in calendar and NEB section~~ — Also removed. The elections happened. They're over. The NEB section is gone. The calendar is clean. We are streamlined.
- ~~Share menu looked like it was from a different website~~ — Restyled with the deep purple gradient, neon magenta border, and tighter proportions. Now it looks like it belongs. Barely.
- ~~Share button was a floating pill in the hero card~~ — It popped out and broke the visual flow. Moved it to the actions grid as a third card. Now it's Hotel | Calendar | Share. The share menu is now a bottom sheet that slides up instead of a dropdown. We deleted 35 lines of floating button CSS. The hero card is clean. The page flows. We are at peace.
- ~~Action cards had chunky colored icon boxes~~ — Looked like stock image buttons from a 2019 UI kit. Removed the icon boxes entirely. Made them subtle glass cards. Then realized glass cards are invisible on a page that's already all gradients and glass. We are not smart.
- ~~Action cards were invisible glass on glass~~ — Applied actual color theory. Each card now has a distinct gradient: indigo (`#5a67d8 → #4c51bf`) for calendar, magenta (`#e040fb → #c030d8`) for share. White icons, white text, drop shadows. They exist now. You can see them. We have learned that visibility is a feature.
- ~~Had "Hotel" and "Book Hotel" on the same page~~ — Redundant. The sticky bar already has Hotel and it's always visible. Removed the teal action card. Now it's a clean two-column grid: Calendar and Share. We have learned that less is more. At 3:49am. Growth.

### Still Standing
- On desktop the sticky bar disappears, which means desktop users only get *one* way to pre-register instead of *three*. Tragic.
- The hotel reservation link is a Marriott deep link that could expire at any moment. We live on the edge.
- The share menu has 10 platforms in it. For a landing page with three buttons. We have a 10-item share menu. We have problems.
- There are still image files in the repo (`isa2-15.JPG`, `zp1.JPG`, `neb1.png`) that aren't used by the site. Digital ghosts. We could delete them but that feels like closure and we're not ready for that.

## FAQ

**Q: Why is this a single HTML file?**
A: Because we replaced hard drugs with overengineering and this is what recovery looks like.

**Q: Is the committee chat really that active?**
A: Someone left their phone for two hours and came back to a debate about whether meth counts as pre-workout, a fascism election, and a sober haunted house pitch where someone dresses as a resentment and screams "I'M YOUR NUMBER ONE OFFENDER" at you in the dark. So yes.

**Q: Why is the README like this?**
A: This place is a prison.

**Q: Why did you delete all the images?**
A: Images are a commitment. CSS gradients are a mood. We are not ready for that kind of relationship with external assets.

**Q: Should I pre-register?**
A: The button is pulsing. It will not stop pulsing. You know what you have to do.

**Q: Four days? Really?**
A: Three days wasn't enough. We don't know why. It just wasn't. The fourth day is for... something. We'll figure it out. Probably a second talent show. Or a third. Or someone will suggest we all write amends letters to our landlords and it will get weird.

## License

No license. This code is free like the coffee at the convention. Take it. We don't care. We're too busy arguing about whether shipping containers are just jungle rooms that haven't been born yet.

---

*Built with love, sleep deprivation, energy drinks, and the kind of chaotic devotion that only exists between found family who got sober together and somehow manage to act like my actual fucking family.*
