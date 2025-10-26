# Deployment of n8n in my k8s cluster 

n8n=# CREATE TABLE deployments (
n8n(#   id SERIAL PRIMARY KEY,
n8n(#   app_name VARCHAR(255) NOT NULL,
n8n(#   yaml_content TEXT NOT NULL,
n8n(#   image VARCHAR(255),
n8n(#   replicas INTEGER,
n8n(#   cpu_request VARCHAR(50),
n8n(#   memory_request VARCHAR(50),
n8n(#   status VARCHAR(50) DEFAULT 'pending',
n8n(#   created_at TIMESTAMP DEFAULT NOW(),
n8n(#   deployed_at TIMESTAMP,
n8n(#   denied_at TIMESTAMP
n8n(# );
CREATE TABLE
n8n=# CREATE INDEX idx_app_status ON deployments(app_name, status);
CREATE INDEX
