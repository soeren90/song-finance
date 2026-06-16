# Prototype → production

The build story behind the tool, and why the AI-prototype-first approach was the
right call.

## Why prototype with AI first

The risky question wasn't "can this be built?" — most things can. It was
**"does the model actually produce useful, trustworthy valuations against real
data, and will the people who need it understand the output?"** That's a
*product* risk, and the cheapest way to retire it is a working artifact, not a
spec.

AI-assisted development made that artifact cheap and fast: load real-shaped
data, implement the model, put a number on the screen, iterate on the workflow
with real feedback. Days, not months — and disposable by design.

## What a prototype is *for* (and not for)

| The prototype's job | Explicitly **not** its job |
| --- | --- |
| Prove the model is sound | Production reliability |
| Make the workflow tangible | Clean architecture |
| Surface the real edge cases | Scale / performance |
| Earn the decision to invest | Long-term maintainability |

Conflating these is how prototypes turn into unmaintainable production systems.
Keeping them separate is what made the handoff clean.

## The handoff

Once the concept was de-risked, a **professional engineering team rebuilt the
tool for production**. The prototype's value at that point wasn't its code — it
was everything it had made concrete:

- a **validated model** the engineers could trust and reimplement,
- a **known set of edge cases** discovered by running real data,
- a **proven workflow** so they were building the right thing, not guessing.

A good prototype de-risks the engineering investment and then **gets out of the
way**. That's the whole arc: prove it fast, hand it over cleanly, let the
specialists build it to last.

## The takeaway

> The skill on display here isn't writing the production system — it's knowing
> *what to prove before you build it*, proving it cheaply, and handing it off
> without ego. AI made the proving step nearly free; the judgment about when to
> stop prototyping and bring in the pros is the part that matters.
