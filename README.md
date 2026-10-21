# fastapi-migration-brief

Due-diligence brief on migrating our small Node/Express REST service to **FastAPI**, prepared for the architecture review.

The completed brief lives at **[docs/fastapi-due-diligence.md](docs/fastapi-due-diligence.md)** and covers, in order:

1. Project status & maintenance activity
2. Data validation & models
3. Async endpoints & built-in documentation
4. Express → FastAPI pattern mapping (middleware, routers, centralized error handling)
5. Risks & recommendation

**TL;DR — Conditional go.** FastAPI is very actively maintained (v0.159.1, released 2026-10-21) with first-class Pydantic validation, automatic Swagger UI/ReDoc docs, and a direct equivalent for each of our Express patterns. The conditions: a blocking-IO audit before going async, and pinned versions given the pre-1.0 release line. Details and reasoning in the brief.
