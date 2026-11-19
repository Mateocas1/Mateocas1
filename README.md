## Mateo Vazquez Castiglione

**Desarrollador backend e integraciones con IA** · Buenos Aires. Construyo backend en TypeScript/Node y PostgreSQL, y también en Python, Go y Java. Integro LLMs en flujos reales con confirmación humana y evals.

Busco un puesto de backend o de integraciones con IA, full-time, con inicio inmediato, remoto o híbrido en AMBA. Inglés: C1.
[Portfolio](https://mateocas1.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/vazquezmateo) · castiglionemateo1@gmail.com

### ofertaSUPER · [ofertasuper.com](https://ofertasuper.com) · [repo](https://github.com/Mateocas1/ofertaSUPER)

Comparador de precios de Carrefour, Coto, Disco, Jumbo y Vea: muestra el precio y la oferta de cada producto en cada cadena y permite armar una canasta que mezcla tiendas. Cubre más de 25.000 productos. Un job diario en GitHub Actions lee los catálogos (la API de VTEX y la búsqueda de Coto), une cada producto por su código GTIN-14 y lo concilia en PostgreSQL bajo un advisory lock. El sitio sirve ese catálogo como un snapshot JSON versionado, sin base de datos al leer y a costo USD 0.
`TypeScript` `Next.js` `PostgreSQL` `GitHub Actions`

### Mena Nails · trabajo para una clienta, may – oct 2026 · [receipt-verifier](https://github.com/Mateocas1/receipt-verifier) · [mena-assistant](https://github.com/Mateocas1/mena-assistant)

Un estudio de uñas necesitaba reservas con seña online y poder consultar turnos y stock desde el celular. Hice la API de inventario, un asistente de Telegram que no escribe nada hasta que la dueña lo confirma con un botón, y un verificador de comprobantes donde la aprobación la decide código determinístico y no el modelo. Elegí el modelo del asistente con un eval propio de 87 casos sobre 6 LLMs: el elegido aprobó completos 84 de 87. Con los modelos elegidos, el verificador aprobó 0 de 30 comprobantes adversariales en un set sintético de 150. El trabajo está terminado y quedó en pre-lanzamiento.
`Go` `PostgreSQL` `TypeScript` `MCP` `Python`

### Rinde tu Plata · [repo](https://github.com/Mateocas1/rindetuplata)

Muestra dónde rinden más los pesos (plazo fijo, fondos money market, billeteras) y si cada opción le gana a la inflación esperada. Los datos llegan de 9 fuentes que fallan cada una a su manera: con un job de Spring Batch por fecha, re-ejecutar un día no duplica datos y una fuente caída no frena a las demás. Las alertas salen por un outbox hacia RabbitMQ (at-least-once con deduplicación), con tests de integración contra PostgreSQL y RabbitMQ reales. Todavía no está desplegado.
`Java 21` `Spring Boot` `PostgreSQL` `RabbitMQ`

### Planner · [repo](https://github.com/Mateocas1/planner)

App de escritorio con un agente LLM que organiza tareas pero no puede cambiar nada sin que el usuario lo confirme en una tarjeta. La API key queda en el keyring del sistema y la llamada HTTPS la hace Rust, así que nunca llega al webview. Un `delete_all` inyectado en un mail pegado queda inerte, y un test lo prueba. El CI corre los tests unitarios y los del núcleo en Rust.
`Tauri 2` `Rust` `React` `Firestore`

**Cómo trabajo.** Diseño, decido y verifico: defino los tests, los criterios de revisión y las mediciones. Agentes de IA escriben buena parte del código bajo esos tests y esa revisión. Cada proyecto está contado con el problema, la decisión y el resultado en el [portfolio](https://mateocas1.github.io/portfolio/).

Frontend cuando hace falta: React, Next.js, Astro, Svelte.

---

**English.** Backend & AI integrations developer in Buenos Aires: I build backends in TypeScript/Node and PostgreSQL, and also in Python, Go and Java, and I integrate LLMs into real workflows with human confirmation and evals. Above: [ofertaSUPER](https://ofertasuper.com), a live price comparator for 5 Argentine supermarkets with more than 25,000 products, fed by a daily GitHub Actions pipeline that matches products by GTIN-14 in PostgreSQL; client work for a nail studio (May – Oct 2026, finished, pre-launch) whose public pieces are a receipt verifier that approved 0 of 30 synthetic adversarial receipts with the chosen models and a Telegram assistant that writes nothing until the owner confirms; a Java/Spring savings comparator with integration tests against real PostgreSQL and RabbitMQ; and a desktop planner whose LLM agent only changes data through actions the user confirms. I design, decide and verify: I define the tests, the review criteria and the measurements. AI agents write much of the code under those tests and that review. English: C1. Looking for a full-time role, available immediately, remote or hybrid in Buenos Aires.
