---
name: project-conventions
description: Use when adding or changing API endpoints, models or routes in this FastAPI project. Covers folder layout, naming and error format.
---
# Project conventions
- Pydantic models go in app/schemas/, one file per resource.
- Routes go in app/routers/, registered in app/main.py.
- Errors return {"error": {"code": str, "message": str}} with the right HTTP status.
- Use snake_case everywhere. No print(); use the logger in app/core/logging.py.
