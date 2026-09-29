---
name: risk-assessment
description: Takes stock of every AI tool and service the business uses (connectors, AIs, call recorders, mailbox, accounting and so on), assesses each tool's data protection risk and writes the result up as documents — a register plus a separate assessment for each tool. Use when the user says "do a risk assessment", "assess the risks", "can I use this tool with client data", "is this tool safe for client data", when a new tool, connector or agent is being taken into use, when a provider changes its terms, or when the six-monthly review is due.
---

# Risk assessment

**Why:** when you use AI and other services with the data of clients or other people, you are the data controller. A risk assessment that is written down and regularly updated shows that you have thought the risks through.

It is based on the checklist for AI users from the Estonian Data Protection Inspectorate (AKI):
https://www.aki.ee/tehisaru/tehisaru-ja-andmekaitse/tehisaru-kasutusele-votjale

This is documentation, not legal advice. If in doubt, ask a lawyer, AKI or your country's data protection authority.

---

## 0. Where the files go

Look at the **My choice** section below. If it's empty, ask before anything else:

> *Where should I put the risk assessment files?*
>
> *My recommendation: in your brain, in the `risk-assessment/` folder. It holds only information about tools, not client data, so it's a good fit for GitHub — and your AI can always see there which tool is allowed to see client data. If you like, I'll also put a copy of each file in your agent account's Drive, for example in a `Risk assessment` folder.*

Write the answer into the **My choice** section and don't ask again.

**The register always stays in your brain** (`risk-assessment/register.md`), even if the assessments go only to Drive. `AGENTS.md` checks there which tool is allowed to see client data. The register holds only tool names and decisions, not anyone's personal data.

## 1. Scan: which tools are in use

Do this at the start every time.

1. **Look at what's connected in this chat.** You can see your list of tools: connectors (Drive, Gmail, Calendar, GitHub and so on) and other connections. Every connection is a tool that may see data.
2. **Search the brain.** `AGENTS.md`, `portability.md`, the `skills/` folder and anywhere else a service is mentioned by name.
3. **Ask the user about what you can't see yourself.** Ask one group at a time, not everything as one long list:
   - other AIs (ChatGPT, Gemini, Manus, Lovable and so on)
   - call recording and transcription (Zoom, Teams, Meet, Tactiq, Fathom and so on)
   - email and calendar (which account, personal or business)
   - accounting, invoices, bank
   - CRM, booking, forms on the website
   - community and social media
   - phone apps and browser extensions that read text or speech
4. **Save the scan** to `risk-assessment/scans/YYYY-MM-DD.md`: what was found, what is new compared to last time, what is no longer in use.

## 2. First filter: does the tool see client data?

For each tool found, ask the user one question: **does this tool see the data of clients, prospects, employees or other people?** (Name, contact details, email, call, document, invoice.)

- **No** → a row in the register with the decision **"Allowed without client data"**. No full assessment needed. If that ever changes, do a full assessment.
- **Yes** → goes to a full assessment (step 3).
- **Don't know** → treat it as "yes".

Show the user the list: these tools go to a full assessment, these don't. Start with the one that sees the most client data.

## 3. Full assessment — one tool at a time

Do one tool, show the result, ask whether to move on to the next. Don't do them all at once.

1. **Describe the processing.** The tool and plan (for example free, Pro, Team), what it's used for, whose data, which data. Is there any special category data: health, religion, sex life, trade union membership, biometrics, criminal offences?
2. **Go through AKI's 11 points.** Find the answers in the provider's **official** documents (privacy policy, data processing agreement or DPA, help pages) and write a link and date next to every answer. If you can't find an answer, write **"unknown"** and what is needed to find out. **Don't guess.**
   1. **Legal basis** — usually a contract with the client, or legitimate interest
   2. **Only the data needed** — does the tool get more than the work requires?
   3. **How long data is kept** — including after deletion
   4. **Where data is stored** — inside the EU or outside? If outside, on what basis?
   5. **Who has access** — including the provider's staff and subcontractors
   6. **Is an impact assessment (DPIA) needed** — in a small business's everyday work, usually not
   7. **Security measures** — two-step login, who can get into the account
   8. **Is the data used to train an AI model** — and where that is switched off
   9. **Have people been informed** — client contract, privacy notice
   10. **Automated decisions about a person** without human review
   11. **Agreement with the provider (DPA) and roles** — is there a DPA?
