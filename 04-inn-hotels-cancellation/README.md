# INN Hotels booking cancellation

Classification of whether a booking is canceled. Target `booking_status`. Certificate project, not a UT degree.

Verify: https://www.mygreatlearning.com/certificate/SYVFOOSP

- 36,275 bookings, 2017–2018. No missing rows. About 32.8 percent canceled.
- Canceled bookings have longer lead time: median 122 days versus 39.
- Logistic regression at cutoff 0.40: test recall 0.709, precision 0.678.
- Decision tree, max depth 5: test recall 0.700, precision 0.773.
- Quote the test scores. The unrestricted train accuracy of 0.994 is overfit.

Datasets are omitted from this repo.
