# code-graph-storage

Infrastructure and tooling for indexing codebases into Neo4j and exposing them via MCP (Model Context Protocol).

## Project Structure

- `k8s/neo4j/` - Kustomization to deploy Neo4j Community on k3s

## Neo4j

- Namespace: `agentic-tools`
- Auth: disabled (`NEO4J_AUTH=none`)
- Plugin: APOC
- Storage: `local-path` (10Gi)
- NodePort access: HTTP `30474`, Bolt `30687`

## Apply to cluster

```bash
kubectl apply -k k8s/neo4j/
```
