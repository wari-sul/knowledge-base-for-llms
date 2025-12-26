# Environment Variables in Coolify Docker Compose

## Overview
Coolify reads variables from your `docker-compose.yml` and exposes them in UI where applicable.

---

## Variable Detection

### Hardcoded values
Not visible in UI but passed to container:
```yaml
- SOME_VALUE=hello
```

### Editable variables
Visible and editable in Coolify:
```yaml
- APP_MODE=${APP_MODE}
```

### Editable with default
```yaml
- DEBUG=${DEBUG:-false}
```

---

## Required Environment Variables
Coolify supports Docker's `:?` validation syntax.

```yaml
- DATABASE_URL=${DATABASE_URL:?}
- API_KEY=${API_KEY:?}
- PORT=${PORT:?3000}
```

### Behavior
- Required fields appear first
- Missing values show red warning
- Deployment is blocked until filled
- Prevents partial deployments

---

## Shared Environment Variables
Shared variables can be reused but must be explicitly mapped.

Steps:
1) Create shared variable in Coolify
2) Reference variable in Compose
3) Map in UI using:
```
{{environment.SHARED_VARIABLE_NAME}}
```

---

## Magic Environment Variables
Coolify can auto-generate values using:

```
SERVICE_<TYPE>_<IDENTIFIER>
```

### Supported Types
- URL
- FQDN
- USER
- PASSWORD / PASSWORD_64
- BASE64 / BASE64_64 / BASE64_128

### Identifier Rule
If using ports:
- Use hyphens (`-`)
- Do not use underscores

❌ `SERVICE_URL_APPWRITE_SERVICE_3000`  
✅ `SERVICE_URL_APPWRITE-SERVICE_3000`

---

## Key Benefits
- Automatic URLs / routing values
- Stable + reusable values
- Visible in UI
- FQDN + URL not editable (others are)
