# ⚙️ n8n Automation Portfolio — Alberto Duque

Selección curada de workflows de **n8n** desarrollados en entornos productivos, sanitizados y documentados para portafolio público. Cada carpeta es un proyecto independiente con su propio README, diagrama de arquitectura y guía de despliegue.

De más de 90 workflows revisados, se descartaron pruebas, copias y flujos desechables (`TEST`, `PRUEBA`, `My workflow N`, duplicados), quedando solo los que aportan valor real de portafolio y los que se complementan entre sí como un sistema.

---

## 📂 Proyectos

| Proyecto | Descripción | Stack |
|---|---|---|
| [`enterprise-bulk-data-automation/`](./enterprise-bulk-data-automation) | Motor genérico config-driven (3 workflows) para generar plantillas e insertar masivamente cualquier entidad, integrado con la API FastAPI `enterprise-template-api`. | `n8n` `FastAPI` `SQL Server` `JavaScript` |
| [`devops-chatops-bridge/`](./devops-chatops-bridge) | Agente de IA (LangChain + OpenAI + MCP) que ejecuta operaciones DevOps desde Teams/Telegram. | `n8n` `OpenAI` `LangChain` `PostgreSQL` `Azure` |
| [`jarvis-ai-assistant/`](./jarvis-ai-assistant) | Asistente personal de IA modular con Telegram, calendario y recordatorios. | `n8n` `Telegram` `PostgreSQL` `Redis` `Google Calendar` |

---

## 🔒 Sobre la sanitización

Todos los workflows en este repositorio fueron revisados y limpiados de información sensible antes de publicarse:

- Dominios y URLs internas de la empresa original → reemplazados por dominios de ejemplo (`yourcompany.example`).
- URLs firmadas de Azure Logic Apps (SAS) y claves de Azure Functions → reemplazadas por placeholders.
- Correos, teléfonos, IDs de chat/calendario y códigos secretos → anonimizados.
- Se **excluyó** cualquier workflow que contuviera secretos hardcodeados irremplazables (ej. client secrets de OAuth).

Las credenciales de n8n (`credentials`) nunca incluyen el secreto real en el export — solo un ID y nombre de referencia — pero igual se revisó cada nodo `Code` / `HTTP Request` en busca de valores embebidos manualmente.

---

## 👤 Autor

**Alberto José Duque Gámez** — Backend & Automation Engineer
[GitHub](https://github.com/AlbertoDuque1006) · [LinkedIn](https://www.linkedin.com/in/alberto-jose-duque-gamez-088a04355/) · albertoduquegamez@gmail.com
