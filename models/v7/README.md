todo: resolve which of vaughn and andrey's modifications are version 7

from vaughn:
- Added encoding of description text
- At first, it was making the accuracy slightly worse
- But then as per Andrey's suggestion, I implemented a separate, lower learning rate for the pre-trained encoder vs. the rest of the network
- now we have an accuracy of 0.88 (ZAMN)


from andrey:
Evaluated the quality of various IDs as metadata, added a couple of them that were previously being discarded.
Fixed imputation of nans with mean: now correctly take the mean specifically of the training dataset.
Added fixed text embedding. Btw, the previous approach to text embedding had a silly fault. I forgot to add a cls token.
Widened the hidden layer and added another one. Also added dropout.
Metadata is now normalized as part of its extraction.
Tried 5 options for the text encoder.

(note: ongoing work)
