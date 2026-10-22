# Nail Karimov — Senior QA Automation Engineer

15 years in software testing, 6 of them building test automation.
I design test strategies, build maintainable automation frameworks
and turn test results into clear reports and quality metrics.

### Focus

- UI and API test automation · Page Object, fixtures, CI-ready suites
- Accessibility (WCAG 2.2 / EN 301 549), performance (Core Web Vitals),
  privacy compliance (GDPR consent)
- Reporting and CI: Allure, GitHub Actions

### Portfolio

Which types of testing are covered, against which standards, and where: [testing map](testing-map.md) ·
[interactive version](https://nailkarimov.github.io/api-test-automation/testing-map.html).


| Project | What it shows |
| --- | --- |
| [3sMoneyTests](https://github.com/NailKarimov/3sMoneyTests) | Web quality audit of a fintech site: 61 Playwright tests, 9 documented defects, Allure report on GitHub Pages |
| [api-test-automation](https://github.com/NailKarimov/api-test-automation) | REST and GraphQL API testing: OpenWeather (zod contracts, boundary values, decision tables), Petstore CRUD on a private Docker container, Rick and Morty GraphQL with schema drift, security headers, a Bruno collection run in CI; 123 tests + 18 Bruno requests, daily CI, Allure on GitHub Pages |
| [contract-testing-lab](https://github.com/NailKarimov/contract-testing-lab) | Three layers of contract testing on Petstore: Schemathesis property-based fuzzing, oasdiff contract drift, Pact consumer-driven contracts |
| [microservices-testing](https://github.com/NailKarimov/microservices-testing) | 13-container Sock Shop in Docker: service and end-to-end tests, chaos, RabbitMQ events, OWASP API Top 10, k6 load tests (closed and open models) with metrics in Prometheus and a Grafana dashboard per run; 94 tests |
| [ledger-api-testing](https://github.com/NailKarimov/ledger-api-testing) | Own Ledger API on Fastify and PostgreSQL, tested with Testcontainers: atomic transfers, idempotency keys, concurrency, mutation check; OAuth 2.0 / JWT with its own authorization server (PKCE, forged tokens, BOLA); 119 tests |
| [api-protocols-testing](https://github.com/NailKarimov/api-protocols-testing) | Beyond REST on our own FX quotes service: gRPC (all four call kinds, deadlines, status codes, health, reflection, buf breaking checks), WebSocket and SSE (resume without gaps, heartbeats, close codes); 79 tests |
| [ai-api-testing](https://github.com/NailKarimov/ai-api-testing) | Testing AI-facing APIs: an MCP server of our own over stdio and Streamable HTTP (tool schemas, errors a model can act on, progress and cancellation, OAuth scopes, tool-poisoning guards, MCP Inspector as an independent client) and an LLM endpoint on Claude (plumbing tests on a fake API, evals for correctness, groundedness and prompt injection); 120 tests + 13 evals |
| [ui-e2e-testing](https://github.com/NailKarimov/ui-e2e-testing) | UI end-to-end on OWASP Juice Shop: the customer journey from search to order history, Page Objects with role locators, API login, Chromium / Firefox / WebKit / Pixel 7 / iPhone 15, traces and videos in Allure, flaky-test reporting; accessibility to WCAG 2.2 AA (axe with a ratchet, Pa11y as a second engine, keyboard-only checkout, reflow at 320 px) visual regression with baselines from Playwright's Docker image, and Lighthouse CI performance budgets with INP from a user flow; 22 defects found (DOM XSS, nameless controls, contrast); 217 tests + 12 screenshots |
| [python-testing](https://github.com/NailKarimov/python-testing) | **Python.** Own Bookshop API (FastAPI + SQLite): pytest + httpx, Hypothesis properties against an independent oracle, Schemathesis contract fuzzing, database integration, security, Locust load with p95 budgets (found a threading bug no functional test saw); 77 tests, 11/11 planted bugs caught |
| [java-testing](https://github.com/NailKarimov/java-testing) | **Java.** Own Library API on the JDK: REST Assured + JUnit 5 (boundary tables, JSON Schema, a race for the last copies), WireMock as a failing external catalogue with call counts, Cucumber for the lending rules, Pact JVM consumer and provider with states; 89 tests, 88 % coverage, 14/14 planted bugs caught |
| [dotnet-testing](https://github.com/NailKarimov/dotnet-testing) | **C#.** Own room-booking app on ASP.NET Core: NUnit + WebApplicationFactory in memory with a fake TimeProvider (overlap and boundary tables, ProblemDetails, a race for one slot), Reqnroll scenarios, Playwright for .NET on Kestrel; 54 tests, 100 % line coverage, 12/12 planted bugs caught |
| [android-testing](https://github.com/NailKarimov/android-testing) | **Kotlin / Android.** Own split-the-bill app: JUnit on the JVM, Espresso and Appium 3 (UiAutomator2) on an API 30 emulator in GitHub Actions; 33 tests, 7/7 planted bugs caught |
| [go-testing](https://github.com/NailKarimov/go-testing) | **Go.** Two services of our own behind a fault-injecting proxy: timeouts, idempotent retries, circuit breaker, concurrency under `-race`, native fuzzing, benchmarks; 14/14 planted bugs caught, 94.5 % coverage |

### Stack

Languages: TypeScript · Python · Java · C# · Go · Kotlin

Playwright · zod · Bruno · REST Assured · WireMock · Cucumber · Reqnroll · Pact · pytest · Espresso · Appium · Hypothesis · Locust · k6 · Allure · GitHub Actions · axe-core · Docker
