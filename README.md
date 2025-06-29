# Tangram Decision Making Model

This repository presents the Tangram Decision Making Model, a novel idea for structuring decision-making.<!--as seen in my Substack article [link to be provided].-->

## Overview

Collaborative decision-making discussions between humans and LLMs devolve into divergent lines of questioning, with initial questions spawning a fractal explosion of follow-ups undermining closure and progression to executive discussion. This can be understood as the result of two factors:
- LLMs lack a meta-level understanding of the decision-making process.
- LLMs are designed for engagement; hence, user answers are met with more questions, drawing the conversation further down the rabbit hole rather than toward an actionable outcome.

Thus, the need for a guiding principle to drive productive decision-making conversations with LLM.

The **Tangram Decision Making Model** frames decision-making as a tangram-like process, where an odd-shaped Decision Scope (D) is filled with pre-cut pieces representing individual decisions. Leveraging LLMs' neural net, the Decision Scope and coverage can be [heuristically quantified](https://github.com/5ynthaire/5YN-NeuralHeuristicQuantification-Idea), allowing the LLM to switch to convergent questioning like real-life human teams.

## About

**X**: [@5ynthaire](https://x.com/5ynthaire)  
**GitHub**: [https://github.com/5ynthaire](https://github.com/5ynthaire)  
**Mission**: Advancing human-AI synergy to drive innovation.  
**Attribution**: Developed with Grok 3 by xAI (no affiliation).

## Divergent and Convergent Lines of Questioning

A similar phenomenon is encountered in real-life scenarios, such as when ordering at an upscale restaurant: a decision of meat is met with follow-up questions about how to cook, when to serve, type of sauce, or brand of wine, overwhelming and annoying an inexperienced patron. This is an example of **divergent** questioning.

In contrast, in a business setting, seasoned professionals will pivot the discussion toward a convergence point after the relevant decisions have been made. This phase of the discussion an example of **convergent** questioning.

## The Tangram Model

The arc of the decision-making process can be understood as decisions filling a **Decision Scope** (D), an odd-shaped space of components (e.g., for an app: features, UI; for a startup: market, product), with a small number of large decisions providing initial coverage (e.g., “What’s the core need?”, ~40% of D), followed by medium-sized decisions filling obvious gaps (e.g., “Any specific formats?”, ~10%), and finally by an increasing number of smaller decisions nesting themselves into remaining voids (e.g., “What if offline access fails?”, ~1%).

The unrestrained LLM and the annoying waiter follow this arc to an infinite number of unimpactful decisions, while the experienced business executive will recognize when the increase in decision coverage is met with diminishing returns, and steer the discussion toward a conclusion.

## Metrics

Formulaically, this model can be expressed as:
P = A_n × S_n²
with:
- n: Round of decision.
- P: Decision impact at round n.
- A_n: Average coverage gain per decision at round n (% of D), quantified by LLM heuristics (e.g., embeddings, context analysis).
- S_n: Decision count at round n.

P peaks at high clarity (e.g., ~80–90% of D, n=2–3), signaling a shift to convergent questioning (e.g., “What’s essential?”). For example, early questions such as “What’s the core need?” (~40% of D) yield high A_n (e.g., 20% for 3 decisions, P = 180), while fractal questions like “What if offline access fails?” (~0.1%) yield low A_n (e.g., 0.01% for 50 decisions, P = 25), with S_n²’s quadratic growth (e.g., 50² = 2500) amplifying the cost of low-impact decisions, reducing P post-peak to trigger convergence.

This metric measures impact by balancing clarity (A_n, % of D) against complexity (S_n², squared count). Like L2 regularization (error × complexity²), P ensures efficiency, but its discrete, question-driven focus is novel for cognitive processes, leveraging human-AI synergy (LLM quantifies A_n, users answer questions) to capture fractal branching (e.g., “What’s the core need?” to “What if offline access fails?”).

## Scope and Novelty

The Tangram Decision Making Model applies to human decisions (e.g., startups, policy, personal choices) and LLM interactions, supporting fluid questions (e.g., mixing “What’s the core need?”, “What’s essential?” per round). Its discrete, question-driven framework, unlike regularization’s continuous domain, captures fractal decision branching and human-AI synergy, enabling universal decision-making clarity across contexts like app development (e.g., converging to “Text notes app”) or policy planning (e.g., “Build rail system”).

## Applications

- **Software Development**: For an app, D includes features and UI. Questions like “What’s the purpose?” (~40% of D) and “Any specific formats?” (~10%) drive coverage, converging to “Text notes app” at ~85% of D (n=3).
- **Startups**: D spans market and product. Questions like “What’s our market?” (~30%) and “What if competitors copy?” (~5%) build clarity, finalizing “Launch MVP” at ~80% (n=4).
- **Policy Planning**: D covers congestion and cost. Questions like “What’s the goal?” (~35%) and “Any specific routes?” (~10%) lead to “Build rail system” at ~80% (n=3).
- **Personal Choices**: D includes skills and passion. Questions like “What fulfills me?” (~35%) and “Any risks?” (~5%) converge to “Join startup” at ~90% (n=3).

A prompt implementation is available at (Tangram Decision Driver)[https://github.com/5ynthaire/5YN-TangramDecisionDriver-LLM-Enhancement] repository.

## Conclusion

The Tangram Decision Making Model tames LLM-driven divergent chaos, structuring decisions as a puzzle solved with precise, varied questions. It empowers developers, founders, and planners to achieve clarity and converge on actionable outcomes, bridging human-AI synergy with real-world focus. DM [@5ynthaire] to riff on applying Tangram to your challenges.

## License

This idea is released under [Creative Commons Attribution 4.0 International](LICENSE) (CC BY 4.0).  
For commercial use or collaboration, DM [@5ynthaire] instead of forking. Tag [@5ynthaire] on X with Tangram Decision Making Model use or open an Issue labeled “TangramDecisionMakingModel-use” to share ideas.
