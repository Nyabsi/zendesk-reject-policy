# zendesk-reject-policy

## Technical Information

Each e-mail ZenDesk sends through their ticketing system is marked through an header `X-Zendesk-From-Account-Id` and this header is an unique identifier that is 7 characters long hex sequence, this is unique for each ZenDesk account.

So we can use this to build an list of known of "bad compliance" accounts, which do not have configured ZenDesk properly and allow users to send unauthenticated tickets through their system which is used for spam.

By default the configuration rejects *all* ZenDesk accounts but ideally over-time you should collect each violation and create an curated list of account ids which do not implement their ticketing system behind an registration.
