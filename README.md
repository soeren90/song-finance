# Song Finance — an AI-built prototype for music-royalty finance modeling

> Built the prototype with AI to prove the concept fast. It worked — and was
> then rebuilt for production by a professional engineering team.

This is a **sanitized, generalized showcase** of a tool I prototyped for the
music-rights world: modeling the economics of songs and catalogs — what a
stream of royalties is worth, how a deal recoups, and what a catalog is worth
today. The point of this repo is the **product thinking and the
prototype-to-production story**, not a runnable binary. Specifics tied to a
particular product or company are removed.

---

## The problem

Music royalties are a real, recurring cash flow — but a messy one. Income
arrives from many sources, on a delay, splits across many rights holders, and
decays (or spikes) over time. Anyone trying to make a decision against that
cash flow — an artist weighing an advance, a label sizing a deal, an investor
valuing a catalog — has to answer the same hard questions:

- **What is this future income actually worth today?**
- **If money is paid up front, when (and whether) does it recoup?**
- **How sensitive is that answer to the assumptions** — decay rate, discount
  rate, royalty splits?

Spreadsheets get you part of the way and then collapse under the number of
moving parts. The tool exists to make those questions answerable quickly and
consistently.

---

## What it models

The domain mechanics any such tool has to get right:

| Concept | What it captures |
| --- | --- |
| **Royalty streams** | Income by source (streaming, sync/licensing, mechanical, performance), each with its own timing and behavior |
| **Decay / lifecycle curves** | How a song's income changes over time — early peak, long tail |
| **Splits** | How income divides across rights holders (writer/publisher/master, collaborators) |
| **Advances & recoupment** | Money paid up front, and the schedule by which future royalties pay it back |
| **Discounting / present value** | Translating an uncertain future stream into a value *today* |
| **Scenario & sensitivity** | How the valuation moves when the key assumptions move |

**Inputs:** historical royalty data + deal terms + assumptions (decay,
discount rate, splits).
**Outputs:** a present-value / catalog valuation, a recoupment timeline, and a
sensitivity view showing which assumptions drive the result.

---

## The story: AI prototype → production rebuild

This is the part worth showing in a portfolio.

1. **Prototype with AI.** I built a working prototype quickly using AI-assisted
   development — enough to load real-shaped data, run the model, and put a
   number on the screen. The goal wasn't clean code; it was to **de-risk the
   idea** and see whether the model held up against reality.

   The prototype was built in **Python**.

2. **Validate.** The prototype proved the concept: the model produced sane,
   useful valuations and the workflow made sense to the people who'd use it.

3. **Rebuild for production.** With the concept de-risked, a **professional
   engineering team rebuilt it properly** — production architecture,
   reliability, and maintainability that a prototype isn't meant to carry.

The lesson this repo is really about: **an AI-built prototype is a cheap,
fast way to prove a hard idea is worth real engineering investment** — and a
clean handoff from prototype to a pro team is its own skill.

See [docs/prototype-to-production.md](docs/prototype-to-production.md) for the
handoff in more detail, and [docs/concept.md](docs/concept.md) for the finance
model.

---

## Status & scope

A showcase, not a product. The production tool lives elsewhere, built and owned
by the team that rebuilt it. Everything here is generalized music-finance
domain modeling plus the build narrative — no proprietary product details,
data, or numbers.

Shared for reference, not licensed for reuse.
