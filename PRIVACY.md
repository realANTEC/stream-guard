# Stream Guard — Privacy Policy

_Last updated: 9 July 2026_

Stream Guard is a private, non-commercial moderation tool operated by an
individual developer to protect a single YouTube channel that the operator
moderates. It uses YouTube API Services under the
[YouTube API Services Terms of Service](https://developers.google.com/youtube/terms/api-services-terms-of-service).
By using Stream Guard (or authorizing it against your Google account) you also
agree to the [Google Privacy Policy](https://policies.google.com/privacy) and
the [YouTube Terms of Service](https://www.youtube.com/t/terms).

## Who uses this tool

Stream Guard has exactly two authorized users: the developer/operator and the
owner of the protected channel. It is not offered to the public, has no user
accounts of its own, and is not distributed, sold, or licensed to anyone.

## What data it accesses

Through the YouTube Data API, with the channel moderator's OAuth consent,
Stream Guard accesses:

- **Live chat messages** of the protected channel's streams (message text,
  author display name, author channel ID) — to detect and remove spam and to
  ban coordinated bot accounts.
- **Public video and channel statistics** (concurrent viewers, view counts,
  subscriber counts) — to detect and document artificial-traffic attacks
  against the channel.

## What it stores, where, and for how long

- All data is processed and stored **locally on the operator's personal
  computer only**. Nothing is transmitted to any server operated by the tool.
- Stored data consists of timestamped logs: viewer-count samples, channel
  statistics, and chat messages that were flagged as spam (including the
  author's display name and channel ID, as evidence of the violation).
- Logs are retained only to document platform-policy violations for reports to
  YouTube, and are deleted at the operator's discretion. They can be deleted
  at any time on request to the operator.
- OAuth tokens are stored locally and used solely to make the API calls above.

## What it never does

- It never sells, shares, publishes, or transfers API data to any third party.
- It never displays API data publicly; the tool's dashboard is accessible only
  on the operator's own machine (localhost).
- It never uses API data for advertising, profiling, creditworthiness, or any
  purpose other than moderation of the protected channel and abuse reporting
  to YouTube.
- It never accesses data of any channel other than the protected channel and
  the public chat of its live streams.

## Revoking access

Authorized users can revoke Stream Guard's access at any time via their Google
account security settings: <https://myaccount.google.com/permissions>.
Revoking access immediately prevents all further API access by the tool.

## Contact

For any privacy question or data-deletion request, contact the operator at the
email address listed on this repository's profile.
