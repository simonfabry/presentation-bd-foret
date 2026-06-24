# Tiltfile pour présentation reveal.js avec Docker Compose

# # Lancer docker-compose
# local_resource(
#     'Service Up',
#     'docker-compose up -d',
#     deps=['docker-compose.yml'],
#     labels=['docker']
# )

# # Arrêter les conteneurs en quittant Tilt
# local_resource(
#     'Service Down',
#     'docker-compose down',
#     trigger_mode=TRIGGER_MODE_MANUAL,
#     labels=['docker']
# )

local_resource(
    'Install dependencies',
    'npm install',
    deps=["package.json"],
    labels=['slidev']
)

local_resource(
    'Service Up',
    serve_cmd='npm run dev_simple',
    links=["http://localhost:3030"],
    deps=["ign-theme/"],
    resource_deps=["Install dependencies"],
    labels=['slidev']
)