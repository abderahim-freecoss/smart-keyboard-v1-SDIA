# Submission report (five lines)

1. We split by document: 960 sentences for training and 240 for testing, avoiding topic leakage between related sentences.
2. The interpolated model gives the highest top-3 accuracy in the main comparison: 64.7%, 0.6 percentage points above the trigram with k=0.1.
3. The trigram with k=0.1 gives the lowest perplexity in the main comparison: 5.06 versus 5.15 for interpolation, a difference of 0.09.
4. Without smoothing, 4.6% of test tokens have zero probability and perplexity becomes infinite; add-k smoothing assigns probability to unseen events.
5. The exploratory sweep reaches perplexity 4.63 for the trigram at k=0.01, but this uses the test set for tuning, so a validation split is needed for a proper study.
