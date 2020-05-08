# Hello
This PR stops all current key takeaway emails (by removing it from the guinea pig experience), and updates the eligibility logic for relaunching the test.

## bye
The eligibility is now requiring that a request to the key takeaways microservice succeed, before bucketing. This requires that we actually complete the request, and attach it to the RecommendationCandidate so it's passed to the sender job.

@IAPark I remember you didn't like having RecommendationCandidate carry algo-specific data, we might want to discuss doing something else.
pre-deploy

rebase commits
post-deploy checks

Sentry: expect no errors
Librato: expect a decrease in sender failures
start a new PR to release the test
