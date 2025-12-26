# Networking & Service Exposure in Coolify

## Core Networking Model
When deploying Docker Compose stacks, Coolify:
- Creates an isolated Docker network per deployment
- Injects its proxy service into that network
- Allows internal communication using service names
- Prevents unintended exposure by default

Each stack is isolated unless explicitly configured otherwise.

---

## Making Services Public

### Recommended: Domain-Based Exposure
Assign a domain in Coolify:
- If service listens on port **80**
  - Use `http://example.com`
- If service listens on **another port**
  - Use `http://example.com:3000`

The port tells Coolify which container port to route to.  
Externally it is still proxied normally.

You can customize routing further using Coolify magic environment variables.

---

## Host Port Mapping (Use With Caution)
To expose directly on the host:

```yaml
ports:
  - "3000:3000"
```

Optional: restrict to localhost

```yaml
ports:
  - "127.0.0.1:3000:3000"
```

### Risks
- Bypasses Coolify proxy
- May unintentionally expose private services
- Dangerous if using same file in dev + prod

---

## Private/Internal Services
If you do **not**:
- assign a domain
- or map a port

Then the service remains private inside the Coolify network.

Internal access example:

```
http://backend:3000
http://auth:1234
```

This uses Docker DNS naming.

---

## Summary
| Feature | Behavior |
|--------|----------|
Domains | Safest & recommended |
Port Mapping | Direct exposure, risky |
No exposure | Service stays private |
Networking | Fully internal unless changed |
