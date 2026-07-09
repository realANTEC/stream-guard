# Stream Guard

A private, non-commercial tool that protects a single YouTube livestream channel
from spam and third-party artificial-engagement attacks. It runs locally on the
operator's own computer and is used only by the channel's moderator and the
channel owner.

## What it does

Stream Guard uses the official **YouTube Data API** (with the channel
moderator's OAuth consent) to:

- **Moderate live chat in real time** — detect and remove spam, and ban
  coordinated bot accounts that raid the stream's chat.
- **Detect artificial-traffic attacks** — sample concurrent-viewer counts and
  channel statistics to spot fake-view and subscriber-bot injections, using
  robust statistics and chat-activity correlation (a real audience talks; a
  view-bot does not).
- **Document attacks as evidence** — write timestamped logs and compile them
  into reports the channel can submit to YouTube, which is the only party that
  can actually remove invalid traffic.

It also tracks when YouTube purges fake engagement (proof the traffic was
invalid) and forecasts likely attack windows from the history it records.

## What it is *not*

- Not a bot that generates views, subscribers, or engagement of any kind.
- Not a tool that touches, attacks, or sends traffic to any other channel or
  system. It only ever reads the protected channel and moderates its own chat.
- Not a public service. There is no signup, no hosting, no third party. All
  data stays on the operator's machine.

Fake views and subscribers hit YouTube's servers, not the channel, so no
external tool can "block" them. Stream Guard's job is to keep chat clean, to
document attacks so YouTube can act, and to confirm when it does.

## How it works (high level)

- A local Node.js application with a localhost-only web dashboard.
- Authorizes via Google OAuth 2.0 using the `youtube.force-ssl` scope (required
  to moderate live chat).
- Adaptive API polling keeps usage within quota during long (8–12h) daily
  streams: it polls faster during activity or an active attack, and backs off
  when chat is idle.

## Privacy

See [PRIVACY.md](PRIVACY.md). In short: data is processed and stored locally
only, is never shared or published, is used solely for moderation and abuse
reporting, and access can be revoked at any time via
<https://myaccount.google.com/permissions>.

## Status

Private tool for a single channel. Not distributed or accepting external users.
