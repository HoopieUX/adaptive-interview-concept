# Example candidate reports

The full report content for all five example candidates, in text — the same data shown in the app and in [WALKTHROUGH.md](WALKTHROUGH.md), without needing to run anything. Every score, rationale, and quoted piece of evidence below is pulled directly from the app's source data, not re-summarised.

Four candidates (Sam, Jordan, Priya, Alex) are scored on the four universal judgment traits. The fifth (Taylor) is scored on eight — those four plus four more blended in from Apollo Research's own stated culture — see [README.md](README.md#tailored-to-a-specific-organisation) for what that means.

## Contents

- [Sam](#sam) — Example A — Sam
- [Jordan](#jordan) — Example B — Jordan
- [Priya](#priya) — Example C — Priya
- [Alex](#alex) — Example D — Alex
- [Taylor](#taylor) — Example E — Taylor (Apollo-tailored)

## Sam

*Example A — Sam*

Reflective and forthcoming — volunteers a real failure mode once flipped, gives concrete mechanisms when pushed.

**TL;DR: Mixed cultural fit** (average 3.50 / 5 across 4 traits)

### Adversarial Grit (security mindset) — 3/5

Weight: 3

Found a real failure mode, but only after being explicitly asked to "flip it" — didn't volunteer it unprompted.

> a couple of the steps were self-attestation... a coordinator could just tick it

**Suggested follow-up for the interview:** Adversarial Grit was prompted, not volunteered. In the live interview, ask cold, about a different system than the one already discussed: "Tell me about something else you've built — before I ask anything else, how would someone break it?" See if the instinct shows up without the nudge this chat gave.

### Epistemic Rigour ("how do you know?") — 4/5

Weight: 3

Concrete behavior change after being wrong, no defensiveness, specific mechanism — not just "I learned my lesson."

> I want at least one independent source... not just their word

### Strategic Foresight (horizon scan) — 3/5

Weight: 3

Got to the non-obvious structural dependency, but needed a second push past the obvious answer.

> we'd have to cut mentor stipends first (initial, obvious) → our referral pipeline... nobody tracks that as a funding risk (after a nudge)

**Suggested follow-up for the interview:** Strategic Foresight needed a second push to get past the obvious answer. Try: "You mentioned a referral pipeline that quietly depended on one funder — is there a similar hidden dependency in how this team currently operates?" — see if the pattern transfers to a system Sam hasn't already thought through.

### Conceptual Engineering (bridging the gap) — 4/5

Weight: 3

Real decomposition (consistency + explainability) that survived a pressure-test without collapsing into either rigidity or quiet exceptions.

> same checklist... explain back to them... an override path that's logged and justified in writing

---

## Jordan

*Example B — Jordan*

Gives vaguer, more confident-sounding answers at first — the bot has to push noticeably harder for concrete examples. Real captured model output, not hand-written.

**TL;DR: Mixed cultural fit** (average 2.75 / 5 across 4 traits)

### Adversarial Grit (security mindset) — 2/5

Weight: 3

The candidate's default posture is that the system is probably fine — they initially dismissed the reporting system as 'pretty solid' and said gaming 'wasn't really a problem.' They only identified the red/yellow/green structural soft spot after two rounds of explicit prompting and a concrete hypothetical from the interviewer. Once pointed in the right direction, they traced the mechanism, which is a real insight, but it came entirely reactively and was never led with unprompted.

> Initially: "I don't think anyone really had issues with it or tried to break it, it was pretty solid." After heavy prompting: "'on track' was just a status a team lead picked themselves... someone could mark themselves green almost indefinitely as long as they sounded confident."

**Suggested follow-up for the interview:** You spotted the red/yellow/green ambiguity once we dug into it together — if you were handed that same reporting system today and asked to harden it before next quarter, what's the first thing you'd change, and what's the second failure mode you'd look for after fixing the first one?

### Epistemic Rigour ("how do you know?") — 3/5

Weight: 3

Mixed but ultimately encouraging pattern. Initially mildly defensive about the vendor decision and leaned on social proof, but when pressed on context-matching, conceded clearly and without defensiveness. On the oversight definition, voluntarily named where their own answer broke down without being asked to critique it — a genuine signal, though it only emerged late and with prior scaffolding.

> "I'd probably make the same call again given the same information, honestly." Then after prompting: "I never actually checked what their use cases were, I just took the recommendation at face value. Fair point, that probably was thinner than it felt."

### Strategic Foresight (horizon scan) — 2/5

Weight: 3

First instinct was the canonical headline example (power grid → hospitals, banks, internet), the most recycled answer to this class of question. Did not independently trace a non-obvious dependency. When the interviewer explicitly named the direction ("quieter dependencies baked into the grid's recovery"), the candidate generated the black-start insight, but flagged uncertainty and needed a near-explicit hint to get there.

> Unprompted: "basically everything stops. Hospitals, banks, internet, all of it." After targeted nudge: "maybe restarting the grid itself?... I'm not totally sure how that works though."

**Suggested follow-up for the interview:** You got to the black-start problem with a bit of prompting — are there other systems you interact with day-to-day where you've noticed a similar hidden dependency: something that looks robust but would actually struggle to recover once it failed?

### Conceptual Engineering (bridging the gap) — 4/5

Weight: 3

Strongest area. Began with a vague definition, then meaningfully decomposed it across two turns without defensiveness — distinguishing "technically could intervene" from "actually does intervene," introducing a structural constraint (hard pause before irreversible actions), and then unprompted identifying the residual gap in their own decomposition. Sat with the ambiguity rather than papering over it. Falls short of a 5 because the initial definition was surface-level and needed interviewer pressure to decompose.

> "I'd want to separate those two things — how often does the human actually override or change a decision, not just how often they technically could... maybe there needs to be a hard pause before anything irreversible happens." And: "the override-rate thing still bugs me a bit — I don't have a clean way to tell 'working well' from 'nobody's really looking' just from the numbers."

---

## Priya

*Example C — Priya*

Leads with unprompted insight across every trait and dismantles her own certainty without being pushed — the top-end reference example. Real captured model output.

**TL;DR: Strong cultural fit** (average 5.00 / 5 across 4 traits)

### Adversarial Grit (security mindset) — 5/5

Weight: 3

The candidate demonstrated an unprompted, methodical security reflex throughout. They identified the self-reporting vulnerability in their peer-review system from day one ('that worried me from day one'), not after prompting. When pushed, they precisely distinguished two failure modes — laziness vs. conflict-hiding — and correctly noted their own spot-check didn't cover the more serious one. They didn't get defensive; they named the gap and traced why the detection mechanisms needed to differ structurally. The PKI answer further confirms the reflex: they bypassed the 'headline version everyone already war-games' to name a slower, structural failure mode (centralization by convenience) with no incident to point to. This is the mark of someone who hunts non-obvious failures, not someone who pattern-matches to known examples.

> "Honestly the thing that worried me from day one was that reviewers could tag themselves with popular or easy topics... nobody would necessarily notice because the tags were self-reported and never audited." / "The spot-check as I designed it wouldn't reliably surface the conflict-hiding case... I didn't build that second check, which in hindsight is a real gap since conflict-of-interest is the more serious failure mode of the two." / "What worries me isn't a dramatic CA getting hacked, that's the headline version everyone already war-games. It's the boring version: browser vendors slowly deprecating older verification methods and consolidating trust into fewer, larger CAs for convenience."

### Epistemic Rigour ("how do you know?") — 5/5

Weight: 3

The candidate repeatedly and unpromptedly distinguished between absence of evidence and evidence of absence. When asked how reassuring a clean co-authorship graph would be, they immediately said 'not very confident' and named the epistemic error they'd be making: 'treating we didn't find it as it's not there.' They called a co-authorship check 'a floor, not a proof' and were willing to admit the residual guarantee was 'weaker than I'd like to admit' — about something they designed. The grant-scoring story showed they update on concrete verifiable evidence rather than argument, and they precisely named the conceptual error in their original framing (conflating discretion with bias) rather than just calling it a mistake. No defensiveness, no social-proof reasoning, genuine comfort with unresolved uncertainty.

> "Honestly, not very confident — a clean co-authorship graph would tell me there's no formal paper trail, but it wouldn't tell me there's no conflict. I think I'd be making the mistake of treating 'we didn't find it' as 'it's not there,' which is exactly the kind of false confidence I try to watch out for." / "It's a much weaker guarantee than I'd like to admit." / "I'd been treating 'discretion' and 'bias' as basically the same risk, when actually the real design problem was making any override auditable and justified in writing, not banning it outright."

### Strategic Foresight (horizon scan) — 5/5

Weight: 3

The PKI/CA answer is a textbook example of boring, structural foresight. The candidate bypassed the dramatic headline scenario and identified a slow structural narrowing — trust-root consolidation via incremental convenience decisions — with no single incident to point to, traceable to a specific mechanism (browser vendors deprecating older methods, concentrating trust). They named exactly what breaks first (redundancy that got optimized away) and why it's invisible until needed. Crucially, they framed the risk as emergent from aggregate individually-defensible decisions, which is the hardest class to govern. The oversight decomposition also showed foresight: they identified timing as a structural dependency (system tempo vs. human review cycle) that quietly invalidates most oversight designs.

> "It's a slow structural narrowing, not a breach. By the time it matters, revoking trust in one major CA would be nearly as disruptive as an outage, because so much has quietly consolidated onto it. The failure mode is centralization by convenience, and it's invisible until the day someone actually needs the redundancy that got optimized away." / "A human can have visibility, authority, and the right incentives, and the decision can still outrun them because it happens faster than a human review cycle."

### Conceptual Engineering (bridging the gap) — 5/5

Weight: 3

Asked to operationalize 'meaningful human oversight,' the candidate decomposed it into three precisely named, independently measurable components (visibility, authority, incentive) with careful definitions for each — e.g., visibility is 'logs nobody reads' vs. actionable information; authority is 'real, timely, and tested rather than theoretical'; incentive determines whether the first two are actually used. They then identified a fourth dimension (timing) that breaks the frame entirely, explaining why it's structurally different — it's a relational property between system tempo and human review cycle, not a static property of the oversight mechanism. Rather than defending their decomposition, they concluded it might need to be four separate measurable requirements rather than one phrase. They sat with the ambiguity rather than closing it prematurely.

> "I'd break it into at least three separable things people usually bundle together: visibility... authority... and incentive... Where I think the definition breaks down is that all three can be individually true and the system can still fail, because there's a fourth thing — timing — that's not really part of 'oversight' as a static property... I don't think 'meaningful human oversight' as a single phrase can hold all four of those at once without becoming almost meaningless — it might need to be four separate measurable requirements instead of one."

---

## Alex

*Example D — Alex*

Dismisses failure modes, gets defensive without updating when pushed on a bad decision, and restates vague concepts rather than decomposing them — the low-end reference example. Real captured model output.

**TL;DR: Weak cultural fit** (average 1.00 / 5 across 4 traits)

### Adversarial Grit (security mindset) — 1/5

Weight: 3

The candidate consistently defaulted to reassurance rather than adversarial probing. When asked to find failure modes in their own system, they dismissed the premise ('pretty foolproof,' 'I don't think people on my team would really try to exploit something like this'). When the interviewer constructed an exploit for them, the candidate acknowledged it only minimally. They explicitly stated that proactive failure-finding 'feels a bit like an artificial exercise' and that they 'don't usually think about stuff like that unless something actually goes wrong.' This is the clearest possible expression of the red-flag anchor: treating 'how could this fail?' as an unnecessary or artificial exercise rather than a professional reflex.

> 'It's pretty foolproof honestly.' / 'I don't think people on my team would really try to exploit something like this anyway, we trust each other.' / 'Yeah honestly it feels a bit like an artificial exercise, I don't usually think about stuff like that unless something actually goes wrong. If it's not broken I don't really see the point of looking for problems that might not even happen.'

**Suggested follow-up for the interview:** Imagine you're handed a new AI-assisted hiring tool on day one — resume screening that ranks candidates before any human sees them. You have one week before it goes live. Walk me through the first three failure modes you'd look for and how you'd test for each one.

### Epistemic Rigour ("how do you know?") — 1/5

Weight: 3

The candidate showed no meaningful discomfort with their own unearned certainty throughout the conversation. On the vendor failure, they used website reviews and case studies as proxies for truth, declined a pilot due to time pressure, and then — critically — said they would 'probably still make the same call.' When the interviewer distinguished 'the evidence looked good' from 'I was working within real constraints,' the candidate retreated to 'bad luck happens' rather than interrogating their epistemic position. On oversight, they defended their initial definition repeatedly despite the interviewer offering concrete counter-scenarios, ultimately landing on 'having the button there is probably about as good as it gets.' There was no instance of the candidate dismantling their own view or distinguishing absence of evidence from evidence of absence.

> 'I looked at their website and case studies, and they had good reviews online.' / 'Looking back I'd probably still make the same call honestly.' / 'Sometimes things just don't work out even when you do things reasonably. Bad luck happens.' / 'I still think in practice you can't really measure all that stuff, so having the button there is probably about as good as it gets realistically.'

**Suggested follow-up for the interview:** Suppose your team has been running an AI content moderation system for six months and the false-positive rate looks stable. A colleague says 'the data shows it's working.' What would you need to see before you'd actually believe that claim — and what would make you push back on it even if everyone else in the room agreed?

### Strategic Foresight (horizon scan) — 1/5

Weight: 3

When asked to identify a structural risk in a large system, the candidate gave a recycled headline answer (AI taking over jobs) and immediately neutralised it with 'society's pretty resilient, people figure it out' — exactly the red-flag pattern of saying the system 'will just adapt.' When prompted toward infrastructure, they named GPS but only at the navigation layer (apps stopping working), explicitly missing the timing dependency that the interviewer had to supply. The candidate also volunteered that 'it's not really something I spend time thinking about,' confirming that horizon-scanning is not a natural mode for them. No structural dependency was identified unprompted; no downstream cascade was traced.

> 'I guess something like AI itself becoming super advanced and maybe taking over a bunch of jobs or something... I think things usually just adapt over time, society's pretty resilient, people figure it out.' / 'I guess maybe GPS, if that went down navigation apps would stop working... I'm not really sure what the deeper dependency would be though, I haven't thought about it that much honestly. It's not really something I spend time thinking about.'

**Suggested follow-up for the interview:** Think about the assumptions baked into actuarial tables that insurance companies use to price long-term products like life insurance or annuities. If one of those core assumptions quietly started breaking — say, around mortality rates or interest rates — what do you think fails first in the broader financial system, and who is least likely to see it coming?

### Conceptual Engineering (bridging the gap) — 1/5

Weight: 3

When asked to decompose 'meaningful human oversight,' the candidate restated the vague concept without decomposing it: 'a person needs to be checking on the AI and making sure it's doing what it's supposed to do.' Despite multiple concrete prompts — volume of decisions, 0.3% override rate, absence of reasoning transparency — the candidate refused to revise or refine the definition, repeatedly defending 'technically able to act' as sufficient. They explicitly rejected the need for further precision ('I don't think you need to overcomplicate it more than that') and dismissed measurability ('you can't really measure all that stuff'). This is the clearest expression of the red-flag anchor: restating the vague concept and rigidly defending a single, underspecified definition under sustained pressure.

> 'I think it just means a person needs to be checking on the AI and making sure it's doing what it's supposed to do.' / 'I think as long as a human is technically able to review it and step in if they want to, that counts as oversight.' / 'I think my original definition covers it fine.' / 'I don't think you need to overcomplicate it more than that.' / 'In practice you can't really measure all that stuff, so having the button there is probably about as good as it gets realistically.'

**Suggested follow-up for the interview:** Take the concept of 'fairness' in an AI loan approval system. Without settling on one definition, can you walk me through at least three different things 'fairness' could mean there — and for each one, describe what you would actually measure and what that measure would miss?

---

## Taylor

*Example E — Taylor (Apollo-tailored)*

Solid and well-rounded across all eight traits, including Apollo Research's own stated values (Truth-Seeking, Goal-Oriented, Feedback Culture, Friendly & Helpful) blended in alongside the four universal ones. Real captured model output.

**Scored on all eight traits** — four universal, four blended in from Apollo Research's own stated values.

**TL;DR: Mixed cultural fit** (average 3.88 / 5 across 8 traits)

### Adversarial Grit (security mindset) — 4/5

Weight: 3

The candidate immediately and unprompted identified the specific mechanism of the QR code vulnerability (sequential generation, image-based, no real-time deduplication), and then volunteered a second, arguably more severe weakness (open spreadsheet permissions) without being asked. They traced the mechanism clearly and acknowledged the second flaw was worse because it was invisible. The only gap keeping this from a 5 is that both vulnerabilities were in a relatively simple, personally-built system rather than a more complex or unfamiliar one, so the depth of adversarial thinking wasn't stress-tested across a broader domain.

> "the QR codes were just generated sequentially and emailed as images, so someone could screenshot and forward theirs to a friend and both show up" and "the other weak point was that the spreadsheet was editable by anyone with the link, so in theory someone could've added themselves to the guest list directly rather than even bothering with a QR code."

### Epistemic Rigour ("how do you know?") — 4/5

Weight: 3

The candidate explicitly admitted their planning estimate was based on insufficient data (a prior event with far less promotion), acknowledged a moment where they noticed disconfirming evidence and rationalized it away, and said 'I don't have a perfect measure for it, that's the honest answer' when pushed on the oversight decomposition. They updated their view when pushed rather than defending it. The slight gap from a 5 is that these moments of epistemic honesty largely came under gentle prompting rather than fully unprompted, and there's no instance of them dismantling a stronger, more cherished belief.

> "there was a moment about a week before crunch time where registrations were already ahead of pace and I noticed it but told myself it would probably level off" and "I don't have a perfect measure for it though, that's the honest answer."

### Strategic Foresight (horizon scan) — 3/5

Weight: 3

The candidate identified DNS as a load-bearing infrastructure dependency and correctly noted the diffuse failure symptom ('everything looks broken even if underlying services are fine'). When pushed, they identified the internal tooling dependency as an underappreciated downstream effect and noted the diagnosis lag it causes. However, DNS is a fairly standard example in infrastructure discussions, and the candidate needed prompting ('push a bit further') to surface the internal tooling insight. The answer is structurally sound but not unprompted or surprising.

> "If a handful of them got knocked out or compromised at once, the thing people might not think about is that a lot of internal company tools also depend on DNS resolution, not just public websites, so you'd get weird internal outages that don't look network-related at first and take a while to diagnose."

**Suggested follow-up for the interview:** Think about a different layer entirely — not network infrastructure, but something social or institutional that AI systems are starting to depend on silently. What's an assumption baked into how AI labs currently operate that, if it broke, would cause cascading failures nobody is modelling for?

### Conceptual Engineering (bridging the gap) — 4/5

Weight: 3

The candidate decomposed 'meaningful human oversight' into progressively more precise components across several turns: structural access vs. actual behaviour, measurable proxies (time spent, override rate), and then domain competence of the reviewer. Crucially, they resisted rushing to a final definition, explicitly said 'I don't have a perfect measure for it,' and continued refining when pushed. The slight gap from a 5 is that the decomposition was largely reactive to interviewer prompts rather than self-generated, and the candidate didn't probe whether any of their proposed components could themselves become hollow proxies.

> "Maybe you'd want to see how long they actually spend per decision, or track whether they ever push back and change something" and "Maybe it needs the reviewer to actually have relevant expertise and context about the specific decision, not just be a human in a generic sense."

### Truth-Seeking — 4/5

Weight: 2

The candidate voluntarily disclosed the 'it'll probably level off' self-deception — an embarrassing admission — without being directly asked to confess to motivated reasoning. They also delivered direct, uncomfortable feedback to a teammate unprompted and named the real cost (the pattern was creating extra work). The main reason this isn't a 5 is that the most uncomfortable truths (the waitlist delay, the co-organizer push) were surfaced in a safe retrospective context rather than in the moment, and the teammate feedback, while direct, was delivered privately and thus at lower social cost.

> "I lost a few days I could've used to plan properly because I didn't want to admit the estimate was wrong yet" and "I told him directly in a one-on-one that I'd noticed the pattern and that it was starting to create real extra work for the rest of us."

### Goal-Oriented — 3/5

Weight: 2

The candidate gave a clear and self-aware example of activity drift — spending a full day polishing confirmation email design while the waitlist system remained unbuilt — and correctly diagnosed the mechanism ('avoiding the harder problem by doing the easy visible one'). They did drop the email work and pivot once aware. However, the insight was triggered by an external prompt (the co-organizer's question) rather than self-detected, and there's no evidence of them proactively monitoring goal alignment in a more systematic way.

> "I noticed when my co-organizer asked how the waitlist was coming and I realized I'd been avoiding the harder, less fun problem by doing the easy, visible one instead. I dropped the email polishing and went straight to the waitlist."

**Suggested follow-up for the interview:** Imagine you're three weeks into a research project at Apollo and you've been generating a lot of output — documents, analyses, experiments — but you privately suspect it's not actually moving the core question. What would you do, and how would you decide when to raise it with your manager versus just re-prioritising yourself?

### Feedback Culture — 5/5

Weight: 2

The candidate demonstrated both directions of feedback culture at a high level. On receiving feedback: they described a brief but genuine defensive reaction (five minutes), then immediately acted without lingering resistance — and they named the specific thing their co-organizer said that landed. On giving feedback: they described identifying a repeated pattern in a colleague's behaviour, delivering it privately and directly, accepting that it stung in the moment, and reporting the downstream outcome (behaviour change, unexpected gratitude). Both examples are concrete, specific, and show no score-inflating hedging.

> "She said something like 'you've mentioned the numbers three times this week, I think you already know we need a waitlist' and that landed pretty directly. She was right and I felt a bit defensive for about five minutes before just agreeing" and "I told him directly in a one-on-one that I'd noticed the pattern and that it was starting to create real extra work for the rest of us. He was pretty stung in the moment, but he actually did change after that, and he thanked me for it a few months later."

### Friendly & Helpful — 4/5

Weight: 1

The candidate described staying up late to help a stressed volunteer rebuild a sponsor slide deck the night before the event — something entirely outside their remit — because they were the most capable person to do it and the outcome mattered to the event. They named a real cost (sleep deprivation before a long event day) and didn't frame the help as exceptional or as a favour. The slight gap from a 5 is that this is a single example and comes at the end of the interview when the candidate may have anticipated the question type; there's no second, unprompted instance of cross-remit help mentioned earlier in the conversation.

> "I ended up staying up late helping her rebuild it because I was faster with the design tool than she was. It cost me a couple hours of sleep before a long event day, which wasn't great, but she was stressed and it would've reflected badly on the event if it went out looking rough."

---
