# Awesome-Desktop-API-Proxy-Agent

## Top Desktop API Proxy & Agent Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Local Traffic Interception, API Debugging & Secure Tunneling*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Desktop API Proxy & Agents**. These tools run locally on your machine to intercept, inspect, and modify HTTP/HTTPS traffic—bypassing browser CORS restrictions, debugging mobile app requests, or exposing local services to the internet for webhook testing and demos.

**Examples** include Postman Desktop Agent, Proxyman, Charles Proxy, Fiddler Everywhere, mitmproxy, Burp Suite, OWASP ZAP, ngrok, and LocalXpose (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted traffic interception, open-source security proxies, and community-driven tunneling agents—ideal for developers and security testers seeking transparency and full control over their debugging traffic. The open-source landscape is exceptionally strong here: **mitmproxy** is the scriptable standard for automated interception [citation:5], **OWASP ZAP** remains the world's most deployed DAST proxy [citation:15], and **Requestly** combines an API client with an interceptor as a local-first Postman alternative [citation:18].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Postman Desktop Agent](https://www.postman.com/downloads/)** | Local agent that bypasses browser CORS limitations for the Postman web app. Routes API requests through your machine and network, supporting HTTP, WebSocket, Socket.IO, gRPC, MQTT, and GraphQL. **Does not support Safari**. Postman recommends the full desktop app for unrestricted use [citation:1]. | Free (included with Postman account) | **Free**: full agent functionality; Postman web app free tier is single-user only |
| **[Proxyman](https://proxyman.com/)** | Native macOS/Windows/Linux HTTPS debugging proxy with iOS companion app. Features SSL proxying, breakpoints, Map Local/Remote, scripting, network conditions, and request/response diffing. **Commercial use requires a paid license after a 2-week trial**; personal use trial is unlimited [citation:2]. | Pro license (quote via website); iOS Premium subscription from ~S$12.98/month  | **Personal trial**: unlimited duration with feature limits (2 pinned domains, 2 rules per tool); **Commercial trial**: 2 weeks |
| **[Charles Proxy](https://www.charlesproxy.com/)** | Long-standing cross-platform HTTP/HTTPS proxy with SSL proxying, bandwidth throttling, breakpoints, rewrite rules, and AJAX/AMF inspection. Charles 5 is a paid upgrade from v4 [citation:3][citation:13]. | New license: USD $50 (estimated from upgrade pricing: $20 upgrade = 40% of new) [citation:3] | Free trial with 30-minute session limits and nag screen |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler)** | Cross-platform web debugging proxy with traffic capture, inspection, rules-based modification, and team collaboration. SOC 2, HIPAA, and GDPR compliant [citation:4]. | Lite: **$7/user/month** (annual); Pro: **$13/user/month**; Enterprise: **$37/user/month** [citation:4] | **Lite** plan available; Pro features require paid subscription |
| **[ngrok](https://ngrok.com/)** | Secure tunneling agent exposing local services to the internet. Essential for webhook testing and local API demos. Free and Hobbyist plans allow up to **3 simultaneous endpoints** [citation:8]. | Pay-as-you-go: **$20/month** base (includes $20 usage); endpoint hours and traffic billed beyond [citation:8] | **Free/Hobbyist**: 3 simultaneous endpoints, included credit for limited usage |
| **[LocalXpose](https://localxpose.io/)** | Tunneling service for exposing local HTTP/HTTPS/TCP/UDP services. Starter plan is free with **2 active tunnels** and unique subdomains [citation:9]. | PRO: **$8/month** (annual, $96/year); Starter: **$0** [citation:9] | **Starter (free)**: 2 active HTTP/HTTPS tunnels, SSL/TLS encryption, unique subdomains [citation:9] |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** | [![Stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | **The standard open-source scriptable intercepting proxy.** Interactive SSL/TLS-capable proxy for HTTP/1, HTTP/2, and WebSockets. Intercept and modify requests/responses on the fly, save conversations for replay, and use **Python scripts** to automate changes. Transparent proxy mode on macOS/Linux; SSL certificates generated on the fly [citation:5]. **Best for developers who want to automate traffic manipulation.** |
| **[OWASP ZAP](https://github.com/zaproxy/zaproxy)** | [![Stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=social&color=white)](https://github.com/zaproxy/zaproxy/stargazers) | **The world's most widely deployed open-source DAST proxy.** Intercepting proxy with passive scanning (safe, no attack traffic) and active scanning (intrusive, test environments only). Includes traditional and AJAX spiders for JavaScript-heavy apps. **Baseline scans are CI-ready**—run `zap-baseline.py` on every PR for security header checks without risk [citation:7][citation:15]. **Best for security testing integrated into CI/CD.** |
| **[Burp Suite Community Edition](https://github.com/PortSwigger/burp)** | [![Stars](https://img.shields.io/github/stars/PortSwigger/burp?style=social&color=white)](https://github.com/PortSwigger/burp/stargazers) | Free edition of the professional web security testing toolkit. Includes HTTP(S)/WebSocket proxy and history, Repeater, Decoder, Sequencer, and Comparer. **Intruder is demo-only** (rate-limited); the full web vulnerability scanner is Pro-only [citation:6]. **Best for learning AppSec and manual testing.** |
| **[Requestly](https://github.com/requestly/requestly)** | [![Stars](https://img.shields.io/github/stars/requestly/requestly?style=social&color=white)](https://github.com/requestly/requestly/stargazers) | **Local-first combination of API client and HTTP interceptor.** Positioned as a free alternative to Postman and Charles Proxy. Desktop app or browser extension. Features REST client, environments, URL redirects (Map Local/Remote), header/body modification, API mocking, and 1-click imports from Postman and Charles [citation:18]. **Best for teams wanting API testing and interception in one local-first tool.** |
| **[Inspectr](https://github.com/inspectr-hq/inspectr)** | [![Stars](https://img.shields.io/github/stars/inspectr-hq/inspectr?style=social&color=white)](https://github.com/inspectr-hq/inspectr/stargazers) | Lightweight API request inspector with proxy mode, live traffic monitor, webhook capture, and **OpenAPI-based mock mode** (beta). Point your frontend at Inspectr's proxy URL to inspect requests without modifying backend code. Can expose local endpoints publicly for webhook testing [citation:22]. **Best for frontend developers debugging API integrations.** |
| **[apiflow](https://github.com/wildsell/apiflow)** | [![Stars](https://img.shields.io/github/stars/wildsell/apiflow?style=social&color=white)](https://github.com/wildsell/apiflow/stargazers) | **Fully free open-source Postman/Apifox alternative with offline and self-hosted capabilities.** API testing, Mock, WebSocket, AI Agent, team collaboration, and local-first design. Docker deployment for enterprise private hosting. OpenAPI 3.0 import/export; 1-click export to Postman . **Best for teams wanting a self-hosted Postman replacement with no paid tiers.** |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Viaduct](https://pypi.org/project/viaduct-sh/)** | — | Open-source tunneling client with **access control built in**. Expose local services with `--basic-auth`, `--bearer` token, or `--allow-ip` restrictions enforced at the edge. Python and Node clients; pytest fixture for webhook testing. Self-hostable server [citation:17]. **Best for secure webhook testing without a paid ngrok plan.** |
| **[Gatecrash](https://pkg.go.dev/github.com/jclement/gatecrash)** | — | Self-hosted tunneling server with **passkey authentication, OIDC, IP allowlists, and audit logging**. Designed as a public edge—do not put behind a reverse proxy. Revocable sessions and service secrets for CI/webhooks [citation:25]. **Best for teams needing auditable, self-hosted tunnel infrastructure.** |

**Frameworks for building custom systems**: Choose **mitmproxy** for scriptable, automated traffic interception in Python; **OWASP ZAP** for CI-integrated security scanning; **Requestly** or **apiflow** for local-first API testing with interception; and **Viaduct** or **Gatecrash** for secure, self-hosted tunneling—creating a fully open-source desktop proxy and agent stack without paid licenses.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Desktop proxies intercept sensitive traffic including credentials and session tokens; **only intercept traffic you own or have explicit permission to inspect**. Install root certificates only in controlled environments and remove them when finished.
- **Commercial proxies have significant licensing constraints.** Proxyman requires paid licenses for commercial use after a 2-week trial; personal use is unlimited but feature-limited [citation:2]. Charles Proxy is paid software with a session-limited trial [citation:3]. **Free tunneling tiers are constrained**: ngrok's free plan allows only **3 simultaneous endpoints** [citation:8], and LocalXpose's Starter plan offers **2 active tunnels** [citation:9]. Open-source alternatives like **Viaduct** and **Gatecrash** provide self-hosted tunneling without endpoint limits, but require server infrastructure. **Burp Suite Community Edition's Intruder is demo-only**—the full attack tooling requires Pro [citation:6].

---

**Made for developers, QA engineers, security testers, and teams debugging API traffic.**  
Let's make desktop API proxying and tunneling more open, scriptable, and secure.
