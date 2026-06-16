# The finance model

This describes the general mechanics of valuing music royalties — the domain the
prototype modeled. It's standard music-finance reasoning, not a description of
any proprietary formula.

## 1. Royalty streams are not one number

A song earns from several sources, and they behave differently:

- **Streaming** — high volume, small per-unit, fairly continuous, decays over
  time after release.
- **Sync / licensing** — lumpy and unpredictable: a placement in a film, ad, or
  game can be a large one-off.
- **Mechanical** — tied to reproduction/sales.
- **Performance** — radio, public play, venues; collected via PROs, paid on a
  delay.

A useful model treats these separately, because their timing and volatility
differ.

## 2. Income decays (mostly) along a curve

A new release typically peaks early and then settles into a long tail.
Catalog songs behave differently from new releases. The model needs a
**lifecycle / decay curve** per song or per cohort, because "last year's
income" is not "next year's income."

## 3. Money splits before anyone gets paid

Gross income is divided across rights holders along two axes:

- **Composition** (writer / publisher share)
- **Recording** (master / label share)

…and then again across collaborators within each. A valuation is only as good
as the split assumptions feeding it.

## 4. Advances and recoupment

Often money is paid **up front** (an advance), and future royalties pay it back
before the recipient sees further income. Modeling this means projecting the
royalty stream forward and walking down the outstanding balance period by
period to find the **recoupment point** — the moment the advance is paid off.

## 5. Present value: what is future income worth *today*

Future, uncertain income is worth less than cash now. Discounting future
royalty cash flows back to the present gives a **valuation** — the core output.
The two assumptions that dominate the result:

- **Discount rate** — how hard you penalize future, risky income.
- **Decay rate** — how fast you assume income falls off.

## 6. Sensitivity is the whole point

Because the valuation hinges on a few assumptions, a single number is
misleading on its own. The model earns its keep by showing **how the answer
moves** when you flex the inputs — a range and the drivers behind it, not a
false-precision point estimate.

---

### Why this is hard in a spreadsheet

Each of the six pieces above is manageable alone. Together — many songs, many
sources, per-song curves, nested splits, recoupment schedules, and a
sensitivity sweep across all of it — a spreadsheet becomes fragile and slow.
That fragility is the gap the tool was built to close.
