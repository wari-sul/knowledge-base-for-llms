# Deployment & Advanced Networking

## Predefined Networks
By default:
- Each stack = separate network
- Containers communicate internally only

If **Connect to Predefined Network** is enabled:
- Cross-stack communication is allowed
- Coolify renames services:
  ```
  postgres-<uuid>
  laravel-<uuid>
  ```
- Applications must reference renamed hosts
- Internal Docker DNS behavior changes

---

## Raw Docker Compose Deployment
For advanced users only.

### Behavior
- Deploys compose file as-is
- Minimal Coolify automation
- Still adds Coolify management labels
- Requires Traefik labels for proxy use

Example:
```yaml
labels:
  - coolify.managed=true
  - traefik.enable=true
```

---

## Recommendation
Use Raw mode only if:
- You fully understand Docker networking
- You need non-standard routing
- You require manual proxy control
