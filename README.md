# closebot gohighlevel: how to connect it, build your first booking agent, and what it really costs

If you typed "closebot gohighlevel" into a search bar, you probably aren't looking for another AI manifesto. You want to know whether this thing actually plugs into your GoHighLevel sub-accounts, how painful the setup is, what it costs on top of your GHL subscription, and whether it's worth switching away from Conversation AI.

Here's the short version before we get into the details: CloseBot connects to HighLevel through an OAuth app inside your sub-account, builds agents with a drag-and-drop flow builder, and books straight into GHL calendars. The free plan covers 100 messages a month forever. Paid business plans start at $64/mo, and the agency plan is $397/mo flat with rebilling.

Everything below is pulled from CloseBot's current plans page, its help center, and what GHL users are actually saying in public. Where the documentation contradicts itself, I'll say so instead of pretending it doesn't.

## What CloseBot actually is (and isn't)

CloseBot is a conversational AI platform for lead qualification and appointment setting. It's CRM-native, not channel-native: it doesn't connect to Instagram or WhatsApp itself. It sits on top of HighLevel, HubSpot, LeadConnector, or a custom CRM and takes over the text conversations already flowing through that CRM's inbox.

That distinction matters more than any feature bullet. If your Instagram DMs are connected to your GHL Conversations inbox, CloseBot can answer them. If you don't run a CRM at all, CloseBot isn't a standalone DM tool and you'd be buying a CRM just to run an agent.

The workflow shape is objective-driven rather than button-tree-based. You tell the agent what to accomplish (collect name and email, check service area, book a consultation), give it a persona and knowledge, and it reasons through the conversation instead of matching keywords.

CloseBot's own marketing puts it at 1M+ booked appointments, ~150,000 messages a day, and 1,000+ agencies on the platform. Those are vendor numbers, not audited ones — treat them as directional.

## Connecting CloseBot to a GoHighLevel sub-account

The connection itself is the easy part. Here's the actual sequence:

1. In CloseBot, go to the **Sources** page and add a new source.
2. Select **HighLevel Sub-Account** and click **Connect**. A popup OAuth window opens.
3. If you're not already signed into HighLevel, sign in. Then approve the CloseBot app permissions at the bottom of the permissions screen.
4. Pick the sub-account you want to connect, then head back to the CloseBot tab.
5. Click **Add Source**. You'll land on the Sources list, and the connection is confirmed.

CloseBot also has a separate **LeadConnector** connection path, which is the one agencies tend to use when they want to deploy across client accounts without manually authorizing each sub-account.

Once the source is live, the part that actually determines whether your bot behaves is the **source filters**. These are the per-source rules that switch your agent ON or OFF — channel by channel, tag by tag, list by list. Skipping this step is the most common reason people report an agent "not responding" or replying to conversations it shouldn't touch.

