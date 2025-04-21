# Gridica Node Orchestrator

Gridica Node Orchestrator is a core component of the Gridica decentralized inference network. It coordinates job execution by selecting suitable nodes, assigning tasks, and monitoring node status in real time.

## Overview

The orchestrator maintains persistent WebSocket connections with active nodes. It tracks hardware profiles, supported models, uptime metrics, and region affinity. Jobs are dispatched based on availability, compatibility, and priority, with results routed back to the system.

All node interactions are stateless and verifiable. Job execution and result submission are signed and linked to specific job identifiers.

## Responsibilities

- Maintain a live registry of connected nodes
- Assign jobs from the queue to eligible nodes
- Collect results and forward them to the control layer
- Monitor node health and TTL via heartbeats
- Track model versions and region topology

### Internal Components

- `socket_hub`: provides interaction with the nodes
- `job_queue`: manages the pool of incoming jobs and scheduling logic
- `result_collector`: handles signed output from nodes
- `ping_api`: accepts heartbeat pings and resource updates from nodes

## Requirements

- Part of the internal Gridica server layer

## Development Status

This repository contains the orchestration logic in planning. Testnet rollout is scheduled for Q2 2025.

## Resources

- [Project site](https://gridica.network)
- [Overview](https://gridica.gitbook.io/v1)  
- [Orchestrator role](https://gridica.gitbook.io/v1/system-architecture/gridica-server-layer/node-orchestrator)

## License

MIT License
