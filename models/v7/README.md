Evaluated the quality of various IDs as metadata, added a couple of them that were previously being discarded.
Fixed imputation of nans with mean: now correctly take the mean specifically of the training dataset.
Added fixed text embedding. Btw, the previous approach to text embedding had a silly fault. I forgot to add a cls token.
Widened the hidden layer and added another one. Also added dropout.
Metadata is now normalized as part of its extraction.
Tried 5 options for the text encoder.

(note: ongoing work)
