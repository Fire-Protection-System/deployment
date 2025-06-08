## Deployment 

### Structure 
```
.
├── docker-compose.yml
├── environments
│   ├── common.env
│   ├── fire-backend.env
│   ├── fire-configuration.env
│   ├── fire-visualization.env
│   └── fire-simulation.env
├── fire-backend
├── fire-configurations
├── fire-simulation
├── fire-visualization
├── scripts
│   └── clone_repos.sh 
└── README.md

```

### Running services 

```bash
docker compose -f docker-compose.yml up --build     
```

or 

```bash 
docker compose -f docker-compose.yml up --build "rabbitmq-service"  
docker compose -f docker-compose.yml up --build "forest-simulator-service"  
docker compose -f docker-compose.yml up --build "mongo"  
docker compose -f docker-compose.yml up --build "fire-backend-service" 
docker compose -f docker-compose.yml up --build "fire-configuration-service"  
docker compose -f docker-compose.yml up --build "fire-visualization-service"  
```

