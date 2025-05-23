# Understanding Kanban and Its Implementation

## What is a Kanban Board?

In my own words, a Kanban board is a visual workflow management tool that represents tasks as cards moving through defined process stages (columns) from initiation to completion. Originating from the Japanese manufacturing system at Toyota, "Kanban" literally means "visual signal" or "card." It transforms invisible knowledge work into a visible, tangible format that teams can observe, discuss, and improve together. It provides real-time visibility into work status, helps identify bottlenecks, and enables continuous process improvement by limiting work-in-progress (WIP).


Unlike static project plans, a Kanban board is a dynamic, living artifact that evolves with the project, providing real-time status information and revealing process bottlenecks. At its core, Kanban is about visualizing work, limiting work-in-progress, and enhancing flow through a system.

## How Our Board Visualizes Workflow

Our Student Mental Wellness Academic Support System Kanban board visualizes workflow in several key ways:

### 1. Process Transparency

Our board makes the entire workflow visible by representing each stage as a column:
- **Backlog** → **Ready** → **In Progress** → **Clinical/Academic Review** → **In Review** → **Compliance Check** → **Done**

This visualization shows exactly where each user story is in the development process. For example, seeing US-001 (Registration) in the "In Progress" column immediately communicates to all stakeholders that development has started but the feature isn't ready for review yet.

## Implementation

### 1. Workflow Visualization
Our board uses seven columns to map the complete development lifecycle:
1. **Backlog**: All identified requirements (16 user stories)
2. **Ready**: Prioritized items for current sprint (5 stories)
3. **In Progress**: Actively developed items (currently US-001)
4. **Clinical Review**: Mental health feature validation
5. **Academic Review**: Education functionality verification
6. **Compliance Check**: Final security/privacy gate
7. **Done**: Completed work

*Visual Example*:  
`US-001 (Registration)` moving from `Backlog` → `Ready` → `In Progress` shows concrete progress to all stakeholders.
### 2. Work Type Differentiation

Our board uses color-coded labels to visualize different types of work:
- Purple labels for clinical mental health features
- Green labels for academic support features  
- Red labels for security and compliance features
- Blue labels for core technical implementation

This allows team members to quickly identify what type of work each card represents, facilitating better task selection based on expertise.
### 3. Parallel Workflows

The board's design with separate "Clinical Review" and "Academic Review" columns visualizes our parallel domain-specific review processes. This shows that:
- Mental health features require clinical validation
- Academic support features require educational expertise validation
- Both types of features eventually converge at technical review and compliance check

This visualization makes it immediately apparent which domain's review process might be creating bottlenecks.

## Limiting Work-in-Progress (WIP)

Our Kanban implementation limits work-in-progress to prevent overloading team members and ensure focused effort:

### 1. Explicit WIP Limits

We've implemented the following WIP limits:
- **In Progress**: 3 items maximum
- **Clinical Review**: 2 items maximum
- **Academic Review**: 2 items maximum
- **In Review**: 3 items maximum
- **Compliance Check**: 2 items maximum
- **Review Columns**: Max 2 items each
- **Ready**: Max 5 prioritized items

These limits are visually indicated on the board, showing when a column is approaching or exceeding its capacity.

*Bottleneck Prevention*: When "Clinical Review" reaches 2 items, the board visually alerts us to allocate more clinical resources before developers complete additional mental health features.
### 2. Bottleneck Prevention

By limiting WIP, our board helps prevent bottlenecks in several ways:
- Prevents developers from starting new work when too many items are awaiting review
- Highlights when review processes are becoming overloaded
- Creates a "pull system" where new work is only started when capacity exists

For example, if the "Clinical Review" column reaches its limit of 2 items, it signals that clinical staff may be overloaded and need support before more mental health features are developed.

### 3. Focus and Quality

Our WIP limits promote:
- Increased focus by preventing multitasking
- Higher quality through concentrated effort
- Faster completion of individual features
- Earlier identification of process impediments

For instance, our team has found that limiting "In Progress" items to 3 (rather than the default 16) has already improved our completion rate for Sprint 1 features.

## Supporting Agile Principles

Our Kanban implementation supports core Agile principles in the following ways:
### 3. Agile Principles Support

| Agile Principle | Kanban Implementation | Example from Our Board |
|-----------------|-----------------------|------------------------|
| Continuous Delivery | Small, testable increments | US-001 can deploy after passing Compliance Check |
| Adaptability | Easy reprioritization | Can drag US-010 ahead if scheduling becomes urgent |
| Customer Collaboration | Domain review columns | Clinical team approves US-003 before release |
| Sustainable Pace | WIP limits prevent overload | Developers focus on 3 items max |

Our Kanban board has transformed how our team works on the Student Mental Wellness Academic Support System. Rather than relying on status meetings or reports, we now have a shared visual understanding of our work progress, allowing us to identify and resolve issues more quickly and collaborate more effectively across our specialized domains.

## Key Customizations
1. **Dual Review Columns**  
   Added "Clinical Review" and "Academic Review" to:  
   - Ensure mental health features meet therapeutic standards  
   - Verify academic functions align with educational requirements  

2. **Compliance Gate**  
   Added "Compliance Check" column to:  
   - Enforce FERPA/HIPAA requirements  
   - Serve as final quality gate before "Done"

*"By limiting 'In Progress' to 3 items, our team maintains focus while the specialized review columns ensure both clinical validity and academic usefulness in our Student Wellness System."*
