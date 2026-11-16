# Nail Karimov — Senior QA Automation Engineer

ISTQB Certified Tester (Foundation Level), based in Riga. 14 years in software testing, 7 of them in test
automation, in banking and fintech, telecom billing, automotive e-commerce and access-control systems. I design
test strategies, build maintainable automation frameworks, and turn test results into clear reports and quality
metrics.

**Open to work:** QA automation and SDET roles in Riga or remote. [Contact me on LinkedIn](https://www.linkedin.com/in/karimovnail).

**Portfolio at a glance:** [nailkarimov.github.io](https://nailkarimov.github.io/) · all bug reports on the [defect board](https://github.com/users/NailKarimov/projects/2).

| | |
| --- | --- |
| **Experience** | SEB (test automation, C# and SQL, regulatory reporting) · Sun Finance (QA lead, PHP automation for loan platforms in 8 countries) · Tele2 (E2E billing migration) · Complevo for Mercedes-Benz · fintech and access-control platforms |
| **Programming languages** | TypeScript · Python · Java · C# · Go · Kotlin · SQL · PHP |
| **Testing** | UI and mobile · REST, GraphQL, gRPC, WebSocket, MCP · device protocols (Modbus RTU/TCP, SunSpec, OCPP 1.6 and 2.0.1) · energy control laws · contracts · databases · security · accessibility · performance and load · chaos · BDD |
| **Standards** | ISO/IEC/IEEE 29119 · ISO/IEC 25010 · WCAG 2.2 AA / EN 301 549 · OWASP API Top 10 · OAuth 2.0 · Core Web Vitals · Modbus · SunSpec · OCPP · IEC 61851-1 |
| **Portfolio** | 16 repositories, all in GitHub Actions with published reports. [Testing map](testing-map.md) ([interactive](https://nailkarimov.github.io/api-test-automation/testing-map.html)) · [toolbox](https://nailkarimov.github.io/api-test-automation/toolbox.html) |

## How every project is built

- **A system I can look inside.** Most projects test a service written for them, or a private copy in Docker
  instead of a shared sandbox. The tests can then check what was really stored, move the clock, and forge
  tokens.
- **Proof that the tests work.** Where the system is my own, bugs are planted on purpose, one at a time, and the
  tables show which test caught each one. On third-party systems, every defect found is pinned by a test that
  turns red when the defect is fixed.
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
| [ui-e2e-testing](https://github.com/NailKarimov/ui-e2e-testing) | TypeScript | OWASP Juice Shop in 5 browsers and devices: Page Objects with role locators, API login, accessibility to WCAG 2.2 AA, visual regression, Lighthouse CI budgets; 217 tests, 20 defects including a DOM XSS |
| [web-quality-audit](https://github.com/NailKarimov/web-quality-audit) | TypeScript | a web quality audit of a training shop, run on its bug build and on its clean build as the reference: functional, content, accessibility, SEO, responsive, speed, API; 86 runs, 17 defects |
| [android-testing](https://github.com/NailKarimov/android-testing) | Kotlin | an own Android app: JUnit, Espresso and Appium 3 on an emulator in GitHub Actions; 33 tests, 7/7 planted bugs caught |

### Devices and energy protocols

| Project | Language | What it shows |
| --- | --- | --- |
| [solar-inverter-testing](https://github.com/NailKarimov/solar-inverter-testing) | Python | an own simulator of a 5 kW solar inverter (Modbus RTU and TCP, SunSpec map) tested by three independent clients: hand-built frames, pymodbus and the official SunSpec client; grid-loss and over-temperature safety, power limits, fuzzing; 359 tests on three links, 38/38 planted bugs caught. [A visual page](https://nailkarimov.github.io/solar-inverter-testing/solar-inverter.html) explains the run to a reader with no technical background |
| [ev-charging-testing](https://github.com/NailKarimov/ev-charging-testing) | Python | an own simulator of an EV charge point speaking OCPP 1.6J and 2.0.1 over WebSocket: every message judged by the JSON schemas published with the standard, the reference `ocpp` library as the counterparty both ways; sessions, loss of network mid-charge, smart-charging limits, the 6 A floor of IEC 61851-1; 269 tests in four passes, 41/41 planted bugs caught. [A visual page](https://nailkarimov.github.io/ev-charging-testing/ev-charging.html) lets a reader plant a bug and watch a check turn red |
| [solar-surplus-charging](https://github.com/NailKarimov/solar-surplus-charging) | Python | a controller that charges an electric car from the surplus of a rooftop solar array, and the suite that prices its three promises in kilowatt-hours: buy nothing from the grid, spill nothing the car could take, leave the car alone; the same control law driven straight into the model, over Modbus TCP and over OCPP 1.6J and compared decision by decision; 125 tests, 37/37 planted bugs caught. [A visual page](https://nailkarimov.github.io/solar-surplus-charging/surplus-charging.html) shows a whole day with the grid line sitting on zero |

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
Pact · WireMock · Cucumber · Reqnroll · Bruno · pymodbus · pysunspec2 · k6 · Locust · Lighthouse CI · axe-core · Pa11y · Testcontainers ·
Docker · Prometheus · Grafana · Allure · GitHub Actions · Jira · Zephyr · Confluence · Azure Pipelines · Jenkins

## Contact

[LinkedIn](https://www.linkedin.com/in/karimovnail) · English, Russian, Latvian
