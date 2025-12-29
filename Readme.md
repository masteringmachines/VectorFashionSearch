# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
ENV/
.venv
*.egg-info/
dist/
build/
.pytest_cache/
.mypy_cache/
.ruff_cache/

# Node.js
node_modules/
.next/
out/
.npm
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Environment files
.env
.env.local
.env.*.local
*.env

# IDEs
.vscode/
.idea/
*.swp
*.swo
*~
.DS_Store

# Database
*.db
*.sqlite
*.sqlite3

# Docker
.docker/

# Logs
logs/
*.log

# ML Models (large files)
*.pth
*.pkl
*.h5
*.onnx
ml/models/downloaded/

# Data
data/
*.csv
*.json
!package.json
!tsconfig.json

# SSL Certificates
*.pem
*.key
*.crt
infrastructure/nginx/ssl/*
!infrastructure/nginx/ssl/.gitkeep

# Monitoring
infrastructure/monitoring/prometheus/data/
infrastructure/monitoring/grafana/data/

# OS
Thumbs.db
.DS_Store

# Temporary files
tmp/
temp/
*.tmp

# Coverage
