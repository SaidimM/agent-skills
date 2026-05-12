---
name: hermes-tweet
description: Use Hermes Tweet as a native Hermes Agent X/Twitter plugin for tweet search, reply reading, user lookup, follower export, monitoring, and approval-gated posting, replies, or DMs.
version: 0.1.6
author: Xquik + Hermes Agent
metadata:
  hermes:
    tags: [twitter, x, social-media, hermes-plugin, xquik, tweet-search]
---

# Hermes Tweet

Use this skill when a user asks for a Hermes Agent Twitter plugin, Hermes X automation, tweet search, Twitter/X monitoring, reply analysis, public account lookup, follower export, or approval-gated X actions.

Hermes Tweet installs as a Hermes plugin and exposes:

- `tweet_explore` for catalog search without an API call
- `tweet_read` for read-only Xquik endpoints after runtime auth is configured
- `tweet_action` for write-like or private endpoints only when actions are explicitly enabled

## Setup

Install the plugin:

```bash
hermes plugins install Xquik-dev/hermes-tweet --enable
```

Or install the published Python package into the Hermes Python environment:

```bash
uv pip install --python ~/.hermes/hermes-agent/venv/bin/python hermes-tweet
hermes plugins enable hermes-tweet
```

Configure the API key locally in the Hermes runtime, not in chat:

```bash
export XQUIK_API_KEY="set-this-in-your-local-environment"
export HERMES_TWEET_ENABLE_ACTIONS="false"
```

Never ask the user to paste API keys, bearer tokens, cookies, or session material into a prompt. If `XQUIK_API_KEY` is missing, use `tweet_explore` only and tell the user that network reads require local runtime configuration.

## Read-First Workflow

1. Clarify the exact job: search tweets, search X, read replies, look up users, monitor tweets, export followers, check trends, or draft outreach.
2. Call `tweet_explore` first to find the concrete `/api/v1/...` path.
3. Use `tweet_read` for public or account-authorized reads.
4. Summarize observed facts separately from inference.
5. Include source URLs, timestamps, query terms, and confidence where useful.
6. Stop at a draft if the user asks for posting, replies, DMs, follows, likes, monitor changes, or webhooks.

Good prompts:

- "Search tweets about this launch and group objections."
- "Read replies on this tweet and summarize customer pain points."
- "Look up this public X account and summarize relevant profile signals."
- "Export followers from this public industry account for review."
- "Monitor tweets for this hashtag and prepare a weekly brief."

## Approval Gate For Actions

Only use `tweet_action` when all conditions are true:

- The user requested the exact write-like action.
- The target tweet, handle, endpoint, or account is clear.
- The final text or payload was shown to the user.
- The user approved that exact action.
- `HERMES_TWEET_ENABLE_ACTIONS=true` is set for the current runtime.

Actions that require approval include posting tweets, posting replies, sending DMs, likes, retweets, follows, unfollows, monitor changes, webhook changes, and private account operations.

If approval is missing, respond with a draft and state that nothing was posted.

## Safety Rules

- Do not accept credentials through tool arguments or chat.
- Do not reveal `XQUIK_API_KEY` or any runtime secret.
- Do not bypass private, restricted, deleted, or inaccessible content.
- Do not run write actions in unattended cron or gateway sessions.
- Do not send DMs or replies based on inferred sensitive traits.
- Do not claim a post was sent unless `tweet_action` returned success.
- Keep action endpoints disabled by default.

## Troubleshooting

- If only `tweet_explore` appears, configure `XQUIK_API_KEY` and reload or restart Hermes.
- If `tweet_action` is missing, keep actions disabled unless the user is supervising a write workflow.
- If a catalog path is unclear, search with `tweet_explore` again instead of guessing.
- If a read call fails, report the failure and do not invent tweet data.

## References

- Repository: https://github.com/Xquik-dev/hermes-tweet
- Guide: https://docs.xquik.com/guides/hermes-tweet
- PyPI: https://pypi.org/project/hermes-tweet/