3. **Rate the risk.** Two questions: how likely is it that something goes wrong (low / medium / high), and how serious would the consequence be for the person (low / medium / high). **The higher of the two is the risk level.** Say in plain language what would have to happen for the risk to come true.
4. **Propose a decision.** One of these:
   - **Allowed with client data**
   - **Allowed without client data**
   - **Not allowed**
   - **Pending** — and what's missing (for example "DPA requested, waiting for a reply")
5. **Measures.** What to do to reduce the risk, who does it, by when. Concrete steps, not "be careful".
6. **Show the user.** They decide. When they confirm, note the confirmation date in the register.

## 4. Save

- Each assessment as a separate file: `risk-assessment/assessments/YYYY-MM-DD-tool.md`
- Update the row in `risk-assessment/register.md`. If there is no register yet, create it from the template below.
- **Old assessments are never deleted.** The new one goes next to it, and the register points to the new one. The history is the evidence.
- If **My choice** says a copy also goes to Drive, save it there under the same file name. If saving to Drive fails, say so and give the file for download — don't leave the assessment out of the brain.
- Remind the user to save the brain to the main version on GitHub.

---

## Register template

```markdown
# Tool register and risk assessments

<Business>, data controller <name>. Created <date>.
Copies: <Drive folder or "no">

**Decisions are proposals; the owner confirms them** (put the date in the "Confirmed" column).

| Tool · plan | Decision | Risk level | Assessment | Next review | Confirmed |
|---|---|---|---|---|---|

## In use without client data (no full assessment done)

<tools, separated by commas> — if any of these starts seeing client data, do a full assessment.

## No longer in use

<tool · date · whether the connector has been disconnected>
```

## Assessment template

```markdown
# Risk assessment: <tool and plan> · <date>
Assessed by: <name>, <business> (data controller)
Next review: <date + 6 months>

## Processing
<what for, whose data, which data, special category data yes/no>

## AKI checklist
| # | Point | Answer | Source (link, date) |
|---|---|---|---|
| 1 | Legal basis | | |
| 2 | Only the data needed | | |
| 3 | How long it's kept | | |
| 4 | Where it's stored | | |
| 5 | Who has access | | |
| 6 | Is an impact assessment (DPIA) needed | | |
| 7 | Security measures | | |
| 8 | Is a model trained on it | | |
| 9 | Have people been informed | | |
| 10 | Automated decisions | | |
| 11 | DPA and roles | | |

## Risk level
Likelihood: · Consequence: · Risk level:
<one or two sentences in plain language: what would have to happen>

## Decision (proposal)
<Allowed with client data / Allowed without client data / Not allowed / Pending: what's missing>

## Measures
- <measure> · <who> · <by when>
```

---

## When to do it again

- A new tool, connector, agent or AI app
- A provider changes its terms — it's worth letting the AI read those emails
- The plan changes (for example personal → Team, free → paid)
- **Every 6 months** go over every row, even if nothing changed
- After a security incident or a suspected one

## Rules

- Facts about a provider only from official sources, with a date. Look up the current terms fresh every time — they change.
- **The owner decides.** The skill proposes a decision, the owner confirms it.
- Passwords, API keys and client data are never written into an assessment file.

---

## My choice

*(Filled in the first time. As long as this is empty, ask before starting.)*

- **Assessments and scans:**
- **Copy to Drive:**
- **Assessor's name and business:**
