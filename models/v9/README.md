Pick the most promising model(s) for encoding text fields.
Drop user.description. (Maybe finetune with it later, but not from the start.)

Slightly worse (81.2% instead of 82%), suggesting that user descriptions are in fact useful, if prone to overfitting.

Also implement per-user reconciliation. Up to 81.9%. When applied to the version with user.description, that previously achieved 82%, that one went up to 82.4%. So this is at least useful, yes