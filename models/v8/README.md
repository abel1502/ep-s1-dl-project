Evaluated the quality of various IDs as metadata, added a couple of them that were previously being discarded.
Fixed imputation of nans with mean: now correctly take the mean specifically of the training dataset.
Added fixed text embedding (of full_text and of user.description). Btw, the previous approach to text embedding had a silly fault. I forgot to add a cls token.
Widened the hidden layer and added another one. Also added dropout.
Metadata is now normalized as part of its extraction.
Tried 5 options for the text encoder.

- dummy (no text encodings): 81% at e10
- distilbert-base-cased: 80.5% at e10, 80.5% at e08, 81.4% at e06
- camembert-base: 79.9% at e10, 82% at e04
- camembert-large: 79.9% at e10, 82% at e03
- camembertav2-base: TBD
- distilbert-base-en-fr-cased: 79.6% at e10, 80.7% at e05, 81.5 at e03
- flaubert_base_cased: 77.1% at e10, 78.9% at e04
- flaubert_small_cased: 77.6% at e10, 79.1% at e04

(note: ongoing work)

Probably overfitting on user description. There does appear to be some distribution shift in the users