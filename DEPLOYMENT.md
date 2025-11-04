
---

## 📄 DEPLOYMENT.md

```markdown
# Deployment Guide

## 1. Infrastructure Requirements

### Minimum Specifications
```yaml
# docker-compose.requirements.yml
version: '3.8'
services:
  # Blockchain Nodes
  xrpl-validator:
    image: xrpllab/validator:latest
    resources:
      limits:
        memory: 8G
        cpus: '4.0'
  
  xdc-node:
    image: xinfin/xdc-node:latest
    resources:
      limits:
        memory: 16G
        cpus: '8.0'

  # AI Services
  ai-swarm-orchestrator:
    resources:
      limits:
        memory: 12G
        cpus: '6.0'
        gpu: 1  # Optional for enhanced learning
