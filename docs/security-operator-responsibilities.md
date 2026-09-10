# Security responsibilities when running Higress

This guide is for the people who install and operate Higress. Higress applies
the routes and security policies you configure. You are responsible for choosing
those policies and securing the Kubernetes cluster and external services.

| Area | What Higress or its dependencies do | What you need to do |
| --- | --- | --- |
| Who can change configuration | The Kubernetes API server checks identity, RBAC permissions, and configured admission policies before Higress reads a resource. | Restrict who can change routes, Secrets, plugins, and permissions. Review the controller's broad permissions. Higress does not create a least-privilege policy for your organization. |
| Routes and plugin settings | Kubernetes checks resources against the installed schemas. Higress translates accepted configuration, and Envoy validates the configuration it receives. Individual plugins perform their own configuration checks. | Review custom resources (CRs) and plugin settings before applying them. A setting can be valid but unsafe, such as sending traffic to the wrong backend or disabling authentication. Use admission policies where you need additional restrictions. |
| Request protection | Envoy and installed plugins apply configured authentication, rate limits, timeouts, and other request policies. | Enable the protections your service needs and choose their values. Test both allowed and denied requests. Installing Higress does not automatically protect every route with authentication or rate limiting. |
| CPU, memory, and traffic limits | Kubernetes enforces configured container resource limits. Envoy and plugins apply the traffic limits you enable. | Set CPU and memory requests and limits, timeouts, and traffic limits for your workload. Test under load and monitor resource use. Default values may not suit your deployment. |
| Plugin code and OCI images | Higress loads the plugins you configure. Wasm provides runtime isolation, but a plugin can read or change traffic exposed to it. Native filters run inside the gateway process. | Install code from sources you trust. Review the publisher, image version, plugin configuration, and intended traffic scope. Use immutable image digests where supported. Verify signatures or attestations when available, using your deployment tooling; do not assume Higress performs that verification automatically. Project-wide signature and attestation coverage is incomplete. |
| Plugin scope | `defaultConfig` can apply across the selected gateway workload; `matchRules` select intended plugin execution by ingress, domain, or service. | Check which traffic a plugin will receive. Treat installed plugins as trusted code. Matching rules do not make a malicious plugin safe. |
| Secrets and external services | Higress uses the certificates, credentials, backends, and external integrations you configure. | Protect Secret access, rotate credentials, choose trusted services, and restrict network access. Review what request data plugins, logs, and external providers can receive. |
| Configuration outages | Envoy can keep serving with its last accepted configuration when updates stop. | Monitor configuration delivery. A policy change has not taken effect until the gateway receives it. If access must be revoked during an outage, use an independent control, such as blocking traffic at the network entry point. |

Before exposing a deployment, check that an unauthorized user cannot change
routes, Secrets, or plugins; an unauthenticated request is denied on protected
routes; and configured traffic limits take effect. Review logs to ensure they
do not expose credentials or sensitive request bodies. Keep admin and debug
endpoints restricted to trusted operators.

These are deployment checks, not a claim that every deployment is secure after
following this guide. The [security self-assessment](./cncf/security-self-assessment.md)
describes the current threats and known limitations. Report suspected Higress
vulnerabilities through the [project security policy](https://github.com/higress-group/higress/blob/main/SECURITY.md).
