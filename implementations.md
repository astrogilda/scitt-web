# SCITT Implementations

A list of projects and companies that have SCITT implementations.
As the draft evolves, each implementation should specify which version of the draft it's compatible with to enable interoperable testing.

## DataTrails

- Draft Version: [10](https://datatracker.ietf.org/doc/draft-ietf-scitt-architecture/10/)
- Documentation: [Quickstart: SCITT Statements (Preview)](https://docs.datatrails.ai/developers/developer-patterns/scitt-api/)

### DataTrails SCITT GitHub Action

- [SCITT GitHub Action](https://github.com/marketplace/actions/datatrails-scitt-api)

A GitHub Action for registering SCITT Signed Statements to DataTrails.

### DataTrails vCon Conserver Link

- [SCITT Conserver Link](https://github.com/vcon-dev/vcon-server/tree/main/server/links/scitt)

## agent-evidence-vectors

- Draft Version: the published RFCs, [RFC 9943](https://www.rfc-editor.org/rfc/rfc9943.html) (architecture) and [RFC 9942](https://www.rfc-editor.org/rfc/rfc9942.html) (receipts)
- Conformance vectors and reference verifier: [astrogilda/agent-evidence-vectors](https://github.com/astrogilda/agent-evidence-vectors)

A carriage profile and conformance corpus for SCITT Transparent Statements whose payload is an
in-toto Statement about what an automated agent did at run time. The corpus is 27 vectors, split
6 accept, 17 reject and 4 indeterminate, judged by a Go verifier that recomputes each outcome
from the signed bytes. The four indeterminate members are the ones to read first: each records a
question the two RFCs leave open, and the readings a conforming verifier could take, because a
corpus that answered them would be inventing a rule the standards do not carry. The profile the
corpus enforces is `profiles/scitt-cose.md`. Apache-2.0.
