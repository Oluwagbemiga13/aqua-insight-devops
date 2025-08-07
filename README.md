# 🌍 aqua-insight-devops


This repository hosts the infrastructure setup for a spatial data platform using **PostgreSQL with PostGIS** and **GeoServer**. The project uses a **branch-per-environment** model to manage different configurations across development, staging, and production.

---

## 🔀 Branching Model

We follow an **environment-based branching strategy**:

| Branch     | Purpose                      |
|------------|------------------------------|
| `master`   | Information about repository  |
| `dev`      | Local development and testing |
| `stage`  | Pre-production QA environment |
| `prod`   | Production-ready configuration |

Each branch contains its own `docker-compose.yml`, `.env`, and environment-specific setup.  
**Do not edit files directly in `master` — always work through `dev` and promote changes forward.**

---

## 🧭 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Oluwagbemiga13/aqua-insight-devops.git
cd aqua-insight-devops
```

## 2. List Available Branches

```bash
git branch -a
```
## 3. Switch to Environment Branch

To use the `dev` setup (for example):

```bash
git checkout dev
```

## 📄 Environment-Specific Docs

Each environment branch contains its own `README.md` with instructions for:

- Running `docker-compose` for that environment
- Setting up the `.env` file
- Accessing services (GeoServer, PostgreSQL)
- Custom extensions (e.g. pgAdmin, shapefile loaders)

👉 **See the DEV branch README for local development setup.**

---


