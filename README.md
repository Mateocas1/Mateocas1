# Hola, soy Mateo Vazquez

Full-stack developer orientado a producto, integraciones, datos y automatización con IA.

Busco mi primera oportunidad IT en un equipo donde pueda crecer con code review, testing, buenas prácticas y producto real. Vengo de experiencia operativa en retail/logística y estoy construyendo proyectos aplicados con Next.js, TypeScript, APIs, pagos, datos, OCR, calendarios y automatización.

Formación verificada: Diplomatura en Professional Full-Stack Developer aprobada en UTN FRBA y Curso de Desarrollo con NodeJS con nota Excelente.

Portfolio público: https://mateocas1.github.io/portfolio/

## Proyectos principales

### Mena Nails — turnos, pagos y automatización para negocio local

Aplicación full-stack para digitalizar reservas, pagos de seña, comprobantes y agenda operativa de un salón de manicura/uñas. Son dos repositorios privados: uno de turnos y pagos, y otro de inventario.

- Demo vigente: https://test-kimi.vercel.app/
- Case study: https://mateocas1.github.io/portfolio/mena-nails.html
- Turnos y pagos: la transferencia se verifica contra la API de Mercado Pago antes de leer la imagen, después pasa por un servicio propio de verificación de comprobantes y recién al final por OCR; ninguna de esas capas confirma el pago por su cuenta. Además: panel admin, alertas de operación por Telegram y sincronización con Google Calendar.
- Inventario: PWA local-first con API en Go y PostgreSQL para recetas, descuento de insumos por servicio, alertas de stock y precios con vigencia.
- Stack: Next.js, React, TypeScript, Tailwind CSS, Convex (funciones y almacenamiento de archivos), Clerk, MercadoPago, Google Calendar API, Vitest y Playwright; en el inventario, SvelteKit, Go, PostgreSQL, sqlc y OpenAPI.
- Límite honesto: los repositorios son privados, así que el código no es público. El OCR y el verificador de comprobantes son apoyo para la revisión de la dueña del salón, nunca autoridad final de pago. Lo desplegado es una demo, no un servicio en producción.

### ShelfOps — operaciones de estantería con backend verificable

MVP backend para gestionar incidentes y operaciones de estantería.

- Repo y demo reproducible (`pnpm demo`): https://github.com/Mateocas1/shelfops
- Foco: contratos, autorización OIDC, concurrencia, idempotencia, PostgreSQL y CI.
- Infraestructura como código: Terraform sobre AWS (VPC, RDS PostgreSQL, ECS Fargate, ALB, CloudFront, Secrets Manager, alarmas y presupuesto), con OIDC de GitHub para CI/CD sin claves guardadas y permissions boundary en todos los roles.
- Stack: TypeScript, Fastify, PostgreSQL, OpenAPI, GitHub Actions, Terraform y AWS (ECS, RDS, CloudFront, Cognito).
- Límite honesto: backend de portfolio sin interfaz gráfica. La infraestructura está verificada con `terraform validate`, tflint, checkov y el subconjunto que emula LocalStack; el `apply` real contra AWS sigue pendiente.

### ofertasSUPER — comparador de ofertas y precios

Aplicación full-stack para buscar productos, comparar precios y armar una canasta local con foco en la confianza del dato.

- Sitio: https://ofertasuper.com
- Repo: https://github.com/Mateocas1/ofertaSUPER
- Case study: https://mateocas1.github.io/portfolio/ofertas-super.html
- Foco: identidad GTIN-14, ingesta diaria en GitHub Actions sin depender de una PC, búsqueda, comparación por supermercado, canasta mixta y control de calidad del dato.
- Datos: snapshot del 2026-10-02 con ~2,7k productos y ~3,9k ofertas; `/bajas` con feed Atom; analítica con Parquet, DuckDB y dbt (índice de canasta contra el IPC del INDEC en `/inflacion`).
- Stack: Next.js, TypeScript, Prisma, PostgreSQL, Redis, Clerk, Tailwind CSS, GitHub Actions, DuckDB y dbt.
- Límite honesto: la frescura depende del refresh diario y el sitio siempre muestra el último snapshot con su fecha de observación; las promos bancarias y de fidelidad quedan fuera de esta versión; el índice de inflación publica un estado "datos insuficientes" mientras la serie no alcance una ventana comparable.

