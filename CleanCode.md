---
title: "**Clean Code**"
sub_title: by Robert C. Martin (Summarized)
---

Chapter 1 — The Foundation of Professional Software
===

<!-- 
speaker_note: |
  Welcome to Chapter 1. This is where we set the stage for everything to come.
  Clean Code isn’t just about writing something that works — it’s about writing code that lasts.
  Let’s dig into what makes clean code such a core part of being a professional.
-->

<!-- end_slide -->

Why Clean Code?
===

- Code is read far more often than it's written.
- Clean code reduces bugs, improves team velocity, and builds trust.
- Writing clean code is a sign of professionalism.

<!-- 
speaker_note: |
  Let’s face it — we spend more time reading code than writing it.
  And bad code slows us down, introduces bugs, and frustrates everyone involved.
  Writing clean code isn’t optional if you want to call yourself a professional.
-->

<!-- end_slide -->

There Will Be Code
===

- Some believe code will disappear — replaced by specs or visual tools.
- But code *is* the specification — it's how we express exact behavior.
- Higher abstraction doesn't remove code — it transforms it.

<!-- 
speaker_note: |
  You might hear people say, “Soon we won’t need to write code.”
  But the truth is: code is how we capture detail. It *is* the final layer of specification.
  Even with AI or high-level tools, someone will always need to define the logic precisely — and that’s code.
-->

<!-- end_slide -->

Why Bad Code Happens
===

- We often trade quality for speed — under pressure.
- Common excuses: tight deadlines, fatigue, "we'll fix it later."
- Reality: later almost always means *never*.

<!-- 
speaker_note: |
  Let’s be honest — we’ve all made a mess to get something working.
  Deadlines, stress, or that "I’ll clean it up later" mindset creep in.
  But as LeBlanc’s Law says: “Later equals never.” Those messes stay with us.
-->

<!-- end_slide -->

The Cost of Messy Code
===

- Short-term gains, long-term pain.
- Messy code leads to:
  - Fragile systems
  - Slow development
  - Frustrated teams

<!-- 
speaker_note: |
  Messy code builds technical debt fast.
  What started as a small trade-off turns into a mountain of pain — where every change breaks three other things.
  Over time, your team slows to a crawl. Morale drops. Delivery suffers.
-->

<!-- end_slide -->

The Grand Redesign in the Sky
===

- Eventually, teams beg for a rewrite.
- A "tiger team" builds Version 2.0.
- But without changing habits, the new system becomes just as bad.

<!-- 
speaker_note: |
  I've seen this pattern too many times.
  The team can’t take it anymore, so they start from scratch. But they bring the same bad habits.
  Six months in, the new codebase looks just as bad.
  Rewrites don’t solve bad discipline — they repeat it.
-->

<!-- end_slide -->

Attitude Makes the Difference
===

- Clean code is a matter of attitude, not just skill.
- Our job is to advocate for quality — even under pressure.
- Push back professionally when speed threatens sustainability.

<!-- 
speaker_note: |
  This is key: writing clean code is a mindset.
  It's about pride in your work, responsibility to your team, and the courage to defend quality — even when it’s hard.
  That’s what separates professionals from amateurs.
-->

<!-- end_slide -->

What Is Clean Code?
===

- Code that is easy to read and understand.
- Clear, expressive, and intention-revealing.
- Like a good story — every line should make sense.

<!-- 
speaker_note: |
  Clean code doesn’t hide meaning — it reveals it.
  It reads like prose. Someone new to the team should be able to follow along without needing a translator.
  That’s the level of clarity we’re aiming for.
-->

<!-- end_slide -->

The Boy Scout Rule
===

> "Always leave the campground cleaner than you found it."

- Improve code every time you touch it.
- Small refactors = big long-term impact.

<!-- 
speaker_note: |
  This principle is gold.
  Don’t wait for a big refactor. If you're in the code anyway, make it a bit better than you found it.
  Rename a variable. Break a method. These small acts compound over time.
-->

<!-- end_slide -->

Conclusion
===

- Clean code is a mindset — and a practice.
- It takes discipline, patience, and pride.
- Up next: the first tool in your clean code toolbox — **meaningful names**.

