## Mateo Vazquez Castiglione

**Desarrollador backend e integraciones con IA** · Buenos Aires. Construyo backend en TypeScript/Node y PostgreSQL, y también en Python, Go y Java. Integro LLMs en flujos reales con confirmación humana y evals.

| Proyecto | Qué es | Estado | Stack | Link |
|---|---|---|---|---|
| **Mena Nails** (clienta, may – oct 2026) | Turnos con seña, stock y un asistente de Telegram para un estudio de uñas. El asistente no escribe nada sin confirmación humana; elegí su modelo con un eval de 87 casos sobre 6 LLMs (84 de 87 aprobados completos) | Trabajo terminado, en pre-lanzamiento. Públicos el verificador y el asistente | Go, PostgreSQL, TypeScript, MCP, Python | [receipt-verifier](https://github.com/Mateocas1/receipt-verifier): 0 de 30 comprobantes adversariales aprobados (set sintético de 150) · [mena-assistant](https://github.com/Mateocas1/mena-assistant): respuestas en streaming y memoria por chat |
| **ofertaSUPER** | Compara 5 supermercados sobre unos 24.500 productos. Un índice por EAN bajó la CPU por página de 10-16 s a 18-173 ms (réplica local) | Sitio pausado por Vercel hasta el 14/11; refresh diario verde desde el 27/10 | TypeScript, Next.js, PostgreSQL, GitHub Actions | [repo](https://github.com/Mateocas1/ofertaSUPER) |
| **Rinde tu Plata** | Dónde rinden más los pesos frente a la inflación esperada. Outbox hacia RabbitMQ, at-least-once con deduplicación | No desplegado; 905 tests backend contra PostgreSQL y RabbitMQ reales | Java 21, Spring Boot, PostgreSQL, RabbitMQ | [repo](https://github.com/Mateocas1/rindetuplata) |
| **Planner** | App de escritorio con un agente LLM que solo modifica datos mediante acciones que el usuario confirma | Repo público con CI; 1.013 tests unitarios y 449 E2E medidos localmente | Tauri 2, Rust, React, Firestore | [repo](https://github.com/Mateocas1/planner) |

Cada proyecto está contado como historia (problema, qué descubrí, qué construí, resultado, qué cambiaría) en el [portfolio](https://mateocas1.github.io/portfolio/).

**Cómo trabajo.** Diseño, decido y verifico: defino los tests, los criterios de revisión y las mediciones. Agentes de IA escriben buena parte del código bajo esos tests y esa revisión.

**Busco** un puesto de backend o de integraciones con IA, full-time, con inicio inmediato, remoto o híbrido en AMBA. castiglionemateo1@gmail.com · [LinkedIn](https://www.linkedin.com/in/vazquezmateo) · [Portfolio](https://mateocas1.github.io/portfolio/)

Frontend cuando hace falta: React, Next.js, Astro, Svelte.

---

**English.** Backend & AI integrations developer in Buenos Aires: I build backends in TypeScript/Node and PostgreSQL, and also in Python, Go and Java, and I integrate LLMs into real workflows with human confirmation and evals. Above, in order: client work for a nail studio (May – Oct 2026, finished, pre-launch), whose public pieces are a receipt verifier that approved 0 of 30 synthetic adversarial receipts and the Telegram assistant; a price comparator for 5 supermarkets whose CPU fix took pages from 10-16 s to 18-173 ms on a local replica; a Java/Spring service with 905 backend tests; and a desktop planner whose LLM agent only changes data through actions the user confirms. I design, decide and verify: I define the tests, the review criteria and the measurements. AI agents write much of the code under those tests and that review. English: C1. Looking for a full-time role, available immediately, remote or hybrid in Buenos Aires.
