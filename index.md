---
layout: default
title: DSC 180A Methodology Assignment 4
---

# Ethan Lam

- **Email:** [e7lam@ucsd.edu](mailto:e7lam@ucsd.edu)
- **Section:** D01
- **Mentor:** Ali Arsanjani
- **Domain:** AI for Good: Misinformation and Disinformation Detection, Ranking, and Mitigation

---

**What is the most interesting topic covered in your domain this quarter?**

The most interesting topic has been Fractal Chain of Thought (FCoT). Standard chain-of-thought prompting asks a model to reason step by step in a single pass. FCoT applies that reasoning recursively at several levels of detail, from individual claims up to the article as a whole, and revisits earlier conclusions as it goes. This is a good fit for misinformation detection, because an article's credibility depends both on the accuracy of each factual claim and on how those claims are framed and combined. We have been using FCoT as the reasoning backbone of our veracity engine, which estimates how far an article can be trusted.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

For Quarter 2, we would like to turn the veracity engine into a reliable, usable tool: a Chrome extension that analyzes the page a user is reading and returns a veracity score with a short explanation of the reasoning behind it. This would require us to:

- extract the article text cleanly from arbitrary websites,
- make the score consistent, so the same article gets a similar score across runs,
- evaluate the score against labeled misinformation datasets so we know how much to trust it, and
- present the result in a way that helps users think critically, not just hands them a number.

If the full extension turns out to be too ambitious, a smaller version could score individual claims a user highlights. If it goes faster than expected, we could add source-level reputation signals or compare our scores against professional fact-checks.

**What is one potential change you would make to your current Quarter 1 approach?**

We would change how we document and organize our work. Our GitHub repository has become fairly unorganized, so it would be hard for someone outside the team to reproduce our results or get onboarded to the project. Going forward, we want a clear repository structure that separates data, source code, prompts, and results; a README with setup and run instructions; pinned dependencies; and a record of the prompts, model versions, and parameters behind each experiment. This would make our results reproducible and make the move into Quarter 2 much smoother.

**What other techniques would you be interested in using?**

We are interested in adversarial testing, such as a "Truth Prompt" challenge, in which we deliberately build misleading, subtly altered, or manipulative inputs to try to fool the veracity engine. This would show where the model's reasoning breaks down, whether it can be manipulated by framing or confident-sounding language, and how robust the veracity score really is. What we learn from these failures could then guide improvements to our prompts and scoring.
