# Building PromptOS: A Non-Technical PM's First Real Build

**From frustrated user → functioning product in 21 days**

*January 2025*

---

## The Problem I Couldn't Ignore

I'm not a developer. Three months ago, I couldn't read a React component if my life depended on it.

But I kept hitting the same wall: **learning to prompt effectively felt like studying for an exam that kept changing the questions**.

Every day brought new "prompt engineering best practices." Every model had different rules. Every use case needed a different structure. I'd spend 15-20 minutes crafting a prompt, only to realize I'd forgotten to add constraints or specify output format.

The frustration wasn't just personal - I saw teammates struggling with the same thing:
- Engineers writing vague prompts and getting inconsistent results
- PMs unable to reuse prompts across similar tasks
- No central place to learn prompt structure
- No way to know if a prompt was "good" before hitting send

**The insight**: Prompting isn't a skill you learn once. It's a *workflow* that needs structure.

---

## The Hypothesis

**What if there was a system that:**
1. Taught you *how* to structure prompts (not just what to say)
2. Stored your best prompts for reuse
3. Made prompt quality measurable
4. Worked for non-technical users

I didn't want another "awesome prompts" collection. I wanted a **prompt operating system** - something that made prompting repeatable, not artisanal.

---

## Day 1: The Non-Technical PM Problem

Here's what I knew on January 1st, 2025:
- ❌ How to write React
- ❌ How to set up a database
- ❌ How to deploy a web app
- ❌ What Supabase was

Here's what I had:
- ✅ A clear problem I experienced daily
- ✅ Claude Sonnet 4.6 and Bolt
- ✅ 3 weeks of focus time

**Decision #1**: Don't learn to code first. Ship first, learn along the way.

---

## Week 1: The 6-Step Framework

I started by mapping my own prompt-writing process. When I wrote a *good* prompt, what structure did it follow?

After analyzing 20+ of my best prompts, I found a pattern:

**The 6-Step Prompt Structure:**
1. **Intent** - What do you actually want?
2. **Context** - What background does the model need?
3. **Constraints** - What boundaries exist?
4. **Output Format** - How should the response be structured?
5. **Examples** - Show, don't just tell
6. **Validation** - How will you know it worked?

This became the core of PromptOS. Instead of a blank text box, users walk through these 6 steps.

**Why this mattered**: It turns prompt writing from creative guesswork → structured process.

I built this first. Everything else came later.

---

## Week 2: Everything Broke

Bolt generated the initial interface. I thought I was done.

Then I tried to explain it to a colleague.

**What I said**: "It's a structured prompt builder with a 6-step framework"

**What they heard**: "It's... another prompt library?"

**The problem**: The product worked, but the *value* was invisible.

Users didn't want to "fill out 6 fields" - they wanted their prompt to just *work*. The structure felt like extra work, not a solution.

**What I changed**:
- Added real-time preview (see your prompt as you build it)
- Made steps collapsible (advanced users could skip familiar steps)
- Added "Skill Files" - pre-built prompt templates for common use cases

The Skill Files idea came from watching people use the tool. They'd build a great prompt for "code review," then want to save it for next time. Instead of just saving the text, I created structured templates.

---

## Week 3: The Tech Stack I Inherited

**Why React?** Bolt chose it by default. I didn't know enough to argue.

**Why Supabase?** Free tier, and someone told me it was "the easiest database for beginners."

**Why Claude Sonnet 4.6?** I was already using Claude for everything. Made sense to build with what I knew.

**What I'd change**: If I rebuilt tomorrow, I'd use Next.js instead of vanilla React, and I'd connect the backend properly from day 1 instead of bolting it on later. But that's the point - I didn't know these things existed when I started.

**The irony**: I built a tool about structured prompting... with zero structured planning. I should have used my own product before building it.

---

## The Reality Check

**Current metrics (as of today):**
- 👥 **8 total users** (including me)
- ⏱️ **Personal time saved**: ~80% (15min → 3min per prompt iteration)
- 📝 **12 Skill Files created** (meeting summaries, code review, PRD writing)
- 🎯 **Consistency improvement**: Hard to measure, but my prompts *feel* more reliable

**Honest feedback from users:**
- "Good" - most common response
- "The 6 steps make sense once you use it twice"
- "Can you add [feature X]?" - everyone wanted something different

**What surprised me**: Nobody cared about the tech. They cared about whether it saved them time.

---

## What Actually Worked

### 1. The 6-Step Framework
This was the core insight. Prompting *is* structured - people just don't realize they follow patterns.

Making the structure explicit reduced my iteration time by 80%. That's not a guess - I timed myself before and after.

