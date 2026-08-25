# Higress CNCF Incubation Application - Working Draft

This working draft follows the CNCF TOC
[Project Incubation Application v1.6](https://github.com/cncf/toc/blob/main/.github/ISSUE_TEMPLATE/template-incubation-application.md),
verified on 2026-08-25. The project-side application material is complete. The
remaining filing prerequisite is submission of 5-7 consenting adopter contacts
through the CNCF Adopter Interview Questionnaire.

## Review Project Moving Level Evaluation

- [ ] I have reviewed the TOC moving-level readiness triage guide, ensured the
  criteria are met before opening the issue, and understand that unmet criteria
  will result in closure.

Check this box immediately before filing, after the adopter contacts have been
submitted through the official questionnaire.

## Project information

- **Project repositories:**
  [`community`](https://github.com/higress-group/community),
  [`higress`](https://github.com/higress-group/higress),
  [`higress-console`](https://github.com/higress-group/higress-console),
  [`higress-standalone`](https://github.com/higress-group/higress-standalone),
  [`plugin-server`](https://github.com/higress-group/plugin-server), and
  [`wasm-go`](https://github.com/higress-group/wasm-go)
- **Project site:** <https://higress.ai/en/>
- **Subprojects:** `higress-console`, `higress-standalone`, `plugin-server`,
  and `wasm-go`; authoritative scope is in
  [`GOVERNANCE.md`](https://github.com/higress-group/community/blob/main/GOVERNANCE.md)
- **Related projects:** none declared for this application
- **Communication:**
  [`COMMUNITY.md`](https://github.com/higress-group/community/blob/main/COMMUNITY.md),
  including the public meeting process in
  [`MEETINGS.md`](https://github.com/higress-group/community/blob/main/MEETINGS.md)
- **Project points of contact:** Yuanxiao Zhao
  (<1766508902@qq.com>) and Yiquan Dong (<ch3cho@qq.com>)

## Incubation Criteria Summary

### Application Level Assertion

- [x] Higress is currently Sandbox. Its
  [Sandbox vote passed on 2026-03-12](https://github.com/cncf/sandbox/issues/445#issuecomment-4044548879),
  and it is applying to Incubation.
- [ ] Higress is applying to join CNCF directly at Incubation level. Not
  applicable; remove this option from the filed issue.

### Adoption Assertion

Public production adopters in
[`ADOPTERS.md`](https://github.com/higress-group/community/blob/main/ADOPTERS.md)
include Ant Digital, Kuaishou, Trip.com, Vipshop, and Labring.

- [ ] Submit 5-7 consenting adopter contacts through the official CNCF
  [Adopter Interview Questionnaire](https://docs.google.com/forms/d/1n1oLC6IKj5-7S_xeEjIdEjbtS9SWniuAo7IIOyLFuK8/edit)
  before DD assignment. CNCF conducts the interviews and adopter verification
  during DD; those interviews do not need to be completed before filing.

## Application Process Principles

### Suggested

- [ ] Engage with the appropriate domain-specific TAG(s) to present the
  technical architecture. This is suggested, not a filing prerequisite in
  v1.6. A future presentation should be linked here if completed.

### Required

- [x] Complete a General Technical Review. The project self-assessment is in
  [`general-technical-review.md`](https://github.com/higress-group/community/blob/main/docs/cncf/general-technical-review.md);
  the project copy was approved and merged in
  [#4177](https://github.com/higress-group/higress/pull/4177). The CNCF Project
  Reviews request is open as
  [cncf/toc#2266](https://github.com/cncf/toc/issues/2266); external verification
  and the dated TOC snapshot remain pending.
- [x] Complete a Governance Review. The self-assessment is in
  [`governance-review.md`](https://github.com/higress-group/community/blob/main/docs/cncf/governance-review.md),
  has no project-side Must-Fix items, and is submitted for external verification
  in [cncf/toc#2267](https://github.com/cncf/toc/issues/2267). The dated TOC
  snapshot remains pending.
- [x] All project metadata and resources are vendor-neutral. Higress can run on
  any conformant Kubernetes cluster across public clouds, private clouds,
  on-premises environments, and local environments. It does not require an
  Alibaba Cloud account, API, or commercial service. Alibaba Cloud currently
  sponsors a project-specific public registry for release image distribution;
  the image registry is configurable, and the images can be reproduced from
  public source. The historical `github.com/alibaba/higress` module path is
  retained for compatibility and does not create a runtime dependency.
  Alibaba Cloud's commercial Higress offering is a downstream distribution and
  has no additional authority in project governance. Other vendors may provide
  distributions and services on the same terms.
- [x] Review and acknowledgement of Sandbox expectations and maturity-level
  requirements. The Higress Sandbox vote passed on 2026-03-12, onboarding was
  [completed on 2026-06-17](https://github.com/cncf/sandbox/issues/481), and
  this application explicitly acknowledges the current requirements.
- [ ] Due Diligence Review. This is completed through CNCF review, resolution
  of concerns, and public comment after a ready application is filed.
- [x] Appropriate installation, end-user, reference, and sample documentation
  is linked from the project README and website.

## Governance and Maintainers

### Suggested

- [ ] Complete external verification with the CNCF Project Reviews subproject;
  [cncf/toc#2267](https://github.com/cncf/toc/issues/2267) is pending. This is
  suggested and does not block filing once the project copy is complete.
- [x] Governance is discoverable and version controlled.
- [x] Governance documents actual public decision, leadership, role,
  security-team, and recurring public meeting processes.
- [x] Governance documents vendor-neutral project direction and conflicts.
- [x] Leadership, contribution, CNCF request, governance, goal, and subproject
  decisions use a public process.
- [x] Function-based team assignment, onboarding, removal, conflicts, and
  retirement are documented.
- [x] The complete maintainer lifecycle is documented.
- [ ] Demonstrate a completed maintainer lifecycle event. Suggested; no public
  addition, replacement, or emeritus transition is yet linked.
- [x] Subproject scope, leadership model, contribution, status, and lifecycle
  are documented.

### Required

- [x] Current maintainers include names, GitHub contact, responsibility domain,
  and affiliation in
  [`MAINTAINERS.md`](https://github.com/higress-group/community/blob/main/MAINTAINERS.md).
- [x] Seven active maintainers are appropriate to the primary repository and
  four subprojects; the annual activity review links public evidence for each.
- [x] Code and documentation ownership matches the documented code-owner and
  maintainer roles.
- [x] The CNCF Code of Conduct is adopted and linked.
- [x] The Code of Conduct is cross-linked from governance.
- [x] All current subprojects are listed in governance.

## Contributors and Community

### Suggested

- [x] Contributor, code-owner, and maintainer roles form a contributor ladder;
  objective code-owner progression criteria remain an improvement item.

### Required

- [x] Issue and change submission are documented.
- [x] Public GitHub and Discord communication channels are documented.
- [x] All official project, subproject, and narrowly scoped non-public channels
  are inventoried in `COMMUNITY.md`.
- [x] The monthly Higress Community Meeting has a public schedule, joining
  information, agenda and meeting-record process in
  [`MEETINGS.md`](https://github.com/higress-group/community/blob/main/MEETINGS.md),
  and a recurring entry on the
  [LFX public calendar](https://zoom-lfx.platform.linuxfoundation.org/meetings/higress).
  Meeting notes are published in the
  [`meetings`](https://github.com/higress-group/community/tree/main/meetings)
  directory, beginning with the
  [2026-08-20 meeting](https://github.com/higress-group/community/blob/main/meetings/2026/2026-08-20.md).
- [x] Contribution documentation is maintained.
- [x] Contributor activity and recruitment are demonstrated through GitHub,
  DevStats, contribution labels, and maintainer activity links.

## Engineering Principles

### Suggested

- [x] The roadmap change process is documented in
  [`ROADMAP.md`](https://github.com/higress-group/community/blob/main/ROADMAP.md).
- [x] Regular release history is public in GitHub Releases and versioned
  release notes.

### Required

- [x] Project goals, differentiation, need, and cloud-native use cases are
  documented in the README and GTR.
- [x] What Higress does and why it exists are documented in the README and GTR.
- [x] A maintained public roadmap and change process are linked from
  `ROADMAP.md`.
- [x] Architecture and software design are documented in
  [`docs/architecture.md`](https://github.com/higress-group/higress/blob/main/docs/architecture.md)
  and the GTR.
- [x] The release process is documented in
  [`RELEASE.md`](https://github.com/higress-group/higress/blob/main/RELEASE.md).

## Security

### Suggested

- [ ] Complete a joint assessment with CNCF TAG Security and Compliance. This
  is suggested, not a v1.6 filing prerequisite.

### Required

- [x] Vulnerability reporting is documented in
  [`SECURITY.md`](https://github.com/higress-group/higress/blob/main/SECURITY.md).
- [x] Repository access controls are enforced. The protected `main` branch
  requires a CODEOWNER review and successful `license/cla`, `build`, `lint`
  (Go vet), and `Analyze (go)` (CodeQL) checks against the current base branch.
  Force pushes and branch deletion are disabled. The CodeQL and build controls
  are defined in the public
  [CodeQL](https://github.com/higress-group/higress/blob/main/.github/workflows/codeql-analysis.yaml)
  and
  [Build and Test](https://github.com/higress-group/higress/blob/main/.github/workflows/build-and-test.yaml)
  workflows. A project maintainer verified the branch protection settings on
  2026-08-25.
- [x] Named security-response membership, incident roles, two-person review,
  conflicts, report handling, and escalation are documented.
- [x] The Security Self-Assessment is documented in
  [`security-self-assessment.md`](https://github.com/higress-group/community/blob/main/docs/cncf/security-self-assessment.md)
  and submitted to `cncf/toc` in
  [#2268](https://github.com/cncf/toc/pull/2268). The canonical TOC copy remains
  under CNCF review.
- [x] Higress has achieved the
  [OpenSSF Best Practices Passing badge](https://www.bestpractices.dev/projects/12667).
  The result was verified on 2026-08-25. The supporting work includes CodeQL on
  pull requests, pushes to `main`, and a weekly schedule
  ([#4186](https://github.com/higress-group/higress/pull/4186)); an enforced Go
  vet warning gate
  ([#4193](https://github.com/higress-group/higress/pull/4193)); and an auditable
  disposition for all tracked Critical/High CodeQL findings
  ([#4207](https://github.com/higress-group/higress/issues/4207)). The `main`
  branch now requires the build, Go vet, and CodeQL checks, and the repository
  had no open Code Scanning alerts when verified on 2026-08-25.

## Ecosystem

### Required

- [x] The public adopter list records organizations, contacts, environment, and
  use cases.
- [x] At least three independent adopters report production use; five are
  publicly listed.
- [ ] TOC adopter verification is completed during DD after CNCF receives the
  adopter questionnaire. It is not a project-side filing prerequisite.
- [x] Integrations and compatibility with Kubernetes, Gateway API, Envoy,
  Istio, Prometheus/OpenTelemetry, OCI, service registries, and model providers
  are documented in the GTR, architecture, README, and user documentation.

## Current filing decision

The project-side criteria and application material are complete. File the
application after 5-7 consenting adopter contacts have been submitted through
the official questionnaire and check the readiness attestation at the top of
this document.

The CNCF review requests are already open:

- [Technical Review #2266](https://github.com/cncf/toc/issues/2266)
- [Governance Review #2267](https://github.com/cncf/toc/issues/2267)
- [Security Self-Assessment PR #2268](https://github.com/cncf/toc/pull/2268)

External verification, the dated TOC snapshots, adopter interviews, TOC adopter
verification, and Due Diligence continue after filing. CNCF reviewer
availability is not a project-side blocker after the project copies and review
requests are complete.
