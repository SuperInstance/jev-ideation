# When the Heat Pump Lies

*An ideation piece from the GLM lane. The premise: Jevs become background infrastructure — tiny ternary judgment models humans stop watching, like a heat pump keeping the house warm. The question nobody asks until it's too late: what breaks when the background is wrong and nobody's looking?*

## The failure you don't get: a crash

A Jev never crashes. It gets confidently wrong, and the ternary format hides the magnitude — a drifted −0.51 renders identical to a certain −0.98. There is no error signal because nobody expected one from infrastructure. The heat pump doesn't beep when it starts heating the crawlspace instead of the house. It just runs, and the bill goes up, and you don't notice until the pipes freeze.

This is the first failure mode: **silent drift**. Probabilities rot as the world moves under them. The judgments were calibrated on last year's world, and this year's world is close enough that nothing looks broken — just slightly, systematically off, in a direction nobody is measuring because the whole point of background infrastructure is that you stopped measuring it.

## The failure that scales: correlation

Human background judgment errs idiosyncratically. Your spam triage misses things mine catches; across a population, errors cancel. A Jev errs *identically* a million times.

One systematic −1 — say, on non-native-English phrasing, or on a document format the training set underrepresented — becomes silent deprioritization of an entire population, everywhere the layer is embedded, simultaneously. And the aggregate metrics look fine, because the baseline drifted along with the model. You're measuring the judges against judges trained on the same rot.

This is the failure mode with teeth. Not one wrong judgment — a million copies of the same wrong judgment, invisible to every dashboard, because the dashboard was built from the same assumptions.

## The failure you finally see: absence

When it breaks, it doesn't present as anomaly. It presents as *absence*. The inbox just feels quiet. The feed seems fine. Then someone asks "did you see the email about X?" and the search surfaces hundreds, going back fourteen months.

The patch is cheap — retrain, redeploy, done by Friday. The audit isn't. Every downstream decision stacked on contaminated judgments is now suspect. No ground truth was ever collected, because collecting it was the thing you offloaded. And the humans who gave the skill away no longer have it to re-verify. You can't hand-check fourteen months of triage when you've forgotten how to triage.

**The skill atrophies faster than the model drifts.** That's the sentence to sit with.

## The minimum honest mechanism

If drift, correlation, and absence are the failure modes, what's the cheapest stack that keeps the layer honest? Three parts, minimum:

1. **Rotating canary set.** A few hundred human-adjudicated cases per year, held by an *adversarial* party, provably outside the training data. Scored quarterly. This is the only piece that catches correlated drift of the judges themselves — everything else measures the model against its own assumptions.

2. **Disagreement sampling.** Two judges with different training provenance run on ~1% of traffic; humans review only the disagreements. Nearly free when healthy (disagreement is rare), fires instantly on unilateral corruption. The cost scales with the problem, not with the traffic.

3. **Bounty economics.** Pay per *confirmed failure found*, not per audit passed. This terminates the recursion: the watcher of the watcher is whoever profits from breaking it, not another model. Adversarial funding beats compliance staffing, because compliance optimizes for passing and bounties optimize for finding.

## The binding constraint

It isn't technical. Infrastructure monitoring is a budget line trending toward zero — every efficiency gain gets reinvested into cheaper operation, not better oversight. That's Jevons pressure applied to trust itself: the more reliable the heat pump seems, the less anyone pays to check it, until the checking is gone and only the seeming remains.

So the mechanism has to be adversarially funded, not compliance-staffed. Someone has to *want* the heat pump to fail, and get paid when it does. That's the only watcher that doesn't fall asleep.

The heat pump is a beautiful idea. Just don't forget what's underneath the house when it stops working and nobody noticed for a year.
