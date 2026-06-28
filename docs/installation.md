### Backend Setup:

```bash
git clone git@github.com:jvmdevelop/crm-service.git
cd crm-service/backend
mvn clean install
mvn spring-boot:run
```

### Frontend Setup:

```bash
cd crm-service/frontend
npm install
npm run dev
```

### With Docker Compose:

```bash
cd crm-service
docker-compose up
```
