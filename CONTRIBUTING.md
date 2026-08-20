# Contributing to Vobiz

Thanks for taking the time to contribute. This guide applies to every repository
in the [`vobiz-ai`](https://github.com/vobiz-ai) organisation — the official
SDKs, the agent skills, and the sample applications.

## Before you start

- Check the [documentation](https://vobiz.ai/docs/introduction) and the
  [OpenAPI specification](https://vobiz.ai/openapi.json). Many questions about a
  request field or response shape are answered there.
- Search the repository's existing issues. If someone has already reported it,
  add your reproduction to that thread rather than opening a duplicate.
- Never include credentials in an issue, a pull request, or a commit. Redact
  `X-Auth-ID`, `X-Auth-Token`, SIP passwords, webhook signing secrets, and any
  real phone number before you paste a log or a request.
- If you have found a security vulnerability, do not open a public issue. Follow
  [SECURITY.md](./SECURITY.md) instead.

## Filing an issue

Use the bug report or feature request template in the repository you are filing
against. Whichever you pick, the report is far more actionable when it says:

- **Which repository** the problem is in, and which version, tag, or commit.
- **Which SDK and language version** you are running — for example
  `Vobiz-Python-SDK` on Python 3.12, or `Vobiz-Node-SDK` on Node.js 22.
- **What you did**, as a minimal reproduction: the method call or the HTTP
  request, with credentials and real numbers redacted.
- **What you expected** and **what actually happened**, including the full error
  message, the HTTP status code, and the response body.

If the behaviour involves a live call, including the `call_uuid` and the
approximate timestamp helps us correlate it against the platform side.

## Opening a pull request

1. Fork the repository and create a branch off `main`.
2. Keep the change focused. One fix or one feature per pull request reviews far
   faster than a mixed batch.
3. Run whatever checks the repository documents in its README — build, tests,
   linters, or the validation commands for the agent skills repository.
4. Match the existing code style rather than reformatting surrounding code.
5. Write a clear commit message and pull request description: what changed, why,
   and how you verified it.
6. Confirm no credentials, production identifiers, or real phone numbers appear
   in the diff.

Documentation fixes, corrected examples, better error messages, and new tests are
all welcome and are reviewed on the same terms as code.

## A note on the generated SDKs

The official Vobiz SDKs — Node.js, Python, Go, Java, Ruby, and C# — are
**generated from the Vobiz OpenAPI specification** with
[Fern](https://buildwithfern.com). The client classes, method signatures,
request and response types, and enum constants in those repositories are build
output, not hand-written source.

That means a change to any of the following will not survive the next
regeneration, so it belongs upstream in the OpenAPI specification rather than in
a pull request against the SDK:

- a wrong or missing endpoint, path, or HTTP method
- a wrong parameter name, type, or required/optional flag
- a wrong response model or enum value
- an incorrect description carried through from the specification

If you spot one of these, please **open an issue** on the affected SDK
repository describing the mismatch between the SDK and the API. We will correct
the specification and the fix will flow into every language at once. Mentioning
which endpoint is affected and what the API actually returns is enough — you do
not need to find the spec change yourself.

Pull requests against the SDK repositories are very much welcome for everything
that is not generated: READMEs and usage guides, hand-written wrappers and
helpers, examples, tests, CI configuration, and packaging.

The sample application repositories and
[`Agent-Skills`](https://github.com/vobiz-ai/Agent-Skills) are entirely
hand-written, so pull requests there can touch any file.

## Licensing

Unless a repository states otherwise, contributions are accepted under that
repository's licence — MIT for the public SDKs, skills, and samples. By opening a
pull request you confirm you have the right to submit the code under that
licence.

## Questions

Open an issue on the relevant repository, or email
[piyush@vobiz.ai](mailto:piyush@vobiz.ai).
