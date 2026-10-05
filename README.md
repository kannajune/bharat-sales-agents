# Bharat Sales Agents

**AI sales agents for Indian B2B selling.** Eleven Claude Code subagents built for how deals actually close in India: WhatsApp follow ups, founder led buying, 50% advances, GST and TDS on invoices, pricing in lakhs, IndiaMART and Naukri signals, Tamil and Hindi messaging, and a financial year that ends on 31 March.

Most open source sales agents are excellent and built for a different market. They assume a CRM, a sales team, an email first sequence, a buying committee, a procurement process and a security questionnaire. If you are a small Indian IT services firm selling to funded startups and SMEs, almost none of that describes your week.

This pack is for that week.

---

## What makes it different

The reference point for this project is [Agency Agents](https://github.com/msitarzewski/agency-agents), an excellent MIT licensed library of 230 plus agents with a strong Sales division. Across its 329 agent files, **WhatsApp appears zero times**, and so do IndiaMART, lakh and crore. That is not a criticism, it is a market gap, and it is the gap this pack fills.

What the agents here assume instead:

| Imported assumption | What this pack assumes |
|---|---|
| Email first sequences | WhatsApp first, with email as the formal record |
| A buying committee with a champion and an economic buyer | One founder or owner who decides, advised by a chartered accountant you will never meet |
| Procurement, legal review, a security questionnaire | A work order, an email, or a WhatsApp message saying go ahead |
| Net 30 after delivery | 50% advance, milestone payments, and active collection |
| Invoices without tax mechanics | GST breakup, SAC codes, TDS deducted at source, 26AS reconciliation |
| G2 reviews, 10-K filings, BuiltWith | Naukri postings, MCA filings, GST status, Indian funding press |
| Social proof as a line in a cold email | A reference who will take a live call, before price is discussed |
| A calendar year ending in December | A financial year ending 31 March, plus Diwali and regional festivals |
| One language | Tamil, Hindi, English, and the code mixed registers people actually use |

---

## The agents

| Agent | What it does |
|---|---|
| [WhatsApp Sales Strategist](sales/sales-whatsapp-strategist.md) | Runs the deal inside WhatsApp: read receipt signals, voice notes, register control, follow up ladders that change the angle instead of the frequency |
| [Advance and Collections Strategist](sales/sales-advance-collections-strategist.md) | Structures advances and milestones, then collects using GST timing, TDS reconciliation and MSME statutory leverage without burning the relationship |
| [Founder Led Deal Navigator](sales/sales-founder-led-deal-navigator.md) | Sells where one person is the budget, the evaluator and the champion, and where the real decision happens in a call you are not part of |
| [Reference and Trust Strategist](sales/sales-reference-trust-strategist.md) | Builds the credibility stack that clears before price: live reference calls, verifiable legitimacy, durability signals |
| [Inbound Enquiry Qualifier](sales/sales-inbound-enquiry-qualifier.md) | Triages IndiaMART, Justdial, web form and WhatsApp enquiries, separating real buyers from price shoppers and competitor fishing |
| [India Buying Signal Scout](sales/sales-india-signal-scout.md) | Finds intent in data that exists for Indian companies: hiring, MCA filings, GST status, Udyam records, Indian funding press |
| [Lakh Pricing and Negotiation Strategist](sales/sales-lakh-pricing-strategist.md) | Prices against structural cost sensitivity, the discount ritual, the pilot instinct, and competitors from freelancers to foreign agencies |
| [Multilingual Outreach Writer](sales/sales-multilingual-outreach-writer.md) | Writes in Tamil, Hindi, English and mixed registers, calibrated by buyer age, region, city tier and channel |
| [Indian Sales Calendar Strategist](sales/sales-india-calendar-strategist.md) | Times outreach and closes against 31 March, the Jan to March budget flush, Diwali, regional festivals and audit cycles |
| [Startup and SME Motion Strategist](sales/sales-startup-sme-motion-strategist.md) | Detects which of the two Indian buyers you have and switches the whole motion, from channel to contract |
| [Quotation and Work Order Strategist](sales/sales-quotation-work-order-strategist.md) | Produces the quotation Indian buyers expect, with GST breakup and SAC codes, and defends scope without a change order culture |

---

## Install

Each file is a standalone agent definition in markdown with YAML frontmatter. Nothing to build and no dependencies.

### Claude Code

Copy the agents into your user level agents directory:

```bash
git clone https://github.com/kannajune/bharat-sales-agents.git
cp bharat-sales-agents/sales/*.md ~/.claude/agents/
```

Or into a single project, so they are available only there:

```bash
mkdir -p .claude/agents
cp /path/to/bharat-sales-agents/sales/*.md .claude/agents/
```

Then invoke one by describing the task, or by name:

```
Use the WhatsApp Sales Strategist. This buyer read my quotation two days
ago and has not replied. Draft the next message.
```

**A note on frontmatter.** These files use the same frontmatter as Agency Agents, where `name` is a display name with spaces. Claude Code itself conventionally expects a lowercase hyphenated agent name. The files work as subagents either way, but if you want the name to match the filename exactly, change the `name` field to the hyphenated form, for example `whatsapp-sales-strategist`.

### Other tools

The format is plain markdown with frontmatter, so these work with Cursor rules, Windsurf, OpenCode, or any system that reads a system prompt from a file. Agency Agents also ships conversion scripts for several tools if you want their output formats.

### Use them as reading material

Half the value here is not automation. Each agent is a written playbook with specifics most of this knowledge never gets written down: what a blue tick at 48 hours means, which section TDS is deducted under, why Pongal falls inside your best closing window. Reading the files is a legitimate way to use this pack.

---

## Who this is for

- Small and mid sized Indian IT services firms, agencies and studios
- Founders doing their own selling, which in India is most founders
- Indian SaaS and product companies selling domestically rather than to the United States
- Anyone selling into India from outside and wondering why the usual playbook is not landing
- Sales teams in Indian SMEs with no CRM, no SDR function and no sales operations

It is not built for enterprise selling to large Indian corporates or for public sector tenders. Those are different motions, with empanelment, GeM registration and formal procurement, and they deserve their own agents rather than a footnote in these.

---

## On the tax and compliance content

Several agents cover GST, TDS, MSME registration and invoicing mechanics, because you cannot sell in India without them and because no other agent pack addresses them.

**Confirm every number with your chartered accountant.** Section numbers, rates, turnover thresholds and statutory timelines change with each Finance Act and with notifications in between. The agents state the structure and the arithmetic, and each one tells you to verify the current figures. Nothing here is tax advice.

---

## Credit

This project exists because of [**Agency Agents**](https://github.com/msitarzewski/agency-agents) by [msitarzewski](https://github.com/msitarzewski) and the AgentLand contributors. Their agent file format, their division structure and the depth they set as a standard are all borrowed here directly. If you want agents for engineering, design, product, finance or security, go there first, because this pack deliberately covers one market and one function.

Agency Agents is MIT licensed, and so is this. The original copyright notice is retained in [LICENSE](LICENSE), with the derivation recorded in [NOTICE](NOTICE).

---

## Contributing

India is not one market and nobody can write this alone. The gaps I know about:

- **Regional depth.** The language agent covers Tamil and Hindi properly and is thinner on Bengali, Marathi, Gujarati, Telugu, Kannada and Malayalam
- **Segment coverage.** These agents are written from IT services selling. Manufacturing, logistics, pharma and education each sell differently
- **Public sector and enterprise.** Tenders, GeM, empanelment and EMD are deliberately out of scope and would make a good separate set
- **Corrections.** If a statutory detail here is out of date or wrong, open an issue. That matters more than any new agent

Open an issue or a pull request. If you are adding an agent, make it genuinely new rather than an existing one with place names changed, and keep the frontmatter format consistent with the rest.

---

## Licence

MIT. See [LICENSE](LICENSE).
