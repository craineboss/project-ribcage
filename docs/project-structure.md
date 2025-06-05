# Project Ribcage - Structure Overview

## Repository Structure

```
project-ribcage/
├── README.md                    # Project overview and getting started
├── docs/                        # Documentation
│   ├── phase-1-overview.md     # Phase 1 detailed breakdown
│   ├── project-structure.md    # This file
│   └── architecture/           # Architecture documents
├── .github/                    # GitHub configuration
│   ├── ISSUE_TEMPLATE/        # Issue templates
│   │   ├── epic.md           # Epic template
│   │   └── task.md           # Task template
│   └── workflows/             # CI/CD workflows (future)
├── src/                       # Source code (Phase 2+)
├── charts/                    # Helm charts (Phase 2+)
├── scripts/                   # Development scripts (Phase 2+)
└── tests/                     # Test suites (Phase 2+)
```

## Issue Management

### Labels
- **Priority**: `critical`, `high`, `medium`, `low`
- **Phase**: `phase-1`, `phase-2`, `phase-3`, etc.
- **Type**: `epic`, `task`, `bug`, `enhancement`
- **Component**: `architecture`, `AAMI`, `frameworks`, `integration`
- **Framework**: `kagent`, `autogen`, `crewai`, `langgraph`
- **Status**: `research`, `design`, `implementation`, `testing`

### Issue Types
- **Epics**: Major feature areas spanning multiple issues
- **Tasks**: Specific deliverable work items
- **Bugs**: Issues requiring fixes
- **Enhancements**: Improvements to existing functionality

### Workflow States
1. **Backlog**: Issues created but not yet started
2. **Ready**: Issues ready to be worked on
3. **In Progress**: Issues currently being worked on
4. **Review**: Issues completed and under review
5. **Done**: Issues completed and approved

## Project Management

### GitHub Projects
- **Project Ribcage - Phase 1**: Foundation & Research
- **Project Ribcage - Phase 2**: Core Infrastructure (future)
- **Project Ribcage - Phase 3**: Multi-Framework Support (future)

### Milestones
- **Phase 1 Complete**: All foundation and research work finished
- **Phase 2 Complete**: Core infrastructure implemented
- **MVP Release**: Minimum viable product ready
- **Production Release**: Full production-ready system

## Development Phases

### Phase 1: Foundation & Research (Weeks 1-2)
Architecture design, framework research, AAMI integration planning

### Phase 2: Core Infrastructure (Weeks 3-5)
Ribcage core engine, kagent adapter, AAMI integration, Kubernetes packaging

### Phase 3: Multi-Framework Support (Weeks 6-8)
Additional framework adapters, cross-framework coordination, avatar-agency binding

### Phase 4: Dashboard & Integration (Weeks 9-12)
Management dashboard, production readiness, comprehensive testing

### Phase 5: Integration & Packaging (Weeks 13-15)
End-to-end integration, advanced features, documentation

### Phase 6: Testing & Polish (Weeks 16-18)
Comprehensive testing, performance optimization, launch preparation

## Contributing

1. Check the GitHub Issues for current tasks
2. Assign yourself to an available issue
3. Create a feature branch from main
4. Implement your changes
5. Submit a pull request
6. Request review from team leads
7. Merge after approval

## Communication

- **Issues**: Primary communication for specific tasks
- **Discussions**: High-level design discussions
- **Wiki**: Knowledge base and documentation
- **Projects**: Visual progress tracking