<!-- 
speaker_note: |
  So that's Chapter 1 — a powerful reminder that clean code isn’t just about style, it’s about responsibility.
  Next, we’ll dive into one of the most powerful tools you have for clarity: choosing great names.
-->

<!-- end_slide -->

Chapter 2 — Meaningful Names
===

<!-- 
speaker_note: |
  Welcome to Chapter 2 — probably the most underestimated chapter in the whole book.
  Naming things well is one of the simplest ways to write clean, readable code — and yet so often, we rush it.
  Let’s fix that.
-->

<!-- end_slide -->

Why Names Matter
===

- Code is read 10x more than it's written.
- Good names eliminate the need for comments.
- They reduce bugs and improve collaboration.

<!-- 
speaker_note: |
  We spend most of our time reading code, not writing it.
  Names are our first, best chance to explain what the code is doing — so why waste that chance?
-->

<!-- end_slide -->

Reveal Intent
===

- Choose names that answer: *What is this? What does it do?*
- ❌ `d` or `tmp`
- ✅ `elapsedTimeInDays`, `totalRevenue`

<!-- 
speaker_note: |
  A name should eliminate confusion, not cause it.
  If you have to explain it in a comment, you probably need a better name instead.
  Let the name do the talking.
-->

<!-- end_slide -->

Avoid Disinformation
===

- Misleading names cause subtle bugs.
- ❌ `accountList` when it's a `Set`
- ❌ `timeout` (in ms) → name it `timeoutInMillis`

<!-- 
speaker_note: |
  Think of names as contracts. If the name says one thing and the reality is another, it’s a broken contract.
  Keep names honest — even the little ones.
-->

<!-- end_slide -->

Make Meaningful Distinctions
===

- Don’t use noise words or numbers.
- ❌ `info1`, `info2`, `userDataTmp`
- ✅ `userProfile`, `adminProfile`

<!-- 
speaker_note: |
  Think of names like labels. If you can’t tell two variables apart by name, something’s wrong.
  Give each item a name that reflects its *role*, not its *order*.
-->

<!-- end_slide -->

Use Pronounceable & Searchable Names
===

- Pronounceable: ✅ `customerAddress`, ❌ `custAddr`
- Searchable: ✅ `elapsedTime`, ❌ `k`

<!-- 
speaker_note: |
  If a name is hard to say, people won’t say it. If it’s hard to search, you’ll hate maintaining it.
  Give your future self and your teammates a break — use clear, searchable names.
-->

<!-- end_slide -->

Avoid Encodings and Prefixes
===

- ❌ `strName`, `iCount`, `bDone`
- ✅ `name`, `count`, `isFinished`
- Let tools handle type — focus names on purpose.

<!-- 
speaker_note: |
  Encoding types in names made sense in the ‘90s. Today, it’s just noise.
  Your IDE already knows the type. Focus the name on what it *means*.
-->

<!-- end_slide -->

Consistent Vocabulary
===

- Use one word per concept.
- ❌ `fetch`, `retrieve`, `get` used interchangeably
- ✅ Choose one — and stick to it.

<!-- 
speaker_note: |
  This is about consistency. If `get` means something in your codebase, use it everywhere for that concept.
  Don't make your readers guess whether `fetch`, `retrieve`, and `get` do the same thing.
-->

<!-- end_slide -->

Provide Context — When Needed
===

- ✅ `addressState` instead of `state`
- ❌ `productId` inside a `Product` class → just `id` is fine

<!-- 
speaker_note: |
  Use context to disambiguate, but don’t go overboard.
  If you’re inside a `Product` class, you don’t need to call everything `productSomething`.
-->

<!-- end_slide -->

Conclusion
===

- Naming is a communication skill, not just a technical one.
- Good names reduce confusion, bugs, and wasted time.
- Great code starts with great names.

<!-- 
speaker_note: |
  Naming is where clean code begins. Take the time to name things well, and you’ll save hours of debugging and explaining later.
  Up next — functions: how to write them clean, clear, and powerful.
-->

<!-- end_slide -->

