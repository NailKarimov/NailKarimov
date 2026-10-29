# Testing map: type of testing → standard → repository → report

Which kinds of testing this portfolio covers, against which standard or specification, where the code is and
where the published report is. Every repository runs in GitHub Actions; reports are on GitHub Pages
(`https://nailkarimov.github.io/<repository>/`).

| Type of testing | Standard / reference | Repository | Tools | Report |
| --- | --- | --- | --- | --- |
| Functional API testing | ISO/IEC/IEEE 29119-4 techniques: boundary values, equivalence classes, decision tables | api-test-automation, python-testing, java-testing, dotnet-testing, go-testing | Playwright, pytest + httpx, REST Assured, NUnit + WebApplicationFactory, Go httptest | Allure, JaCoCo, coverage HTML |
| API collections | — | api-test-automation | Bruno (`bru run`) | Allure + Bruno HTML |
| Contract testing | OpenAPI 3, Pact specification v3 | contract-testing-lab, java-testing | Schemathesis, oasdiff, Pact JS, Pact JVM | pact files, oasdiff reports |
| Property-based testing and fuzzing | OpenAPI-driven generation | contract-testing-lab, python-testing, go-testing | Schemathesis, Hypothesis, `go test -fuzz` | Schemathesis report, CI logs |
| GraphQL | GraphQL specification | api-test-automation | Playwright, GraphQL Inspector | Allure |
| gRPC, WebSocket, SSE | gRPC status codes, RFC 6455, HTML SSE | api-protocols-testing | grpc-js, buf, ws | Allure |
| AI interfaces | Model Context Protocol, OWASP Top 10 for LLM applications | ai-api-testing | MCP Inspector, evals on Claude | Allure, eval results |
| Database and integration | ACID transactions | ledger-api-testing, python-testing | Testcontainers + PostgreSQL, SQLite | Allure |
| Security | OWASP API Security Top 10 (2023), OAuth 2.0 (RFC 6749) with PKCE (RFC 7636), JWT (RFC 7519) | ledger-api-testing, microservices-testing, api-test-automation, ui-e2e-testing | own auth server, header checks, BOLA tests | Allure |
| Mocking and service virtualisation | — | java-testing | WireMock (call counts, faults, stateful scenarios) | Allure |
| UI end-to-end | — | ui-e2e-testing, dotnet-testing | Playwright (TS, .NET), Page Object | Allure with traces and videos |
| Accessibility | WCAG 2.2 AA, EN 301 549 | ui-e2e-testing, web-quality-audit | axe-core, Pa11y, keyboard-only flows | Allure, Pa11y summary |
| Visual regression | — | ui-e2e-testing | Playwright `toHaveScreenshot` | Allure diffs |
| Web performance | Core Web Vitals (LCP, CLS, INP) | ui-e2e-testing | Lighthouse CI, user flows | Lighthouse reports |
| Load and capacity | ISO/IEC 25010 performance efficiency | microservices-testing, python-testing | k6 → Prometheus → Grafana, Locust | Grafana snapshots, k6 dashboard |
| Chaos and resilience | Principles of Chaos Engineering | microservices-testing, go-testing | container faults, own fault-injecting proxy, circuit breaker | Allure, coverage HTML |
| Concurrency | — | python-testing, java-testing, dotnet-testing, go-testing, ledger-api-testing | parallel requests, `-race` | CI |
| BDD | Gherkin | java-testing, dotnet-testing | Cucumber, Reqnroll | Allure, Cucumber HTML |
| Mobile (Android) | W3C WebDriver (Appium) | android-testing | JUnit, Espresso, Appium UiAutomator2 on an emulator | Allure, Espresso and Appium reports |
| Web quality audit: content, SEO, links | — | web-quality-audit | Playwright, a reference build | Allure |
| Mutation checks (test quality) | — | every repository with an own system; web-quality-audit uses a reference build instead | planted-bug scripts, differential runs | `mutants/result.md` on Pages |

## By language

| Language | Repository | Stack |
| --- | --- | --- |
| TypeScript | api-test-automation, contract-testing-lab, microservices-testing, ledger-api-testing, api-protocols-testing, ai-api-testing, ui-e2e-testing, web-quality-audit | Playwright, zod, Pact JS, k6 |
| Python | python-testing | pytest, Hypothesis, Schemathesis, Locust, Appium client |
| Java | java-testing | JUnit 5, REST Assured, WireMock, Cucumber, Pact JVM, JaCoCo |
| C# | dotnet-testing | NUnit, WebApplicationFactory, Reqnroll, Playwright .NET |
| Go | go-testing | `testing`, httptest, `-race`, fuzzing, benchmarks |
| Kotlin | android-testing | JUnit, Espresso |

All tools, with why each one is used and where it is in the code:
[toolbox](https://nailkarimov.github.io/api-test-automation/toolbox.html).
