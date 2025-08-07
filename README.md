# aqua-insight-devops

## 📦 Services

### 1. PostgreSQL + PostGIS
- Image: `postgis/postgis:latest`
- Exposes port `5432`
- Stores data in a named Docker volume `postgres_data`
- Uses credentials from `.env`

### 2. GeoServer
- Image: `kartoza/geoserver:latest`
- Exposes port `8080`
- Depends on the database service
- Uses admin credentials from `.env`
- Persists data in volume `geoserver_data`

---

## 🚀 Getting Started

Run the services:

```bash
docker-compose up -d
```

## 🌐 Access the Services

- **PostgreSQL (with PostGIS)**: `localhost:5432`
- **GeoServer UI**: [http://localhost:8080/geoserver](http://localhost:8080/geoserver)  
  Login with `${GEOSERVER_ADMIN_USER}` / `${GEOSERVER_ADMIN_PASSWORD}`

---

## 🗃️ Data Volumes

- `postgres_data`: Stores PostgreSQL and PostGIS database files.
- `geoserver_data`: Stores GeoServer config and workspace data.

---

## 🧼 Stopping & Cleaning

To stop and **remove** all containers, networks, and **volumes**:

```bash
docker-compose down -v
```
## 📚 References

- [PostGIS Docker Image](https://hub.docker.com/r/postgis/postgis)
- [Kartoza GeoServer Image](https://hub.docker.com/r/kartoza/geoserver)
- [GeoServer Documentation](https://docs.geoserver.org/)

---

## 🧭 License

This project is provided as-is under the MIT License.


