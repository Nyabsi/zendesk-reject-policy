# zendesk-reject-policy

## Technical Information

Each e-mail ZenDesk sends through their ticketing system is marked through an header `X-Zendesk-From-Account-Id` and this header is an unique identifier that is 7 characters long hex sequence, this is unique for each ZenDesk account.

So we can use this to build an list of known of "bad compliance" accounts, which do not have configured ZenDesk properly and allow users to send unauthenticated tickets through their system which is used for spam.

The list is not even anywhere near *completed* it blocks some known worst-cases but there is still a lot of unknown senders, consider helping by making an pull request or an issue, each blocked account id helps our mailboxes to have less spam :)