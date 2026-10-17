# Hola, soy Mateo Vazquez

Full-stack developer orientado a producto, integraciones, datos y automatización con IA.

Busco mi primera oportunidad IT en un equipo donde pueda crecer con code review, testing, buenas prácticas y producto real. Vengo de experiencia operativa en retail/logística y estoy construyendo proyectos aplicados con Java y Spring Boot, Next.js, TypeScript, APIs, pagos, datos, OCR, calendarios y automatización.

Formación verificada: Diplomatura en Professional Full-Stack Developer aprobada en UTN FRBA y Curso de Desarrollo con NodeJS con nota Excelente.

Portfolio público: https://mateocas1.github.io/portfolio/

## Proyectos principales

### rindetuplata — ¿dónde rinde tu plata hoy? (Java y Spring Boot)

Comparador argentino de rendimientos: plazos fijos por banco, fondos money market, billeteras remuneradas y cripto, ordenados por los pesos que ganás con tu monto y tu plazo, y por cuánto le ganan a la inflación.

- Repo: https://github.com/Mateocas1/rindetuplata
- Case study: https://mateocas1.github.io/portfolio/rindetuplata.html
- Problema: con inflación alta una tasa no dice si ganás plata; cada opción tiene topes, tramos y plazos mínimos, y ninguna fuente guarda el historial por banco o billetera.
- Resultado: ordena 398 opciones de ahorro por retorno real para cualquier monto y plazo, con ingesta diaria idempotente de 9 fuentes (Spring Batch), matemática financiera en `BigDecimal` probada contra valores calculados a mano, y alertas por email con outbox transaccional a RabbitMQ y login por magic link.
- Calidad: 450 tests de backend con Testcontainers (PostgreSQL y RabbitMQ reales), 398 de frontend y un end-to-end con Playwright sobre el stack completo en Docker Compose.
- Stack: Java 21, Spring Boot 4, Spring Batch, Spring Security, PostgreSQL, Flyway, RabbitMQ, Astro, React, Docker y GitHub Actions.
- Límite honesto: corre como preview privada; todavía no tiene despliegue público.

### Mena Nails — turnos, pagos y automatización para negocio local

Aplicación full-stack para digitalizar reservas, pagos de seña, comprobantes y agenda operativa de un salón de manicura/uñas.

- Demo vigente: https://test-kimi.vercel.app/
- Case study: https://mateocas1.github.io/portfolio/mena-nails.html
- Foco: producto real, reglas de disponibilidad, MercadoPago, transferencia con apoyo OCR, panel admin y Google Calendar.
- Stack: Next.js, React, TypeScript, Tailwind CSS, Convex, Clerk, MercadoPago, Gemini OCR, Google Calendar API, Vitest y Playwright.
- Límite honesto: OCR funciona como apoyo a revisión, no como autoridad final de pago.

### ShelfOps — operaciones de estantería con backend verificable

MVP backend para gestionar incidentes y operaciones de estantería.

- Repo y demo reproducible (`pnpm demo`): https://github.com/Mateocas1/shelfops
- Foco: contratos, autorización OIDC, concurrencia, idempotencia, PostgreSQL y CI.
- Stack: TypeScript, Fastify, PostgreSQL, OpenAPI y GitHub Actions.
- Límite honesto: backend de portfolio sin interfaz gráfica ni servicio SaaS desplegado.

### ofertasSUPER — comparador de ofertas y precios

Aplicación full-stack para buscar productos, comparar precios y armar una canasta local con foco en confianza del dato.

- Demo: https://ofertas-super.vercel.app
- Repo: https://github.com/Mateocas1/ofertaSUPER
- Case study: https://mateocas1.github.io/portfolio/ofertas-super.html
- Foco: APIs públicas, búsqueda, canasta local, ingesta, normalización/deduplicación, control de calidad de datos, cache/rate limiting y documentación de límites.
- Stack: Next.js, TypeScript, Prisma, Supabase/PostgreSQL, Redis, Clerk, Tailwind CSS y GitHub Actions.
- Límite honesto: demo/portfolio con smoke público; no afirmo producción cerrada ni ingesta productiva activa sin evidencia fresca.

### invent-stock — inventario operativo por Telegram

Proyecto orientado a operación de stock, alertas y consultas rápidas para negocio local.

- Case study: https://mateocas1.github.io/portfolio/invent-stock.html
- Foco: comandos Telegram, gestión de stock, alertas, métricas y deploy operativo.
- Límite honesto: lo presento como proyecto en evolución hasta cerrar evidencia pública y conexión final con Mena Nails.

## Cómo trabajo

- Priorizo claims verificables, documentación clara y debugging con evidencia.
- Uso IA como herramienta de ingeniería para planificar, dividir tareas, revisar errores, escribir tests y documentar decisiones.
- No uso IA como piloto automático: valido outputs, reviso tradeoffs y separo lo probado de lo supuesto.
- Me interesa aprender en equipo con code review, testing, arquitectura y buenas prácticas.

## Stack principal

Java · Spring Boot · RabbitMQ · React · Next.js · TypeScript · Node.js · APIs · PostgreSQL/Supabase · Prisma · Convex · Redis · Clerk · MercadoPago · Google Calendar · Gemini OCR · Playwright · Vitest · GitHub Actions

## Contacto

- Portfolio: https://mateocas1.github.io/portfolio/
- LinkedIn: https://www.linkedin.com/in/vazquezmateo
- GitHub: https://github.com/Mateocas1
- Email: castiglionemateo1@gmail.com
