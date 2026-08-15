# Prompt Gallery

## One topic, three audiences

Prompt:

```text
$explain Explain OAuth for a curious five-year-old,
a new backend engineer, and an engineering executive.
```

### Curious five-year-old

OAuth is like giving a helper a special visitor badge. The badge lets the helper do one approved job—such as seeing your photos—without giving it the key to your whole house.

The real system uses digital tokens rather than physical badges. A token has rules about what it can access and how long it works.

### New backend engineer

OAuth is an authorization framework: it lets a client access a resource on a user's behalf without receiving the user's password. The authorization server authenticates the user and issues an access token. The client presents that token to the resource server, which verifies its scope and validity before returning protected data.

OAuth does not define user identity by itself. Use OpenID Connect when authentication and identity claims are required.

### Engineering executive

OAuth lets customers authorize integrations without sharing passwords. It reduces credential exposure and enables revocable, limited access, but it adds implementation and operational complexity. The decision should account for identity-provider reliability, token security, integration support, audit requirements, and incident response.

## Rewrite without losing precision

Prompt:

```text
$explain Rewrite the following deployment guide for a junior engineer.
Keep commands, environment variables, API fields, thresholds, and warnings exact.
```

Expected behavior:

- Explain the purpose before each group of steps.
- Define unavoidable terminology in plain language.
- Preserve exact technical tokens.
- Keep prerequisites, validation, failure conditions, and recovery steps.
- Do not invent missing commands or silently resolve ambiguity.

## Layered explanation

Prompt:

```text
$explain Explain database indexes in three layers:
a one-sentence answer, a beginner mental model, and optional technical detail.
```

This format works well for mixed audiences because readers can stop at the depth they need.
