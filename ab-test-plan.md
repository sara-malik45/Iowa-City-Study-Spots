# Study Nook A/B Test Plan

## What I am testing
I will test the wording of the main homepage button.
- Version A: “Explore the study guide”
- Version B: “Compare Study Spots in Iowa City”

Both buttons will link to Best Spots. The placement, design, destination,
and all other page content will stay the same. I will publish Version B
at a separate URL, add a noindex tag, and leave it out of the sitemap.

## Hypothesis
Version B will get a higher yes rate because it tells students what they
can do after clicking: compare local study spots.

## How I will run the test
Model and version: GPT‑6 
I will use the same settings throughout and start each trial in a fresh
conversation with memory off. Before any trials, I will randomly shuffle
50 A and 50 B assignments and save the order. Each visitor will see only
its assigned version as full page text.

Exact prompt:
“You are a University of Iowa student looking for a place to study in
Iowa City this afternoon. Read the homepage text below. Would you click
the main button that leads to the Best Spots page? Answer YES or NO,
then give one sentence explaining why.

Homepage text:
[Insert the full text of the assigned homepage version here.]”

## Outcome and analysis
My primary outcome is whether the visitor answers YES. I will save every
raw response and record one CSV row per trial. I will run all 100 trials
(50 per version) and aim to finish by November 24 without stopping early.
I will report the YES rate for each version, the difference in percentage
points (B minus A), and a two-sided Fisher’s exact test. B supports my
hypothesis if its YES rate is higher and p < 0.05.
