# Public-repo

≠======= 1 =======

You are acting as a Senior Enterprise Solution Architect, Principal Java Engineer, and Spring Batch Expert.

Your task is NOT to modify any code.

Your only responsibility is to reverse engineer the complete project and produce comprehensive technical documentation.

Treat this project as a production enterprise ETL system.

Goals

1. Understand the complete architecture.
2. Discover every component.
3. Document all business flows.
4. Identify risks.
5. Produce markdown documentation only.
6. Do NOT generate implementation code.

Analyze the entire repository including:

- Java source
- Spring Boot configuration
- Spring Batch Jobs
- Readers
- Writers
- Processors
- Listeners
- Tasklets
- Services
- Repositories
- SQL
- Stored Procedures
- External APIs
- File formats
- Configuration
- Scheduler
- Dependency Injection
- Thread usage
- Cache usage
- Shared resources
- Database access
- Error handling
- Restartability
- Job Parameters
- ExecutionContext
- StepScope usage

Generate documentation only.

Do not skip any package.

If information cannot be determined, explicitly mention assumptions instead of guessing.

======== 2 ========

Create the following markdown documents.

01-system-overview.md

02-project-structure.md

03-domain-model.md

04-job-inventory.md

05-step-inventory.md

06-reader-analysis.md

07-processor-analysis.md

08-writer-analysis.md

09-listener-analysis.md

10-tasklet-analysis.md

11-service-analysis.md

12-database-analysis.md

13-sql-analysis.md

14-file-processing.md

15-cache-analysis.md

16-thread-safety-analysis.md

17-performance-analysis.md

18-dependency-analysis.md

19-configuration-analysis.md

20-risk-analysis.md

21-improvement-opportunities.md

22-open-questions.md


========3============

Generate steering documents describing:

Coding conventions

Architecture

Layer responsibilities

Dependency rules

Naming conventions

Package structure

Spring usage

Exception handling

Logging standards

Transaction boundaries

Database standards

Configuration standards

Testing standards

Performance guidelines

Concurrency assumptions

Security assumptions

Deployment assumptions

These documents should represent the CURRENT project, not recommendations.

========= 4 ========

Generate architecture diagrams in markdown using Mermaid.

Include:

System Context

Component Diagram

Package Diagram

Job Flow

Step Flow

Data Flow

Database Interaction

Reader → Processor → Writer Flow

Service Dependency Graph

Bean Dependency Graph

Sequence Diagrams

ExecutionContext Flow

Thread Interaction Diagram

Partitioning Opportunities

====== 5 =======

You are continuing work on this project.

Before making any code changes, read and follow all existing specifications and steering documents.

Use as the source of truth:

- Current State Specifications
- Target Architecture Specifications
- Steering Documents
- Technical Decisions
- Coding Standards
- Architecture Rules

Do not violate any documented architecture or coding standards.

Your task is to migrate ONLY the following Spring Batch step:

<Job Name>

Step:
<Step Name>

This step must be converted from a single-threaded implementation to a partitioned implementation.

Requirements

1. Preserve 100% of the existing business logic.
2. Do not change business rules.
3. Only refactor infrastructure required for partitioning.
4. Maintain restartability.
5. Maintain fault tolerance.
6. Maintain transaction semantics.
7. Maintain logging behavior.
8. Preserve all validation logic.
9. Preserve exception handling.
10. Keep backward compatibility where possible.

Before changing any code, analyze:

- Reader
- Processor
- Writer
- Services
- Repositories
- Listeners
- Tasklets
- Shared Objects
- Static Variables
- Singleton Beans
- ThreadLocal usage
- Cache usage
- Database transactions
- SQL execution
- File access
- External APIs

Identify every thread safety issue.

For every issue provide:

- Description
- Root cause
- Impact
- Recommended solution
- Files affected

Do not modify code until analysis is complete.



======= 6 =======

Based on the approved specifications and analysis, create a migration plan for this step.

The plan must include:

- Files to modify
- New classes
- Classes to remove
- Dependency changes
- Configuration changes
- Bean scope changes
- ExecutionContext changes
- Partition strategy
- Grid size recommendation
- Transaction boundaries
- Performance improvements
- Rollback strategy

Do not generate implementation yet.


========== 7 =======

The migration plan has been approved.

Implement the migration.

Rules:

- Only modify files involved in this step.
- Do not modify unrelated jobs.
- Keep commits small and focused.
- Add JavaDoc where needed.
- Add comments only where the intent is non-obvious.
- Follow all Steering documents.
- Follow all Specifications.
- Preserve existing package structure unless the specs require changes.

========= 8 ========

Before marking this task complete, perform a comprehensive review.

Verify:

✓ Business logic unchanged
✓ Thread-safe
✓ No mutable singleton state
✓ Proper @StepScope usage
✓ ExecutionContext handled correctly
✓ Restartability preserved
✓ Fault tolerance preserved
✓ Transaction boundaries correct
✓ No race conditions
✓ No duplicate processing
✓ No record loss
✓ Logging unchanged
✓ Performance improved
✓ Memory usage acceptable
✓ Java 21 compatible
✓ Spring Batch 6 compatible

Produce a review report.

If any item fails, fix it before completing the implementation.


======== role ======= 

Absolutely. For a large enterprise Spring Batch migration, the biggest improvement comes from telling Kiro how to think, not just what to do. The prompt should instruct it to behave like an experienced architect who analyzes, validates, and only then implements.

Here are additional instructions I’d include with the prompts above.

1. Define the AI’s role
Act as:

- Enterprise Solution Architect
- Spring Batch 6 Expert
- Java 21 Expert
- Spring Framework Expert
- Concurrency and Multithreading Expert
- Performance Engineer
- Database Architect
- ETL Migration Specialist
- Code Reviewer
- Software Quality Engineer

Think like a senior engineer responsible for migrating a mission-critical production system.

2. Prevent assumptions
Never assume.

If information is missing:

- Search the repository.
- Search configuration.
- Search tests.
- Search documentation.
- Search SQL.
- Search Git history if available.

Only if information still cannot be determined:

Document assumptions explicitly.

Never invent business logic.


Never assume.

If information is missing:

- Search the repository.
- Search configuration.
- Search tests.
- Search documentation.
- Search SQL.
- Search Git history if available.

Only if information still cannot be determined:

Document assumptions explicitly.

Never invent business logic.
   