### mena-assistant — asistente por Telegram con MCP y LLM

Asistente que consulta y opera los sistemas de Mena Nails a través de herramientas MCP y un modelo de lenguaje, con confirmación humana obligatoria en cada escritura.

- Repo: privado por ahora (todavía no hay código público).
- Foco: tool calling con MCP, permisos por chat, propuestas con botón de confirmación (el modelo nunca escribe directo), auditoría con datos personales redactados, resumen diario a las 08:00 de Argentina y trazas OpenTelemetry.
- Evals: dataset de 87 casos con acierto de herramienta y de argumentos, fabricaciones y propuestas de escritura, más una comparación en vivo de 6 modelos (94–98,9 % de acierto de herramienta, 93,1–97,7 % de acierto de argumentos y ~1 % de fabricaciones) que define el modelo por defecto y el de respaldo con datos.
- Stack: TypeScript, Node.js, Telegram Bot API, MCP, tool calling con LLM, OpenTelemetry y Vitest.
- Límite honesto: el repositorio es privado y falta el deploy en la VM del salón, así que todavía no hay uso real de la dueña del negocio.

### receipt-verifier — verificador de comprobantes de transferencia

Servicio que extrae los datos de un comprobante bancario argentino y decide si se aprueba, se rechaza o va a revisión humana midiendo cuántas falsificaciones se le escapan.

- Repo: https://github.com/Mateocas1/receipt-verifier
- Foco: la pregunta interesante no es si el modelo lee un comprobante, sino cuántos aprueba de más; dataset etiquetado y versionado, set adversario, validador determinista que es el único que aprueba, cascada de extractores (modelo de visión → OCR local) con circuit breakers y servicio FastAPI.
- Resultados: sobre 150 comprobantes sintéticos (30 adversarios), la cascada y los modelos elegidos por medición (`deepseek-v4-flash` primario y `qwen3.8-flash` secundario) no aprobaron ninguna falsificación (0/30); los dos modelos descartados sí aprobaron 1 y 2 de 30.
- Stack: Python, FastAPI, Pydantic, Tesseract, pytest y Docker.
- Límite honesto: todos los números publicados salen de datos sintéticos; el espacio previsto para comprobantes reales anonimizados está vacío, así que la tasa de aprobaciones falsas todavía no está medida sobre datos reales.

### invent-stock — inventario operativo por Telegram (archivado)

Bot de inventario por Telegram que fue el precursor de `mena-nails`, el sistema que hoy lo reemplaza (inventario, recetas y alertas de stock con validación, historial y auditoría).

- Case study: https://mateocas1.github.io/portfolio/invent-stock.html
- Estado: archivado y sin mantenimiento; se conserva como referencia.

## Cómo trabajo

- Priorizo claims verificables, documentación clara y debugging con evidencia.
- Uso IA como herramienta de ingeniería para planificar, dividir tareas, revisar errores, escribir tests y documentar decisiones.
- No uso IA como piloto automático: valido outputs, reviso tradeoffs y separo lo probado de lo supuesto.
- Me interesa aprender en equipo con code review, testing, arquitectura y buenas prácticas.

## Stack principal

React · Next.js · SvelteKit · TypeScript · Node.js · Go · PostgreSQL · Prisma · Convex · Redis · Clerk · MercadoPago · Google Calendar · MCP y tool calling con LLM · Terraform · AWS (ECS, RDS, CloudFront, Cognito) · Python · FastAPI · DuckDB · dbt · Playwright · Vitest · pytest · GitHub Actions

## Contacto

- Portfolio: https://mateocas1.github.io/portfolio/
- LinkedIn: https://www.linkedin.com/in/vazquezmateo
- GitHub: https://github.com/Mateocas1
- Email: castiglionemateo1@gmail.com
