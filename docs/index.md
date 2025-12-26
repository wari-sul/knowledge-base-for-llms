# Coolify + Docker Compose Knowledge Base

This documentation explains how Coolify works with Docker Compose deployments and how to correctly configure networking, domains, environment variables, storage, and deployment modes.

Coolify treats the `docker-compose.yml` file as the **single source of truth**, meaning configuration normally handled through UI must instead be defined in Compose.

---

## Sections

### Networking & Exposure
Learn how services communicate internally and externally.
→ See: [Networking](./networking.md)

### Environment Variables
Covers detected variables, required fields, shared variables, and magic variables.
→ See: [Environment Variables](./env-variables.md)

### Storage
Covers volumes, automatic directory creation, file content injection, and health checks.
→ See: [Storage](./storage.md)

### Deployment & Networks
Covers predefined networks and raw compose mode.
→ See: [Deployment](./deployment.md)
