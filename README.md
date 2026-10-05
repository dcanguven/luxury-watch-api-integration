# Luxury Watch Price Data API Integration

- The frontend supports filtering by brand, model, price, and year.
- The backend is built with FastAPI and runs on Cloudflare Workers.
- Market data is stored in a Supabase PostgreSQL database.
- Cloudflare Hyperdrive is used between the Worker and PostgreSQL.
- The project includes an authenticated REST API with API key access and rate limiting.
- `luxury_watch_api_client.ipynb` shows how an external user can connect to the live API and retrieve data.
- The project demonstrates API design, backend integration, database access, security, and production deployment.
- Live site: https://watches.dcanguven.com



## Architecture

```mermaid
flowchart LR
    A["Web User"] --> B["React Frontend"]
    B --> C["Web API /api/web"]

    D["External API Client"] --> E["Developer API /api/v1"]

    C --> F["FastAPI on Cloudflare Workers"]
    E --> F

    F --> G["Cloudflare Hyperdrive"]
    G --> H["Supabase PostgreSQL"]
```

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?logo=cloudflareworkers&logoColor=white)
