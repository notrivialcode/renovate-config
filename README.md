# renovate-config

The shared Renovate policy of notrivial's repositories. A repository uses it with a `renovate.json` of

```json
{ "extends": ["github>notrivialcode/renovate-config"] }
```

and, only where CI runs real tests, `["github>notrivialcode/renovate-config", "github>notrivialcode/renovate-config:automerge"]`.

What the policy does: one grouped pull request of minor and patch updates before 6:00 on Monday (Paris), a separate
pull request per major, security fixes at any time, a lockfile refresh once a month, a 3-day wait on every new release
(a hijacked package is usually pulled within days), nothing merges by itself unless the automerge add-on is extended.
Majors of the frameworks (Next, React, Sanity, Vue, Expo, React Native, Flask) wait for a tick on the dependency dashboard.
