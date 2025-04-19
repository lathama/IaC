# Secrets

All passwords or other sensitive secrets shall be documented. Every service or
system shall have a break-glass solution.

## Passwords

- Passwords should be documented as encrypted text in this GIT repository.
- Passwords shall note the username, url/service, and the date of last change.
- Passwords shall be audited on a rolling basis.
- It is well understood that systems vary as do requirements for them.

## Two Factor Authentication

- 2FA devices should be used when possible
- Recovery codes shall be stored in this GIT repository
- Phone numbers(SMS Text) should not be used as 2FA

## Break Glass

- Situations arise where headcount changes.
- Disaster Recovery will require access to multiple systems.
- An alternate domain with email shall be maintained for backup.
- Break Glass shall be noted next to emergancy access passwords.
- Printed copies of breakglass shall be maintained by administrators.

## Tokens

- Tokens shall be treated like passwords.
- Tokens shall be audited often.
- Risk impact shall be documented for each Token.