👉 [👉 Connect your first HighLevel sub-account for free](https://app.closebot.com/a?fpr=li87)

## Building the first job flow

In CloseBot V2, agents run on **job flows**. You'll find them under the Agents tab:

- Click **+** to create a new flow, name it, and pick the workflow type. Note that the type **cannot be changed later**, so decide before you click.
- Connect a source, or leave it for later.
- Choose a starting point: from scratch, from the template library (15+ templates on paid plans, 50+ on annual), from an AI prompt, or from a template marketplace.
- Drag nodes onto the canvas. The agent always starts at **START** and follows the arrows.

The nodes you'll use most:

- **Objectives** — the agent works through a task step by step. Putting "get name and email" in a single objective node makes it ask for both in one message instead of two, which is a small detail with a real effect on reply rates.
- **Conversation** — free back-and-forth chat when you want the agent to just talk instead of pushing toward the next step.
- **Custom scenario** — a sub-flow the agent jumps to when it detects something specific, like "this person wants to book."
- **GHL Booking** — conversationally books to a HighLevel calendar. You can pick the calendar from a dropdown or paste the calendar ID.

When a custom scenario finishes, the agent returns to where it left off on the main flow, or you can tell it where to jump back in.

Two things people get stuck on: **personas are mandatory**. You cannot publish or test a job flow without one attached. And **Bot Information** — the context about the business and why the conversation is happening — is a separate field from the persona. Fill both in.

You'll also want to set up **tags**. CloseBot can add GHL tags that trigger your existing workflows, which is where the real leverage shows up: a `ready-to-book` tag fires your scheduling link, a `lead-qualified` tag hands the contact to a rep, a `dnd` tag stops the bot cold. If you already have GHL automations built, this is how you avoid rebuilding them.

Test in the flow's testing portal before publishing. Pause the AI and take over manually on any conversation when a human needs to step in.

## CloseBot vs GoHighLevel's native Conversation AI

This is the comparison most people searching this topic are really after.

GoHighLevel's Conversation AI has improved, and for straightforward SMS qualification it's usable. It's also free with your CRM, which is not a small thing. Where it tends to fall short is SMS-specific nuance — the back-and-forth rhythm, rescheduling, and multi-rep routing.

GHL users who have run both say roughly the same thing in public threads: CloseBot handles conversational booking and rescheduling better, but it's aimed at a higher-end market. One cleaning business owner in r/gohighlevel described native GHL as "pretty clunky for SMS specifically," while others note that both tools can be overkill if you just need basic follow-up.

Two honest counterpoints worth knowing before you pay for anything:

- A two-year CloseBot user in the same subreddit wrote that "when it works, it's great," but called it "EXTREMELY unreliable," describing weekly support chats where blame moved between prompts and HighLevel webhooks. Another user complained the bot "was on LSD over the weekend, making up shit."
- G2 reviews are mostly positive about setup speed and conversation quality, with recurring complaints about limited bot functionality, occasional irrelevant answers, and no voice support.

Single complaints aren't a verdict, and unhappy customers are louder than happy ones. But if you're selling AI setting to clients, the reliability question isn't hypothetical — a hallucinated discount is a client-losing event. Budget time to test and supervise rather than assuming you can set it and forget it.

## All CloseBot plans and pricing

Pricing is split into a business track (message costs included in the base price) and an agency track (flat platform fee, usage rebilled to clients). Here's the full current lineup:

| Plan | Best for | What's included | Price | Billing |
| --- | --- | --- | --- | --- |
| Free | Testing the platform, low-volume businesses | 100 messages/mo, 1 agent, 1 user seat, 1 MB storage, unlimited account connections, always free | $0 | — |
| Core (Business) | Businesses automating their own lead qualification and booking | Message costs included in base price, 15+ templates, human support, add-on users ($5/seat), add-on storage, add-on agents | From $64/mo (annual: $53/mo equivalent, billed $640/yr) | Monthly or annual |
| Agency | Agencies building and rebilling AI agents for clients | Unlimited agents and sources, white-label client portal, rebill all costs, client wallets with your own markup, 1 user seat included | $397/mo (annual equivalent reported around $331/mo) | Monthly or annual |
| Growth | High volume, regulated industries | Everything in lower tiers plus HIPAA compliance, quarterly audits, 99.99% priority uptime, priority support, 50+ templates | Custom quote | Custom |

👉 [👉 Start on the free plan — no credit card needed](https://app.closebot.com/a?fpr=li87)

A few notes that matter more than the headline numbers:

**Business plans scale with your monthly message ceiling.** The plans page runs a slider from 100 up to 100K+ messages, and the price moves with it. The $64/mo entry point covers the base ceiling of 500 messages. Third-party reviews from 2026 list examples like $84 for 1,000 messages, $109 for 2,000, $176 for 5,000 — I'd treat those as indicative rather than guaranteed, since the slider is the source of truth and it changes.

**Message = segment, with one caveat.** One message counts as one segment, unless you've unlocked the Agent Node's "unlimited potential" (many tools, unlimited instruction size). Then you're billed on token costs and a single message can burn several segments. If you build heavy agents, budget conservatively.

**Free plan overages are $0.08/message.** The help center states free accounts are capped at 100 messages but can pay as you go beyond that. Business plans that exceed their ceiling pay a 2x overage rate drawn from a wallet.

**Storage and seats are separate line items.** Business plans include 1 MB, with add-on storage from $0.10 to $3.00 per MB per month depending on volume. Extra users are $5 each. Agency accounts can mark both up when rebilling.

**There's a documented pricing conflict on the agency per-message rate.** CloseBot's plans page FAQ says agencies are billed $0.012 per message, while the help center article on plans still states $0.006. Neither is presented as historical. If agency margins are central to your decision, confirm the current rate in-app before you price a client offer around it.

**Annual billing gets you ten months for twelve.** The plans page shows Core at $53/mo billed as $640/yr, and G2 lists the agency tier starting at $331/mo. Annual also unlocks the larger 50+ template library.

## The cost nobody puts in the headline

CloseBot doesn't replace your CRM. It runs on top of it. So the real monthly number is CloseBot plus GoHighLevel:

- GoHighLevel Starter: $97/mo (3 sub-accounts)
- GoHighLevel Unlimited: $297/mo
- GoHighLevel Agency Pro: $497/mo

A solo business running about 1,000 AI messages a month is realistically looking at $84 for CloseBot plus $97 for GHL Starter — roughly $181/month before anything else. That's not a knock on CloseBot's pricing; it's just the honest total.

For agencies, the math flips. Agency plan at $397/mo with rebillable usage, spread across several clients billing $300–$500 each, changes the per-client cost from an expense into a margin line. That's the whole pitch, and it holds up — assuming your support burden stays manageable.

## Who should buy this, and who shouldn't

**CloseBot is a reasonable fit if you:**

- Already run GoHighLevel and want something better than native Conversation AI on SMS
- Run an agency and want white-label client portals with rebilling and markup control
- Work in real estate, home services, or healthcare, where built-in tools (property data, HIPAA compliance) do things a generic bot won't
- Want high message volume with costs baked into the plan rather than metered on top of a separate API bill

**It's probably the wrong tool if you:**

- Are a solo coach whose leads arrive as Instagram or WhatsApp DMs and who has no CRM
- Want Instagram-native mechanics like comment-to-DM triggers handled in the same product
- Need a fixed all-in cost with nothing running underneath it
- Want to plug in your own OpenAI or Anthropic key to control spend — the plans page says CloseBot doesn't allow bring-your-own-key for security reasons

That last point is worth flagging because the help center is inconsistent here too. Some CloseBot docs describe V2 as requiring your own API keys and not covering provider costs; the AI providers article describes paid plans using CloseBot's own access to OpenAI, Anthropic, Gemini, and Grok. The plans page FAQ is the most current-looking source and says BYO key isn't supported. If your model spend needs to be predictable and yours, get this confirmed in writing before you build.

## Setting up without wasting your first week

A few things that will save you time:

- **Start on the free plan with one agent.** 100 messages is enough to test conversation quality on real traffic before you spend anything.
- **Test in the portal, not on live leads.** The testing portal exists so you can break things safely. Use it on any flow that touches pricing, discounts, or availability.
- **Set source filters before you go live.** Wrong filters are the number one cause of an agent answering the wrong conversations.
- **Use tags to bridge into existing GHL workflows.** Don't rebuild automations you already have.
- **Watch the message ceiling.** Overages on business plans run at 2x, and heavy agent-node usage multiplies segment counts.

## FAQ

**Does CloseBot connect directly to GoHighLevel?**

Yes, through a native OAuth integration. You add a HighLevel sub-account as a source from the Sources page. LeadConnector is also supported for agency-style deployments, and HubSpot plus custom CRMs are available too.

**Do I need my own API key?**

The current plans page says no — CloseBot doesn't allow bring-your-own-key. Some older help articles describe V2 as requiring your own provider keys. Verify this in-app before committing, because it changes your cost model.

**Is there a free trial?**

Two things, technically: a free plan that stays free as long as you stay under 100 messages a month, and a 7-day trial of any paid plan before you're billed. CloseBot states plainly that there are no refunds, so the trial is where your testing happens. Plans are month to month.

**How does CloseBot compare to GoHighLevel's Conversation AI?**

Native GHL is cheaper and simpler for basic qualification. CloseBot handles conversational booking, rescheduling, and multi-rep routing better, and it adds agency features GHL doesn't have — white-label portals and rebilling. Public user reports are mixed on reliability, so test before you commit to a client-facing rollout.

**Does CloseBot work with voice?**

No. It's text-based, covering the channels connected inside your CRM. G2 reviewers specifically list the lack of voice interaction as a gap.

**Can CloseBot close sales?**

No. It qualifies leads, follows up, and books appointments. The close happens on the call with a human. Any vendor implying otherwise — including CloseBot — is overselling.

## The bottom line

If you're already running GoHighLevel and your AI setting is limited by native Conversation AI, CloseBot is the most agency-shaped option in the category. The connection is a five-minute OAuth flow, the flow builder doesn't require code, and the rebilling model is genuinely built for agencies selling AI as a service.

If your pipeline lives in Instagram DMs and you don't run a CRM, stop here. You'd be buying a CRM to run an agent, which roughly doubles both your cost and your setup work.

Test it on the free plan this week with one agent and your own real conversations. That will tell you more about whether the conversation quality fits your market than any review will.

👉 [👉 Try CloseBot on the free plan](https://app.closebot.com/a?fpr=li87)
