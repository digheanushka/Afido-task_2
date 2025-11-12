# Afido-task_2
Web Application vunerabiity Scanning
What is web-app vulnerability scanning (quick)

##Automated tools and structured processes that probe a web application to find security weaknesses (injection, auth/logic flaws, misconfigurations, outdated components). Scans speed up discovery but don’t replace manual testing — they find low-hanging fruit and reduce the scope for deeper manual review.

Legal & ethical musts (don’t skip)

Always have written permission (scope, targets, allowed hours, accounts).

Define out-of-scope assets (third-party services, payment processors, public APIs you don’t own).

Use non-destructive settings on production (or test/staging environment).

Notify stakeholders in advance (ops, legal, incident response).


##Types of scans

Unauthenticated (blackbox) — no login; finds trivially exposed issues.

Authenticated (greybox) — scans with user credentials; finds issues behind login.

Dynamic Application Security Testing (DAST) — runtime scanning (ZAP, Burp).

Static Application Security Testing (SAST) — code analysis (SonarQube, Semgrep).

Dependency / Software Composition Analysis (SCA) — finds vulnerable libraries (OWASP Dependency-Check, Snyk).

Passive vs Active: passive listens/observes, active sends probes that may affect app behavior.


##Common tools (practical)

Short tool list and a one-line example to get started. Use test/staging first.

OWASP ZAP (DAST) — great free scanner with GUI + API.

Quick: run a baseline scan via Docker:
docker run --rm -v $(pwd):/zap/wrk/:Z owasp/zap2docker-stable zap-baseline.py -t https://example.com
