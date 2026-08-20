# Security policy

This policy applies to every repository in the
[`vobiz-ai`](https://github.com/vobiz-ai) organisation and to the Vobiz platform
and API.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues,
pull requests, or discussions.**

Email [piyush@vobiz.ai](mailto:piyush@vobiz.ai) with the subject line
`SECURITY` and a description of the issue. If a repository has GitHub private
vulnerability reporting enabled, you may also use the **Security → Report a
vulnerability** button there.

To help us reproduce and assess the report quickly, please include what you can
of the following:

- the affected repository, SDK, endpoint, or service, and the version or commit
- the type of issue — for example authentication bypass, injection, credential
  exposure, privilege escalation, or SSRF
- step-by-step instructions to reproduce it, including any proof-of-concept code
- the impact you believe it has, and which accounts or data it could reach
- any configuration required to trigger it

Please report in English.

## What happens next

We will acknowledge your report by email and let you know whether we have been
able to reproduce it. We will keep you informed as we investigate and work on a
fix, and we will tell you when it has been resolved.

We are grateful for reports made in good faith and are happy to credit you when
we publish a fix, if you would like that.

## Please do

- Give us a reasonable opportunity to fix the issue before disclosing it
  publicly or to any third party.
- Test only against your own Vobiz account and your own numbers and data.
- Stop as soon as you have confirmed a vulnerability. Extract only the minimum
  needed to demonstrate it.

## Please do not

- Access, modify, or delete data belonging to another Vobiz account.
- Run denial-of-service, load, spam, or automated brute-force testing against
  Vobiz systems or numbers.
- Use social engineering, phishing, or physical attacks against Vobiz staff,
  customers, or infrastructure providers.
- Place calls or send messages to people who have not consented to your testing.

## Handling credentials

If you believe a Vobiz credential of yours has been exposed — an `X-Auth-ID` and
`X-Auth-Token` pair, a SIP password, or a webhook signing secret — rotate it
immediately in the [Developer Console](https://console.vobiz.ai) and email
[piyush@vobiz.ai](mailto:piyush@vobiz.ai) so we can review account activity.

Never include live credentials in a report. Redact them, and tell us where they
were exposed instead.

## Non-security issues

For bugs that do not have a security impact, please open a normal issue on the
relevant repository. See [CONTRIBUTING.md](./CONTRIBUTING.md).
