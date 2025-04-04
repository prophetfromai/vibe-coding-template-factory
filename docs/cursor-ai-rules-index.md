# Cursor AI Role-Specific Rules

> **AI Agent Instructions**
> 
> As an AI code generation agent, you must follow this exact workflow:
> 1. Read the top-level `README.md` first to understand repository principles and structure
> 2. Consult this index to identify the appropriate role context for your current task
> 3. Read and apply the specific rules from the relevant role context file
> 4. Verify all generated code conforms to both global repository principles and role-specific rules
> 5. Ensure all work adheres to the branch structure described in the documentation
> 
> Important: You are bound by the constraints in these documents. Do not generate code outside your defined role scope.
>
> For detailed workflow instructions, see [ai-agent-workflow.md](./ai-agent-workflow.md)

This directory contains role-specific rule sets for constraining AI development in Cursor when working on specific tasks. These rules help ensure that AI assistance remains focused on the appropriate scope of work and follows best practices for each specialized area.

## AI Workflow Visualization

```mermaid
graph TD
    A[Task Request] --> B[1. Read Top-level README.md]
    B --> C[2. Consult this Index]
    C --> D[3. Select Appropriate Role]
    D --> E[4. Apply Role-specific Rules]
    E --> F[5. Generate Code in ai-gen/ Branch]
    
    D -->|UI Focus| G[UI Component Developer]
    D -->|API Focus| H[API Developer]
    D -->|Auth Focus| I[Auth & Security Specialist]
    D -->|Data Focus| J[Database & Schema Developer]
    D -->|Dashboard Focus| K[Dashboard Developer]
    
    G --> L[UI Components Only]
    H --> M[API Endpoints Only]
    I --> N[Auth & Security Only]
    J --> O[Schema & Data Only]
    K --> P[Dashboard Components Only]
    
    L --> F
    M --> F
    N --> F
    O --> F
    P --> F
    
    style B fill:#d0f0c0,stroke:#333,stroke-width:2px
    style D fill:#c0d0f0,stroke:#333,stroke-width:2px
    style F fill:#f0c0c0,stroke:#333,stroke-width:2px
```

## Available Role-Specific Rules

| Role | Description | File |
|------|-------------|------|
| **Dashboard Developer** | Rules for modifying dashboard components and visualizations | [cursor-ai-rules-dashboard-developer.md](./cursor-ai-rules-dashboard-developer.md) |
| **API Developer** | Rules for creating and modifying API endpoints | [cursor-ai-rules-api-developer.md](./cursor-ai-rules-api-developer.md) |
| **Authentication & Security Specialist** | Rules for implementing and auditing security features | [cursor-ai-rules-auth-security-specialist.md](./cursor-ai-rules-auth-security-specialist.md) |
| **Database & Schema Developer** | Rules for designing and modifying database schemas | [cursor-ai-rules-database-schema-developer.md](./cursor-ai-rules-database-schema-developer.md) |
| **UI Component Developer** | Rules for creating and modifying UI components | [cursor-ai-rules-ui-component-developer.md](./cursor-ai-rules-ui-component-developer.md) |
| **Template** | Template for creating new role-specific rules | [cursor-ai-rules-template.md](./cursor-ai-rules-template.md) |

## How to Use These Rules

1. **Identify the appropriate role** for your current development task
2. **Copy the relevant rules file** into your project workspace
3. **Reference these rules in your prompt** to Cursor AI to constrain its development focus
4. **Ensure the AI understands the repository workflow** by pointing it to the top-level README.md
5. **Verify generated code** adheres to both the role-specific rules and global repository guidelines

Example prompt:

```
I need help modifying the dashboard to add a new chart component.
First, please read the top-level README.md to understand our repository structure and branch workflow.
Then, follow the rules in the cursor-ai-rules-dashboard-developer.md file.
The new chart should display...
```

## Common Structure

Each role-specific rules file follows a common structure:

1. **Role Context** - Defines the specific responsibility and focus area
2. **Core Constraints** - Specific limitations on what can be modified
3. **Workflow Guidelines** - Process recommendations for the specific role
4. **Security/Performance Considerations** - Role-specific concerns
5. **Branch Management** - How to manage code changes within the AI workflow
6. **Communication Protocol** - How to request clarification or suggest improvements

## Creating Custom Role Rules

To create custom role-specific rules for your project:

1. Copy one of the existing files as a template
2. Modify the rules to match your specific role requirements
3. Add the new file to this index

## Integration with Repository Workflow

These role-specific rules complement the overall repository workflow defined in the main README.md. The branch structure and promotion process should be followed regardless of the specific role. 