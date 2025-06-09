# openribcage - A2A Protocol Client for Avatar Interfaces

[![GitHub issues](https://img.shields.io/github/issues/craine-io/project-openribcage)](https://github.com/craine-io/project-openribcage/issues)
[![GitHub stars](https://img.shields.io/github/stars/craine-io/project-openribcage)](https://github.com/craine-io/project-openribcage/stargazers)
[![License](https://img.shields.io/github/license/craine-io/project-openribcage)](LICENSE)

## Overview

openribcage is an A2A (Agent2Agent) protocol client designed to enable avatar-based interfaces for AI agent coordination. It serves as the backend communication layer for avatar management interfaces, providing standardized agent discovery, communication, and orchestration capabilities.

## The Vision

Transform complex multi-agent coordination from technical complexity into natural conversation with AI agents through avatar interfaces. Instead of managing disparate AI frameworks through different technical interfaces, coordinate with unified digital colleagues via the A2A protocol standard.

## Key Features

- **A2A Protocol Client**: Full implementation of the Agent2Agent communication standard
- **Agent Discovery**: Automatic discovery and registration of A2A-compliant agents
- **Real-time Communication**: JSON-RPC 2.0 with Server-Sent Events (SSE) streaming
- **Multi-Agent Orchestration**: Coordinate multiple AI agents simultaneously
- **Avatar Interface Ready**: Designed for integration with avatar-based user interfaces

## Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                 Avatar Interface Layer                          │
│          (Natural conversation with AI agents)                  │
├─────────────────────────────────────────────────────────────────┤
│              openribcage - A2A Protocol Client                 │
│           (Agent discovery, communication, orchestration)       │
├─────────────────────────────────────────────────────────────────┤
│              A2A Protocol (JSON-RPC 2.0 / HTTP)               │
│                  (Standard agent communication)                 │
├─────────────────────────────────────────────────────────────────┤
│              A2A-Compliant Agent Frameworks                    │
│           (kagent, LangGraph, CrewAI, Google ADK)              │
└─────────────────────────────────────────────────────────────────┘
```

## Supported A2A Agents

openribcage connects to any A2A-compliant agent framework:

- **kagent** - Kubernetes-native agent framework with A2A endpoints
- **LangGraph** - Graph-based agent workflows with A2A support
- **CrewAI** - Role-based team coordination via A2A protocol
- **Google ADK** - Agent Development Kit with native A2A implementation

## Development Phases

### Phase 1: A2A Protocol Foundation (Weeks 1-2) ✅ Current Phase
- A2A protocol specification analysis
- Agent discovery and AgentCard parsing
- Basic JSON-RPC 2.0 client implementation

### Phase 2: Core A2A Client (Weeks 3-5)
- Complete A2A method implementation (`message/send`, `message/stream`, etc.)
- Real-time streaming via Server-Sent Events
- Agent lifecycle and task management

### Phase 3: Multi-Agent Orchestration (Weeks 6-8)
- Multi-agent discovery and coordination
- Agent capability mapping and routing
- Cross-agent communication patterns

### Phase 4: Avatar Interface Integration (Weeks 9-12)
- AgentCard to avatar persona mapping
- Dynamic UI adaptation based on agent capabilities
- Real-time avatar updates from A2A streams

### Phase 5: Production Deployment (Weeks 13-15)
- End-to-end integration testing
- Performance optimization
- Production deployment patterns

### Phase 6: Testing & Polish (Weeks 16-18)
- Comprehensive A2A compliance testing
- Performance optimization
- Documentation and launch preparation

### Phase 7: Enterprise Scale (Future)
- [Agent Gateway](https://agentgateway.dev/) integration for enterprise data plane
- Federated agent discovery across environments
- Enterprise security with RBAC
- Production observability and monitoring

## Getting Started

### Prerequisites

- Docker
- Go 1.21+
- Node.js 18+
- kubectl (for kagent testing)

### Quick Start

```bash
# Clone the repository
git clone https://github.com/craine-io/project-openribcage.git
cd project-openribcage

# Test A2A client with kagent (Coming in Phase 2)
./scripts/test-a2a-client.sh

# Deploy openribcage A2A client (Coming in Phase 2)
helm install openribcage ./charts/openribcage
```

## A2A Protocol Compliance

openribcage implements the full [Agent2Agent Protocol](https://github.com/google-a2a/A2A) specification:

- **Agent Discovery**: `.well-known/agent.json` AgentCard parsing
- **Communication**: JSON-RPC 2.0 over HTTP(S)
- **Streaming**: Server-Sent Events for real-time updates
- **Task Management**: Complete A2A task lifecycle support
- **Content Types**: TextPart, FilePart, and DataPart handling
- **Authentication**: Standard HTTP authentication schemes

## Integration with Avatar Interfaces

openribcage is designed to integrate with avatar-based management interfaces that provide natural, conversational user experiences for AI agent coordination.

**Note**: Avatar interface implementations are developed as separate projects within the Craine Technology Labs ecosystem.

## Contributing

We welcome contributions to enhance openribcage's A2A protocol implementation!

**Scope**: A2A protocol compliance, agent communication, discovery mechanisms  
**Out of Scope**: Avatar interface implementations, UI components, proprietary integrations

### Development Workflow

1. Check the [GitHub Issues](https://github.com/craine-io/project-openribcage/issues) for current tasks
2. Fork the repository
3. Create a feature branch
4. Make your changes
5. Submit a pull request

## Project Management

This project uses GitHub Issues and Projects for task management. Each development phase is broken down into:

- **Epics**: Major feature areas (A2A client, agent discovery, etc.)
- **Issues**: Specific deliverable tasks
- **Milestones**: Phase completion markers

## Related Projects

- [AAMI](https://github.com/craine-io/aami) - Avatar Agency Management Interface (Private)
- [A2A Protocol](https://github.com/google-a2a/A2A) - Agent2Agent communication standard
- [A2A Python SDK](https://github.com/google-a2a/a2a-python) - Official A2A SDK
- [Agent Gateway](https://agentgateway.dev/) - Enterprise AI connectivity data plane
- [kagent](https://kagent.dev/) - Kubernetes-native agent framework

## Testing with kagent

Use the [kagent sandbox](https://github.com/craine-io/istio-envoy-sandboxes/tree/main/k3d-sandboxes/kagent-sandbox) to test A2A client functionality:

```bash
# Set up kagent with A2A endpoints
cd kagent-sandbox
./scripts/cluster-setup-k3d-kagent-everything.sh

# Test openribcage A2A client (Phase 2+)
# kagent A2A endpoint: http://localhost:8083/api/a2a/kagent/
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Contact

- **Project Lead**: Jason T Clark, Craine Technology Labs
- **GitHub**: [@craineboss](https://github.com/craineboss)  
- **Issues**: [GitHub Issues](https://github.com/craine-io/project-openribcage/issues)

## Acknowledgments

- Google for the Agent2Agent (A2A) protocol specification
- Solo.io for kagent framework and A2A implementation
- The open-source AI agent community

---

*Transform complex multi-agent coordination into natural conversation through A2A protocol compliance and avatar-based interfaces.*