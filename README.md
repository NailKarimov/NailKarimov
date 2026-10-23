# Nail Karimov — Senior QA Automation Engineer

15 years in software testing, 6 of them building test automation. I design test strategies, build maintainable
automation frameworks, and turn test results into clear reports and quality metrics.

| | |
| --- | --- |
| **Languages** | TypeScript · Python · Java · C# · Go · Kotlin |
| **Testing** | UI and mobile · REST, GraphQL, gRPC, WebSocket, MCP · contracts · databases · security · accessibility · performance and load · chaos · BDD |
| **Standards** | ISO/IEC/IEEE 29119 · ISO/IEC 25010 · WCAG 2.2 AA / EN 301 549 · OWASP API Top 10 · OAuth 2.0 · Core Web Vitals |
| **Portfolio** | 13 repositories, all in GitHub Actions with published reports. [Testing map](testing-map.md) ([interactive](https://nailkarimov.github.io/api-test-automation/testing-map.html)) · [toolbox](https://nailkarimov.github.io/api-test-automation/toolbox.html) |

## How every project is built

- **A system I can look inside.** Most projects test a service written for them, or a private copy in Docker
  instead of a shared sandbox. The tests can then check what was really stored, move the clock, and forge
  tokens.
- **Proof that the tests work.** In every project, bugs are planted on purpose, one at a time, and the tables show
  which test caught each one.
- **One layout.** Every README follows the same order: at a glance, what is tested, findings, running it,
  structure, CI, documentation. Each repository has a test plan and a test summary report (ISO/IEC/IEEE 29119-3),
  a text guide and an interactive guide for every tool.

## Portfolio

### API and contracts

| Project | Language | What it shows |
| --- | --- | --- |
| [api-test-automation](https://github.com/NailKarimov/api-test-automation) | TypeScript | REST and GraphQL: OpenWeather (zod contracts, boundary values, decision tables), Petstore in a private container, Rick and Morty GraphQL with schema drift, security headers, a Bruno collection in CI; 123 tests + 18 Bruno requests |
| [contract-testing-lab](https://github.com/NailKarimov/contract-testing-lab) | TypeScript | three layers of contract testing on Petstore: Schemathesis fuzzing (83 spec violations → 8 defects), oasdiff drift, Pact consumer-driven contracts |
| [api-protocols-testing](https://github.com/NailKarimov/api-protocols-testing) | TypeScript | an own FX quotes service over gRPC (four call kinds, deadlines, buf breaking checks), WebSocket and SSE (resume without gaps); 79 tests, 26/26 planted bugs caught |
| [ai-api-testing](https://github.com/NailKarimov/ai-api-testing) | TypeScript | an own MCP server (two transports, scopes, tool-poisoning guards) and an LLM endpoint on Claude (plumbing on a fake API, evals for groundedness and prompt injection); 126 tests + 13 evals |

### Systems, data and security

| Project | Language | What it shows |
| --- | --- | --- |
| [ledger-api-testing](https://github.com/NailKarimov/ledger-api-testing) | TypeScript | an own money service on PostgreSQL with Testcontainers (atomicity, idempotency, races) and an own OAuth 2.0 server (PKCE, 11 forged tokens, BOLA); 119 tests, 18/18 planted bugs caught |
| [microservices-testing](https://github.com/NailKarimov/microservices-testing) | TypeScript | 13-container Sock Shop: service and end-to-end tests, chaos, RabbitMQ events, OWASP API Top 10, k6 load (closed and open models) with Grafana dashboards per run; 94 tests, 18 defects |

### UI and mobile

| Project | Language | What it shows |
| --- | --- | --- |
| [ui-e2e-testing](https://github.com/NailKarimov/ui-e2e-testing) | TypeScript | OWASP Juice Shop in 5 browsers and devices: Page Objects with role locators, API login, accessibility to WCAG 2.2 AA, visual regression, Lighthouse CI budgets; 217 tests, 22 defects including a DOM XSS |
| [3sMoneyTests](https://github.com/NailKarimov/3sMoneyTests) | TypeScript | an independent audit of a fintech website: functional, responsive, accessibility, performance, SEO, links, GDPR consent; 10 documented defects |
| [android-testing](https://github.com/NailKarimov/android-testing) | Kotlin | an own Android app: JUnit, Espresso and Appium 3 on an emulator in GitHub Actions; 33 tests, 7/7 planted bugs caught |

### The same ideas in other languages

| Project | Language | What it shows |
| --- | --- | --- |
| [python-testing](https://github.com/NailKarimov/python-testing) | Python | an own Bookshop API: pytest + httpx, Hypothesis against an oracle, Schemathesis, Locust (found a threading bug under load); 77 tests, 11/11 planted bugs caught |
| [java-testing](https://github.com/NailKarimov/java-testing) | Java | an own Library API: REST Assured, WireMock with call counts, Cucumber, Pact JVM; 89 tests, 88 % coverage, 14/14 planted bugs caught |
| [dotnet-testing](https://github.com/NailKarimov/dotnet-testing) | C# | an own booking app on ASP.NET Core: WebApplicationFactory with a fake clock, Reqnroll, Playwright for .NET; 54 tests, 12/12 planted bugs caught |
| [go-testing](https://github.com/NailKarimov/go-testing) | Go | own microservices behind a fault-injecting proxy: idempotent retries, circuit breaker, `-race`, fuzzing; 94.5 % coverage, 14/14 planted bugs caught |

The [qa-project-template](https://github.com/NailKarimov/qa-project-template) is the starter for new projects and
holds the [portfolio standard](https://github.com/NailKarimov/qa-project-template/blob/main/docs/portfolio-standard.md).

## Stack

Playwright · REST Assured · pytest · NUnit · JUnit · Go `testing` · Espresso · Appium · Hypothesis · Schemathesis ·
Pact · WireMock · Cucumber · Reqnroll · Bruno · k6 · Locust · Lighthouse CI · axe-core · Pa11y · Testcontainers ·
Docker · Prometheus · Grafana · Allure · GitHub Actions
