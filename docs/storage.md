# Storage in Coolify Docker Compose Deployments

## Storage Definition
Storage is defined in your Docker Compose file.  
Coolify respects all standard Docker storage behaviors plus adds enhancements.

---

## Automatic Directory Creation
```yaml
volumes:
  - type: bind
    source: ./srv
    target: /srv
    is_directory: true
```

Coolify ensures directory exists.

---

## File Creation with Content
Coolify allows binding files with content.

```yaml
volumes:
  - type: bind
    source: ./srv/99-roles.sql
    target: /docker-entrypoint-initdb.d/init-scripts/99-roles.sql
    content: |
      ALTER USER ...
```

Supports:
- configuration bootstrapping
- database initialization
- dynamic env reference

---

## Healthcheck Exclusion
Exclude services from global health monitoring:

```yaml
exclude_from_hc: true
```

Useful for:
- migration containers
- one-shot jobs
- tasks that stop intentionally
