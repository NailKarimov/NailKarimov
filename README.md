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

| Project | What it shows |
| --- | --- |
| [3sMoneyTests](https://github.com/NailKarimov/3sMoneyTests) | Web quality audit of a fintech site: 61 Playwright tests, 9 documented defects, Allure report on GitHub Pages |
| [api-test-automation](https://github.com/NailKarimov/api-test-automation) | REST and GraphQL API testing: OpenWeather (zod contracts, boundary values, decision tables), Petstore CRUD on a private Docker container, Rick and Morty GraphQL with schema drift, security headers; 123 tests, daily CI, Allure on GitHub Pages |
| [contract-testing-lab](https://github.com/NailKarimov/contract-testing-lab) | Three layers of contract testing on Petstore: Schemathesis property-based fuzzing, oasdiff contract drift, Pact consumer-driven contracts |
| [microservices-testing](https://github.com/NailKarimov/microservices-testing) | 13-container Sock Shop in Docker: service and end-to-end tests, chaos, RabbitMQ events, OWASP API Top 10, k6 load tests; 94 tests |
| [ledger-api-testing](https://github.com/NailKarimov/ledger-api-testing) | Own Ledger API on Fastify and PostgreSQL, tested with Testcontainers: atomic transfers, idempotency keys, concurrency, mutation check; OAuth 2.0 / JWT with its own authorization server (PKCE, forged tokens, BOLA); 119 tests |
| [api-protocols-testing](https://github.com/NailKarimov/api-protocols-testing) | Beyond REST on our own FX quotes service: gRPC (all four call kinds, deadlines, status codes, health, reflection, buf breaking checks), WebSocket and SSE (resume without gaps, heartbeats, close codes); 79 tests |
| [ai-api-testing](https://github.com/NailKarimov/ai-api-testing) | Testing AI-facing APIs: an MCP server of our own over stdio and Streamable HTTP (tool schemas, errors a model can act on, progress and cancellation, OAuth scopes, tool-poisoning guards, MCP Inspector as an independent client) and an LLM endpoint on Claude (plumbing tests on a fake API, evals for correctness, groundedness and prompt injection); 120 tests + 13 evals |
| [ui-e2e-testing](https://github.com/NailKarimov/ui-e2e-testing) | UI end-to-end on OWASP Juice Shop: the customer journey from search to order history, Page Objects with role locators, API login, Chromium / Firefox / WebKit / Pixel 7 / iPhone 15, traces and videos in Allure, flaky-test reporting, 8 UI defects found (DOM XSS, nameless controls); 35 tests × 5 browsers |

### Stack

Playwright · TypeScript · zod · Allure · GitHub Actions · axe-core · Docker