### 2. Skill Files
Originally called "templates," I renamed them "Skills" because that's what they teach. A good Skill File isn't just a saved prompt - it's a reusable process.

Example: My "Code Review Skill" prompts for:
- Language/framework
- What to focus on (security, performance, style)
- Output format (inline comments, summary, priority list)

Same structure, different inputs = consistent quality.

### 3. Building in Public (Even When Terrified)
I'm documenting this *while* figuring it out. That's uncomfortable. But it's also the point.

---

## What Didn't Work

### 1. Assuming Technical Users
My first UI had fields like "System Prompt" and "Temperature Settings." Nobody knew what those meant.

**Learning**: Build for the user you are, not the user you want to be.

### 2. Over-Engineering the Eval Layer
I spent 2 days trying to build "prompt scoring" before realizing: I don't have enough usage data to know what "good" means yet.

**Learning**: Ship the simple version. Add measurement later.

### 3. No Onboarding
8 users. 5 needed me to walk them through it personally. That doesn't scale.

**Next sprint**: 2-minute video walkthrough + interactive tutorial.

---

## The Uncomfortable Truth

This isn't a "I built an AI startup" story. This is a "I solved my own problem and 7 other people found it useful" story.

**PromptOS isn't ready for 10,000 users.** It might never be.

But it's ready for the 10 people who have the same specific frustration I had: scattered prompt knowledge and no systematic way to improve.

That might be enough.

---

## What I Learned (That Nobody Tells You)

### 1. AI tools lower the floor, not the ceiling
Bolt + Claude let me ship without coding knowledge. But I hit the ceiling fast. Want to add a database migration? Want to optimize performance? Want to integrate with APIs?

Suddenly you're learning to code anyway.

**The lesson**: AI tools are incredible for 0→1. For 1→10, you need fundamentals.

### 2. Product thinking > technical skill (for the first version)
My code is probably terrible. My architecture definitely is.

But the **6-step framework** works because I understood the user problem deeply. I was the user.

### 3. "Ship fast and iterate" is harder than it sounds
Everyone says this. Nobody warns you about the paralysis of "just one more feature before I show anyone."

I showed version 1 to users on Day 8. It was embarrassing. It was also necessary.

### 4. The real product is the second version
Version 1 was built on assumptions.
Version 2 (current) was built on feedback.
Version 3 will be built on usage data.

This is the actual PM skill: knowing when to trust your instincts vs when to trust the data.

---

## What's Next

**Immediate (Next 30 Days):**
- Add multimodal prompt testing (upload images, test how the prompt handles them)
- Build proper onboarding (stop manually explaining to every user)
- Document all 12 Skill Files as public templates

**Medium-term (90 Days):**
- Rebuild on Next.js (better architecture foundation)
- Add prompt versioning (Git-style history)
- Real A/B testing for prompt variations

**Long-term (Honest Goal):**
If 50 people use PromptOS daily, I'll know the 6-step framework generalizes beyond my specific workflow. That's the validation I'm chasing.

---

## Why This Matters

Most "PM builds product" stories are either:
1. Former engineer who already knew how to code
2. PM who "had an idea" and hired developers
3. Total fabrication

**This is different.** I'm a non-technical PM who shipped a real product using AI tools.

Three months ago, I couldn't read a console.log statement.
Today, I maintain a live web app with 8 active users.

That's not impressive by SaaS standards.
But it's revolutionary by "non-technical PM" standards.

**The real lesson**: The barrier to building products isn't technical knowledge anymore. It's product clarity.

You need to understand:
- What problem you're solving
- Why existing solutions fail
- What "good enough" looks like
- When to ship vs when to polish

AI tools handle the syntax. You handle the thinking.

---

## Honest Self-Assessment

**Am I a senior PM?** No. Not even close.

**Am I a technical PM?** Debatable. I can read code and debug basic issues, but I wouldn't pass a coding interview.

**Am I a PM who ships?** Yes. And that matters.

**Where I am**: Junior-to-mid PM who's learning product craft by building in public.

**Where I'm going**: Mid-to-senior PM who combines product instinct with technical capability.

**Timeline**: 6-12 months if I keep shipping weekly.

---

## Connect

If you're building AI tools, learning to ship with Claude/GPT, or just starting your PM journey:

- 🔗 Try PromptOS: [prompt-os.bolt.host](https://prompt-os.bolt.host)

**I'm documenting everything.** The wins, the failures, the "I have no idea what I'm doing" moments.

Because if I can ship a product as a non-technical PM, anyone can.

---

*This is Build Story #1. More coming as I learn.*
